---
title: アセットソーシングの設定
seo-title: アセットソーシングの設定
description: AEM Assetsのアセットソーシング機能の設定に関する洞察を得ます。
seo-description: AEM Assetsのアセットソーシング機能の設定に関する洞察を得ます。
uuid: null
content-type: reference
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: tm+mt
source-git-commit: add4009bd99e5af8ed0c9ffea63647c166b7c75d

---


# アセットソーシングの設定 {#configure-asset-sourcing}

AEM管理者は、AEMオーサ **ーインスタンス** 内からアセットソーシングを設定できます。 管理者は、 **AEM Web Console Configurationからアセットソーシング機能のフラグ設定を有効にし** 、アクティブなBrand portalユーザリストを **AEM Assetsにアップロードします**。

>[!NOTE]
>
>設定を開始する前に、AEM AssetsインスタンスがBrand portalと統合されていることを確認します。 See, [Configure AEM Assets integration with Brand Portal](https://helpx.adobe.com/experience-manager/6-5/assets/using/brand-portal-configuring-integration.html).


次のビデオでは、AEMオーサーインスタンスでアセットソーシングを設定する方法について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/29771?captions=jpn)

## アセットソーシングの有効化 {#enable-asset-sourcing}

AEM 管理者は、AEM Web コンソール設定（Configuration Manager）内からアセットソーシングを有効にできます。

**アセットソーシングを有効にするには：**
1. AEM オーサーインスタンスにログインして、Configuration Manager（デフォルト URL：http:// localhost:4502/system/console/configMgr）を開きます。
1. キーワード「**Asset Sourcing**」を使用して検索し、**[!UICONTROL Asset Sourcing Feature Flag Config]** を探します。
1. 「**[!UICONTROL Asset Sourcing Feature Flag Config]**」をクリックして、設定ウィンドウを開きます。
1. 「**[!UICONTROL feature.flag.active.status]**」チェックボックスを有効にします。
1. 「**[!UICONTROL 保存]**」をクリックします。

![](assets/enable-asset-sourcing.png)

## Brand Portal ユーザーリストのアップロード {#upload-bp-user-list}

AEM 管理者は、AEM Assets のアクティブな Brand Portal ユーザーリストを含む Brand Portal ユーザー 設定（.csv）ファイルをアップロードできます。コントリビューションフォルダーは、ユーザーリストで定義されたアクティブな Brand Portal ユーザーのみ共有できます。また、管理者は、設定ファイルに新規ユーザーを追加して、変更したユーザーリストをアップロードできます。

管理者は、AEM Admin Console で新規ユーザーを追加できます。詳しくは、[ユーザーの管理](brand-portal-adding-users.md)を参照してください。Admin Console でユーザーを追加したら、これらのユーザーを Brand Portal ユーザー設定ファイルに追加して、コントリビューションフォルダーへのアクセス権を割り当てることができます。

**Brand Portal ユーザーリストをアップロードするには：**
1. AEM オーサーインスタンス（デフォルト URL：http:// localhost:4502/aem/start.html）にログインします。
1. **ツール**（![](assets/tools.png)）パネルで、**[!UICONTROL アセット／Brand Portal ユーザー]**に移動します。
   ![](assets/upload-user-list1.png)
1. Brand Portal 寄稿者をアップロードウィンドウが開きます。ローカルマシンから参照して、アクティブな Brand Portal ユーザーリストを含む&#x200B;**設定（.csv）ファイル**&#x200B;をアップロードします。
1. 「**[!UICONTROL 保存]**」をクリックします。
   ![](assets/upload-user-list2.png)


管理者は、コントリビューションフォルダーを設定する際に、このユーザーリストから特定のユーザー／グループに対してアクセス権を付与できます。

詳しくは、[コントリビューションフォルダーの設定](brand-portal-contribution-folder.md)を参照してください。
