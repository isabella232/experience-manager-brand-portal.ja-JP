---
title: コントリビューションフォルダーの作成
seo-title: コントリビューションフォルダーの作成
description: 'AEM Assets でコントリビューションフォルダーを作成する方法を説明します。 '
seo-description: AEM Assets でコントリビューションフォルダーを作成する方法を説明します。
uuid: null
content-type: reference
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: ht
source-git-commit: 413a6bd17d689d0af0cce20bbd7dedb6ae3cf9b5

---


# コントリビューションフォルダーの作成 {#create-contribution-folder}

追加の&#x200B;**アセットコントリビューション**&#x200B;プロパティを持つ新しいフォルダーを AEM ユーザー（管理者／管理者以外のユーザー）が作成できるので、この新規作成フォルダーを Brand Portal ユーザーによるアセット送信に利用することができます。これにより、新しく作成された&#x200B;**コントリビューション**&#x200B;フォルダー内に **SHARED** および **NEW** という 2 つのサブフォルダーを追加作成するワークフローが自動的にトリガーされます。

**新しいコントリビューションフォルダーを作成するには：**
1. AEM オーサーインスタンス（デフォルト URL：http:// localhost:4502/aem/start.html）にログインします。
1. **[!UICONTROL アセット／ファイル]**&#x200B;に移動します。AEM Assets リポジトリの既存のすべてのフォルダーがリストされます。
1. 「**[!UICONTROL 作成]**」をクリックして、新規フォルダーを作成します。フォルダーを作成ポップアップウィンドウが開きます。
1. フォルダーの「**[!UICONTROL タイトル]**」および「**[!UICONTROL 名前]**」を入力し、「**[!UICONTROL アセットコントリビューション]**」チェックボックスをオンにします。フォルダーの名前には、スペースを含まない小文字のアルファベットを使用することをお勧めします。
1. 「**[!UICONTROL 作成]**」をクリックします。
   ![](assets/create-contribution-folder.png)
1. AEM Assets リポジトリに、新しく作成したコントリビューションフォルダーがリストされます。
1. クリックしてコントリビューションフォルダーを開くと、コントリビューションフォルダー内に **[!UICONTROL SHARED]** と **[!UICONTROL NEW]** の 2 つのサブフォルダーが自動的に作成されているのがわかります。\
   ![](assets/contribution-folder.png)

これで、新しく作成したコントリビューションフォルダーのプロパティを設定できます。[コントリビューションフォルダーのプロパティの設定](brand-portal-configure-contribution-folder-properties.md)を参照してください。