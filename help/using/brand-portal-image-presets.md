---
title: 画像プリセットまたは動的レンディションの適用
seo-title: 画像プリセットまたは動的レンディションの適用
description: '画像プリセットは、マクロと同様、サイズとフォーマットに関するコマンドのコレクションを事前に定義し、特定の名前を付けて保存したものです。画像プリセットを使用すると、サイズ、形式、プロパティが様々に異なる画像を AEM Assets Brand Portal で動的に配信できます。 '
seo-description: '画像プリセットは、マクロと同様、サイズとフォーマットに関するコマンドのコレクションを事前に定義し、特定の名前を付けて保存したものです。画像プリセットを使用すると、サイズ、形式、プロパティが様々に異なる画像を AEM Assets Brand Portal で動的に配信できます。 '
uuid: a3c8705c-5fbd-472c-8b61- f65b3e552c1b
content-type: reference
topic-tags: 管理
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
discoiquuid: a512dfa0- fef3-4c3f- a389- a0a3a7415bac
translation-type: tm+mt
source-git-commit: 32c3cdb8e3fafd74cfb36e6bcfe0811e7152b2d0

---


# 画像プリセットまたは動的レンディションの適用 {#apply-image-presets-or-dynamic-renditions}

Like a macro, an image preset is a predefined [!UICONTROL collection] of sizing and formatting commands saved under a name. Image presets enable [!DNL AEM] Assets [!DNL Brand Portal] to dynamically deliver images of different sizes, formats, and properties.

画像プリセットは、プレビューしたりダウンロードしたりできる画像の動的レンディションを生成するために使用します。画像とそのレンディションをプレビューするときは、プリセットを選択することにより、管理者が設定した仕様で画像を再フォーマットできます。

To view dynamic renditions of an asset in [!DNL Brand Portal], ensure that its PTIFF rendition exists at the [!DNL AEM] author instance from where you publish to [!DNL Brand Portal]. When you publish the asset, its PTIFF rendition is also published to [!DNL Brand Portal]. There is no way of generating the PTIFF rendition from [!DNL Brand Portal].

>[!NOTE]
>
>画像とそのレンディションをダウンロードするときは、既存のプリセットから選択することはできません。その代わりに、カスタム画像プリセットのプロパティを指定できます。詳しくは、[画像をダウンロードする際の画像プリセットの適用](../using/brand-portal-image-presets.md#main-pars-text-1403412644)を参照してください。

画像プリセットの作成時に必要なパラメータについて詳しくは、画像プリセット [の管理]（https://docs.adobe.com/docs/en//6-0/administer/integration/dynamic-media/image-presets.html)[!DNL AEM]）を参照してください。

## 画像プリセットの作成 {#create-an-image-preset}

管理者は、アセットの詳細ページに動的レンディションとして表示される画像プリセットを作成できます。画像プリセットを一から作成することも、既存の画像プリセットに新しい名前を付けて保存することもできます。画像プリセットを作成するときは、画像配信のサイズと、フォーマットコマンドを選択します。画像が表示用に配信されるときには、選択したコマンドに応じて画像の外観が最適化されます。Note that only Administrators can create image presets in [!DNL Brand Portal].

Note that only Administrators can create image presets in [!DNL Brand Portal].

>[!NOTE]
>
>動的レンディションは、PTIFF が使用可能なアセットに対して作成されます。So If an asset does not have Pyramid TIFF rendition created on [!DNL AEM] and published to [!DNL Brand Portal], then only its system renditions can be exported, but dynamic renditions are presented as an option.
Dynamic Media Hybrid mode must be enabled on [!DNL AEM] (author) in order to create pyramid tiff (ptiff) of an asset. When such an asset is published to [!DNL Brand Portal], image presets are applied and dynamic renditions are displayed.

1. From the [!DNL AEM] toolbar at the top, click the Adobe logo to access administrative tools.

   !![]（assets/[!DNL AEM]logo. png）

2. From the administrative tools panel, click **Image Presets**.

   ![](assets/admin-tools-panel-4.png)

3. 画像プリセットページの「**作成**」をクリックします。

   ![](assets/image_preset_homepage.png)

4. In the **Edit Image Preset** page, enter values into the **Basic** and **Advanced** tabs as appropriate, including a name. オプションについて [は、画像プリセットのオプション]（https://docs.adobe.com/docs/en//6-0/administer/integration/dynamic-media/image-presets.html#Image%20preset%20options)[!DNL AEM]）で説明しています。プリセットは左側のウィンドウに表示され、他のアセットにすぐに使用できます。

   ![](assets/image_preset_create.png)

   >[!NOTE]
   >
   >You can also use the **Edit Image Preset** page to edit the properties of an existing image preset. To edit an image preset, select it from the image presets page, and click **Edit**.

5. 「**保存**」をクリックします。画像プリセットが作成され、画像プリセットページに表示されます。
6. 画像プリセットを削除するには、画像プリセットページから削除する画像プリセットを選択し、「**削除**」をクリックします。確認ページで「**削除**」をクリックして、削除することを確認します。指定した画像プリセットが、画像プリセットページから削除されます。

## 画像をプレビューする際の画像プリセットの適用  {#apply-image-presets-when-previewing-images}

画像とそのレンディションをプレビューするときは、既存のプリセットから選択することで、管理者が設定した仕様で画像を再フォーマットできます。

1. [!DNL Brand Portal] インターフェイスから画像をクリックして開きます。
2. Click the overlay icon on the left, and choose **Renditions**.

   ![](assets/image-preset-previewrenditions.png)

3. **レンディション** リストから、適切な動的レンディション（ **例えば、サムネール**）を選択します。選択した動的レンディションに基づいて、プレビュー画像がレンダリングされます。

   ![](assets/image-preset-previewrenditionthumbnail.png)

## 画像をダウンロードする際の画像プリセットの適用 {#apply-image-presets-when-downloading-images}

When downloading images and their renditions from [!DNL Brand Portal], you cannot choose from the existing image presets. ただし、再フォーマットする画像に基づいて、画像プリセットのプロパティをカスタマイズできます。

1. [!DNL Brand Portal] インターフェイスから、次のいずれかの操作を行います。

   * ダウンロードする画像の上にマウスポインターを置きます。From the quick action thumbnails available, click the **Download** icon.
   ![](assets/downloadsingleasset.png)

   * ダウンロードする画像を選択します。From the toolbar at the top, click the **Download** icon.
   ![](assets/downloadassets.png)

2. **ダウンロード**&#x200B;ダイアログボックスで、アセットとそのレンディションを一緒にダウンロードするかどうかに応じて、必要なオプションを選択します。

   ![](assets/donload-assets-dialog.png)

3. アセットの動的レンディションをダウンロードするには、「**動的レンディション**」オプションを選択します。
4. 画像プリセットのプロパティを、画像とそのレンディションをダウンロード時に動的に再フォーマットしたい設定に基づいてカスタマイズします。サイズ、フォーマット、カラースペース、解像度および画像の修飾子を指定します。

   ![](assets/dynamicrenditions.png)

5. 「**ダウンロード**」をクリックします。カスタムの動的レンディションが、ダウンロード対象として選択した画像とレンディションと一緒に ZIP ファイルにダウンロードされます。ただし、ダウンロードするアセットが 1 つだけの場合は、迅速なダウンロードをおこなうために ZIP ファイルは作成されません。
