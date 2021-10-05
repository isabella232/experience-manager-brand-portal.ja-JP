---
title: リリースノート
seo-title: Release Notes
description: Adobe Experience Manager Assets Brand Portal 2021.10.0 リリースの機能、機能強化、修正された重要な問題および既知の問題について説明します。
seo-description: Get an insight into the enhancements, critical issues fixed, and known issues in the Adobe Experience Manager Assets Brand Portal 2021.10.0 release.
uuid: 3d6ffb6f-4608-4e83-8486-5c90e06cdb43
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 79ebb9fc-385c-48a8-979e-374f42517988
exl-id: e4e89080-9863-4857-8f3a-fcd516ef3271
source-git-commit: 262d69829eda31b6f55d2e9c3254efd62fe259c1
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 85%

---

# リリースノート {#release-notes}

Adobe Experience Manager Assets Brand Portal 2021.10.0 リリースの新機能、機能強化、修正された重要な問題および既知の問題について説明します。

## リリース情報 {#release-information}

| 製品 | Adobe Experience Manager Assets Brand Portal |
|---|---|
| バージョン | 2021.10.0 |
| 日付 | 2021 年 10 月 |

## 概要 {#overview}

Adobe Experience Manager（AEM）Assets Brand Portal では、承認されたクリエイティブアセットを容易に取得、制御し、それらのアセットを、デバイスの種類を問わず、外部の関係者や内部のビジネスユーザーに安全に配布できます。アセットの共有を効率化し、アセットの市場投入までの時間を短縮し、コンプライアンス違反や不正アクセスのリスクを低減できます。Brand Portal では、アセットの参照、検索、プレビュー、ダウンロードおよび会社で承認された形式での書き出しを、いつでも、どこでも実行できます。

## 2021.10.0 の新機能 {#whats-new-in-2021.10.0}

<!--
### New Features {#new-features}

This release includes the following new features:

* AEM Assets as a Cloud Service is now entitled to have a pre-configured Brand Portal instance. The Cloud Manager user can activate Brand Portal on the AEM Assets as a Cloud Service instance.

* Asset Sourcing feature is now available on AEM Assets as a Cloud Service. It allows the Brand Portal users to upload assets to the permitted contribution folders and publish the contribution folder from Brand Portal to AEM Assets as a Cloud Service instance. 

* An additional **[!UICONTROL Asset Download]** setting has been introduced under the **[!UICONTROL Download Settings]**. It creates a separate folder for each asset while downloading the folders, collections, or bulk download of assets. 
-->
<!-- 
* The **[!UICONTROL Download]** dialog is revamped in a list view with additional options to exclude the renditions which are not required, apply the same set of rules for similar asset types, and download the selected asset renditions.
-->

<!--
* The new **[!UICONTROL Download]** dialog now appears with all the renditions of the selected assets or folders containing assets in a list view, wherein the Brand Portal users can apply same set of renditions for similar asset types and download the selected asset renditions. 
-->

<!-- 
* Navigation to the **[!UICONTROL Files]**, **[!UICONTROL Collections]**, and **[!UICONTROL Shared Links]** is now possible from all the Brand Portal pages in one-click.  

* The **[!UICONTROL Renditions]** panel in the asset details page now allows the Brand Portal users to select the original asset and (or) specific asset renditions, and directly download them from the **[!UICONTROL Renditions]** panel without having to open the **[!UICONTROL Download]** dialog.
-->

<!--
Brand Portal users can exclude specific renditions which are not required and directly download the original asset and its renditions from the **[!UICONTROL Renditions]** panel on the asset details page. 
-->

<!-- 
* In addition to the existing **[!UICONTROL Download]** configurations, the Brand Portal administrators can also [configure permissions for different group of users]() to view and (or) download the original asset and its renditions from the asset details page. These configurations will define who can access and (or) download the asset renditions.
-->

<!--
### Enhancements {#enhancements}

Brand Portal 2021.08.0 is an internal release that introduces Business profiles for enterprise and teams customers to give organizations better control over their assets. 

This release includes the following enhancements:

* The users now have organization-specific entitlement on the new and migrated organizations. If a user is entitled to multiple organizations, the user has to select the organization at the time of login.

