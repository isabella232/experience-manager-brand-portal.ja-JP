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
source-git-commit: f4f92724cdd4ba8c79d3d72de5cba9451dceadb1
workflow-type: tm+mt
source-wordcount: '1294'
ht-degree: 24%

---


# アセットのダウンロード {#download-assets}

<!-- Before update in Download experience - 26th Aug 2020 by Vishabh.
 All users can simultaneously download multiple assets and folders accessible to them from Brand Portal. This way, approved brand assets can be securely distributed for offline use. Read on to know how to download approved assets from Brand Portal, and what to expect from the [download performance](../using/brand-portal-download-assets.md#main-pars-header).
-->

Adobe Experience Managerアセットブランドポータルは、ブランドポータルから複数のアセットやフォルダーに同時にアクセスできるようにすることで、ダウンロード体験を強化します。 これにより、承認されたブランドアセットを安全に配布して、オフラインで使用できます。Brand Portal から承認済みアセットをダウンロードする方法や、[ダウンロードパフォーマンス](../using/brand-portal-download-assets.md#expected-download-performance)から期待されることについてお読みください。

>[!NOTE]
>
>Brand Portalからアセットをダウンロードする前に、ブラウザーの拡張機能にIBM Aspera Connect 3.9.9をインストールします。


<!--
**Types of renditions in Brand Portal:**

* Original asset rendition

  It is the original binary of the asset uploaded in AEM Assets. 
  
  
* System renditions

  These are the thumbnail renditions which are automatically generated in AEM Assets based on the "DAM update asset" workflow. 
  
* Custom renditions

  These are the additional renditions that an asset might have and its dynamic renditions. Any user can create additional custom renditions, whereas, only the AEM administrator can create dynamic renditions of an image in AEM Assets. To know more, see [how to apply image presets or dynamic renditions](../using/brand-portal-image-presets.md).     
-->

## アセットのダウンロードの設定 {#configure-download}

ダウンロード設定を使用すると、Brand Portal管理者は、Brand Portalユーザがアセットをダウンロードするために使用できるレンディションのセットを定義できます。 管理者は、ブランドポータルインターフェイスからアセットの **[!UICONTROL ダウンロード]** 設定を設定できます。

利用可能な設定は以下の通りです。

* **[!UICONTROL 高速ダウンロード]**

   アセットの高速ダウンロードを有効にします。 詳しくは、 [ガイドを参照して、Brand Portalからのダウンロードを高速化してください](../using/accelerated-download.md)。

* **[!UICONTROL カスタムレンディション]**

   アセットのカスタムレンディションおよび（または）動的レンディションをダウンロードします。
元のアセットおよびシステム生成レンディション以外のすべてのアセットレンディションは、カスタムレンディションと呼ばれます。 アセットに使用できる静的レンディションと動的レンディションが含まれます。 カスタムの静的レンディションは、AEM Assetsで作成できますが、AEM管理者のみがカスタムの動的レンディションを作成できます。 詳しくは、画像プリセットまたはダイナミックレンディション [の適用方法を参照してください](../using/brand-portal-image-presets.md)

* **[!UICONTROL システムレンディション]**

   システム生成のアセットレンディションをダウンロードします。 これらは、「DAM Update Asset」ワークフローに基づいて、AEM Assetsで自動的に生成されるサムネールです。

Brand Portalテナントに管理者としてログインし、 **[!UICONTROL ツール]** / **[!UICONTROL ダウンロードに移動します]**。 デフォルトでは、 **[!UICONTROL 高速ダウンロード]** 設定は **[!UICONTROL ダウンロード設定で有効になっています]**。

管理者は任意の組み合わせを有効にして、アセットのダウンロードプロセスを設定できます。

![](assets/download-configuration.png)


設定に基づいて、ダウンロードワークフローは、スタンドアロンのアセット、複数のアセット、アセットを含むフォルダ、ライセンス済みまたはライセンスされていないアセット、および共有リンクを使用したアセットのダウンロードに対して常に変化しません。


* 「 **[!UICONTROL カスタムレンディション]** 」と「 **[!UICONTROL システムレンディション]** 」の両方の設定がオフになっている場合、アセットの元のレンディションは、追加のダイアログをユーザーに表示することなくダウンロードされます。

<!--
If all the three download configurations are turned-off, or only the **[!UICONTROL Fast Download]** configuration is enabled, the original assets are directly downloaded on your local system with no additional step required.
Test.. 
-->

* カス **[!UICONTROL タムレンディション]** または **[!UICONTROL システムレンディションの設定が有効になっている場合、追加の]****** ダウンロードダイアログボックスが表示され、元のアセットとレンディションをダウンロードするか、特定のレンディションのみをダウンロードするかを選択できます。

>[!NOTE]
>
>管理者のみが、期限切れのアセットをダウンロードできます。 For more information about expired assets, see [manage digital rights of assets](../using/manage-digital-rights-of-assets.md).


## アセットのダウンロード手順 {#steps-to-download-assets}

ブランドポータルからアセットを含むアセットまたはフォルダーをダウンロードする手順は次のとおりです。

1. Brand Portal コンソールで、以下のいずれかの手順を実行します。

   * ダウンロードするフォルダーまたはアセットを選択します。上部のツールバーで「**[!UICONTROL ダウンロード]**」アイコンをクリックします。

      ![](assets/downloadassets-1.png)

   * 特定のアセットまたはフォルダーをダウンロードするには、アセットまたはフォルダーにポインターを置き、クイックアクションのサムネールに表示される **[!UICONTROL ダウンロード]** アイコンをクリックします。

      ![](assets/downloadsingleasset-1.png)


      >[!NOTE]
      >
      >初めてアセットをダウンロードする場合で、ブラウザーにIBM Aspera Connectがインストールされていない場合は、Asperaダウンロードアクセラレーターをインストールするように求めるプロンプトが表示されます。

      >[!NOTE]
      >
      >ダウンロードするアセットに、ライセンスが必要なアセットが含まれている場合は、**[!UICONTROL 著作権管理]**&#x200B;ページにリダイレクトされます。このページで、アセットを選択し、「**[!UICONTROL 同意する]**」をクリックし、「**[!UICONTROL ダウンロード]**」をクリックします。「同意しない」を選択した場合は、ライセンスが必要なアセットはダウンロードされません。
      > 
      >License-protected assets have [license agreement attached](https://helpx.adobe.com/jp/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) to them, which is done by setting asset&#39;s [metadata property](https://helpx.adobe.com/jp/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) in Experience Manager Assets.

      ![](assets/licensed-asset-download-1.png)

      Download Settingsで **[!UICONTROL Custom Renditions]** ( **[!UICONTROL カスタムレンディション]** )または **[!UICONTROL System Renditions]**( **[!UICONTROL システムレンディション]****** )の設定が有効になっている場合、DownloadダイアログにDownload asset(s s selected)asts（s st DefaultでDownload Asset）が表示されます。 「 **[!UICONTROL 高速ダウンロード]** 」設定が有効になっている場合、デフォルトでは「ダウンロードの加速を **[!UICONTROL 有効にする]** 」チェックボックスがオンになっています。

      ![](assets/download-dialog.png)

      >[!NOTE]
      >
      >If the downloading assets are image files, and you select only the **[!UICONTROL Asset(s)]** check box in the **[!UICONTROL Download]** dialog but are not [authorized by the administrator to have access to the original renditions of image files](../using/brand-portal-adding-users.md#main-pars-procedure-202029708) then no image files are downloaded and a notification appears, stating that you have been restricted by the administrator to access original renditions.

      ![](assets/restrictaccess-note.png)

1. 元のアセットに加えてレンディションをダウンロードするには、「 **[!UICONTROL レンディション]** 」チェックボックスをオンにします。 ただし、システム生成レンディションとカスタムレンディションをダウンロードする場合は、「システムレンディションを **[!UICONTROL 除外]** 」チェックボックスをオフにします。

   ![](assets/download-system-rendition.png)

   * レンディションのみをダウンロードするには、「 **[!UICONTROL アセット]** 」チェックボックスをオフにします。

      >[!NOTE]
      >
      >デフォルトでは、アセットのみがダウンロードされます。ただし、[画像ファイルのオリジナルのレンディションへのアクセスが管理者によって許可](../using/brand-portal-adding-users.md#main-pars-procedure-202029708)されていない場合は、画像ファイルのオリジナルのレンディションはダウンロードされません。

   * 選択したアセットをリンクを介して他のユーザーと共有するには、「 **[!UICONTROL 電子メール]** 」チェックボックスをオンにします。 ダウンロードリンクを含むユーザーに電子メール通知が送信されます。 To know how to download assets from shared links, see [downloading assets from shared links](../using/brand-portal-link-share.md#main-pars-header-1703469193).

      ![](assets/download-link.png)

      >[!NOTE]
      >
      >電子メール通知時のダウンロードリンクは、45日後に期限切れになります。
      >
      >The administrators can customize email messages, that is, logo, description, and footer, using the [Branding](../using/brand-portal-branding.md) feature.

   * 定義済みの画像プリセットを選択するか、 **[!UICONTROL ダウンロード]** ダイアログボックスからカスタムダイナミックレンディションを作成できます。

      To apply a [custom image preset to the asset and its renditions](../using/brand-portal-image-presets.md#applyimagepresetswhendownloadingimages), select the **[!UICONTROL Dynamic Rendition(s)]** check box. 画像プリセットのプロパティ（サイズ、形式、カラースペース、解像度、画像修飾子など）を指定し、アセットとそのレンディションのダウンロード中にカスタム画像プリセットを適用します。 動的レンディションのみをダウンロードするには、「 **[!UICONTROL アセット]** 」チェックボックスをオフにします。

      ![](assets/dynamic-rendition.png)

      >[!NOTE]
      >
      >Brand Portalでは、HybirdとScene 7の両方のモードでのダイナミックメディアの設定をサポートしています。
      >
      >(*If AEM author instance is running on **Dynamic Media Hybrid mode***)      >アセットの動的レンディションをプレビューまたはダウンロードするには、動的メディアが有効で、アセットのピラミッドTIFFレンディションが、アセットが公開されたAEM Assetsオーサーインスタンスに存在することを確認します。 Brand Portal にアセットを公開すると、そのピラミッド TIFF レンディションも公開されます。

   * To preserve the Brand Portal folder hierarchy while downloading assets, select the **[!UICONTROL Create separate folder for each asset]** check box. デフォルトでは、Brand Portalのフォルダ階層は無視され、すべてのアセットがローカルシステムの1つのフォルダにダウンロードされます。

1. 「**[!UICONTROL ダウンロード]**」をクリックします。

   アセット（および選択されている場合はレンディション）がzipファイルとしてローカルフォルダーにダウンロードされます。 ただし、レンディションなしで単一のアセットをダウンロードした場合、zipファイルは作成されません。

   管理者が元のレンディションへのアクセスを [許可していない場合](../using/brand-portal-adding-users.md#main-pars-procedure-202029708)、選択したアセットの元のレンディションはダウンロードされません。

   >[!NOTE]
   >
   >個別にダウンロードされたアセットは、アセットダウンロードレポートに表示されます。 ただし、アセットを含むフォルダーをダウンロードする場合、フォルダーとアセットはアセットダウンロードレポートに表示されません。


## 期待されるダウンロードパフォーマンス {#expected-download-performance}

ユーザーのクライアントが様々な場所にある場合、ファイルのダウンロードエクスペリエンスは、ローカルのインターネット接続やサーバーのレイテンシなどの要因によって異なります。異なるクライアントの場所で観察される2 GBのファイルのダウンロードパフォーマンスは次のとおりです。米国のオレゴンのブランドポータルサーバーは次のとおりです。

| クライアントの場所 | クライアントとサーバーの間のレイテンシ | 予想されるダウンロード速度 | 2 GBのファイルのダウンロードにかかる時間 |
|-------------------------|-----------------------------------|-------------------------|------------------------------------|
| 米国西部（北カリフォルニア） | 18 ミリ秒 | 7.68 MB/秒 | 4 分 |
| 米国西部（オレゴン） | 42 ミリ秒 | 3.84 MB/秒 | 9 分 |
| 米国東部（北バージニア） | 85 ミリ秒 | 1.61 MB/秒 | 21 分 |
| APAC（東京） | 124 ミリ秒 | 1.13 MB/秒 | 30 分 |
| ノイダ | 275 ミリ秒 | 0.5 MB/秒 | 68 分 |
| シドニー | 175 ミリ秒 | 0.49 MB/秒 | 69 分 |
| ロンドン | 179 ミリ秒 | 0.32 MB/秒 | 106 分 |
| シンガポール | 196 ミリ秒 | 0.5 MB/秒 | 68 分 |

>[!NOTE]
>
>引用されたデータはテスト条件の下で観察されます。テスト条件は、待ち時間や帯域幅が異なる様々な場所のユーザーにとって異なる場合があります。

