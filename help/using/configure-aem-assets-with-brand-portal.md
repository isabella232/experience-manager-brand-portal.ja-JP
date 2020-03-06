---
title: Brand PortalでのAEM Assetsの設定
seo-title: Brand PortalでのAEM Assetsの設定
description: Brand PortalでのAEM Assetsの設定に関する洞察を得ます。
seo-description: Brand PortalでのAEM Assetsの設定に関する洞察を得ます。
uuid: null
content-type: reference
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: tm+mt
source-git-commit: 58110f1635a9e74340d4a8901e86c0c6a99cf4e2

---


# Configure AEM Assets with Brand Portal {#configure-integration}

Adobe Experience Manager (AEM)Assetsは、Adobe I/Oを通じてBrand Portalで設定され、Brand Portalテナントの認証用にIMSトークンを取得します。 この設定により、Brand Portalユーザーのアセットの公開、アセットの配信、およびアセットの貢献度機能が有効になります。

>[!NOTE]
>
>以前は、Brand Portalは従来のOAuth Gatewayを介してクラシックUIで設定されていました。レガシーOAuth Gatewayは、JWTトークン交換を使用して認証用のIMSアクセストークンを取得します。
>
>レガシーOAuthを使用した設定は、2020年4月6日からはサポートされなくなり、Adobe I/Oを使用した設定に変更されました。
>
>レガシーOAuth Gatewayの設定を持つ既存のBrand Portalユーザーの場合は、既存の設定を削除し、Adobe I/Oで新しい設定を作成することをお勧めします。
>
>ただし、設定を変更しない場合は、既存の設定が引き続き機能します。

Brand PortalでAEM Assetsを設定する手順は、AEMのバージョン、および初めて設定するか、既存の設定をアップグレードするかによって異なります。

| **AEM のバージョン** | **新しい設定** | **アップグレード設定** |
|---|---|---|
| **AEM 6.5 （6.5.4.0以降）** | [設定の作成](https://docs.adobe.com/content/help/en/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [アップグレード設定](https://docs.adobe.com/content/help/en/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
| **AEM 6.4 （6.4.8.0以降）** | [設定の作成](https://docs.adobe.com/content/help/en/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [アップグレード設定](https://docs.adobe.com/content/help/en/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-64) |
| **AEM 6.3 （6.3.3.8以降）** | [設定の作成](https://helpx.adobe.com/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html) | [アップグレード設定](https://helpx.adobe.com/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html#Upgradeconfiguration) |
| **AEM 6.2** | サポートへのお問い合わせ | サポートへのお問い合わせ |


<!--
   Comment Type: draft

   <li> </li>
   -->

<!--
   Comment Type: draft

   <li>Step text</li>
   -->
