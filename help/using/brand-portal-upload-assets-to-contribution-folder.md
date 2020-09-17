---
title: 投稿フォルダーへの新しいアセットのアップロード
seo-title: 投稿フォルダーへの新しいアセットのアップロード
description: Brand Portal での投稿フォルダーへの新しいアセットのアップロードについて説明します。
seo-description: Brand Portal での投稿フォルダーへの新しいアセットのアップロードについて説明します。
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: ht
source-git-commit: ea7744001cfcf14cccf0e59eb2aa337ba8a3b1a2
workflow-type: ht
source-wordcount: '331'
ht-degree: 100%

---


# 投稿フォルダーへのアセットのアップロード {#uplad-new-assets-to-contribution-folder}

Brand Portal のユーザーは、[アセット要件](brand-portal-download-asset-requirements.md)をダウンロードして、投稿の必要性を理解できます。
また、投稿用の新しいアセットを作成して、投稿フォルダー内の NEW フォルダーにアップロードできます。

>[!NOTE]
>
>Brand Portal ユーザーは、アセットを NEW フォルダーにのみアップロードできます。
>
>Brand Portal テナントの最大アップロード数は **10** GBです。これは累積的にすべての投稿フォルダーに適用されます。


新しく作成したアセットを AEM Assets に公開した後、Brand Portal のユーザーは、NEW フォルダーからそれらのアセットを削除できます。一方、Brand Portal 管理者は、NEW フォルダーと SHARED フォルダーの両方からアセットを削除できます。

投稿フォルダー作成の目的を達成したら、Brand Portal 管理者は投稿フォルダーを削除して、他のユーザーが使用できるようアップロード領域を解放できます。

>[!NOTE]
>
>投稿フォルダーを AEM Assets に公開した後、アップロード領域を解放し、他の Brand Portal ユーザーが投稿に使用できるようにすることをお勧めします。
>
>Brand Portal テナントのアップロード制限を拡張して **10** GB を超えるようにする必要がある場合は、Adobe サポートに連絡して、要件を指定してください。


**新しいアセットをアップロードするには：**

1. Brand Portal インスタンスにログインします。新しく共有された投稿フォルダーと共に、Brand Portal ユーザーに対して許可された既存のすべてのフォルダーが Brand Portal ダッシュボードに反映されます。

1. 投稿フォルダーを選択し、クリックして開きます。投稿フォルダーには、**[!UICONTROL SHARED]** と **[!UICONTROL NEW]** の 2 つのサブフォルダーが含まれます。

1. **[!UICONTROL NEW]** フォルダーをクリックします。

   ![](assets/upload-new-assets1.png)

1. **[!UICONTROL 作成]**／**[!UICONTROL ファイル]**&#x200B;をクリックして、複数のアセットを含む個別のファイルまたはフォルダー（.zip）をアップロードします。

   ![](assets/upload-new-assets2.png)

1. アセット（ファイルまたはフォルダー）を参照し、**[!UICONTROL NEW]** フォルダーへとアップロードします。

   ![](assets/upload-new-assets3.png)

すべてのアセットまたはフォルダーを NEW フォルダーにアップロードしたら、投稿フォルダーを AEM Assets に公開します。[AEM Assets への投稿フォルダーの公開](brand-portal-publish-contribution-folder-to-aem-assets.md)を参照してください。