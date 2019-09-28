---
title: Brand Portal でのダイナミックビデオのサポート
seo-title: Brand Portal でのダイナミックビデオのサポート
description: Brand Portal でのダイナミックビデオのサポート
seo-description: Brand Portal でのダイナミックビデオのサポート
uuid: a3502a4d-3971-4ea4-953c-44ba04446269
contentOwner: mgulati
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: download-install
discoiquuid: e18d992a-a3b5-45f2-9696-8161993213ee
translation-type: tm+mt
source-git-commit: 86d4d5c358ea795e35db2dce8c9529ed14e9ee2d

---


# Brand Portal でのダイナミックビデオのサポート {#dynamic-video-support-on-brand-portal}

Dynamic Media をサポートしている Brand Portal でビデオをアダプティブにプレビューおよび再生します。また、ポータルおよび共有リンクから動的レンディションをダウンロードします。 Brand Portal を使用すると、次のことが可能になります。

* アセットの詳細ページ、カード表示、リンク共有のプレビューページでビデオをプレビューする。
* アセットの詳細ページでビデオエンコードを再生する。
* アセットの詳細ページの「レンディション」タブで動的レンディションを表示する。
* ビデオを格納したフォルダーとビデオエンコードをダウンロードする。

>[!NOTE]
>
>To work with videos and to publish them to Brand Portal, make sure that your AEM Author instance is set up either on Dynamic Media Hybrid mode or Dynamic Media [!DNL Scene 7] mode.

ビデオをプレビュー、再生、ダウンロードするために、Brand Portal では次の 2 つの設定を管理者に公開しています。

