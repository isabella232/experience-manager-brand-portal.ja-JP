---
title: Brand Portal へのタグの公開
seo-title: Brand Portal へのタグの公開
description: AEM Assets から Brand Portal にタグを公開する方法を学習します。
seo-description: AEM Assets から Brand Portal にタグを公開する方法を学習します。
uuid: 4167367e-1af8-476b-97a5-730c43bd0816
topic-tags:  
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
content-type: reference
discoiquuid: 3c8e9251-195d-4c56- a9a9-27bc8b2a82a4
translation-type: tm+mt
source-git-commit: 32c3cdb8e3fafd74cfb36e6bcfe0811e7152b2d0

---


# Brand Portal へのタグの公開 {#publish-tags-to-brand-portal}

Learn how to publish tags from [!DNL AEM] Assets to [!DNL Brand Portal].

タグはアセットの整理に役立ちます。また、アセットにタグを関連付けると検索性が向上します。タグはアセットに関連付けられるキーワードやラベル（メタデータ）のようなもので、検索結果の中から目的のアセットをすばやく見つけるために役立ちます。To know how to assign tags to assets in [!DNL AEM] Assets, refer [use tags to organize assets](https://helpx.adobe.com/experience-manager/6-5/assets/using/organize-assets.html#Usetagstoorganizeassets).

Tags (associated with assets and collections in [!DNL AEM]) are auto-published to [!DNL Brand Portal] when the assets (and collections) with associated tags are published to [!DNL Brand Portal]. 公開されたタグは、そのタグに関連付けられているアセットを検索で探す際に役立ちます。

>[!NOTE]
>
>It is, however, recommended to exclusively publish tags to [!DNL Brand Portal] before publishing the assets (and collections) with which the tags are associated. This ensures faster publishing of the assets (and collections) to [!DNL Brand Portal].

## Manage tags {#manage-tags}

You can use the pre-existing tags to attach to an asset or create new tags from [!DNL AEM] Tags console (**Tools | Tagging |[!DNL AEM]Tags**). In both the scenarios you must first publish the tags to [!DNL Brand Portal] and then associate them with appropriate assets.

To create tags on [!DNL AEM], publish the tags on [!DNL Brand Portal], and associate the tags with appropriate assets (or collections), follow these steps:

1. **タグ**&#x200B;の作成管理者権限を持つ [!DNL AEM] 作成者インスタンスにログインし、グローバルナビゲーションから **[!DNL AEM]タグ** コンソールにアクセスします。

   1. **ツールを選択**

   2. **一般を選択**

   3. **タグ付けの選択**

2. Select **Create** and then select **Create Tag** option.
3. 以下を指定します。

   * **タイトル**
      *（必須）* タグの表示タイトル。
   * **名前**
      *（必須）* タグの名前。指定しない場合、有効なノード名が「タイトル」から作成されます。[tagId](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/framework.html#TagID)を参照してください。
   * **説明**
      *（オプション）* タグの説明。
   * **タグのパス** タグの JCR パス。

4. 「**送信**」を選択すると、タグが作成されます。

   Once you have created a tag on [!DNL AEM] instance, the tag will be available to be attached to an asset (using Properties section or Manage Tags section of that asset).

5. **タグを公開[!DNL Brand Portal]**&#x200B;します。

   **[!DNL AEM]タグ** コンソール（ツール）|タグ付け| [!DNL AEM] タグ）で、目的のタグを選択し、「投稿 **[!DNL Brand Portal]**&#x200B;先」を選択します。

6. タグをアセット（またはコレクション）に関連付けます&#x200B;****。

   アセット（またはコレクション）を選択し、そのアセットの「プロパティ」セクションまたは「タグを管理」セクションを使用して、目的のタグを関連付けます。To know more about how to assign tags to assets in [!DNL AEM] Assets, refer [use tags to organize assets](https://helpx.adobe.com/experience-manager/6-5/assets/using/organize-assets.html#Usetagstoorganizeassets).

7. **アセット（またはコレクション）を公開[!DNL Brand Portal]**&#x200B;します。\
   When you publish an asset (or collection) to [!DNL Brand Portal], the attached tag is also available on [!DNL Brand Portal].

   To see the attached tag on the respective asset (or collection) in [!DNL Brand Portal], log in to [!DNL Brand Portal] and select the asset, under Properties section you will see the attached Tag.

## 昇格を検索 {#search-promote}

[!DNL AEM] Assets では、キーワードタグに基づいて特定のアセットを検索結果の一番上に持ってくることができます。[!DNL Brand Portal]

アセットを昇格させる検索キーワードを設定するには、次のようにします。

1.  オーサーインスタンスでアセットの&#x200B;**プロパティ**&#x200B;ページを開きます。[!DNL AEM]
2. 「**詳細**」タブに移動します。
3. In **Search Promote** within **Elevate for search keywords** section, select **Add** to add the search keywords or tags.

   ![](assets/search-promote.png)

4. 変更内容を保存します。
5. Publish the asset to [!DNL Brand Portal].
6. Log in to [!DNL Brand Portal]. アセットの「**プロパティ**」セクションの「**詳細**」タブを表示します。**Search Promote** キーワードは、そのアセットのプロパティにも表示されます。
