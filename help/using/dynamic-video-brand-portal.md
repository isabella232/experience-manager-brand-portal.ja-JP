---
title: Brand Portal でのダイナミックビデオのサポート
seo-title: Brand Portal でのダイナミックビデオのサポート
description: Brand Portal でのダイナミックビデオのサポート
seo-description: Brand Portal でのダイナミックビデオのサポート
uuid: a3502a4d-3971-4ea4-953c-44ba04446269
contentOwner: ムムラティ
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
content-type: reference
topic-tags: ダウンロードインストール
discoiquuid: e18d992a- a3b5-45f2-9696-8161993213ee
translation-type: tm+mt
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# Brand Portal でのダイナミックビデオのサポート {#dynamic-video-support-on-brand-portal}

Dynamic Media をサポートしている Brand Portal でビデオをアダプティブにプレビューおよび再生します。ポータルおよび共有リンクから動的レンディションをダウンロードします。
 Brand Portal を使用すると、次のことが可能になります。

* アセットの詳細ページ、カード表示、リンク共有のプレビューページでビデオをプレビューする。
* アセットの詳細ページでビデオエンコードを再生する。
* アセットの詳細ページの「レンディション」タブで動的レンディションを表示する。
* ビデオを格納したフォルダーとビデオエンコードをダウンロードする。

>[!NOTE]
>
>To work with videos and to publish them to Brand Portal, make sure that your AEM Author instance is set up either on Dynamic Media Hybrid mode or Dynamic Media [!DNL Scene 7] mode.

ビデオをプレビュー、再生、ダウンロードするために、Brand Portal では次の 2 つの設定を管理者に公開しています。

