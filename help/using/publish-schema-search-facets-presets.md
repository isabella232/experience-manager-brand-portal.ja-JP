---
title: Brand Portal へのプリセット、スキーマ、ファセットの公開
seo-title: Brand Portal へのプリセット、スキーマ、ファセットの公開
description: プリセット、スキーマ、ファセットを Brand Portal に公開する方法を説明します。
seo-description: プリセット、スキーマ、ファセットを Brand Portal に公開する方法を説明します。
uuid: c836d9bb-074a-4113-9c91-b2bf7658b88d
topic-tags:  
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
discoiquuid: bc305abc-9373-4d33-9179-0a5f3904b352
translation-type: tm+mt
source-git-commit: 86d4d5c358ea795e35db2dce8c9529ed14e9ee2d

---


# Brand Portal へのプリセット、スキーマ、ファセットの公開 {#publish-presets-schema-and-facets-to-brand-portal}

この記事では、画像プリセット、メタデータスキーマおよびカスタム検索ファセットを AEM オーサーインスタンスから Brand Portal へ公開する方法について説明します。公開機能を使用すると、組織はAEM Authorインスタンスで作成/変更された画像プリセット、メタデータスキーマ、検索ファセットを再利用できるので、重複する作業を減らすことができます。

>[!NOTE]
>
>画像プリセット、メタデータスキーマおよび検索ファセットを AEM オーサーインスタンスから Brand Portal へ公開する機能は、AEM 6.2 SP1-CFP7 および AEM 6.3 SP 1-CFP 1（6.3.1.1）以降で使用できます。

## Brand Portal への画像プリセットの公開 {#publish-image-presets-to-brand-portal}

画像プリセットとは、画像配信の際に画像に適用される一連のサイズ変更コマンドやフォーマットコマンドをまとめたものです。画像プリセットは Brand Portal で作成したり修正したりできます。 または、AEM作成者インスタンスがダイナミックメディアモードで実行されている場合、ユーザーはAEM作成者でプリセットを作成し、AEM Assets Brand Portalに公開して、Brand Portalで同じプリセットを再作成する必要がありません。\
プリセットを作成すると、それがアセット詳細のレンディションレールとダウンロードダイアログに動的レンディションとしてリストされます。

>[!NOTE]
>
>If AEM Author instance is not running in [!UICONTROL Dynamic Media Mode] (customer has not purchased Dynamic Media), then the [!UICONTROL Pyramid TIFF]  rendition of the assets are not created at the time of upload. Image presets or dynamic renditions work on [!UICONTROL Pyramid TIFF] of an asset, so if [!UICONTROL Pyramid TIFF] is not available on AEM Author instance then it is not available on Brand Portal as well. したがって、動的レンディションがアセット詳細ページのレンディションレールやダウンロードダイアログに表示されません。

画像プリセットを Brand Portal に公開するには、次のようにします。

1. In AEM Author instance, tap/ click the AEM logo to access the global navigation console and tap/ click the Tools icon and navigate to **[!UICONTROL Assets]** &gt; **[!UICONTROL Image Presets]**.
1. 画像プリセットのリストから目的の画像プリセットを 1 つまたは複数選択し、「**[!UICONTROL Brand Portal に公開]**」をクリックまたはタップします。

![](assets/publishpreset.png)

>[!NOTE]
>
>ユーザーが「**[!UICONTROL Brand Portal に公開]**」をクリックすると、画像プリセットが公開用のキューに入ります。レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

ブランドポータルから画像プリセットを非公開にするには：

1. In AEM Author instance, tap/ click the AEM logo to access the global navigation console and tap/click the **[!UICONTROL Tools]** icon and navigate to **[!UICONTROL Assets &gt; Image Presets]**.
1. 画像プリセットを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]**」を選択します。

## Brand Portal へのメタデータスキーマの公開 {#publish-metadata-schema-to-brand-portal}

メタデータスキーマは、アセットまたはコレクションのプロパティページに表示されるレイアウトとプロパティを記述します。

![](assets/metadata-schema-editor.png) ![](assets/asset-properties-1.png)

AEM作成者インスタンスのデフォルトのスキーマを編集し、ブランドポータルのデフォルトのスキーマと同じスキーマを使用する場合は、単にメタデータスキーマフォームをBrand portalに発行できます。 このようなシナリオでは、Brand Portalのデフォルトのスキーマは、AEM Authorインスタンスから発行されたデフォルトのスキーマによって上書きされます。

