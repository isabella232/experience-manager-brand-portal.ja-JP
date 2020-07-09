---
title: 投稿フォルダーの作成
seo-title: 投稿フォルダーの作成
description: 'AEM Assets で投稿フォルダーを作成する方法を説明します。 '
seo-description: AEM Assets で投稿フォルダーを作成する方法を説明します。
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: tm+mt
source-git-commit: 7ec61993e627f07c20a2e5a2b43f2daa629622d6
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 36%

---


# 投稿フォルダーの作成 {#create-contribution-folder}


AEM管理者および管理者以外のユーザーは、新しいAEM Assetsーを作成する権限を持つと、フォルダー内に貢献度フォルダーを作成できます。
貢献度フォルダーを作成するには、アセット貢献度タイプの新しいフォルダーを作成し、新しく作成したフォルダーを開いて、Brand Portalユーザーがアセットの送信を行えるようにします。  これにより、貢献度フォルダー内にSHAREDとNEWという2つの追加のサブフォルダーを作成するワークフローが自動的にトリガーされます。

>[!NOTE]
>
>1 つのフォルダー内に複数の投稿フォルダーを作成できますが、投稿フォルダー内に別の投稿フォルダーは作成できません。


貢献度フォルダーを作成するには：
1. AEM オーサーインスタンスにログインします。

   デフォルトのURLは、http:// localhost:4502/aem/start.htmlです。

1. Navigate to **[!UICONTROL Assets]** > **[!UICONTROL Files]**. It lists all the existing folders in the AEM Assets repository.

1. 「**[!UICONTROL 作成]**」をクリックして、新規フォルダーを作成します。**[!UICONTROL 「フォルダを作成]** 」ダイアログが開きます。

1. Enter **[!UICONTROL Title]** and **[!UICONTROL Name]** of the folder and enable the **[!UICONTROL Asset Contribution]** checkbox.
フォルダーの名前には、スペースを含めずに小文字を使用することをお勧めします。

1. 「**[!UICONTROL 作成]**」をクリックします。貢献度AEM Assetsーは、フォルダーリポジトリに一覧表示されます。

   >[!NOTE]
   >
   >管理者以外のユーザーは、アセット貢献度フォルダーを作成および共有できますが、変更または削除はできません。

   ![](assets/create-contribution-folder.png)

1. クリックして投稿フォルダーを開くと、投稿フォルダー内に **[!UICONTROL SHARED]** と **[!UICONTROL NEW]** の 2 つのサブフォルダーが自動的に作成されているのがわかります。

   ![](assets/contribution-folder.png)

You can now [configure the contribution folder properties](brand-portal-configure-contribution-folder-properties.md).


