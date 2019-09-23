---
title: Brand Portal へのゲストによるアクセス
seo-title: Brand Portal へのゲストによるアクセス
description: ゲストによるアクセスを許可し、認証が不要な多数のユーザーのオンボーディングにかかる労力を省きます。
seo-description: ゲストによるアクセスを許可し、認証が不要な多数のユーザーのオンボーディングにかかる労力を省きます。
uuid: edb4378d-1710-44a2-97a6-594d99f62fff
contentOwner: mgulati
topic-tags: introduction
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: b9e9fe7b-0373-42d1-851b-7c76b47657c2
translation-type: tm+mt
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# Brand Portal へのゲストによるアクセス {#guest-access-to-brand-portal}

AEM Brand Portal は、ゲストによるポータルへのアクセスを許可します。ゲストユーザーは資格情報がなくてもポータルに入ることができ、ポータルの公開アセット（およびコレクション）へのアクセス権を持ちます。Users in the guest session can add assets to their lightbox (private collection) and download the same until their session lasts, which is 2 hours from the beginning of the session unless the guest user chooses to [[!UICONTROL End Session]](#exit-guest-session).

ゲストによるアクセス機能を使用すれば、組織は対象オーディエンスのオンボーディングをおこなわなくても、[承認済みアセットをすばやく共有](../using/brand-portal-sharing-folders.md#how-to-share-folders)することができます。Brand Portal 6.4.2 以降には、複数の同時ゲストユーザー（組織あたりの合計ユーザークォータの 10%）に対応する機能が搭載されています。ゲストアクセスを許可すると、Brand Portalで限られた機能を使用する必要があるユーザーの管理やオンボードスコアを時間を節約できます。\
Organizations can enable (or disable) guest access on Brand Portal account of the organization using **[!UICONTROL Allow Guest Access]** option from **[!UICONTROL Access]** settings in the administrative tools panel.

<!--
Comment Type: annotation
Last Modified By: mgulati
Last Modified Date: 2018-08-17T10:42:59.879-0400
Removed the first para: "AEM Assets Brand Portal allows public users to enter the portal anonymously and have restricted access to the allowed public resources as guests. Organization users with guest role need not seek access and authentication from administrators."
-->

![](assets/enable-guest-access.png)

## ゲストセッションの開始 {#begin-guest-session}

匿名で Brand Portal に入るには、Brand Portal ようこそ画面で&#x200B;**[!UICONTROL ゲストとしてアクセスしますか？]**&#x200B;の横にある「**ここをクリックしてください** Brand portalのようこそ画面に表示されます。 ユーザーは、アクセス権を要求したり、管理者から認証を受けてアクセス権が付与されるのを待たなくても、Brand Portal を使用することができます。

![](assets/bp-login-screen.png)

## ゲストセッションの期間 {#guest-session-duration}

ゲストユーザーセッションは 2 時間アクティブのままになります。This means that the state of the [!UICONTROL Lightbox] is preserved until 1 hour from the session start time, and after 2 hours the current guest session restarts so the Lightbox state is lost.\
For example, a guest user logs in to the Brand Portal at 1500 hours and adds assets to Lightbox for download at 16:50 hours. If the user doesn't download the [!UICONTROL Lightbox] collection (or its assets) before 17:00 hours, the [!UICONTROL Lightbox] will become empty as the user will have to restart the session at the end of 1 hour (that is 1700 hours).

## 許可されている同時ゲストセッション {#concurrent-guest-sessions-allowed}

同時ゲストセッションの数は、組織あたりの合計ユーザークォータの 10% に制限されます。つまり、ユーザークォータが 200 の組織の場合、最大 20 人のゲストユーザーが同時に作業をすることができます。21番目のユーザはアクセスを拒否され、20人のアクティブなゲストユーザのセッションが終了した場合に限り、ゲストとしてアクセスできます。

## ゲストユーザーの Brand Portal の操作 {#guest-user-interaction-with-brand-portal}

### ゲスト UI ナビゲーション

On entering the Brand Portal as the guest, users can see all the [assets and folders shared](../using/brand-portal-sharing-folders.md#sharefolders) publicly or with guest users exclusively. これはコンテンツのみの表示であり、アセットがカード、リストまたは列レイアウトで表示されます。

![](assets/disabled-folder-hierarchy1.png)

However, the guest users see the folder tree (starting from the root folder) and the shared folders arranged within their respective parent folders on logging in to the Brand Portal, if administrators have enabled [Enable Folder Hierarchy](../using/brand-portal-general-configuration.md#main-pars-header-1621071021) configuration.

これらの親フォルダーは仮想フォルダーであり、これらに対してアクションを実行することはできません。仮想フォルダーは鍵のアイコン付きで表示されます。

No action tasks are visible on hovering or selecting them in [!UICONTROL Card View], unlike the shared folders. [!UICONTROL 「概要] 」ボタンは、「列ビュー」と「リストビュー」で仮想フォル [!UICONTROL ダを選択する] とき [!UICONTROL に表示されます]。

>[!NOTE]
>
>仮想フォルダーのデフォルトのサムネールは最初の共有フォルダーのサムネール画像になることに注意してください。

![](assets/enabled-hierarchy1.png) ![](assets/hierarchy1-nonadmin.png) ![](assets/hierarchy-nonadmin.png) ![](assets/hierarchy2-nonadmin.png)

[!UICONTROL View Settings option allows the guest users to adjust card sizes in Card View or columns to display in List View.]

![](assets/nav-guest-user.png)

The [!UICONTROL Content tree] lets you move through assets hierarchy.

![](assets/guest-login-ui.png)

Brand Portal provides [!UICONTROL Overview] option to guest users to view [!UICONTROL Asset Properties] of selected assets/folders. The [!UICONTROL Overview] option is visible:

* アセットやフォルダーを選択する際に上部に表示されるツールバー。
* レールセレクターを選択する際のドロップダウン。

On selecting the [!UICONTROL Overview] option while an asset/folder is selected, users can see the title, path, and time of asset creation. Whereas, on asset detail page selecting [!UICONTROL Overview] option lets the users see metadata of the asset.

![](assets/overview-option-1.png)

![](assets/overview-rail-selector-1.png)

左レールの「**[!UICONTROL ナビゲーション]**」オプションでは、ファイルからコレクションに移動したり、ユーザーがファイルやコレクションのアセットから参照できるよう、ゲストセッションに戻ったりすることができます。

**[!UICONTROL 「フィルター]**」オプションを使用すると、ゲストユーザーは管理者が設定した検索用述語を使用して、アセットファイルやフォルダーにフィルターを適用することができます。

### ゲストユーザーの機能

ゲストユーザーは Brand Portal の公開アセットにアクセスできますが、制約もいくつかあります（これについては後で説明します）。

ゲストユーザーが実行できる操作：

* すべての Brand Portal ユーザー向けのすべての公開フォルダーと公開コレクションにアクセスする
* メンバーや詳細ページを参照し、すべての公開フォルダーおよび公開コレクションのメンバーの完全なアセット表示をおこなう。
* 公開フォルダーおよび公開コレクション全体でアセットを検索する。
* Lightbox コレクションにアセットを追加する。コレクションに対するこれらの変更は、セッションの間保持されます。
* アセットを直接、または Lightbox コレクションからダウンロードする。

ゲストユーザーが実行できない操作：

* コレクションや保存済みの検索結果を作成、またはそれらを共有する。
* フォルダーやコレクションの設定にアクセスする。
* アセットをリンクとして共有する

### ゲストセッションでアセットをダウンロードする

ゲストユーザーは、公開アセット、またはゲストユーザーのみと共有されたアセットを Brand Portal で直接ダウンロードできます。Guest users can also add assets to [!UICONTROL Lightbox] (public collection), and download the [!UICONTROL Lightbox] collection before their session expires.

アセットやコレクションをダウンロードするには、次の場所のダウンロードアイコンを使用します。

* アセットまたはコレクションにカーソルを合わせると表示されるクイックアクションサムネール
* アセットまたはコレクションを選択すると表示される上部のツールバー

![](assets/download-on-guest.png)

ダウンロードダイアログで「**[!UICONTROL ダウンロードアクセラレーションを有効化]**[!UICONTROL 」を選択すると、]ダウンロードパフォーマンスを強化[することができます。](../using/accelerated-download.md)

## ゲストセッションの終了 {#exit-guest-session}

ゲストセッションを終了するには、ヘッダーにあるオプションから「**[!UICONTROL セッションを終了]」を使用します。**&#x200B;ただし、ゲストセッションに使用されるブラウザータブが非アクティブになっている場合、アクティビティがおこなわれなくなってから 2 時間が経過するとセッションは自動的に期限切れとなります。

![](assets/end-guest-session.png)

## ゲストユーザーアクティビティの監視 {#monitoring-guest-user-activities}

管理者は、Brand Portal でのゲストユーザーの操作を監視できます。Brand Portal で生成されたレポートは、ゲストユーザーアクティビティに関する重要なインサイトを提供できます。例えばたとえば、**[!UICONTROL ダウンロード]レポートを使用すると、ゲストユーザーによってダウンロードされたアセットの数を追跡できます。****[!UICONTROL ユーザーログイン]**&#x200B;レポートでは、ゲストユーザーがポータルに最後にログインした時刻、および指定期間内のログイン頻度を確認ができます。
