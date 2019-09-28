---
title: Brand Portal への並列公開における問題のトラブルシューティング
seo-title: Brand Portal への並列公開における問題のトラブルシューティング
description: 並列公開における問題のトラブルシューティングです。
seo-description: 並列公開における問題のトラブルシューティングです。
uuid: 51e45cca-8c96-4c69-84ef-2ef34f3bcde2
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: brand-portal
discoiquuid: a4801024-b509-4c51-afd8-e337417e658b
translation-type: tm+mt
source-git-commit: 86d4d5c358ea795e35db2dce8c9529ed14e9ee2d

---


# Brand Portal への並列公開における問題のトラブルシューティング {#troubleshoot-issues-in-parallel-publishing-to-brand-portal}

Brand portalは、AEM Assetsとの統合をサポートし、承認済みのブランドアセットをAEM Assetsオーサーインスタンスからシームレスに取り込む（または公開する）ことができます。 Once [integrated](https://helpx.adobe.com/experience-manager/6-5/assets/using/brand-portal-configuring-integration.html), AEM Author uses a replication agent to replicate the selected asset(s) to Brand Portal cloud service for approved usage by Brand Portal users. 複数のレプリケーションエージェントを使用して、AEM 6.2 SP1-CFP5、AEM CFP 6.3.0.2以降を高速並列パブリッシングに使用します。

>[!NOTE]
>
>AEM Assets Brand Portal と AEM Assets を適切に連携させるには、AEM 6.4.1.0 にアップグレードすることを推奨します。AEM 6.4では、Brand portalとの統合を設定中にエラーが発生し、レプリケーションが失敗するという制限があります。

[!UICONTROL /etc/cloudservice] 下にブランドポータルのクラウドサービスを設定すると、必要なユーザーとトークンがすべて自動生成され、リポジトリに保存されます。クラウドサービスの設定が作成され、レプリケーションに必要なサービスユーザーと、コンテンツをレプリケートするためのレプリケーションエージェントも作成されます。これによって 4 つのレプリケーションエージェントが作成されます。したがって、AEMからBrand portalに多数のアセットを公開すると、これらのアセットは、ラウンドロビンを使用してこれらの複製エージェント間でキューに格納され、配布されます。

However, publishing can fail intermittently due to- large sling jobs, increased Network and [!UICONTROL Disk I/O] on AEM Author instance, or slowed performance of AEM Author instance. そのため、公開を開始する前に、レプリケーションエージェントとの接続テストをおこなうことをお勧めします。

![](assets/test-connection.png)

## Troubleshoot failures in first time publishing: validating your publish configuration {#troubleshoot-failures-in-first-time-publishing-validating-your-publish-configuration}

公開設定を検証するには、次のようにします。

1. エラーログを確認します。
1. レプリケーションエージェントが作成されているかを確認します。
1. 接続をテストします。

**クラウドサービスの作成時のテールログ**

直近のログを確認します。レプリケーションエージェントが作成されているかを確認します。レプリケーションエージェントの作成が失敗している場合は、クラウドサービスに小さな変更を加えることでクラウドサービスを編集します。検証をおこない、レプリケーションエージェントが作成されているかをもう一度確認します。作成されていない場合は、サービスを再編集します。

クラウドサービスを何度か編集しても適切に設定されない場合は、Daycare チケットを発行してください。

**レプリケーションエージェントとの接続テスト**

ログを参照して、レプリケーションログにエラーが記録されている場合は、次のようにします。

1. アドビサポートに問い合わせてください。

1. [クリーンアップ](../using/troubleshoot-parallel-publishing.md#clean-up-existing-config)を再試行し、公開設定をもう一度作成します。

<!--
Comment Type: remark
Last Modified By: Mini Gulati (mgulati)
Last Modified Date: 2018-06-21T22:56:21.256-0400
<p>?? check and compare public key. At times public key is different</p>
<p>?? another thing to check in /useradmin</p>
-->

### 既存の Brand Portal 公開設定のクリーンアップ {#clean-up-existing-config}

Most of the times when publishing is not working, the reason can be that the user who is publishing (for example: [!UICONTROL mac-&lt;tenantid&gt;-replication]) doesn't have the latest private key, and hence publish fails with "401 unauthorized" error and no other error is reported in replication agent logs. その場合は、トラブルシューティングをおこなうのではなく、新しい設定を作成することをお勧めします。新しい設定が正常に機能するように、AEM作成者の設定で次の内容をクリーンアップします。

1. go to [!UICONTROL localhost:4502/crx/de] (considering you are running author instance on [!UICONTROL localhost:4502]):\
   i.delete /etc/replication/agents.author/mp_replication*\
   ii. /etc/cloudservices/mediaportal/&lt;config_name&gt;を削除します。

1. [!UICONTROL localhost:4502/useradmin] に移動します。\
   iユーザー[!UICONTROL mac-&lt;tenantid&gt;-replicationii]を検索し、このユーザーを削除します

これによってシステム全体がクリーンアップされます。これで新しい      cloudservice  config and still use the already existing JWT application in [https://legacy-oauth.cloud.adobe.io/](https://legacy-oauth.cloud.adobe.io/). 新しいアプリケーションを作成する必要はなく、新しく作成したクラウド設定から公開鍵を更新するだけで構いません。

## Developer Connection の JWT アプリケーションテナントの可視性の問題 {#developer-connection-jwt-application-tenant-visibility-issue}

If on [https://legacy-oauth.cloud.adobe.io/](https://legacy-oauth.cloud.adobe.io/), all the  orgs  (tenants) for which the current users hold system administrator are listed. ここに組織名が表示されない場合や、必要なテナントのアプリケーションを作成できない場合は、そのための十分な（システム管理者の）権限を持っているかを確認してください。

このユーザーインターフェイスには、既知の問題が 1 つあります。つまり、どのテナントでも上位 10 件のアプリケーションしか表示されないことです。アプリケーションを作成したら、そのページにとどまり、URL をブックマークしてください。アプリケーションの一覧ページに移動して、自分が作成したアプリケーションを探す必要はありません。ブックマークした URL に直接アクセスして、いつでも必要なときにアプリケーションを更新または削除できます。

作成した JWT アプリケーションが適切にリストされない場合があります。そのため、JWT アプリケーションの作成中に URL をメモするかブックマークすることをお勧めします。

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

それまで問題なく Brand Portal への公開をおこなっていたレプリケーションエージェントが公開ジョブの処理を停止した場合は、レプリケーションログを確認してください。AEM には自動再試行の機能が組み込まれているので、特定のアセットの公開が失敗しても、自動的に再試行されます。ネットワークエラーなどの問題が断続的に発生している場合でも、再試行するうちに公開が成功することがあります。

継続的な発行エラーが発生し、キューがブロックされている場合は、接続のテスト **[!UICONTROL を確認し]** 、報告されるエラーの解決を試みる必要があります。

エラーの内容に基づき、サポートチケットを発行することもできます。その場合は Brand Portal のエンジニアリングチームが問題解決をお手伝いします。
