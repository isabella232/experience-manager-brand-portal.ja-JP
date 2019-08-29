---
title: アセットのダウンロード
seo-title: アセットのダウンロード
description: すべてのユーザーが、複数のアセットやフォルダーを同時にダウンロードできます。これにより、承認されたブランドアセットを安全に配布して、オフラインで使用できます。
seo-description: すべてのユーザーが、複数のアセットやフォルダーを同時にダウンロードできます。これにより、承認されたブランドアセットを安全に配布して、オフラインで使用できます。
uuid: 4b57118e- a76e-4d8a-992a- cb3c3097bc03
content-type: reference
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
topic-tags: ダウンロードインストール
discoiquuid: f90c2214- beea-4695-9102-8b952bc9fd17
translation-type: tm+mt
source-git-commit: 32c3cdb8e3fafd74cfb36e6bcfe0811e7152b2d0

---


# アセットのダウンロード {#download-assets}

All users can simultaneously download multiple assets and folders accessible to them from [!DNL Brand Portal]. これにより、承認されたブランドアセットを安全に配布して、オフラインで使用できます。Read on to know how to download approved assets from [!DNL Brand Portal], and what to expect from the [download performance](../using/brand-portal-download-users.md#main-pars-header).

>[!NOTE]
>
>有効期限が切れたアセットをダウンロードできるのは、管理者のみです。有効期限が切れたアセットについて詳しくは、[アセットのデジタル著作権の管理](../using/manage-digital-rights-of-assets.md)を参照してください。

## アセットのダウンロード手順 {#steps-to-download-assets}

To download assets or folders containing assets for [!DNL Brand Portal], follow these steps:

1. [!DNL Brand Portal] インターフェイスから、次のいずれかの操作を行います。

   * ダウンロードするフォルダーまたはアセットを選択します。From the toolbar at the top, click the **Download** icon.
   ![](assets/downloadassets-1.png)

   * 1 つのフォルダーまたはアセットをダウンロードするには、そのフォルダーまたはアセットの上にマウスポインターを置きます。From the quick action thumbnails available, click the **Download** icon.
   ![](assets/downloadsingleasset-1.png)

   >[!NOTE]
   >
   >ダウンロードするアセットに、ライセンスが必要なアセットが含まれている場合は、**著作権管理**&#x200B;ページにリダイレクトされます。このページで、アセットを選択し、「**同意する**」をクリックし、「**ダウンロード**」をクリックします。「同意しない」を選択した場合は、ライセンスが必要なアセットはダウンロードされません。\
   >License-protected assets have [license agreement attached](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) to them, which is done by setting asset's [metadata property](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) in [!DNL AEM] Assets.

   ![](assets/licensed-asset-download-1.png)

   **ダウンロード** ダイアログボックスがデフォルトで選択されている **状態で、ダウンロード** ダイアログボックスが表示されます。

   ![](assets/donload-assets-dialog-1.png)

   >[!NOTE]
   >
   >If the assets you are downloading are image files, and you select only the **Asset(s)** option in Download dialog but are not [authorized by the administrator to have access to the original renditions of image files](../using/brand-portal-adding-users.md#main-pars-procedure-202029708) then no image files are downloaded and a Notice prompts, stating that you have been restricted by administrator to access original renditions.

   ![](assets/restrictaccess-note.png)

2. To download the renditions of assets in addition to the assets, select **Rendition(s)**. However, to allow auto-generated renditions to download along with custom renditions, deselect **Exclude Auto Generated Renditions**, which is selected by default.

   ![](assets/exclude-auto-renditions.png)

   To download only the renditions, deselect **Asset(s)**.

   >[!NOTE]
   >
   >デフォルトでは、アセットのみがダウンロードされます。However, original renditions of image files are not downloaded if you are not [authorized by the administrator to have access to the original renditions of image files](../using/brand-portal-adding-users.md#main-pars-procedure-202029708).

   * To speed up the download of asset files from [!DNL Brand Portal], select **Enable download acceleration** option and [follow the wizard](../using/accelerated-download.md#main-pars-header-405749062). To know more about faster download of assets refer [Guide to accelerate downloads from [!DNL Brand Portal]](../using/accelerated-download.md).

   * [アセットとそのレンディションにカスタムの画像プリセット](../using/brand-portal-image-presets.md#applyimagepresetswhendownloadingimages)を適用するには、「**動的レンディション**」チェックボックスをオンにします。カスタムの画像プロパティ（サイズ、フォーマット、カラースペース、解像度および画像の修飾子）を指定して、アセットとそのレンディションをダウンロードするときにカスタムの画像プリセットを適用します。動的レンディションのみをダウンロードするには、「**アセット**」チェックボックスをオフにします。
   ![](assets/dynamic-renditions.png)

   >[!NOTE]
   >
   >To preview (or download) dynamic renditions of any asset, ensure that the dynamic media is enabled and the asset's [!UICONTROL Pyramid tiff] rendition exists at the [!DNL AEM] author instance, from where the assets have been published. When an asset is published to [!DNL Brand Portal], its [!UICONTROL Pyramid tiff] rendition is also published. [!UICONTROL ピラミッドTIFF] レンディションを生成する方法はあり [!DNL Brand Portal]ません。

   * To preserve the [!DNL Brand Portal] folder hierarchy while downloading assets, select **Create separate folder for each asset**. By default, [!DNL Brand Portal] folder hierarchy is ignored and all assets are downloaded in one folder in your local system.

   * To send an email notification to users with a link for downloading the assets, select **Email**.
   ![](assets/download-link.png)

   >[!NOTE]
   >
   >電子メール通知に含まれるダウンロードリンクの有効期限は 45 日間です。
   >
   >Administrators can customize email messages, that is, logo, description, and footer, using the [Branding](../using/brand-portal-branding.md) feature.

3. 「**ダウンロード**」をクリックします。

   アセット（および選択されている場合はレンディション）が ZIP ファイルとしてローカルフォルダーにダウンロードされます。ただし、レンディションなしで 1 つのアセットをダウンロードした場合、zip ファイルは作成されないので、すばやくダウンロードを行うことができます。

   [オリジナルのレンディションへのアクセスを管理者によって許可](../using/brand-portal-adding-users.md#main-pars-procedure-202029708)されていない場合、選択したアセットのオリジナルのレンディションはダウンロードされません。

   >[!NOTE]
   >
   >個別に選択してダウンロードしたアセットは、ダウンロードされたアセットレポートに表示されます。ただし、アセットを含むフォルダがダウンロードされている場合、ダウンロードされたアセットには、フォルダとアセットのどちらも表示されません。

   To know how to download assets from shared links, refer [downloading assets from shared links](../using/brand-portal-link-share.md#main-pars-header-1703469193).

## 期待されるダウンロードパフォーマンス {#expected-download-performance}

ファイルのダウンロードエクスペリエンスは、ローカルインターネット接続やサーバー遅延などの要因によって異なります。The expected download performance for 2 GB file observed at different client locations is as follows, with [!DNL Brand Portal] server at Oregon in United States:

| クライアントの場所 | クライアントとサーバーの間のレイテンシ | 予想されるダウンロード速度 | 2GBのファイルのダウンロードにかかる時間 |
|-------------------------|-----------------------------------|-------------------------|------------------------------------|
| 米国西部（北カリフォルニア） | 18 ミリ秒 | 7.68 MB/秒 | 4 分 |
| 米国西部（オレゴン） | 42 ミリ秒 | 3.84 MB/秒 | 9 分 |
| 米国東部（北バージニア） | 85 ミリ秒 | 1.61 MB/秒 | 21 分 |
| APAC（東京） | 124 ミリ秒 | 1.13 MB/秒 | 30 分 |
| ノイダ | 275 ミリ秒 | 0.5 MB/秒 | 68 分 |
| シドニー | 175 ミリ秒 | 0.49 MB/秒 | 69 分 |
| ロンドン | 179 ミリ秒 | 0.32 MB/秒 | 106 分 |
| シンガポール | 196 ミリ秒 | 0.5 MB/秒 | 68 分 |

**注意**:参照データはテスト条件で観察されます。これは、異なる場所のユーザーによって異なる待ち時間や帯域幅が表示される場合があります。
