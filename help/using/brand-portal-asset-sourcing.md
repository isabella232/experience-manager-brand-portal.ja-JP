---
title: Brand Portal でのアセットソーシング
seo-title: Brand Portal でのアセットソーシング
description: Adobe Experience Manager Assets Brand Portal でリリースされたアセットソーシング機能について説明します。
seo-description: Adobe Experience Manager Assets Brand Portal でリリースされたアセットソーシング機能について説明します。
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
product: experience-manager
sub-product: アセット
feature: brand-portal
topics: collaboration, content-velocity, sharing
doc-type: feature-video
activity: use
audience: author, marketer
version: 6.5
kt: 3838
translation-type: tm+mt
source-git-commit: 5a61c42762e111b824163ce7d054d413a4da56bc
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 62%

---


# アセットソーシングの概要 {#overview-asset-sourcing-in-bp}

**アセットソーシング**&#x200B;を使用すると、追加の&#x200B;**アセット投稿**&#x200B;プロパティを持つ新しいフォルダーを AEM ユーザー（管理者／管理者以外のユーザー）が作成できるので、この新規作成フォルダーを Brand Portal ユーザーによるアセット送信に利用することができます。これにより、新しく作成された&#x200B;**投稿**&#x200B;フォルダー内に **SHARED** および **NEW** という 2 つのサブフォルダーを追加作成するワークフローが自動的にトリガーされます。次に、AEM 管理者はプロジェクトの要件を定義します。それには、投稿フォルダーに追加する必要があるアセットのタイプの簡単な説明と一連のベースラインアセットを **SHARED** フォルダーにアップロードして、BP ユーザーが必要な参照情報を確実に入手できるようにします。その後、管理者は、アクティブな Brand Portal ユーザーに投稿フォルダーへのアクセスを許可してから、新しく作成した&#x200B;**投稿**&#x200B;フォルダーを Brand Portal に公開することができます。**NEW** フォルダーへのコンテンツの追加を完了したら、ユーザーは、投稿フォルダーを AEM オーサー環境に公開できます。なお、読み込みが完了し、新しく公開したコンテンツが AEM Assets 内に反映されるまでに数分かかる場合があります。

また、既存の機能はすべてそのままで変わりません。Brand Portal ユーザーは、投稿フォルダーおよび許可された他のフォルダーからアセットを表示、検索およびダウンロードできます。さらに、管理者は投稿フォルダーの共有、プロパティの変更、コレクションへのアセットの追加をおこなうことができます。

## 前提条件 {#prerequisites}

* Cloud ServiceインスタンスとしてのAEM Assets、AEM Assets6.5.2以降。
* AEM Assets インスタンスと Brand Portal の連携が設定されていることを確認します。[AEM Assets と Brand Portal の連携の設定](../using/configure-aem-assets-with-brand-portal.md)を参照してください。
* Brand Portal テナントが 1 つの AEM Assets オーサーインスタンスで構成されていることを確認します。

