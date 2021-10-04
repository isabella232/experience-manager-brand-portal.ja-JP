---
title: Experience Manager Assets と Brand Portal の連携の設定
seo-title: Configure Experience Manager Assets with Brand Portal
description: Brand PortalでのExperience ManagerAssets の設定について説明します。
seo-description: Get an insight into configuring Experience Manager Assets with Brand Portal.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 49%

---

# Experience Manager Assets と Brand Portal の連携の設定 {#configure-integration}

Adobe Experience Manager Assets と Brand Portal の連携を設定すると、Brand Portal ユーザー向けにアセットの公開、アセットの配布、アセットの投稿機能が可能になります。これにより、Experience ManagerAssets ユーザーは、Brand Portalユーザーと共にアセットを公開および配布できます。 Brand Portalのユーザーは、新しいアセットをアセット投稿フォルダーにアップロードしてExperience Managerアセットに公開することで、共有アセットにアクセスして投稿できます。

Brand PortalでのExperience Managerアセットの設定は、次の場所でサポートされています。

* Experience ManagerとしてのCloud Service
* Experience Managerアセット（オンプレミスおよびマネージドサービス）6.3 以降

Experience ManagerアセットをCloud Serviceとして設定するには、Cloud Manager からBrand Portalをアクティベートします。 アクティベーションワークフローは、バックエンドで必要な設定を作成し、Cloud ServiceインスタンスとしてのExperience ManagerAssets と同じ IMS 組織上のBrand Portalをアクティベートします。

これに対し、Experience Managerアセット（オンプレミスおよびマネージドサービス）は、Adobe開発者コンソールを使用してBrand Portalで手動で設定します。開発者コンソールは、Brand Portalテナントの認証用のAdobeIdentity Managementサービス (IMS) トークンを取得します。

>[!NOTE]
>
>***Experience Managerアセット 6.3 以降の場合***
>
>これまで、Brand Portal は、旧来の OAuth ゲートウェイを通じてクラシックインターフェイスで設定されていました。このゲートウェイは、JSON Web トークン（JWT）交換を使用して認証用の IMS トークンを取得します。
>
>旧来の OAuth を使用した設定は、2020 年 4 月 6 日以降はサポートされなくなり、Adobe Developer Console を使用した設定に変更されました。


>[!TIP]
>
>***既存のお客様のみ（オンプレミス版および Managed Services 版）***
>
>旧来の OAuth ゲートウェイを通じた設定は、既存のお客様には引き続きご利用いただけます。
>
>旧来の OAuth ゲートウェイを通じた設定で問題が発生した場合は、Adobe Developer Console で既存の設定を削除して新しい設定を作成します。

AEM Assets と Brand Portal の連携を設定する手順は、AEM のバージョンと、初めて設定するか既存の設定をアップグレードするかによって異なります。

| **AEM のバージョン** | **新しい設定** | **設定のアップグレード** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [Brand Portal のライセンス認証](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html) | - |
| **AEM 6.5（6.5.4.0 以降）** | [設定の作成](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [設定のアップグレード](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
| **AEM 6.4（6.4.8.0 以降）** | [設定の作成](https://experienceleague.adobe.com/docs/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [設定のアップグレード](https://experienceleague.adobe.com/docs/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-64) |
| **AEM 6.3（6.3.3.8 以降）** | [設定の作成](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html) | [設定のアップグレード](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html#Upgradeconfiguration) |
| **AEM 6.2** | サポートへのお問い合わせ | サポートへのお問い合わせ |
