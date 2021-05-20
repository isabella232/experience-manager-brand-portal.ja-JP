---
title: リリースノート
seo-title: リリースノート
description: Adobe Experience Manager Assets Brand Portal 2021.02.0 リリースの機能、機能強化、修正された重要な問題および既知の問題について説明します。
seo-description: Adobe Experience Manager Assets Brand Portal 2021.02.0 リリースの機能強化、修正された重要な問題および既知の問題について説明します。
uuid: 3d6ffb6f-4608-4e83-8486-5c90e06cdb43
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 79ebb9fc-385c-48a8-979e-374f42517988
exl-id: e4e89080-9863-4857-8f3a-fcd516ef3271
source-git-commit: d2bfd06f8cd8a9e78efbc8dd92880e0faae39176
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 100%

---

# リリースノート {#release-notes}

Adobe Experience Manager Assets Brand Portal 2021.02.0 リリースの新機能、機能強化、修正された重要な問題および既知の問題について説明します。

## リリース情報 {#release-information}

| 製品 | Adobe Experience Manager Assets Brand Portal |
|---|---|
| バージョン | 2021.02.0 |
| 日付 | 2021 年 2 月 |

## 概要 {#overview}

Adobe Experience Manager（AEM）Assets Brand Portal では、承認されたクリエイティブアセットを容易に取得、制御し、それらのアセットを、デバイスの種類を問わず、外部の関係者や内部のビジネスユーザーに安全に配布できます。アセットの共有を効率化し、アセットの市場投入までの時間を短縮し、コンプライアンス違反や不正アクセスのリスクを低減できます。Brand Portal では、アセットの参照、検索、プレビュー、ダウンロードおよび会社で承認された形式での書き出しを、いつでも、どこでも実行できます。

## 2021.02.0 の新機能 {#whats-new-in-2021.02.0}

### 新機能 {#new-features}

このリリースには、次の新機能が含まれています。

* AEM Assets as a Cloud Service は、事前設定済みの Brand Portal インスタンスを持つことができるようになりました。Cloud Manager ユーザーは、AEM Assets as a Cloud Service インスタンスに Brand Portal をアクティベートできます。

* アセットソーシング機能が AEM Assets as a Cloud Service で使用できるようになりました。これにより、Brand Portal ユーザーが、許可された投稿フォルダーにアセットをアップロードし、Brand Portal から AEM Assets as a Cloud Service インスタンスに投稿フォルダーを公開できるようになります。

* **[!UICONTROL ダウンロード設定]**&#x200B;に「**[!UICONTROL アセットのダウンロード]**」設定が追加されました。アセットフォルダー、アセットコレクション、複数アセットのいずれかをダウンロードする際にアセットごとに別個のフォルダーが作成されます。

<!-- 
* The **[!UICONTROL Download]** dialog is revamped in a list view with additional options to exclude the renditions which are not required, apply the same set of rules for similar asset types, and download the selected asset renditions. See [steps to download assets from Brand Portal](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/download/brand-portal-download-assets.html#download-assets).
-->

<!--
* The new **[!UICONTROL Download]** dialog now appears with all the renditions of the selected assets or folders containing assets in a list view, wherein the Brand Portal users can apply same set of renditions for similar asset types and download the selected asset renditions. 
-->

<!-- 
* Navigation to the **[!UICONTROL Files]**, **[!UICONTROL Collections]**, and **[!UICONTROL Shared Links]** is now possible from all the Brand Portal pages in one-click.  

* The **[!UICONTROL Renditions]** panel in the asset details page now allows the Brand Portal users to select the original asset and (or) specific asset renditions, and directly download them from the **[!UICONTROL Renditions]** panel without having to open the **[!UICONTROL Download]** dialog. See [download assets from asset details page](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/download/brand-portal-download-assets.html#download-assets-from-asset-details-page).
-->

<!--
Brand Portal users can exclude specific renditions which are not required and directly download the original asset and its renditions from the **[!UICONTROL Renditions]** panel on the asset details page. 
-->

<!-- 
* In addition to the existing **[!UICONTROL Download]** configurations, the Brand Portal administrators can also [configure permissions for different group of users](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/download/brand-portal-download-assets.html#configure-download-permissions) to view and (or) download the original asset and its renditions from the asset details page. These configurations will define who can access and (or) download the asset renditions.
-->

### 機能強化 {#enhancements}

このリリースで強化された機能は次のとおりです。

* フォルダーのダウンロードの場合は、**[!UICONTROL ダウンロード設定]**&#x200B;に関係なく、共有リンクを使用してアセットごとに個別のフォルダーが作成されます。
* Brand Portal の&#x200B;**[!UICONTROL 使用状況レポート]**&#x200B;が変更され、アクティブな Brand Portal ユーザーのみを反映するようになりました。

<!--
* The threshold of session timeout for the guest users has been reduced from 2 hours to 15 minutes.
* The additional **[!UICONTROL View pages]** option has been removed for multi-page PDFs as the user can now view the PDF pages from the Adobe Document Cloud Viewer.
-->


### 修正された重要な問題 {#critical-issues-fixed}

このリリースでは、次の重要な問題が修正されています。

* 元のアセットのみがダウンロードされる場合、そのアセットには独自の拡張子が反映され、拡張子が手動で zip に変更されるまでアセットが開きません。
* コレクションフォルダーのユーザーインターフェイスが、ナビゲーション矢印のクリックに応答しません。
* フォルダーが空でも、**[!UICONTROL 列]**&#x200B;表示で「**[!UICONTROL 作成]**」ボタンが表示されます。
* Brand Portal インスタンスへのアクセス時に Dispatcher がバイパスされた場合、414 エラーメッセージ（要求 URI が長すぎる）が表示されて、**[!UICONTROL オムニサーチ]**&#x200B;が失敗します。
* アセットのファイル名にコンマ（`,`）が含まれている場合、空の zip フォルダーがダウンロードされます。
* 閲覧者ユーザーは、自分が作成したコレクションにユーザーを追加するオプションを使用できます。
* 共有リンクを使用してアセット（サムネールまたは Web レンディション）をダウンロードする場合、動作に一貫性がありません。

詳しくは、[Brand Portal 2021.02.0 の新機能](whats-new.md)を参照してください。


### 既知の問題 {#known-issues}

このリリースには、次の既知の問題が含まれています。

* アセットソーシングの公開ワークフローに関係する電子メール通知がユーザーに届きません。

<!--
### Known Issues {#known-issues}

This release includes the following known issue:

* Search on the **[!UICONTROL Asset Reports]** shows processing on the product interface with no search result.
* The video DM encodes are not visible to the non-admin users on the asset details page.
* The alignment of the size of individual asset renditions and total download size is distorted in the Download dialog.
-->


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

## 製品のアクセスとサポート（制限付きサイト） {#product-access-and-support-restricted-sites}

以下のサイトは既存ユーザーのみが参照できます。アクセス権を必要とするお客様は、アドビのアカウントマネージャーにご連絡ください。

<!--
* [https://daycare.day.com](https://daycare.day.com) 
-->

* [製品へのアクセス](https://login.marketing.adobe.com)

* [アドビカスタマーケア](https://helpx.adobe.com/jp/contact.html)