>[!VIDEO](https://video.tv.adobe.com/v/29365/?quality=12)

![Brand Portal アセットソーシング](assets/asset-sourcing.png)


>[!NOTE]
>
>AEM Assets6.5.4には既知の問題があります。Brand Portalユーザーは、Adobeデベロッパーコンソールにアップグレードする際に、貢献度フォルダーのアセットをAEM Assetsに公開できません。
>
>この問題は AEM 6.5.5 で修正されました。お使いの AEM Assets インスタンスを最新のサービスパック AEM 6.5.5 にアップグレードし、Adobe 開発者コンソールで[設定をアップグレード](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65)してください。
>
>AEM 6.5.4 の即時修正をおこなうには、[ホットフィックスをダウンロード](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041)して、オーサーインスタンスにインストールすることをお勧めします。

## アセットソーシングの設定 {#configure-asset-sourcing}

**アセット** ソースは、AEM Assetsの作成者インスタンス内から設定します。管理者は、**AEM Web Console Configuration**&#x200B;からアセットソーシング機能のフラグ設定を有効にし、**AEM Assets**&#x200B;にアクティブなBrand Portalユーザーリストをアップロードできます。

>[!NOTE]
>
>資産調達は、デフォルトで、Cloud ServiceとしてAEM Assetsで有効になっています。 AEM管理者は、アクティブなBrand Portalユーザを直接アップロードして、アセットソーシング機能へのアクセスを許可できます。

>[!NOTE]
>
>設定を開始する前に、AEM Assets インスタンスと Brand Portal の連携が設定されていることを確認します。[AEM Assets と Brand Portal の連携の設定](../using/configure-aem-assets-with-brand-portal.md)を参照してください。

次のビデオでは、AEM Assets作成者インスタンスでアセットソーシングを設定する方法を示します。

>[!VIDEO](https://video.tv.adobe.com/v/29771)

### アセットソーシングの有効化 {#enable-asset-sourcing}

AEM管理者は、AEM Web Console Configuration（Configuration Managerなど）内でアセットソーシング機能フラグを有効にできます。

>[!NOTE]
>
>この手順は、Cloud ServiceとしてのAEM Assetsには適用されません。


**アセットソーシングを有効にするには：**
1. AEM Assets作成者インスタンスにログインし、Configuration Managerを開きます。
デフォルトURL:http:// localhost:4502/system/console/configMgr.
1. キーワード&#x200B;**アセットソーシング**&#x200B;を使用して&#x200B;**[!UICONTROL アセットソーシング機能フラグConfig]**&#x200B;を検索します。
1. 「**[!UICONTROL アセットソーシング機能フラグ設定]**」をクリックして設定ウィンドウを開きます。
1. 「**[!UICONTROL feature.flag.active.status]**」チェックボックスをオンにします。
1. 「**[!UICONTROL 保存]**」をクリックします。

![](assets/enable-asset-sourcing.png)

### Brand Portal ユーザーリストのアップロード {#upload-bp-user-list}

AEM 管理者は、AEM Assets のアクティブな Brand Portal ユーザーリストを含む Brand Portal ユーザー設定（.csv）ファイルをアップロードできます。投稿フォルダーは、ユーザーリストで定義されたアクティブな Brand Portal ユーザーのみ共有できます。管理者は、設定ファイルに新しいユーザーを追加し、変更したユーザーリストをアップロードすることもできます。

>[!NOTE]
>
>CSVファイルの形式は、一括Admin Consoleインポートのためのユーザーでサポートされている形式と同じです。 電子メールと氏名は必須です。

管理者はAEMAdmin Consoleで新しいユーザーを追加できます。詳しくは、[ユーザーの管理](brand-portal-adding-users.md)を参照してください。 Admin Console でユーザーを追加したら、これらのユーザーを Brand Portal ユーザー設定ファイルに追加して、投稿フォルダーへのアクセス権を割り当てることができます。

**Brand Portal ユーザーリストをアップロードするには：**
1. AEM Assetsインスタンスにログインします。
1. **ツール**&#x200B;パネルで、**[!UICONTROL アセット]**/**[!UICONTROL ブランドポータルユーザー]**&#x200B;に移動します。

1. Brand Portal 投稿者をアップロードウィンドウが開きます。ローカルマシンから参照して、アクティブな Brand Portal ユーザーリストを含む&#x200B;**設定（.csv）ファイル**&#x200B;をアップロードします。
1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/upload-user-list2.png)


管理者は、貢献度フォルダーの設定時に、このユーザーリストーから特定のユーザーへのアクセスを提供できます。 貢献度フォルダーに割り当てられたユーザーのみが、貢献度フォルダーにアクセスし、Brand PortalからAEM Assetsにアセットを公開できます。

## 関連トピック {#reference-articles}

* [貢献度フォルダーを設定し、Brand Portalに公開する](brand-portal-publish-contribution-folder-to-brand-portal.md)

* [AEM Assets への投稿フォルダーの公開](brand-portal-publish-contribution-folder-to-aem-assets.md)
