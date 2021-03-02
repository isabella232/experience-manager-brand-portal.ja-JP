---
title: アセットをアップロードし、Brand PortalからAEM Assetsに貢献度フォルダーを公開する
seo-title: アセットをアップロードし、Brand PortalからAEM Assetsに貢献度フォルダーを公開する
description: 新しいアセットのアップロードと、Brand PortalからAEM Assetsへの貢献度フォルダーの公開について把握できます。
seo-description: 新しいアセットのアップロードと、Brand PortalからAEM Assetsへの貢献度フォルダーの公開について把握できます。
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: tm+mt
source-git-commit: 268ee9dc83e98e01107f474780b658b8ccefafa4
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 79%

---


# AEM Assets への投稿フォルダーの公開 {#using-asset-souring-in-bp}

適切な権限を持つ Brand Portal ユーザーは、複数のアセットや、複数のアセットを含むフォルダーを投稿フォルダーにアップロードできます。ただし、Brand Portal ユーザーは **NEW** フォルダーにのみアセットをアップロードできます。す。**SHARED** フォルダーは、ベースラインアセット（参照用コンテンツ）を配布するためのものです。投稿用の新しいアセットを作成する際に Brand Portal ユーザーが使用できます。

投稿フォルダーへのアクセス権を持つ Brand Portal ユーザーは、次のアクティビティを実行できます。

* [アセット要件のダウンロード](#download-asset-requirements)
* [投稿フォルダーへの新しいアセットのアップロード](#uplad-new-assets-to-contribution-folder)
* [AEM Assets への投稿フォルダーの公開](#publish-contribution-folder-to-aem)

## アセット要件のダウンロード {#download-asset-requirements}

Brand Portal ユーザーは、投稿フォルダーが AEM ユーザーによって共有されるたびに、電子メール／パルス通知を自動的に受け取ります。これにより、アセット要件を確実に理解するための概要（アセット要件）ドキュメントおよびベースラインアセット（参照用コンテンツ）を **SHARED** フォルダーからダウンロードできます。

Brand Portal ユーザーは、アセット要件をダウンロードするために、次のアクティビティを実行します。

* **概要をダウンロード**：投稿フォルダーに添付されている概要（アセット要件ドキュメント）をダウンロードします。アセットのタイプ、目的、サポートする形式、最大アセットサイズなどのアセット関連情報が含まれます。
* **ベースラインアセットをダウンロード**：必要なアセットのタイプを理解するために使用できるベースラインアセットをダウンロードします。Brand Portal ユーザーは、これらのアセットを参照用に使用して、投稿用の新しいアセットを作成します。

新しく共有された投稿フォルダーと共に、Brand Portal ユーザーに対して許可された既存のすべてのフォルダーが Brand Portal ダッシュボードに反映されます。この例では、Brand Portal ユーザーのみが新しく作成された投稿フォルダーへのアクセス権を持ち、他の既存のフォルダーはユーザーと共有されていません。

**アセット要件をダウンロードするには：**

1. Brand Portal インスタンスにログインします。
1. Brand Portal ダッシュボードから投稿フォルダーを選択します。
1. 「**[!UICONTROL プロパティ]**」![](assets/properties.png)をクリックします。プロパティウィンドウが開き、アセットの投稿フォルダーの詳細が表示されます。
   ![](assets/download-asset-requirement1.png)
1. 「**[!UICONTROL 概要をダウンロード]**」![](assets/download.png)をクリックして、アセット要件ドキュメントをローカルマシンにダウンロードします。
   ![](assets/download-asset-requirement2.png)
1. Brand Portal ダッシュボードに戻ります。
1. クリックして投稿フォルダーを開くと、投稿フォルダー内に **[!UICONTROL SHARED]** と **[!UICONTROL NEW]** の 2 つのサブフォルダーが表示されます。SHARED フォルダーには、管理者によって共有されたすべてのベースラインアセット（参照用コンテンツ）が含まれます。
1. すべてのベースラインアセットを含む **[!UICONTROL SHARED]** フォルダーをローカルマシンにダウンロードできます。または、**[!UICONTROL SHARED]** フォルダーを開き、**ダウンロード**&#x200B;アイコン![](assets/download.png)をクリックして、個別のファイル／フォルダーをダウンロードできます。
   ![](assets/download-asset-requirement3.png)

概要（アセット要件ドキュメント）を確認し、ベースラインアセットを参照して、アセット要件を理解します。これで、貢献度の新しいアセットを作成し、貢献度フォルダーにアップロードできます。


## 投稿フォルダーへのアセットのアップロード {#uplad-new-assets-to-contribution-folder}

Brand Portalのユーザーは、アセットの要件を確認した後、貢献度の新しいアセットを作成して、貢献度フォルダー内の新しいフォルダーにアップロードできます。

>[!NOTE]
>
>Brand Portal ユーザーは、アセットを NEW フォルダーにのみアップロードできます。
>
>Brand Portal テナントの最大アップロード数は **10** GBです。これは累積的にすべての投稿フォルダーに適用されます。

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

すべてのアセットまたはフォルダーを NEW フォルダーにアップロードしたら、投稿フォルダーを AEM Assets に公開します。


## AEM Assets への投稿フォルダーの公開 {#publish-contribution-folder-to-aem}

Brand Portal ユーザーは、AEM オーサーインスタンスにアクセスすることなく、投稿フォルダーを AEM Assets に公開できます。

必ずアセット要件を確認してから、投稿フォルダー内の **NEW** フォルダーに新しく作成されたアセットをアップロードします。

**投稿フォルダーを公開するには：**

1. Brand Portal インスタンスにログインします。

1. Brand Portal ダッシュボードから投稿フォルダーを選択します。
1. 「**[!UICONTROL AEM に公開]**」をクリックします。

   ![](assets/export.png)

   ![](assets/publish-contribution-folder-to-aem.png)

公開ワークフローの様々な段階で、電子メール／パルス通知が Brand Portal ユーザーおよび管理者に送信されます。
1. **キューに登録済み** - Brand Portal で公開ワークフローがトリガーされると、Brand Portal ユーザーおよび Brand Portal 管理者に通知が送信されます。

1. **完了** — 投稿フォルダーが AEM Assets へ正常に公開されると、Brand Portal ユーザーおよび Brand Portal 管理者に通知が送信されます。

新しく作成したアセットを AEM Assets に公開した後、Brand Portal のユーザーは、NEW フォルダーからそれらのアセットを削除できます。一方、Brand Portal 管理者は、NEW フォルダーと SHARED フォルダーの両方からアセットを削除できます。

投稿フォルダー作成の目的を達成したら、Brand Portal 管理者は投稿フォルダーを削除して、他のユーザーが使用できるようアップロード領域を解放できます。

**公開ジョブの状態**

管理者は、Brand PortalからAEM Assetsに公開されたアセット貢献度フォルダーのステータスを表示するのに使用できる2つのレポートがあります。

* Brand Portalで、**[!UICONTROL ツール]**/**[!UICONTROL アセット貢献度ステータス]**&#x200B;に移動します。 このレポートは、投稿ワークフローの様々な段階でのすべての投稿ジョブのステータスを反映します。

   ![](assets/contribution-folder-status.png)

* AEM Assets作成者インスタンスで、**[!UICONTROL ツール]** > **[!UICONTROL ジョブ]**&#x200B;に移動します。 このレポートは、すべての公開ジョブの最終状態（成功またはエラー）を反映します。

   ![](assets/publishing-status.png)

>[!NOTE]
>
>Cloud ServiceとしてのAEM Assetsのユーザーインターフェイスには若干の違いがありますが、ワークフローは変わりません。