* [Dynamic Mediaハイブリッド設定](#configure-dm-hybrid-settings)（AEM作成者インスタンスがダイナミックメディアハイブリッドモードで実行されている場合）
* [ダイナミックメディア[!DNL Scene7] AEM作成者インスタンス](#configure-dm-scene7-settings)がダイナミックメディア[!DNL Scene 7] モードで実行されている場合に設定。
Brand Portal テナントの複製先となる AEM オーサーインスタンスに指定した設定に基づいて、これらの設定のいずれかを指定します。

>[!NOTE]
>
>Dynamic videos are not supported on Brand Portal tenants integrated with AEM Author running on [!UICONTROL Scene7Connect] runmode.

## How are dynamic videos played? {#how-are-dynamic-videos-played}

![ビデオエンコードはクラウドから取得される](assets/VideoEncodes.png)

If Dynamic Media configurations ([Hybrid](../using/dynamic-video-brand-portal.md#configure-dm-hybrid-settings) or [[!DNL Scene 7]](../using/dynamic-video-brand-portal.md#configure-dm-scene7-settings) configurations) are set up on Brand Portal, the dynamic renditions are fetched from [!DNL Scene 7] server. したがって、ビデオエンコードは遅延や品質の劣化なしにプレビューおよび再生されます。

As video encodes are not stored in Brand Portal repository and are fetched from [!DNL Scene 7] server, ensure that the Dynamic Media configurations on AEM Author Instance and Brand Portal are the same.

>[!NOTE]
>
>Brand Portal では、ビデオビューアとビューアプリセットはサポートされません。ビデオは Brand Portal のデフォルトのビューアでプレビューおよび再生されます。

## 前提条件 {#prerequisites}

Brand Portal 上でダイナミックビデオを操作するには、必ず以下をおこなってください。

* **AEM Author on DM（Dynamic Media）モード**の起動:
 [Dynamic Mediaハイブリッドモード](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dynamic.html#EnablingDynamicMedia) または [Dynamic Media[!DNL Scene7]モード](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dms7.html#EnablingDynamicMediainScene7mode)。
* **AEM作成者**&#x200B;の動的メディアクラウドサービスの設定AEM作成者の動的メディアモードの実行中、 [Dynamic Mediaクラウドサービス](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dynamic.html#ConfiguringDynamicMediaCloudServices) のいずれかまたは [[!ツールからのAEM作成者](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dms7.html#ConfiguringDynamicMediaCloudServices) のDNL **Scene7]クラウドサービス** | **クラウドサービス** | **ダイナミックメディア**。
* **ダイナミックメディアの設定（AEM作成者のダイナミックメディアクラウド設定に**&#x200B;基づく）、ダイナミックメディア設定の設定 [](#configure-dm-hybrid-settings) 、 [または[!ブランドポータル管理ツール](#configure-dm-scene7-settings) からのDNL Scene7の設定。
Make sure that [separate Brand Portal tenants](#separate-tenants) are used for AEM Author instances configured with Dynamic Media Hybrid and Dynamic Media [!UICONTROL Scene7] modes, if you are using functionalities of Dynamic Media Hybrid and Dynamic Media [!UICONTROL S7].
* **ブランドポータル**&#x200B;適用 [ビデオエンコーディング](https://helpx.adobe.com/experience-manager/6-5/assets/using/video-profiles.html) に適用されたビデオエンコードを使用してフォルダーを公開し、AEM作成者インスタンスからブランドポータルにリッチメディアアセットを含むフォルダーを公開します。
* **ホワイトリストに登録されている場合、SPSで保護されたプレビュー機能**&#x200B;を有効にして[!DNL Scene 7] いる場合（会社に [セキュアプレビューを有効](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html) にした場合）、 [!DNL Scene 7] 会社管理者 [は、SPS（](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html#testing-the-secure-testing-service)[!UICONTROL Scene7] Publishing System）フラッシュUIを使用して、会社の管理者が各地域に対して公開IPアドレスをホワイトリストに登録することをお勧めします。
 エグレス IP は次のとおりです。

| **地域** | **エグレス IP** |
|--- |--- |
| NA | 192.243.237.86 |
| EMEA | 185.34.189.4 |
| APAC | 63.140.44.54 |

To whitelist either of these egress IPs, see [prepare your account for secure testing service](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html#testing-the-secure-testing-service).

## ベストプラクティス

ダイナミックビデオアセットが Brand Portal（および共有リンク）から正常にプレビュー、再生、ダウンロードされるようにするには、次のベストプラクティスに従います。

### ダイナミックメディアハイブリッドモードおよびダイナミックメディアScene7モードのための個別のテナント {#separate-tenants}

ダイナミックメディア [!DNL Scene 7] とダイナミックメディアハイブリッド機能の両方を使用している場合は、ダイナミックメディアのハイブリッドモードとダイナミックメディア [!DNL Scene 7] モードで設定されたAEM作成者インスタンスごとに異なるブランドポータルテナントを使用することをお勧めします。
![オーサーと BP が 1 対 1 に対応](assets/BPDynamicMedia.png)

### AEM作成者インスタンスおよびブランドポータルでの同じ設定の詳細

[!UICONTROL タイトル]、 [!UICONTROL 登録ID]、 [!UICONTROL ビデオサービスURL] （ [!UICONTROL ダイナミックメディアハイブリッド]内）、 [!UICONTROL タイトル]、資格情報（[!UICONTROL 電子メール] とパスワード）、 [!UICONTROL 地域]、 [!UICONTROL 会社] （ダイナミックメディア [!DNL Scene 7]）などの設定の詳細は、ブランドポータルと [!UICONTROL AEMクラウドの設定で同じ]です。

### Dynamic Media Scene7モード用のホワイトリストの公開IPモード

ビデオアセットをブランドポータルに提供するために、Dynamic Media [!UICONTROL Scene7]の [セキュアプレビューを有効にし](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html)た場合、 [!UICONTROL Scene7] はステージング環境または内部アプリケーション用に専用の画像サーバを確立します。このサーバーへのリクエストはすべて、発信元 IP アドレスをチェックします。受信リクエストが IP アドレスの承認済みリストに含まれていない場合は、失敗のレスポンスが返されます。The [!UICONTROL Scene-7] Company Administrator, therefore, configures an approved list of IP addresses for their company’s [!UICONTROL Secure Testing] environment, through [!UICONTROL SPS] (Scene-7 Publishing System) flash UI. 該当するそれぞれの地域のエグレス IP（以下を参照）を、その承認済みリストに必ず追加してください。To whitelist either of these egress IPs, see [prepare your account for secure testing service](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html#testing-the-secure-testing-service).
受信者のIPアドレスは次のとおりです。

| **地域** | **エグレス IP** |
|--- |--- |
| NA | 192.243.237.86 |
| EMEA | 185.34.189.4 |
| APAC | 63.140.44.54 |

## Dynamic Media ハイブリッドの設定 {#configure-dm-hybrid-settings}

If AEM Author instance is running on dynamic media hybrid mode, then use [!UICONTROL Video] tile from administrative tools panel to configure Dynamic Media gateway settings.
>[!NOTE]
>
>[ビデオエンコーディングプロファイル](https://helpx.adobe.com/experience-manager/6-5/assets/using/video-profiles.html) は、代わりにScene7  サーバから取得され、ブランドポータルに公開されません。Therefore, for video encodes to be played successfully in Brand Portal, ensure that the configuration details are the same as the [[!UICONTROL Scene7 cloud configuration]](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dms7.html#ConfiguringDynamicMediaCloudServices) in your AEM Author instance.
Brand Portal テナントで Dynamic Media 設定をセットアップするには：

1. Brand Portal で上部のツールバーにある AEM ロゴをクリックして、管理ツールにアクセスします。

2. From the administrative tools panel, select the **[!UICONTROL Video]** tile.

![Brand Portal での Dynamic Media ハイブリッドの設定](assets/DMHybrid-Video.png)

**[!UICONTROL ダイナミックメディア設定]** ページが開きます。

![Brand Portal での Dynamic Media ハイブリッドの設定](assets/edit-dynamic-media-config.png)

3. **[!UICONTROL 登録ID]** および **[!UICONTROL ビデオサービスURL]** （DM- Gateway URL）を指定します。これらの詳細が、AEM オーサーインスタンスの&#x200B;**[!UICONTROL ツール／クラウドサービス]で指定した詳細と同じであることを確認してください。**

4. 「**保存**」をクリックして、設定を保存します。

## Dynamic Media Scene7 の設定 {#configure-dm-scene7-settings}

If AEM Author instance is running on Dynamic Media- [!UICONTROL Scene 7] mode, then use **[!UICONTROL Dynamic Media Configuration]** tile from administrative tools panel to configure the [!UICONTROL Scene 7] server settings.

To set up Dynamic Media [!UICONTROL Scene 7] configurations on Brand Portal tenants:

1. Brand Portal で上部のツールバーにある AEM ロゴをクリックして、管理ツールにアクセスします。

2. From the administrative tools panel, select the **[!UICONTROL Dynamic Media Configuration]** tile.
   ![[!UICONTROL Brand Portal での Dynamic Media Scene7 の設定]](assets/DMS7-Tile.png)

[!UICONTROL ダイナミックメディア設定] ページが開きます。

![Brand Portal での Scene7 の設定](assets/S7Config.png)

3. 以下を指定します。
   * [!UICONTROL タイトル]
   * Credentials ([!UICONTROL Email ID] and [!UICONTROL Password]) to access the Scene 7 server
   * [!UICONTROL リージョン]これらの値がAEM作成者インスタンスの値と同じであることを確認してください。

4. Select **[!UICONTROL Connect to Dynamic Media]**.

5. **[!UICONTROL 会社名]**&#x200B;を入力し、設定 **[!UICONTROL を保存]** します。
