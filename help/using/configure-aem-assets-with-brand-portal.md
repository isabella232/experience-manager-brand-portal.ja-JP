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
source-git-commit: ba8a1f09573766643f6a5013a8d181f0f0dbb4f2
workflow-type: ht
source-wordcount: '335'
ht-degree: 100%

---


# AEM Assets と Brand Portal の連携の設定 {#configure-integration}

Adobe Experience Manager（AEM）Assets と Brand Portal の連携は、Adobe 開発者コンソールを通じて設定されます。開発者コンソールは Brand Portal テナントの認証用の IMS トークンを取得します。Brand Portal が AEM Assets Cloud Service、AEM Assets 6.3 以降でサポートされるようになりました。

AEM Assets を Brand Portal でサービスできるように設定すると、Brand Portal ユーザーと共にアセットを公開および配布できます。従って、AEM 6.3 以降で Brand Portal を設定すると、Brand Portal ユーザ向けにアセットの公開、アセットの配布、アセットの投稿機能が可能になります。

>[!NOTE]
>
>***AEM Assets 6.3 以降の場合***
>
>これまで、Brand Portal は、旧来の OAuth ゲートウェイを通じてクラシック UI で設定されていました。このゲートウェイは、JWT トークン交換を使用して認証用の IMS アクセストークンを取得します。
>
>旧来の OAuth を使用した設定は、2020 年 4 月 6 日以降はサポートされなくなり、Adobe 開発者コンソールを使用した設定に変更されました。


>[!TIP]
>
>***既存のお客様のみ***
>
>旧来の OAuth ゲートウェイを通じた設定は、既存のお客様には引き続きご利用いただけます。
>
>旧来の OAuth ゲートウェイを通じた設定で問題が発生した場合は、Adobe 開発者コンソールで既存の設定を削除し新しい設定を作成します。


AEM Assets と Brand Portal の連携を設定する手順は、AEM のバージョンと、初めて設定するか既存の設定をアップグレードするかによって異なります。

| **AEM のバージョン** | **新しい設定** | **設定のアップグレード** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [設定の作成](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html) | - |
| **AEM 6.5（6.5.4.0 以降）** | [設定の作成](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [設定のアップグレード](https://docs.adobe.com/content/help/ja-JP/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
| **AEM 6.4（6.4.8.0 以降）** | [設定の作成](https://docs.adobe.com/content/help/ja-JP/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [設定のアップグレード](https://docs.adobe.com/content/help/ja-JP/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-64) |
| **AEM 6.3（6.3.3.8 以降）** | [設定の作成](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html) | [設定のアップグレード](https://helpx.adobe.com/jp/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html#Upgradeconfiguration) |
| **AEM 6.2** | サポートへのお問い合わせ | サポートへのお問い合わせ |


