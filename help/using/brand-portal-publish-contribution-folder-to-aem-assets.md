---
title: AEM Assets への投稿フォルダーの公開
seo-title: AEM Assets への投稿フォルダーの公開
description: Brand Portal の AEM Assets への投稿フォルダーの公開について説明します。
seo-description: Brand Portal の AEM Assets への投稿フォルダーの公開について説明します。
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: tm+mt
source-git-commit: 8e08fdfb95686d28960c0fd440754b90c22ae557
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 69%

---


# AEM Assets への投稿フォルダーの公開 {#publish-contribution-folder-to-aem}

Brand Portal ユーザーは、AEM オーサーインスタンスにアクセスすることなく、投稿フォルダーを AEM Assets に公開できます。

必ず[アセット要件](brand-portal-download-asset-requirements.md)を確認してから、投稿フォルダー内の **NEW** フォルダーに新しく作成されたアセットをアップロードします。[投稿フォルダーへのアセットのアップロード](brand-portal-upload-assets-to-contribution-folder.md)を参照してください。

**投稿フォルダーを公開するには：**

1. Brand Portal インスタンスにログインします。

1. Brand Portal ダッシュボードから投稿フォルダーを選択します。
1. 「**[!UICONTROL AEM に公開]**」をクリックします。

   ![](assets/export.png)

   ![](assets/publish-contribution-folder-to-aem.png)

公開ワークフローの様々な段階で、電子メール／パルス通知が Brand Portal ユーザーおよび管理者に送信されます。
1. **キューに登録済み** - Brand Portal で公開ワークフローがトリガーされると、Brand Portal ユーザーおよび Brand Portal 管理者に通知が送信されます。

1. **完了** — 投稿フォルダーが AEM Assets へ正常に公開されると、Brand Portal ユーザーおよび Brand Portal 管理者に通知が送信されます。


**公開ジョブの状態**

管理者は、Brand PortalからAEM Assetsに公開されたアセット貢献度フォルダーのステータスを表示するのに使用できる2つのレポートがあります。

* Brand Portalで、**[!UICONTROL ツール]**/**[!UICONTROL アセット貢献度ステータス]**&#x200B;に移動します。 このレポートは、投稿ワークフローの様々な段階（キューに登録済みおよび完了）を含む、すべての投稿ジョブのステータスを反映しています。

* AEM Assets作成者インスタンスで、**[!UICONTROL ツール]** > **[!UICONTROL ジョブ]**&#x200B;に移動します。 このレポートには、保留状態の公開ジョブのみが反映されます。




