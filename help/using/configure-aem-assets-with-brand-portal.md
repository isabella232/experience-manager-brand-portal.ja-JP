---
title: AEM Assets と Brand Portal の連携の設定
seo-title: AEM Assets と Brand Portal の連携の設定
description: AEM Assets と Brand Portal の連携の設定について説明します。
seo-description: AEM Assets と Brand Portal の連携の設定について説明します。
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: tm+mt
source-git-commit: bfb0c38bf8d5b542caf9d0d20d3168cdcac649b3
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 60%

---


# AEM Assets と Brand Portal の連携の設定 {#configure-integration}

Brand PortalでAdobe Experience Managerアセットを設定すると、Brand Portalユーザのアセット公開、アセット配信、およびアセット貢献度機能を有効にできます。 これにより、AEM Assetsのユーザは、Brand Portalユーザと共にアセットを公開および配信できます。 Brand Portalのユーザは、アセット貢献度フォルダに新しいアセットをアップロードしてAEM Assetsに公開することで、共有アセットにアクセスして貢献できます。

Brand PortalでのAEM Assetsの設定は、次の場所でサポートされています。
* AEM Assets as a Cloud Service
* AEM Assets(オンプレミスおよびManaged Services) 6.3以降

Cloud ServiceとしてのAEM Assetsは、Cloud ManagerからBrand Portalをアクティブ化することで、Brand Portalで自動的に設定されます。 アクティベーションワークフローは、バックエンドで必要な設定を作成し、Cloud ServiceインスタンスとしてAEM Assetsと同じIMS組織でBrand Portalをアクティブにします。

一方、AEM Assets(オンプレミスおよびManaged Services)は、Adobe開発者コンソールを使用してBrand Portalで手動で設定します。これにより、Brand Portalテナントの認証用にAdobeIdentity Managementサービス(IMS)トークンが調達されます。

>[!NOTE]
>
>***AEM Assets 6.3 以降の場合***
>
>これまで、Brand Portal は、旧来の OAuth ゲートウェイを通じてクラシックインターフェイスで設定されていました。このゲートウェイは、JSON Web トークン（JWT）交換を使用して認証用の IMS トークンを取得します。
>
>旧来の OAuth を使用した設定は、2020 年 4 月 6 日以降はサポートされなくなり、Adobe 開発者コンソールを使用した設定に変更されました。


>[!TIP]
>
>***既存のお客様専用(オンプレミスおよびManaged Services)***
>
>旧来の OAuth ゲートウェイを通じた設定は、既存のお客様には引き続きご利用いただけます。
>
>旧来の OAuth ゲートウェイを通じた設定で問題が発生した場合は、Adobe 開発者コンソールで既存の設定を削除し新しい設定を作成します。

AEM Assets と Brand Portal の連携を設定する手順は、AEM のバージョンと、初めて設定するか既存の設定をアップグレードするかによって異なります。

| **AEM のバージョン** | **新しい設定** | **設定のアップグレード** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [Brand Portal のライセンス認証](https://docs.adobe.com/content/help/ja-JP/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html) | - |
| **AEM 6.5（6.5.4.0 以降）** | [設定の作成](https://docs.adobe.com/content/help/ja/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [設定のアップグレード](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
| **AEM 6.4（6.4.8.0 以降）** | [設定の作成](https://docs.adobe.com/content/help/ja-JP/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [設定のアップグレード](https://docs.adobe.com/content/help/ja-JP/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-64) |
| **AEM 6.3（6.3.3.8 以降）** | [設定の作成](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html) | [設定のアップグレード](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html#Upgradeconfiguration) |
| **AEM 6.2** | サポートへのお問い合わせ | サポートへのお問い合わせ |
