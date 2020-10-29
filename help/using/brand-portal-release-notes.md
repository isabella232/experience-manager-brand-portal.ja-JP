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
source-git-commit: 5cf924ce71433e33506449bbad608d5e57a41b8d
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 86%

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

* The **[!UICONTROL Download]** dialog is revamped in a list view with additional options to exclude the renditions which are not required, apply the same set of rules for similar asset types, and download the selected asset renditions. Brand Portalからアセットをダウンロードする [手順を参照してください](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/download/brand-portal-download-assets.html#download-assets)。

<!--
* The new **[!UICONTROL Download]** dialog now appears with all the renditions of the selected assets or folders containing assets in a list view, wherein the Brand Portal users can apply same set of renditions for similar asset types and download the selected asset renditions. 
-->

* 1 回のクリックで、すべての Brand Portal ページから&#x200B;**[!UICONTROL ファイル]**、**[!UICONTROL コレクション]**、**[!UICONTROL 共有リンク]**&#x200B;へのナビゲーションが可能になりました。

* アセットの詳細ページの&#x200B;**[!UICONTROL レンディション]**&#x200B;パネルで、Brand Portal ユーザーが元のアセットと（または）特定のアセットレンディションを選択し、**[!UICONTROL ダウンロード]**&#x200B;ダイアログを開かなくて&#x200B;**[!UICONTROL レンディション]**&#x200B;パネルから直接ダウンロードできるようになりました。アセットの詳細ページからのアセットの [ダウンロードを参照してください](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/download/brand-portal-download-assets.html#download-assets-from-asset-details-page)。

<!--
Brand Portal users can exclude specific renditions which are not required and directly download the original asset and its renditions from the **[!UICONTROL Renditions]** panel on the asset details page. 
-->

* 既存の&#x200B;**[!UICONTROL ダウンロード]**&#x200B;設定に加えて、Brand Portal 管理者は、様々なユーザーのグループに対し、アセットの詳細ページからの元のアセットとそのレンディションを表示およびダウンロードする権限を設定できます。[](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/download/brand-portal-download-assets.html#configure-download-permissions)これらの設定により、アセットレンディションにアクセスできるユーザー、およびアセットレンディションのダウンロードが定義されます。

### 機能強化 {#enhancements}

このリリースで強化された機能は次のとおりです。

* ゲストユーザーのセッションタイムアウトのしきい値が 2 時間から 15 分に短縮されました。
* ユーザーがAdobe Document Cloud ビューアから PDF ページを表示できるようになったため、複数ページの PDF に対する追加の「**[!UICONTROL ページの表示]**」オプションは削除されました。


<!--
### Critical Issues Fixed {#critical-issues-fixed}

This release includes fixes to the following critical issue:

* The users are not able to view the PDF pages if the PDF contains sub assets.
-->

### 既知の問題 {#known-issues}

このリリースには、次の既知の問題が含まれています。

* **[!UICONTROL Assets レポート]**&#x200B;検索を実行すると、製品インターフェイス上での処理が表示され、検索結果は表示されません。
* アセットの詳細ページでは、管理者以外のユーザーにはビデオ DM エンコードは表示されません。
* ダウンロードダイアログで、個々のアセットレンディションのサイズとダウンロードの合計サイズが正常に整列されません。



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

## 認定プラットフォーム {#certified-platforms}

このリリースの Brand Portal を実行できる認定プラットフォームを確認するには、[技術要件](https://helpx.adobe.com/jp/experience-manager/6-4/sites/deploying/using/technical-requirements.html)の「**オーサリングユーザーインターフェイス向けにサポートされているブラウザー**」節に記載されている表の「**UI のサポート**」列を参照してください。

## リンク {#links}

* [Adobe Experience Manager 製品ページ（adobe.com）](http://www.adobe.com/jp/marketing-cloud/experience-manager.html)
* [Assets Brand Portal のドキュメント](https://helpx.adobe.com/jp/experience-manager/brand-portal/user-guide.html)

## 製品のアクセスとサポート（制限付きサイト）{#product-access-and-support-restricted-sites}

以下のサイトは既存ユーザーのみが参照できます。アクセス権を必要とするお客様は、アドビのアカウントマネージャーにご連絡ください。

<!--
* [https://daycare.day.com](https://daycare.day.com) 
-->

* [製品へのアクセス](https://login.marketing.adobe.com)

* [アドビカスタマーケア](https://helpx.adobe.com/jp/contact.html)
