---
title: Brand Portal への並列公開における問題のトラブルシューティング
seo-title: Brand Portal への並列公開における問題のトラブルシューティング
description: 並列公開における問題のトラブルシューティングです。
seo-description: 並列公開における問題のトラブルシューティングです。
uuid: 51e45ca-8c96-4c69-84ef-2ef34f3bcde2
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
content-type: reference
topic-tags: ブランドポータル
discoiquuid: a4801024- b509-4c51- afd8- e337417e658b
translation-type: tm+mt
source-git-commit: 770c353b1143d879280df310012ce9d4d30b40c9

---


# Brand Portal への並列公開における問題のトラブルシューティング {#troubleshoot-issues-in-parallel-publishing-to-brand-portal}

[!DNL Brand Portal] 統合は、AEM [!DNL AEM Assets] Assets作成者インスタンスからシームレスにインジェスト（または公開）されたブランドアセットを承認できます。[統合](https://helpx.adobe.com/experience-manager/6-5/assets/using/brand-portal-configuring-integration.html)が完了すると [!DNL AEM] 、作成者は複製エージェントを使用して、選択したアセットをクラウドサービスに [!DNL Brand Portal] 複製し、承認された使用をユーザーに [!DNL Brand Portal] 許可します。Multiple replication agents are used [!DNL AEM 6.2 SP1-CFP5], [!DNL AEM CFP 6.3.0.2], and onwards to allow high-speed parallel publishing.

>[!NOTE]
>
>AEM [!DNL AEM 6.4.1.0][!DNL AEM Assets Brand Portal] Assetsに確実に統合されるようにアップグレードすることをお勧めします。A limitation in [!DNL AEM 6.4] gives an error while configuring integration with Brand Portal and replication fails.

[!UICONTROL /etc/cloudservice]のブランドポータルのクラウドサービスを設定すると、必要なすべてのユーザーとトークンが自動生成され、リポジトリに保存されます。クラウドサービスの設定が作成され、複製に必要なサービスユーザーと、コンテンツを複製するために必要なサービスユーザーも作成されます。これによって 4 つのレプリケーションエージェントが作成されます。So when you publish numerous assets from [!DNL AEM] to [!DNL Brand Portal], these are queued and distributed among these replication agents through Round Robin.

However, publishing can fail intermittently due to- large sling jobs, increased Network and Disk [!UICONTROL I/O] on [!DNL AEM] Author instance, or slowed performance of [!DNL AEM] Author instance. したがって、公開を開始する前に複製エージェントとの接続をテストすることをお勧めします。

![](assets/test-connection.png)

## 初めての公開で失敗した場合のトラブルシューティング：公開設定の検証 {#troubleshoot-failures-in-first-time-publishing-validating-your-publish-configuration}

公開設定を検証するには、次のようにします。

1. エラーログを確認します。
2. レプリケーションエージェントが作成されているかを確認します。
3. 接続をテストします。

**クラウドサービスが作成中の場合**

直近のログを確認します。レプリケーションエージェントが作成されているかを確認します。レプリケーションエージェントの作成が失敗している場合は、クラウドサービスに小さな変更を加えることでクラウドサービスを編集します。複製エージェントが作成されたかどうかを検証してチェックします。そうでない場合は、サービスを再編集します。

クラウドサービスを繰り返し編集しても正しく設定されていない場合は、daycareチケットをレポートします。

**レプリケーションエージェントとの接続テスト**

ログを参照して、レプリケーションログにエラーが記録されている場合は、次のようにします。

1. アドビサポートにお問い合わせください。

2. Retry [clean-up](../using/troubleshoot-parallel-publishing.md#clean-up-existing-config) and create publish configuration again.

<!--
Comment Type: remark
Last Modified By: Mini Gulati (mgulati)
Last Modified Date: 2018-06-21T22:56:21.256-0400
<p>?? check and compare public key. At times public key is different</p>
<p>?? another thing to check in /useradmin</p>
-->

### 既存のブランドポータル公開設定のクリーンアップ {#clean-up-existing-config}

発行が機能していない時間のほとんどは、発行するユーザー（mac-&lt; endientid&gt;- replication）が最新の秘密鍵を持っていないので、"401unauthorized"では失敗し、他のエラーは複製エージェントログで報告されません。トラブルシューティングを避けて、代わりに新しい設定を作成することができます。新しい設定が正常に動作するためには、AEM作成者のセットアップから以下をクリーンアップする必要があります。

1. localhostに [!UICONTROL 移動します。4502/crx/de] （localhostで [!UICONTROL 作成者インスタンスを実行しているものと仮定）4502]）:\
   i delete [!UICONTROL /etc/replication/agents.author/mp_replication&amp;#42];\
   ii delete [!UICONTROL /etc/cloudservices/mediaportal/&lt; config_ name&amp; gt];

2. localhostに [!UICONTROL 移動します。4502/useradmin]:\
   i search for user [!UICONTROL mac-&lt; endisiond&gt;- replication]\
   iiこのユーザーを削除

これによってシステム全体がクリーンアップされます。これで新しい  cloudservice  config and still use the already existing [!DNL JWT] application in [https://legacy-oauth.cloud.adobe.io/](https://legacy-oauth.cloud.adobe.io/). 新しく作成したクラウド設定から公開鍵を更新する必要があるのではなく、新しいアプリケーションを作成する必要はありません。

## Developer Connection の JWT アプリケーションテナントの可視性の問題 {#developer-connection-jwt-application-tenant-visibility-issue}

[!UICONTROL https://legacy-oauth.cloud.adobe.io/](https://legacy-oauth.cloud.adobe.io/)の場合、現在のユーザーがシステム管理者を保持しているすべてのOrgs（テナント）が表示されます。ここに組織名が表示されない場合や、必要なテナントのアプリケーションを作成できない場合は、そのための十分な（システム管理者の）権限を持っているかを確認してください。

このユーザーインターフェイスでは、テナントの上位10個のアプリケーションのみが表示されるという既知の問題が発生します。アプリケーションを作成したら、そのページにとどまり、URL をブックマークしてください。アプリケーションの一覧ページに移動して、作成したアプリケーションを検索する必要はありません。このブックマークされたURLを直接ヒットして、必要に応じてアプリケーションを更新または削除することができます。

[!DNL JWT] アプリケーションが適切に表示されないことがあります。そのため、JWT アプリケーションの作成中に URL をメモするかブックマークすることを推奨します。

## 機能していた設定が動作を停止した場合 {#running-configuration-stops-working}

<!--
Comment Type: draft

<p>If the running configuration stops working, either of the following two possibilities
<g class="gr_ gr_15 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar multiReplace" data-gr-id="15" id="15" style="font-size: 12px;">
are
</g> there:</p>
<p>1.
<g class="gr_ gr_14 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar only-ins doubleReplace replaceWithoutSep" data-gr-id="14" id="14">
Connection
</g> has failed, or</p>
<p>2. Publish has failed with permission to dam-replication-service denied, while connection has passed </p>
<p>If the connection has failed [1], the
<g class="gr_ gr_10 gr-alert gr_spell gr_inline_cards gr_run_anim ContextualSpelling ins-del multiReplace" data-gr-id="10" id="10">
fail safe
</g> way to fix it is to <a href="../using/troubleshoot-parallel-publishing.md#main-pars-header-1664955658">clean up</a> the existing Brand Portal publish configuration and recreate a publish configuration. </p>
<p>However, if the
<g class="gr_ gr_18 gr-alert gr_spell gr_inline_cards gr_run_anim ContextualSpelling" data-gr-id="18" id="18">
publish
</g> has failed with
<g class="gr_ gr_16 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar only-ins doubleReplace replaceWithoutSep" data-gr-id="16" id="16">
permission
</g> denied to dam-replication-service, raise a support ticket.</p>
-->

それまで問題なく Brand Portal への公開をおこなっていたレプリケーションエージェントが公開ジョブの処理を停止した場合は、レプリケーションログを確認してください。[!DNL AEM] には自動再試行の機能が組み込まれているので、特定のアセットの公開が失敗しても、自動的に再試行されます。ネットワークエラーなどの問題が断続的に発生している場合でも、再試行するうちに公開が成功することがあります。

しかし、公開が連続して失敗し、キューがブロックされている場合は、「接続をテスト」を確認し、報告されるエラーの解決に取り組んでください。

Based on the errors, you are advised to log a support ticket, so that [!DNL Brand Portal] engineering team can help you resolve issues.
