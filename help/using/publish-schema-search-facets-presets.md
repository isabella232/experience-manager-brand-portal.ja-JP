---
title: Brand Portal へのプリセット、スキーマ、ファセットの公開
seo-title: Brand Portal へのプリセット、スキーマ、ファセットの公開
description: プリセット、スキーマ、ファセットを Brand Portal に公開する方法を説明します。
seo-description: プリセット、スキーマ、ファセットを Brand Portal に公開する方法を説明します。
uuid: c836d9bb-074a-4113-9c91- b2bf7658b88d
topic-tags:  
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
content-type: reference
discoiquuid: bc305abc-9373-4d33-9179-0a5f3904b352
translation-type: tm+mt
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# Brand Portal へのプリセット、スキーマ、ファセットの公開 {#publish-presets-schema-and-facets-to-brand-portal}

この記事では、画像プリセット、メタデータスキーマおよびカスタム検索ファセットを AEM オーサーインスタンスから Brand Portal へ公開する方法について説明します。投稿機能を使用すると、組織は、AEM作成者インスタンスで作成/変更された画像プリセット、メタデータスキーマ、検索ファセットを再利用して、重複する作業を減らすことができます。

>[!NOTE]
>
>画像プリセット、メタデータスキーマおよび検索ファセットを AEM オーサーインスタンスから Brand Portal へ公開する機能は、AEM 6.2 SP1-CFP7 および AEM 6.3 SP 1-CFP 1（6.3.1.1）以降で使用できます。

## Brand Portal への画像プリセットの公開 {#publish-image-presets-to-brand-portal}

画像プリセットとは、画像配信の際に画像に適用される一連のサイズ変更コマンドやフォーマットコマンドをまとめたものです。画像プリセットは Brand Portal で作成したり修正したりできます。 また、AEM作成者インスタンスがダイナミックメディアモードで実行されている場合、ユーザーはAEM作成者にプリセットを作成し、AEM Assetsブランドポータルに公開することができ、ブランドポータルで同じプリセットを再作成することは避けます。\
プリセットを作成すると、それがアセット詳細のレンディションレールとダウンロードダイアログに動的レンディションとしてリストされます。

>[!NOTE]
>
>AEM作成者インスタンスが [!UICONTROL ダイナミックメディアモード] で実行されていない場合（顧客が動的メディアを購入していない場合）、そのアセットの [!UICONTROL ピラミッドTIFF] レンディションはアップロード時に作成されません。Image presets or dynamic renditions work on [!UICONTROL Pyramid TIFF] of an asset, so if [!UICONTROL Pyramid TIFF] is not available on AEM Author instance then it is not available on Brand Portal as well. その結果、アセット詳細ページのレンディションレールに動的レンディションが表示されず、ダイアログがダウンロードされます。

画像プリセットを Brand Portal に公開するには、次のようにします。

1. In AEM Author instance, tap/ click the AEM logo to access the global navigation console and tap/ click the Tools icon and navigate to **[!UICONTROL Assets]** &gt; **[!UICONTROL Image Presets]**.
2. Select the image preset or multiple image presets from the list of image presets and click/ tap **[!UICONTROL Publish to Brand Portal]**.

![](assets/publishpreset.png)

>[!NOTE]
>
>When users click **[!UICONTROL Publish to Brand Portal]** the image presets are queued for publishing. レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

ブランドポータルから画像プリセットの公開を取り消すには:

1. In AEM Author instance, tap/ click the AEM logo to access the global navigation console and tap/click the **[!UICONTROL Tools]** icon and navigate to **[!UICONTROL Assets &gt; Image Presets]**.
2. 画像プリセットを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]」を選択します。**

## Brand Portal へのメタデータスキーマの公開  {#publish-metadata-schema-to-brand-portal}

メタデータスキーマは、アセットまたはコレクションのプロパティページに表示されるレイアウトとプロパティを記述します。

![](assets/metadata-schema-editor.png) ![](assets/asset-properties-1.png)

ユーザーがAEM作成者インスタンスのデフォルトスキーマを編集して、ブランドポータル上のデフォルトスキーマと同じスキーマを使用する場合は、単純にブランドポータルにメタデータスキーマフォームを発行できます。このようなシナリオでは、ブランドポータルのデフォルトのスキーマがAEM作成者インスタンスから発行されたデフォルトのスキーマによってリッピングされます。