AEM作成者インスタンスにカスタムスキーマを作成した場合、ユーザーは同じカスタムスキーマをそこで再作成する代わりに、カスタムスキーマをBrand Portalに発行できます。 公開されたカスタムスキーマは Brand Portal 内の任意のフォルダーまたはコレクションに適用できます。

>[!NOTE]
>
>デフォルトのスキーマがAEMインスタンスでロックされている場合（つまり未編集の場合）、ブランドポータルに公開することはできません。

![](assets/default-schema-form.png)

>[!NOTE]
>
>フォルダーにAEM作成者インスタンスにスキーマが適用されている場合、AEM作成者とブランドポータルのアセットプロパティページの一貫性を維持するために、同じスキーマがBrand Portalにも存在する必要があります。

メタデータスキーマを AEM オーサーインスタンスから Brand Portal へ公開するには、次のようにします。

1. In AEM Author instance, tap/ click the AEM logo to access the global navigation console and tap/click the Tools icon and navigate to **[!UICONTROL Assets &gt; Metadata Schemas]**.
1. メタデータスキーマを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal に公開]**」を選択します。

>[!NOTE]
>
>ユーザーが「**[!UICONTROL Brand Portal に公開]**」をクリックすると、メタデータスキーマが公開用のキューに入ります。レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

Brand Portal へのメタデータスキーマの公開を取り消すには、次のようにします。

1. In AEM Author instance, tap/ click the AEM logo to access the global navigation console and tap/click the Tools icon and navigate to **[!UICONTROL Assets &gt; Metadata Schemas]**.
1. メタデータスキーマを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]**」を選択します。

## Brand Portal への検索ファセットの公開 {#publish-search-facets-to-brand-portal}

検索フォームは、Brand Portal のユーザーに[ファセット検索](../using/brand-portal-search-facets.md)の機能を提供します。検索ファセットは、Brand portalでの検索に対してより細かい精度を与えます。 All the [predicates added](https://helpx.adobe.com/experience-manager/6-5/assets/using/search-facets.html#AddingaPredicate) in the search form are available to users as search facets in search filters.

![](assets/property-predicate-removed.png)
![](assets/search-form.png)

If you are willing to use custom search form **[!UICONTROL Assets Admin Search Rail]** from AEM Author instance, then instead of re-creating the same form on Brand Portal you can publish the customized search form from AEM Author instance to Brand Portal.

>[!NOTE]
>
>Locked search form **[!UICONTROL Assets Admin Search Rail]** on AEM Assets cannot be published to Brand Portal unless it is edited. Once edited and published to Brand Portal, this search form overrides the search form on Brand Portal.

編集された検索ファセットを AEM オーサーインスタンスから Brand Portal へ公開するには、次のようにします。

1. Tap/click the AEM logo, and then go to **[!UICONTROL Tools]** &gt; **[!UICONTROL General]** &gt; **[!UICONTROL Search Forms]**.
1. 編集された検索フォームを選択し、「**[!UICONTROL Brand Portal に公開]**」を選択します。

   >[!NOTE]
   >
   >ユーザーが「**[!UICONTROL Brand Portal に公開]**」をクリックすると、検索ファセットが公開用のキューに入れられます。レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

Brand Portal への検索フォームの公開を取り消すには、次のようにします。

1. In AEM Author instance, tap/ click the AEM logo to access the global navigation console and tap/click the Tools icon and navigate to **[!UICONTROL General &gt; Search Forms]**.
1. 検索フォームを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]**」を選択します。

>[!NOTE]
>
>「**[!UICONTROL Brand Portal で非公開]**」アクションを実行しても、デフォルトの検索フォームが Brand Portal にそのまま残され、公開前まで使用された検索フォームには復元されません。

### 制限事項 {#limitations}

1. Few search predicates are not applicable to search filters on the Brand Portal. このような検索用述語が検索フォームの一部として AEM オーサーインスタンスから Brand Portal へ公開された場合は、適用できない検索用述語が削除されます。Users, therefore, see less number of predicates in the published form at the Brand Portal. 詳しくは、[Brand Portal 上のフィルターに適用可能な検索用述語の一覧](../using/brand-portal-search-facets.md#list-of-search-predicates)を参照してください。

1. For [!UICONTROL Options Predicate], if a user is using any custom path to read options at AEM Author instance, it won't work at the Brand Portal. このような追加のパスやオプションは、検索フォームと一緒に Brand Portal へ公開されません。In this case, users can select the **[!UICONTROL Manual]** option in **[!UICONTROL Add Options]** within **[!UICONTROL Options Predicate]** to add these options manually at Brand Portal.

![](assets/options-predicate-manual.png)
