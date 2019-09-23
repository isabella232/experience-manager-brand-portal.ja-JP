---
title: アセットのダウンロード
seo-title: アセットのダウンロード
description: すべてのユーザーが、複数のアセットやフォルダーを同時にダウンロードできます。これにより、承認されたブランドアセットを安全に配布して、オフラインで使用できます。
seo-description: すべてのユーザーが、複数のアセットやフォルダーを同時にダウンロードできます。これにより、承認されたブランドアセットを安全に配布して、オフラインで使用できます。
uuid: 4b57118e-a76e-4d8a-992a-cb3c3097bc03
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: download-install
discoiquuid: f90c2214-beea-4695-9102-8b952bc9fd17
translation-type: tm+mt
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# アセットのダウンロード {#download-assets}

すべてのユーザーが、Brand Portal から複数のアセットやフォルダーを同時にダウンロードできます。これにより、承認されたブランドアセットを安全に配布して、オフラインで使用できます。Brand Portal から承認済みアセットをダウンロードする方法や、[ダウンロードパフォーマンス](../using/brand-portal-download-users.md#main-pars-header)から期待されることについてお読みください。

>[!NOTE]
>
>有効期限が切れたアセットをダウンロードできるのは、管理者のみです。有効期限が切れたアセットについて詳しくは、[アセットのデジタル著作権の管理](../using/manage-digital-rights-of-assets.md)を参照してください。

## アセットのダウンロード手順 {#steps-to-download-assets}

Brand Portal のアセット、またはアセットを含むフォルダーをダウンロードするには、次の手順に従います。

1. From the Brand Portal interface, do one of the following:

   * ダウンロードするフォルダーまたはアセットを選択します。上部のツールバーで「**[!UICONTROL ダウンロード]」アイコンをクリックします。**
   ![](assets/downloadassets-1.png)

   * 1 つのフォルダーまたはアセットをダウンロードするには、そのフォルダーまたはアセットの上にマウスポインターを置きます。使用できるクイックアクションサムネールから、**[!UICONTROL ダウンロード]アイコンをクリックします。**
   ![](assets/downloadsingleasset-1.png)

   >[!NOTE]
   >
   >ダウンロードするアセットに、ライセンスが必要なアセットが含まれている場合は、**[!UICONTROL 著作権管理]ページにリダイレクトされます。** In this page, select the assets, click **[!UICONTROL Agree]**, and then click **[!UICONTROL Download]**. 「同意しない」を選択した場合は、ライセンスが必要なアセットはダウンロードされません。\
   >License-protected assets have [license agreement attached](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) to them, which is done by setting asset's [metadata property](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) in AEM Assets.

   ![](assets/licensed-asset-download-1.png)

   **[!UICONTROL ダウンロード]**&#x200B;ダイアログボックスが表示されます。デフォルトで「**アセット[!UICONTROL 」チェックボックスがオンになっています。]**

   ![](assets/donload-assets-dialog-1.png)

   >[!NOTE]
   >
   >ダウンロードしようとするアセットが画像ファイルで、ダウンロードダイアログで「**[!UICONTROL アセット]**」オプションのみを選択しているが、[画像ファイルのオリジナルのレンディションへのアクセス権が管理者によって許可](../using/brand-portal-adding-users.md#main-pars-procedure-202029708)されていない場合は、画像ファイルはダウンロードされず、オリジナルのレンディションへのアクセスが管理者によって制限されていることを示す通知が表示されます。

   ![](assets/restrictaccess-note.png)

2. To download the renditions of assets in addition to the assets, select **[!UICONTROL Rendition(s)]**. However, to allow auto-generated renditions to download along with custom renditions, deselect **[!UICONTROL Exclude Auto Generated Renditions]**, which is selected by default.

   ![](assets/exclude-auto-renditions.png)

   To download only the renditions, deselect **[!UICONTROL Asset(s)]**.

   >[!NOTE]
   >
   >デフォルトでは、アセットのみがダウンロードされます。ただし、[画像ファイルのオリジナルのレンディションへのアクセスが管理者によって許可](../using/brand-portal-adding-users.md#main-pars-procedure-202029708)されていない場合は、画像ファイルのオリジナルのレンディションはダウンロードされません。

   * Brand Portal からのアセットファイルのダウンロードをスピードアップさせるには、「**[!UICONTROL ダウンロードアクセラレーションの有効化]**」オプションを選択し、[ウィザードに従います](../using/accelerated-download.md#main-pars-header-405749062)。To know more about faster download of assets refer [guide to accelerate downloads from Brand Portal](../using/accelerated-download.md).

   * To apply a [custom image preset to the asset and its renditions](../using/brand-portal-image-presets.md#applyimagepresetswhendownloadingimages), select **[!UICONTROL Dynamic Rendition(s)]**. カスタムの画像プロパティ（サイズ、フォーマット、カラースペース、解像度および画像の修飾子）を指定して、アセットとそのレンディションをダウンロードするときにカスタムの画像プリセットを適用します。動的なレンディションのみをダウンロードするには、 アセット **[!UICONTROL を選択します]**。
   ![](assets/dynamic-renditions.png)

   >[!NOTE]
   >
   >アセットの動的レンディションをプレビュー（またはダウンロード）するには、動的メディアが有効で、アセットのピラミッドTIFFレンディションがAEM作成者インスタンスに存在し、アセットの公開元であることを確認します。 アセットがBrand Portalに公開されると、ピラミッドTIFFレンディションも公開されます。 Brand portalからピラミッドTIFFレンディションを生成する方法はありません。

   * To preserve the Brand Portal folder hierarchy while downloading assets, select **[!UICONTROL Create separate folder for each asset]**. デフォルトでは、Brand Portalのフォルダー階層は無視され、すべてのアセットがローカルシステムの1つのフォルダーにダウンロードされます。

   * To send an email notification to users with a link for downloading the assets, select **[!UICONTROL Email]**.
   ![](assets/download-link.png)

   >[!NOTE]
   >
   >電子メール通知に含まれるダウンロードリンクの有効期限は 45 日間です。
   >
   >管理者は、電子メールのメッセージ内容、つまりロゴ、説明およびフッターを、[ブランディング](../using/brand-portal-branding.md)機能を使用してカスタマイズできます。

3. Click **[!UICONTROL Download]**.

   アセット（および選択されている場合はレンディション）が ZIP ファイルとしてローカルフォルダーにダウンロードされます。ただし、レンディションなしで 1 つのアセットをダウンロードした場合、zip ファイルは作成されないので、すばやくダウンロードを行うことができます。

   [オリジナルのレンディションへのアクセスを管理者によって許可](../using/brand-portal-adding-users.md#main-pars-procedure-202029708)されていない場合、選択したアセットのオリジナルのレンディションはダウンロードされません。

   >[!NOTE]
   >
   >個別に選択してダウンロードしたアセットは、ダウンロードされたアセットレポートに表示されます。ただし、アセットを含んだフォルダーをダウンロードした場合は、そのフォルダーもアセットも、ダウンロード済みアセットのレポートには表示されません。

   共有リンクからアセットをダウンロードする方法については、「[共有リンクからアセットをダウンロードする](../using/brand-portal-link-share.md#main-pars-header-1703469193)」を参照してください。

## 期待されるダウンロードパフォーマンス {#expected-download-performance}

ユーザーのクライアントが様々な場所にある場合、ファイルのダウンロードエクスペリエンスは、ローカルのインターネット接続やサーバーのレイテンシなどの要因によって異なります。2 GB のファイルを様々なクライアントの場所でダウンロードする際に期待されるパフォーマンスは次のとおりです（Brand Portal のサーバーは米国オレゴン州にあるものとします）。

| クライアントの場所 | クライアントとサーバーの間のレイテンシ | 予想されるダウンロード速度 | 2 GB ファイルのダウンロード所要時間 |
|-------------------------|-----------------------------------|-------------------------|------------------------------------|
| 米国西部（北カリフォルニア） | 18 ミリ秒 | 7.68 MB/秒 | 4 分 |
| 米国西部（オレゴン） | 42 ミリ秒 | 3.84 MB/秒 | 9 分 |
| 米国東部（北バージニア） | 85 ミリ秒 | 1.61 MB/秒 | 21 分 |
| APAC（東京） | 124 ミリ秒 | 1.13 MB/秒 | 30 分 |
| ノイダ | 275 ミリ秒 | 0.5 MB/秒 | 68 分 |
| シドニー | 175 ミリ秒 | 0.49 MB/秒 | 69 分 |
| ロンドン | 179 ミリ秒 | 0.32 MB/秒 | 106 分 |
| シンガポール | 196 ミリ秒 | 0.5 MB/秒 | 68 分 |

**注意**：引用したデータは、テスト条件下において確認されたものであり、レイテンシや帯域幅の異なる場所にいるユーザーの場合は結果が異なる可能性があります。