ユーザーがAEM作成者インスタンスにカスタムスキーマを作成している場合、そこにカスタムスキーマを再作成する代わりに、カスタムスキーマをブランドポータルに発行できます。公開されたカスタムスキーマは Brand Portal 内の任意のフォルダーまたはコレクションに適用できます。

>[!NOTE]
>
>AEMインスタンスでロックされている場合（編集されていない）、デフォルトスキーマはブランドポータルに公開できません。

![](assets/default-schema-form.png)

>[!NOTE]
>
>フォルダーにAEM作成者インスタンスにスキーマが適用されている場合、AEM作成者とブランドポータルのアセットプロパティページの整合性を維持するために、ブランドポータルにも同じスキーマが存在する必要があります。

メタデータスキーマを AEM オーサーインスタンスから Brand Portal へ公開するには、次のようにします。

1. In AEM Author instance, tap/ click the AEM logo to access the global navigation console and tap/click the Tools icon and navigate to **[!UICONTROL Assets &gt; Metadata Schemas]**.
2. メタデータスキーマを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal に公開]」を選択します。**

>[!NOTE]
>
>When users click **[!UICONTROL Publish to Brand Portal]**, the metadata schemas are queued for publishing. レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

Brand Portal へのメタデータスキーマの公開を取り消すには、次のようにします。

1. In AEM Author instance, tap/ click the AEM logo to access the global navigation console and tap/click the Tools icon and navigate to **[!UICONTROL Assets &gt; Metadata Schemas]**.
2. メタデータスキーマを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]」を選択します。**

## Brand Portal への検索ファセットの公開 {#publish-search-facets-to-brand-portal}

検索フォームは、Brand Portal のユーザーに[ファセット検索](../using/brand-portal-search-facets.md)の機能を提供します。検索ファセットはブランドポータルでの検索の精度を高めます。All the [predicates added](https://helpx.adobe.com/experience-manager/6-5/assets/using/search-facets.html#AddingaPredicate) in the search form are available to users as search facets in search filters.

![](assets/property-predicate-removed.png)
![](assets/search-form.png)

If you are willing to use custom search form **[!UICONTROL Assets Admin Search Rail]** from AEM Author instance, then instead of re-creating the same form on Brand Portal you can publish the customized search form from AEM Author instance to Brand Portal.

>[!NOTE]
>
>Locked search form **[!UICONTROL Assets Admin Search Rail]** on AEM Assets cannot be published to Brand Portal unless it is edited. 編集してブランドポータルに公開すると、この検索フォームはブランドポータル上の検索フォームよりも優先されます。

編集された検索ファセットを AEM オーサーインスタンスから Brand Portal へ公開するには、次のようにします。

1. Tap/click the AEM logo, and then go to **[!UICONTROL Tools]** &gt; **[!UICONTROL General]** &gt; **[!UICONTROL Search Forms]**.
2. Select the edited search form, and select **[!UICONTROL Publish to Brand Portal]**.

   >[!NOTE]
   >
   >When users click **[!UICONTROL Publish to Brand Portal]**, the search facets are queued for publishing. レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

Brand Portal への検索フォームの公開を取り消すには、次のようにします。

1. In AEM Author instance, tap/ click the AEM logo to access the global navigation console and tap/click the Tools icon and navigate to **[!UICONTROL General &gt; Search Forms]**.
2. 検索フォームを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]」を選択します。**

>[!NOTE]
>
>**[!UICONTROL ブランドポータル]** のアクションからの非公開では、デフォルトの検索フォームがブランドポータルに残り、公開前に使用された最後の検索フォームに復元されません。

### 制限事項 {#limitations}

1. 検索の述語は、ブランドポータルでは検索フィルタに適用できません。このような検索用述語が検索フォームの一部として AEM オーサーインスタンスから Brand Portal へ公開された場合は、適用できない検索用述語が削除されます。したがって、ブランドポータルでは、発行されたフォーム内の予測の数が少なくなります。詳しくは、[Brand Portal 上のフィルターに適用可能な検索用述語の一覧](../using/brand-portal-search-facets.md#list-of-search-predicates)を参照してください。

2. [!UICONTROL オプションPredicateの場合]、ユーザーがAEM作成者インスタンスで読み取りオプションを使用するためのカスタムパスを使用している場合、ブランドポータルでは動作しません。このような追加のパスやオプションは、検索フォームと一緒に Brand Portal へ公開されません。In this case, users can select the **[!UICONTROL Manual]** option in **[!UICONTROL Add Options]** within **[!UICONTROL Options Predicate]** to add these options manually at Brand Portal.

![](assets/options-predicate-manual.png)
