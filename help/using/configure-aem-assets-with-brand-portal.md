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
translation-type: ht
source-git-commit: dc10879caf91b81deda08682548143c60500fd1b

---


# AEM Assets と Brand Portal の連携の設定 {#configure-integration}

Adobe Experience Manager（AEM）Assets と Brand Portal の連携が、Adobe I/O を通じて設定されます。Adobe I/O は Brand Portal テナントの認証用の IMS トークンを取得します。Brand Portal が AEM Assets Cloud Service、AEM Assets 6.3 以降でサポートされるようになりました。

AEM Assets を Brand Portal でサービスできるように設定すると、Brand Portal ユーザーと共にアセットを公開および配布できます。従って、AEM 6.3 以降で Brand Portal を設定すると、Brand Portal ユーザ向けにアセットの公開、アセットの配布、アセットの投稿機能が可能になります。

>[!NOTE]
>
>***AEM Assets 6.3 以降の場合***
>
>これまで、Brand Portal は、旧来の OAuth ゲートウェイを通じてクラシック UI で設定されていました。このゲートウェイは、JWT トークン交換を使用して認証用の IMS アクセストークンを取得します。
>
>旧来の OAuth を使用した設定は、2020 年 4 月 6 日以降はサポートされなくなり、Adobe I/O を使用した設定に変更されます。


>[!TIP]
>
>***既存のお客様のみ***
>
>既存のレガシー OAuth Gateway 設定を引き続き使用することをお勧めします。レガシー OAuth Gateway 設定に問題が発生した場合は、既存の設定を削除し、Adobe I/O から新しい設定を作成します。


AEM Assets と Brand Portal の連携を設定する手順は、AEM のバージョンと、初めて設定するか既存の設定をアップグレードするかによって異なります。

| **AEM のバージョン** | **新しい設定** | **設定のアップグレード** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [設定の作成](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html) | - |
| **AEM 6.5（6.5.4.0 以降）** | [設定の作成](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [設定のアップグレード](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
| **AEM 6.4（6.4.8.0 以降）** | [設定の作成](https://docs.adobe.com/content/help/ja-JP/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [設定のアップグレード](https://docs.adobe.com/content/help/ja-JP/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-64) |
| **AEM 6.3（6.3.3.8 以降）** | [設定の作成](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html) | [設定のアップグレード](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html#Upgradeconfiguration) |
| **AEM 6.2** | サポートへのお問い合わせ | サポートへのお問い合わせ |


<!--
   Comment Type: draft

   <li> </li>
   -->

<!--
   Comment Type: draft

   <li>Step text</li>
   -->