* [ダイナミックメディアハイブリッ](#configure-dm-hybrid-settings)ド設定：AEM作成者インスタンスがダイナミックメディアハイブリッドモードで実行されている場合。
* [ダイナミックメディア[!DNL Scene 7]の設定](#configure-dm-scene7-settings)AEM作成者インスタンスがダイナミックメディアモードで実行され[!DNL Scene 7] ている場合。
Brand Portal テナントの複製先となる AEM オーサーインスタンスに指定した設定に基づいて、これらの設定のいずれかを指定します。

>[!NOTE]
>
>Dynamic videos are not supported on Brand Portal tenants integrated with AEM Author running on [!UICONTROL Scene7Connect] runmode.

## ダイナミックビデオの再生方法{#how-are-dynamic-videos-played}

![ビデオエンコードはクラウドから取得される](assets/VideoEncodes.png)

If Dynamic Media configurations ([Hybrid](../using/dynamic-video-brand-portal.md#configure-dm-hybrid-settings) or [[!DNL Scene 7]](../using/dynamic-video-brand-portal.md#configure-dm-scene7-settings) configurations) are set up on Brand Portal, the dynamic renditions are fetched from [!DNL Scene 7] server. したがって、ビデオエンコードは遅延や品質の劣化なしにプレビューおよび再生されます。

As video encodes are not stored in Brand Portal repository and are fetched from [!DNL Scene 7] server, ensure that the Dynamic Media configurations on AEM Author Instance and Brand Portal are the same.

>[!NOTE]
>
>Brand Portal では、ビデオビューアとビューアプリセットはサポートされません。ビデオは Brand Portal のデフォルトのビューアでプレビューおよび再生されます。

## 前提条件 {#prerequisites}

Brand Portal 上でダイナミックビデオを操作するには、必ず以下をおこなってください。

* **AEM作成者をDMで起動（ダイナミックメディア）モード** Dynamic Media Hybridモードまたは [Dynamic Media [!DNL Scene 7]モードで、AEM作成者インスタンス（Brand portalの統合に使用）を起動します](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dynamic.html#EnablingDynamicMedia)[](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dms7.html#EnablingDynamicMediainScene7mode)。
* **AEM AuthorでのDynamic Media cloudサービスの設定AEM Authorが実行しているダイナミックメディアモードに基づいて、ツールから** AEM Authorで [Dynamic Media cloudサービス](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dynamic.html#ConfiguringDynamicMediaCloudServices) [!DNL Scene 7]クラウドサービスを設定 [します](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dms7.html#ConfiguringDynamicMediaCloudServices)**** 。|クラ **ウドサービス** |ダイナ **ミックメディア**。
* **Configure Dynamic Media on Brand Portal**
Based on the Dynamic Media cloud configurations on AEM Author, configure [Dynamic Media settings](#configure-dm-hybrid-settings) or [[!DNL Scene 7] settings](#configure-dm-scene7-settings)  from Brand Portal administrative tools.
Make sure that [separate Brand Portal tenants](#separate-tenants) are used for AEM Author instances configured with Dynamic Media Hybrid and Dynamic Media [!UICONTROL Scene7] modes, if you are using functionalities of Dynamic Media Hybrid and Dynamic Media [!UICONTROL S7].
* **Brand portalに適用されたビデオエンコードを含むフォルダーを発行**&#x200B;す [るビデオエンコードを適用し](https://helpx.adobe.com/experience-manager/6-5/assets/using/video-profiles.html) 、AEM AuthorインスタンスからBrand portalにリッチメディアアセットを含むフォルダーを発行します。
* **セキュアプレビューが有効な場合** Scene7のホワイトリスト出力IPs Dynamic Media-[!DNL Scene 7] (会社のセキュアプレビューが有効な場合 [)を使用する場合、会社の管理者は、各SPS](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html) SPS [!DNL Scene 7] SPS [SPS SPS](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html#testing-the-secure-testing-service) SPS SCENE公開システム（UIフラッシュ）を使用している場合)を公開
エグレス IP は次のとおりです。

| **地域** | **エグレス IP** |
|--- |--- |
| 該当なし | 192.243.237.86 |
| EMEA | 185.34.189.4 |
| APAC | 63.140.44.54 |

To whitelist either of these egress IPs, see [prepare your account for secure testing service](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html#testing-the-secure-testing-service).

## ベストプラクティス

ダイナミックビデオアセットが Brand Portal（および共有リンク）から正常にプレビュー、再生、ダウンロードされるようにするには、次のベストプラクティスに従います。

### Dynamic Media ハイブリッドモードと Dynamic Media Scene7 モードでテナントが異なる {#separate-tenants}

If you are using both Dynamic Media [!DNL Scene 7] and Dynamic Media Hybrid features, it is advised that you use different Brand Portal tenants for AEM Author instances configured with Dynamic Media Hybrid and Dynamic Media [!DNL Scene 7] modes.<br />

![オーサーと BP が 1 対 1 に対応](assets/BPDynamicMedia.png)

### AEM オーサーインスタンスと Brand Portal で設定の詳細が同じ

[!UICONTROL Dynamic], [!UICONTROL Registration ID], [!DNL Scene 7]Video Service URL (Dynamic Media Hybrid Title, Dynamic Media Email Email, PasswordEmailEmail, PasswordEMediaIn,MandiaInManMeManyMeポータルとAEMクラウドの設定を参照してください。

### Dynamic Media Scene7 モードの公開エグレス IP をホワイトリストに登録する

If Dynamic Media Scene 7–having secure preview enabled–is used to serve video assets to Brand Portal, then Scene 7 establishes a dedicated image server for staging environments or internal applications. [](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html)このサーバーへのリクエストはすべて、発信元 IP アドレスをチェックします。受信リクエストが IP アドレスの承認済みリストに含まれていない場合は、失敗のレスポンスが返されます。The [!UICONTROL Scene-7] Company Administrator, therefore, configures an approved list of IP addresses for their company’s [!UICONTROL Secure Testing] environment, through [!UICONTROL SPS] (Scene-7 Publishing System) flash UI. 該当するそれぞれの地域のエグレス IP（以下を参照）を、その承認済みリストに必ず追加してください。To whitelist either of these egress IPs, see [prepare your account for secure testing service](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html#testing-the-secure-testing-service).
エグレス IP は次のとおりです。

| **地域** | **エグレス IP** |
|--- |--- |
| 該当なし | 192.243.237.86 |
| EMEA | 185.34.189.4 |
| APAC | 63.140.44.54 |

## Dynamic Media ハイブリッドの設定 {#configure-dm-hybrid-settings}

If AEM Author instance is running on dynamic media hybrid mode, then use [!UICONTROL Video] tile from administrative tools panel to configure Dynamic Media gateway settings.
>[!NOTE]
>
>The [video encoding profiles](https://helpx.adobe.com/experience-manager/6-5/assets/using/video-profiles.html) are not published to Brand Portal, instead are fetched from the [!UICONTROL Scene 7] server. Therefore, for video encodes to be played successfully in Brand Portal, ensure that the configuration details are the same as the [[!UICONTROL Scene7 cloud configuration]](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dms7.html#ConfiguringDynamicMediaCloudServices) in your AEM Author instance.
Brand Portal テナントで Dynamic Media 設定をセットアップするには：

1. Brand Portal で上部のツールバーにある AEM ロゴをクリックして、管理ツールにアクセスします。

2. From the administrative tools panel, select the **[!UICONTROL Video]** tile.<br />
   ![Brand Portal での Dynamic Media ハイブリッドの設定](assets/DMHybrid-Video.png)
   **[!UICONTROL Dynamic Media 設定を編集]**&#x200B;ページが開きます。<br />
   ![Brand Portal での Dynamic Media ハイブリッドの設定](assets/edit-dynamic-media-config.png)

3. Specify **[!UICONTROL Registration ID]** and **[!UICONTROL Video Service URL]** (DM-Gateway URL). これらの詳細が、AEM オーサーインスタンスの&#x200B;**[!UICONTROL ツール／クラウドサービス]で指定した詳細と同じであることを確認してください。**

4. 「**保存**」をクリックして、設定を保存します。

## Dynamic Media Scene7 の設定 {#configure-dm-scene7-settings}

If AEM Author instance is running on Dynamic Media- [!UICONTROL Scene 7] mode, then use **[!UICONTROL Dynamic Media Configuration]** tile from administrative tools panel to configure the [!UICONTROL Scene 7] server settings.

To set up Dynamic Media [!UICONTROL Scene 7] configurations on Brand Portal tenants:

1. Brand Portal で上部のツールバーにある AEM ロゴをクリックして、管理ツールにアクセスします。

2. From the administrative tools panel, select the **[!UICONTROL Dynamic Media Configuration]** tile.<br />
   ![[!UICONTROL Brand Portal での Dynamic Media Scene7 の設定]](assets/DMS7-Tile.png)
   [!UICONTROL Dynamic Media 設定を編集]ページが開きます。<br />
   ![Brand Portal での Scene7 の設定](assets/S7Config.png)

3. 以下を指定します。
   * [!UICONTROL タイトル]
   * Credentials ([!UICONTROL Email ID] and [!UICONTROL Password]) to access the Scene 7 server
   * [!UICONTROL Region]
Make sure these values are the same as those in your AEM Author instance.

4. Select **[!UICONTROL Connect to Dynamic Media]**.

5. **[!UICONTROL 会社名]**&#x200B;を指定し、設定を&#x200B;**保存[!UICONTROL します。]**
