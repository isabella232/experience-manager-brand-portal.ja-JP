---
title: リリースノート
seo-title: リリースノート
description: Adobe Experience Manager Assets Brand Portal 2020.10.0 リリースの機能、機能強化、修正された重要な問題および既知の問題について説明します。
seo-description: Adobe Experience Manager Assets Brand Portal 2020.10.0 リリースの機能強化、修正された重要な問題および既知の問題について説明します。
uuid: 3d6ffb6f-4608-4e83-8486-5c90e06cdb43
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 79ebb9fc-385c-48a8-979e-374f42517988
translation-type: tm+mt
source-git-commit: 2931e19289ad8a722e3bb952e39f25b374f743c4
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 59%

---


# リリースノート {#release-notes}

Adobe Experience Manager Assets Brand Portal 2020.10.0 リリースの新機能、機能強化、修正された重要な問題および既知の問題について説明します。

## リリース情報 {#release-information}

| 製品 | Adobe Experience Manager Assets Brand Portal |
|---|---|
| バージョン | 2020.10.0 |
| 日付 | 2020 年 10 月 |

## 概要 {#overview}

Adobe Experience Manager（AEM）Assets Brand Portal では、承認されたクリエイティブアセットを容易に取得、制御し、それらのアセットを、デバイスの種類を問わず、外部の関係者や内部のビジネスユーザーに安全に配布できます。アセットの共有を効率化し、アセットの市場投入までの時間を短縮し、コンプライアンス違反や不正アクセスのリスクを低減できます。Brand Portal では、アセットの参照、検索、プレビュー、ダウンロードおよび会社で承認された形式での書き出しを、いつでも、どこでも実行できます。

## 2020.10.0 の新機能 {#whats-new-in-2020.10.0}

### 新機能 {#new-features}

このリリースには、次の新機能が含まれています。

* 不要なレンディションを除外し、類似のアセットタイプに同じルールセットを適用し、選択したアセットレンディションをダウンロードするためのオプションを追加した、 **[!UICONTROL ダウンロード]** (Download)ダイアログがリスト表示に改訂されました。

<!--
* The new **[!UICONTROL Download]** dialog now appears with all the renditions of the selected assets or folders containing assets in a list view, wherein the Brand Portal users can apply same set of renditions for similar asset types and download the selected asset renditions. 
-->

* 1回のクリックで、すべてのBrand Portalページから **[!UICONTROL ファイル]**、 **[!UICONTROL コレクション]**、 **[!UICONTROL 共有リンク]** へのナビゲーションが可能になりました。

* アセットの詳細ページの **[!UICONTROL レンディション]** パネルで、Brand Portalユーザーが元のアセットと（または）特定のアセットレンディションを選択し、 **[!UICONTROL レンディションパネルから直接ダウンロードできるようになりました。]** ダウンロード **** ダイアログを開く必要はありません。

<!--
Brand Portal users can exclude specific renditions which are not required and directly download the original asset and its renditions from the **[!UICONTROL Renditions]** panel on the asset details page. 
-->

* 既存の **[!UICONTROL ダウンロード]** 設定に加えて、Brand Portal管理者は、表示に対する様々なグループの権限を設定したり、アセットの詳細ページから元のアセットとそのレンディションをダウンロード（またはその両方）したりできます。 これらの設定により、アセットレンディションにアクセスできるユーザーと、アセットレンディションのダウンロード（またはその両方）が定義されます。


### 修正された重要な問題 {#critical-issues-fixed}

このリリースには、次の重要な問題の修正が含まれています。

* PDFにサブアセットが含まれている場合、ユーザーはPDFページを表示できません。


### 既知の問題 {#known-issues}

このリリースには、次の既知の問題が含まれています。

* ユーザが共有リンクを使用してアセットをダウンロードする場合、「元のファイルのダウンロードを **[!UICONTROL 許可]** 」オプションが無効になっていても、元のアセットがダウンロードされます。



<!--
* Download Settings configuration to configure asset download from Brand Portal. Fast download, custom renditions, and system renditions are the available configurations. 
-->

<!--
* Document Viewer has been introduced to enhance the PDF viewing experience. New options are available for viewing the PDF files in Brand Portal.

* Advances in the asset download process which improves the Brand Portal user experience while [downloading assets from Brand Portal](brand-portal-download-assets.md). Brand Portal administrators can configure **[!UICONTROL Fast Download]**, **[!UICONTROL Custom Renditions]**, and **[!UICONTROL System Renditions]** from the **[!UICONTROL Download]** settings. 

For details, see [what's new in Brand Portal 6.4.7](whats-new.md). 

### Critical Issues Fixed {#critical-issues-fixed-647}

This release includes fixes to the following critical issues:

* The viewer users are not permitted to share link for collections but the option to share is visible to them on the product interface.

* The **[!UICONTROL Download]** button on the options bar does not list all the licensed assets of the selected folder.

* The search takes longer to show the results for certain keywords.

* The **[!UICONTROL Agree]** and **[!UICONTROL Disagree]** check boxes does not appear on bulk selection of licensed and unlicensed assets during download.

* Filter-based search shows processing on the product interface with no search result. 

* The assets do not download from share link if the shared folder contains numerous and large assets.


### Known Issues {#known-issues-647}

This release includes the following known issues:

* If multiple assets are selected, license text does not appear on clicking Terms and Conditions on the license agreement page during download using share link.   

-->

## 言語 {#languages}

Brand Portal ユーザーインターフェイスは次の言語で使用できます。

* 英語
* ドイツ語
* フランス語
* スペイン語
* イタリア語
* ブラジル語ポルトガル語
* 日本語
* 簡体字中国語
* 韓国語

## 認定プラットフォーム  {#certified-platforms}

このリリースの Brand Portal を実行できる認定プラットフォームを確認するには、[技術要件](https://helpx.adobe.com/jp/experience-manager/6-4/sites/deploying/using/technical-requirements.html)の「**オーサリングユーザーインターフェイス向けにサポートされているブラウザー**」節に記載されている表の「**UI のサポート**」列を参照してください。

## リンク {#links}

* [Adobe Experience Manager 製品ページ（adobe.com）](http://www.adobe.com/jp/marketing-cloud/experience-manager.html)
* [Assets Brand Portal のドキュメント](https://helpx.adobe.com/jp/experience-manager/brand-portal/user-guide.html)

## 製品のアクセスとサポート（制限付きサイト）{#product-access-and-support-restricted-sites}

以下のサイトは既存ユーザーのみが参照できます。アクセス権を必要とするお客様は、アドビのアカウントマネージャーにご連絡ください。

* [https://daycare.day.com](https://daycare.day.com)

* [製品へのアクセス](https://login.marketing.adobe.com)

* [アドビカスタマーケア](https://helpx.adobe.com/jp/contact.html)
