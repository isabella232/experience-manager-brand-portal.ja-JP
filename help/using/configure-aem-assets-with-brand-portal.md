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
source-git-commit: de21e84b93a657570db2024c2ceba58704ba5844
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 59%

---


# AEM Assets と Brand Portal の連携の設定 {#configure-integration}

Adobe Experience Managerアセットブランドポータルを使用してCloud ServiceとしてAdobe Experience Managerアセットを設定すると、ブランドポータルユーザと共にアセットを公開および配信できます。 一方、AEM 6.3（およびそれ以降）をBrand Portalで設定すると、Brand Portalユーザーがアセットを公開、配信、およびアセット貢献度機能を使用できます。

Adobe Experience Managerアセットは、Adobe開発者コンソールを介してBrand Portalで設定され、Brand Portalテナントの認証用にAdobeIdentity Managementサービス(IMS)トークンを調達します。

>[!NOTE]
>
>***AEM Assets 6.3 以降の場合***
>
>以前は、Brand Portalは、レガシーOAuth Gateway経由の従来のインターフェイスで設定されていました。レガシーOAuth Gatewayは、JSON Webトークン(JWT)交換を使用して、認証用のIMSトークンを取得します。
>
>旧来の OAuth を使用した設定は、2020 年 4 月 6 日以降はサポートされなくなり、Adobe 開発者コンソールを使用した設定に変更されました。


>[!TIP]
>
>***既存のお客様のみ***
>
>旧来の OAuth ゲートウェイを通じた設定は、既存のお客様には引き続きご利用いただけます。
>
>旧来の OAuth ゲートウェイを通じた設定で問題が発生した場合は、Adobe 開発者コンソールで既存の設定を削除し新しい設定を作成します。


Brand PortalでAEM Assetsを設定する手順は、AEMのバージョンによって異なります。また、初めて設定する場合と、既存の設定をアップグレードする場合でも、それぞれ異なります。

| **AEM のバージョン** | **新しい設定** | **設定のアップグレード** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [設定の作成](https://docs.adobe.com/content/help/ja-JP/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html) | - |
| **AEM 6.5（6.5.4.0 以降）** | [設定の作成](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [設定のアップグレード](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
| **AEM 6.4（6.4.8.0 以降）** | [設定の作成](https://docs.adobe.com/content/help/ja-JP/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [設定のアップグレード](https://docs.adobe.com/content/help/ja-JP/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-64) |
| **AEM 6.3（6.3.3.8 以降）** | [設定の作成](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html) | [設定のアップグレード](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html#Upgradeconfiguration) |
| **AEM 6.2** | サポートへのお問い合わせ | サポートへのお問い合わせ |