* The new users that are added in Admin Console must **Join Team** to get entitled to the organization. 

>[!NOTE]
>
>Business profiles are currently applicable for the new organizations that are created after August 16, 2021. 
>
>Until your organization is migrated, you can continue to use Adobe ID, Enterprise ID, or Federated ID types to access the organization.   
-->

<!-- 
* For folder download, a separate folder is created for each asset using share link irrespective of the **[!UICONTROL Download Settings]**. 
* The Brand Portal **[!UICONTROL Usage Report]** has been modified to reflect only the active Brand Portal users.
-->

<!--
* The threshold of session timeout for the guest users has been reduced from 2 hours to 15 minutes.
* The additional **[!UICONTROL View pages]** option has been removed for multi-page PDFs as the user can now view the PDF pages from the Adobe Document Cloud Viewer.
-->


### 修正された重要な問題 {#critical-issues-fixed}

このリリースでは、次の重要な問題が修正されています。

* 同じサイズの投稿フォルダーのアセットは、Brand PortalからExperience ManagerAssets に公開されません。
* アセット投稿フォルダーを非公開にしても、投稿フォルダーのサイズは小さくなりません。
* ユーザーは、適用されたメタデータスキーマプロファイルをフォルダーから削除できません。
* ユーザー権限ページのグループ数が正しくありません。
* リスト内を移動する際に、コレクションページに時間がかかりすぎる。

<!--
* Asset Sourcing email notifications are not delivered for some organizations. 

* Video files with extension `.mov` are not running on Brand Portal. 

* In the **[!UICONTROL Smart Collections]** dropdown list, only ten saved collections are visible. 
-->
<!--
* *_deleted tenants are listed as valid tenant which fails during the execution of TenantCustomizers/TenantUpdates where tenant id is returned as /etc/tenants/`<nodename>`.
-->

<!--
In case only the original assets are downloaded, the asset reflects its own extension and does not open until the extension is manually changed to zip. 
* The user interface of the collection folder does not respond on clicking the navigation arrow. 
* **[!UICONTROL Create]** button is visible in the **[!UICONTROL Column]** view even when the folders are empty.
* **[!UICONTROL Omni search]** fails with a 414 error message (Request-URI Too Long) if the dispatcher is bypassed while accessing the Brand Portal instance.
* An empty zip folder is downloaded if the asset contains a comma (`,`) in the file name.
* The viewer users get the option to add users to the collection they have created. 
* Inconsistent behavior is experienced when an asset (thumbnail or web rendition) is downloaded using share link.

See [what's new in Brand Portal 2021.02.0](whats-new.md).
-->


### 既知の問題 {#known-issues}

このリリースには、次の既知の問題が含まれています。

* ユーザーは、既存の組織の移行中に Brand Portal にログインできません。

   ただし、Brand Portal にログインしているアクティブなユーザーは、現在のセッションが期限切れになるまで引き続き作業できます。

* 管理者が Brand Portal から Admin Console に移動する際に、組織を選択するための画面が追加で表示される場合があります。


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

## 認定プラットフォーム {#certified-platforms}

このリリースの Brand Portal を実行できる認定プラットフォームを確認するには、[技術要件](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/introduction/technical-requirements.html?lang=ja)の「**オーサリングユーザーインターフェイス向けにサポートされているブラウザー**」節に記載されている表の「**UI のサポート**」列を参照してください。

## リンク {#links}

* [Adobe Experience Manager 製品ページ（adobe.com）](https://business.adobe.com/jp/products/experience-manager/adobe-experience-manager.html)
* [Assets Brand Portal のドキュメント](https://experienceleague.adobe.com/docs/experience-manager-brand-portal/using/home.html?lang=ja)

## 製品のアクセスとサポート（制限付きサイト） {#product-access-and-support-restricted-sites}

以下のサイトは既存ユーザーのみが参照できます。アクセス権を必要とするお客様は、アドビのアカウントマネージャーにご連絡ください。

<!--
* [https://daycare.day.com](https://daycare.day.com) 
-->

<!--
* [Customer Support](https://helpx.adobe.com/contact.html)
-->
