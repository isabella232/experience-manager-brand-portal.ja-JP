---
title: Brand Portal への並列公開における問題のトラブルシューティング
seo-title: Troubleshoot issues in parallel publishing to Brand Portal
description: 並列公開における問題のトラブルシューティングです。
seo-description: Troubleshoot parallel publishing.
uuid: 51e45cca-8c96-4c69-84ef-2ef34f3bcde2
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: brand-portal
discoiquuid: a4801024-b509-4c51-afd8-e337417e658b
role: Admin
exl-id: 631beabc-b145-49ba-a8e4-f301497be6da
source-git-commit: 96ce77b306c207bb20e0fdc56dd218295fbaeffe
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 57%

---

# Brand Portal への並列公開における問題のトラブルシューティング {#troubleshoot-issues-in-parallel-publishing-to-brand-portal}

Brand Portal と AEM Assets の連携を設定すると、承認済みブランドアセットを AEM Assets オーサーインスタンスからシームレスに取り込む（または公開する）ことができます。[設定](../using/configure-aem-assets-with-brand-portal.md)が完了すると、Experience Manager作成者は、レプリケーションエージェントを使用して、選択されたアセットをBrand Portal Cloud Serviceにレプリケートし、Brand Portalユーザーが使用できる状態にします。 Experience Manager6.2 SP1-CFP5、Experience ManagerCFP 6.3.0.2およびそれ以降では、高速な並列公開を実現するために複数のレプリケーションエージェントが使用されています。

>[!NOTE]
>
>Adobeでは、AEM Assets Brand PortalがAEM Assetsで正常に設定されるように、Experience Manager6.4.1.0にアップグレードすることをお勧めします。 Experience Manager6.4では、Brand PortalでAEM Assetsを設定する際にエラーが発生し、レプリケーションが失敗します。

**[!UICONTROL /etc/cloudservice]**&#x200B;の下でBrand Portalのクラウドサービスを設定すると、必要なすべてのユーザーとトークンが自動生成され、リポジトリに保存されます。 クラウドサービスの設定が作成され、レプリケーションに必要なサービスユーザーと、コンテンツをレプリケートするためのレプリケーションエージェントも作成されます。4つのレプリケーションエージェントを作成します。 したがって、多数のアセットをExperience ManagerからBrand Portalに公開する場合、アセットはキューを形成し、レプリケーションエージェント間でラウンドロビンを通じて配布されます。

ただし、大きなSlingジョブや、Experience Managerオーサーインスタンス上のネットワークおよび&#x200B;**[!UICONTROL ディスクI/O]**&#x200B;の増加、Experience Managerオーサーインスタンスのパフォーマンスの低下などの理由で、公開が断続的に失敗する場合があります。 したがって、公開を開始する前に、レプリケーションエージェントとの接続テストをお勧めします。

![](assets/test-connection.png)

## 初回公開で失敗した場合のトラブルシューティング：公開設定の検証 {#troubleshoot-failures-in-first-time-publishing-validating-your-publish-configuration}

公開設定を検証するには、次のようにします。

1. エラーログを確認します。
1. レプリケーションエージェントが作成されているかを確認します。
1. 接続をテストします。

**Cloud Service 作成時のテールログ**

直近のログを確認します。レプリケーションエージェントが作成されているかどうかを確認します。レプリケーションエージェントの作成が失敗している場合は、クラウドサービスに小さな変更を加えることでクラウドサービスを編集します。検証をおこない、レプリケーションエージェントが作成されているかをもう一度確認します。作成されていない場合は、サービスを再編集します。

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

公開がうまくいかない場合によくある原因は、公開を実行するユーザー（例：`mac-<tenantid>-replication`）が最新の秘密鍵を持っていないことです。そのため、公開が「401 Unauthorized」エラーで失敗し、レプリケーションエージェントログに他のエラーは記録されません。トラブルシューティングを避け、代わりに設定を作成することができます。 新しい設定を正しく機能させるには、Experience Manager作成者の設定で以下をクリーンアップします。

1. `localhost:4502/crx/de/` に移動します（localhost でオーサーインスタンスを実行していると仮定）。:4502:\
   i. `/etc/replication/agents.author/mp_replication` を削除します。
ii.次を削除します。 
`/etc/cloudservices/mediaportal/<config_name>`

1. localhost:4502/useradmin に移動します。\
   i. ユーザー `mac-<tenantid>replication` を検索します。
ii.このユーザーを削除します。

これによってシステム全体がクリーンアップされます。これで、クラウドサービス設定を作成し、既存のJWTアプリケーションを引き続き使用できます。 アプリケーションを作成する必要はなく、新しく作成したクラウド設定から公開鍵を更新します。

>[!NOTE]
>
>自動生成された設定は変更しないでください。


## Developer Connection の JWT アプリケーションテナントの可視性の問題 {#developer-connection-jwt-application-tenant-visibility-issue}

`https://legacy-oauth.cloud.adobe.io/` 上であれば、現在のユーザーがシステム管理者を抱えているすべての組織（テナント）が一覧表示されます。ここに組織名が見つからない場合や、必要なテナントのアプリケーションを作成できない場合は、十分な（システム管理者）権限があるかどうかを確認してください。

このユーザーインターフェイスには、既知の問題が1つあります。どのテナントでも上位10件のアプリケーションしか表示されません。 アプリケーションを作成したら、そのページにとどまり、URL をブックマークしてください。アプリケーションの一覧ページに移動して、自分が作成したアプリケーションを探す必要はありません。ブックマークした URL に直接アクセスして、いつでも必要なときにアプリケーションを更新または削除できます。

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

(Brand Portalへの公開に問題なく発行していた)レプリケーションエージェントが公開ジョブの処理を停止した場合は、レプリケーションログを確認します。 Experience Managerには自動再試行の機能が組み込まれているので、特定のアセットの公開が失敗した場合、自動的に再試行されます。 ネットワークエラーなど、断続的な問題がある場合は、再試行中に成功する可能性があります。

公開エラーが引き続き発生し、キューがブロックされる場合は、**[!UICONTROL 接続テスト]**&#x200B;の結果を確認し、報告されるエラーの解決を試みてください。

エラーの内容に基づき、サポートチケットを発行することもできます。その場合は Brand Portal のエンジニアリングチームが問題解決をお手伝いします。


## 接続タイムアウトエラーを回避するためのレプリケーションエージェントの設定 {#connection-timeout}

ジョブの公開がタイムアウトエラーで失敗する場合は、通常、レプリケーションキューに保留中のリクエストが複数あります。この問題を解決するには、タイムアウトを回避するようにレプリケーションエージェントを設定します。

レプリケーションエージェントを設定するには：

1. AEM Assets オーサーインスタンスにログインします。
1. **ツール**&#x200B;パネルで、**[!UICONTROL デプロイメント]**／**[!UICONTROL レプリケーション]**&#x200B;に移動します。
1. レプリケーションページで、「**[!UICONTROL 作成者のエージェント]**」をクリックします。Brand Portal テナントの 4 つのレプリケーションエージェントを表示できます。
1. レプリケーションエージェントのURLをクリックし、「**[!UICONTROL 編集]**」をクリックします。
1. エージェントの設定で「**[!UICONTROL 拡張]**」タブをクリックします。
1. 「**[!UICONTROL 接続を閉じる]**」チェックボックスをオンにします。
1. 手順 4～7 を繰り返して、4 つのレプリケーションエージェントをすべて設定します。
1. サーバーを再起動します。
