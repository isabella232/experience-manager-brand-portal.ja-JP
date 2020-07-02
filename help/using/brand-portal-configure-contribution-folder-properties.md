---
title: 投稿フォルダーのプロパティの設定
seo-title: 投稿フォルダーのプロパティの設定
description: 'AEM Assets で投稿フォルダーのプロパティを設定する方法を説明します。 '
seo-description: 'AEM Assets で投稿フォルダーのプロパティを設定する方法を説明します。 '
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
version: 6.5
discoiquuid: null
translation-type: ht
source-git-commit: 67b905dc71d6b1b4f314a9791e386f7a27781967
workflow-type: ht
source-wordcount: '319'
ht-degree: 100%

---


# 投稿フォルダーのプロパティの設定 {#configure-contribution-folder-properties}

AEM 管理者は、投稿フォルダーのプロパティを設定する際に、次のアクティビティを実行します。

* **説明を追加**：投稿フォルダーの大まかな説明を提供します。
* **概要をアップロード**：アセット関連情報を含むアセット要件ドキュメントをアップロードします。
* **投稿者を追加**：投稿フォルダーへのアクセス権を付与するために Brand Portal ユーザーまたはグループを追加します。

アセット要件は、管理者によって提供された詳細を参照して、投稿者（Brand Portal ユーザー）が投稿フォルダーのニーズおよび要件を理解できるようにします。管理者は、投稿フォルダーに追加する必要があるアセットのタイプおよびアセット関連情報（目的、画像のタイプ、最大サイズなど）に関する概要を含むアセット要件ドキュメントをアップロードします。

その後、管理者は、Brand Portal ユーザー／グループに投稿フォルダーへのアクセス権を付与してから、新しく作成した投稿フォルダーを Brand Portal に公開できます。

**投稿フォルダーのプロパティを設定するには：**
1. AEM オーサーインスタンス（デフォルト URL：http://localhost:4502/aem/start.html）にログインします。
1. **[!UICONTROL アセット／ファイル]**&#x200B;に移動して、投稿フォルダーを探します。
1. 投稿フォルダーを選択して、「**[!UICONTROL プロパティ]**」![](assets/properties.png)をクリックします。フォルダーのプロパティウィンドウが開きます。
   ![](assets/contribution-folder-property1.png)
1. 「**[!UICONTROL アセット投稿]**」タブに移動します。
1. 投稿フォルダーの大まかな&#x200B;**[!UICONTROL 説明]**&#x200B;を入力します。
1. **[!UICONTROL 概要をアップロード]**![](assets/upload.png)をクリックし、ローカルマシンから参照して&#x200B;**アセット要件ドキュメント**&#x200B;をアップロードします。
1. 「**[!UICONTROL ユーザーまたはグループを追加]**」フィールドで、投稿フォルダーを共有したい Brand Portal ユーザーを追加します。追加されたユーザーは、Brand Portal インターフェイスを使用して、投稿フォルダーにアクセスし、アップロードできます。現在、投稿フォルダーにグループを追加することはできません。

1. 「**[!UICONTROL 保存]**」をクリックします。
   ![](assets/contribution-folder-property2.png)

>[!NOTE]
>
>検索結果は、AEM Assets に設定された Brand Portal ユーザーリストに基づきます。Brand Portal ユーザーリストを更新しておくようにします。[Brand Portal ユーザーリストのアップロード](brand-portal-configure-asset-sourcing.md)を参照してください。

