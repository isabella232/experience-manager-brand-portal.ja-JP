---
title: Brand Portal へのゲストによるアクセス
seo-title: Brand Portal へのゲストによるアクセス
description: ゲストによるアクセスを許可し、認証が不要な多数のユーザーのオンボーディングにかかる労力を省きます。
seo-description: ゲストによるアクセスを許可し、認証が不要な多数のユーザーのオンボーディングにかかる労力を省きます。
uuid: edb4378d-1710-44a2-97a6-594d99f62fff
contentOwner: ムムラティ
topic-tags: 概要
content-type: リファレンス
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
discoiquuid: b9e9fe7b-0373-42d1-851b-7c76b47657c2
translation-type: tm+mt
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# Brand Portal へのゲストによるアクセス {#guest-access-to-brand-portal}

AEM Brand Portal は、ゲストによるポータルへのアクセスを許可します。ゲストユーザーは資格情報がなくてもポータルに入ることができ、ポータルの公開アセット（およびコレクション）へのアクセス権を持ちます。Users in the guest session can add assets to their lightbox (private collection) and download the same until their session lasts, which is 2 hours from the beginning of the session unless the guest user chooses to [[!UICONTROL End Session]](#exit-guest-session).

Guest access functionality enables organizations to [quickly share approved assets](../using/brand-portal-sharing-folders.md#how-to-share-folders) with the intended audience at scale without having to onboard them. Brand Portal 6.4.2 以降には、複数の同時ゲストユーザー（組織あたりの合計ユーザークォータの 10%）に対応する機能が搭載されています。ゲストアクセスを許可すると、ブランドポータルで制限機能を使用する必要があるユーザーの管理時間を節約できます。\
組織は、管理ツールパネルの ******[!UICONTROL 「アクセス]** 権の設定」オプションを使用して、組織のブランドポータルアカウントで、ゲストアクセスを有効（または無効）にすることができます。

<!--
Comment Type: annotation
Last Modified By: mgulati
Last Modified Date: 2018-08-17T10:42:59.879-0400
Removed the first para: "AEM Assets Brand Portal allows public users to enter the portal anonymously and have restricted access to the allowed public resources as guests. Organization users with guest role need not seek access and authentication from administrators."
-->

![](assets/enable-guest-access.png)

## ゲストセッションの開始 {#begin-guest-session}

匿名で Brand Portal に入るには、Brand Portal ようこそ画面で&#x200B;**[!UICONTROL ゲストとしてアクセスしますか？]**&#x200B;の横にある「**ここをクリックしてください** を参照してください。ユーザーは、アクセス権を要求したり、管理者から認証を受けてアクセス権が付与されるのを待たなくても、Brand Portal を使用することができます。

![](assets/bp-login-screen.png)

## ゲストセッションの期間 {#guest-session-duration}

ゲストユーザーセッションは 2 時間アクティブのままになります。[!UICONTROL つまり、Lightbox] の状態はセッション開始時間から1時間経過するまで保持され、2時間後に現在のゲストセッションが再開されると、ライトボックスの状態が失われます。\
例えば、ゲストユーザーがブランドポータルに1500時間ログインし、アセットを16:50時間のダウンロード用にライトボックスに追加するとします。If the user doesn't download the [!UICONTROL Lightbox] collection (or its assets) before 17:00 hours, the [!UICONTROL Lightbox] will become empty as the user will have to restart the session at the end of 1 hour (that is 1700 hours).

## 許可されている同時ゲストセッション {#concurrent-guest-sessions-allowed}

同時ゲストセッション数は、組織ごとのユーザー割り当ての合計数の10%に制限されます。つまり、ユーザーの割り当てを200人にする組織では、最大20人のユーザーが同時に作業できます。21人のユーザーがアクセスを拒否され、20人のアクティブなゲストユーザーのセッションが終了した場合にのみゲストとしてアクセスできます。

## ゲストユーザーの Brand Portal の操作 {#guest-user-interaction-with-brand-portal}

### ゲスト UI ナビゲーション

On entering the Brand Portal as the guest, users can see all the [assets and folders shared](../using/brand-portal-sharing-folders.md#sharefolders) publicly or with guest users exclusively. これはコンテンツのみの表示であり、アセットがカード、リストまたは列レイアウトで表示されます。

![](assets/disabled-folder-hierarchy1.png)

However, the guest users see the folder tree (starting from the root folder) and the shared folders arranged within their respective parent folders on logging in to the Brand Portal, if administrators have enabled [Enable Folder Hierarchy](../using/brand-portal-general-configuration.md#main-pars-header-1621071021) configuration.

これらの親フォルダーは仮想フォルダーであり、これらに対してアクションを実行することはできません。仮想フォルダーは鍵のアイコン付きで表示されます。

No action tasks are visible on hovering or selecting them in [!UICONTROL Card View], unlike the shared folders. [!UICONTROL 列ビュー] および [!UICONTROL リストビューで仮想フォルダーを選択するときに、概要ボタンが表示]されます。

>[!NOTE]
>
>仮想フォルダーのデフォルトのサムネールは最初の共有フォルダーのサムネール画像になることに注意してください。

![](assets/enabled-hierarchy1.png) ![](assets/hierarchy1-nonadmin.png) ![](assets/hierarchy-nonadmin.png) ![](assets/hierarchy2-nonadmin.png)

[!UICONTROL 「設定を表示」] オプションを使用すると、カード表示または列の [!UICONTROL カードサイズをリストビューで][!UICONTROL 表示するためのカードサイズを調整]できます。

![](assets/nav-guest-user.png)

[!UICONTROL コンテンツツリー] を使用すると、アセット階層を移動できます。

![](assets/guest-login-ui.png)

Brand Portal provides [!UICONTROL Overview] option to guest users to view [!UICONTROL Asset Properties] of selected assets/folders. [!UICONTROL 「概要] 」オプションは表示されます。

* アセットやフォルダーを選択する際に上部に表示されるツールバー。
* レールセレクターを選択する際のドロップダウン。

On selecting the [!UICONTROL Overview] option while an asset/folder is selected, users can see the title, path, and time of asset creation. Whereas, on asset detail page selecting [!UICONTROL Overview] option lets the users see metadata of the asset.

![](assets/overview-option-1.png)

![](assets/overview-rail-selector-1.png)

**[!UICONTROL 左側のナビゲーションバーのナビゲーション]** オプションを使用すると、ファイルからコレクションに移動して、ユーザーがファイルまたはコレクション内のアセットを参照できるように、ゲストセッションで戻ることができます。

**[!UICONTROL フィルター]** オプションを使用すると、管理者が設定した検索述語を使用して、アセットファイルおよびフォルダーをフィルターできます。

### ゲストユーザーの機能

ゲストユーザーは Brand Portal の公開アセットにアクセスできますが、制約もいくつかあります（これについては後で説明します）。

ゲストユーザーが実行できる操作：

* すべての Brand Portal ユーザー向けのすべての公開フォルダーと公開コレクションにアクセスする
* メンバーや詳細ページを参照し、すべての公開フォルダーおよび公開コレクションのメンバーの完全なアセット表示をおこなう
* 公開フォルダーおよび公開コレクション全体でアセットを検索する
* Lightbox コレクションへのアセットの追加コレクションに対するこれらの変更は、セッションの間保持されます。
* アセットを直接、または Lightbox コレクションからダウンロードする

ゲストユーザーが実行できない操作：

* コレクションや保存済みの検索結果を作成、またはそれらを共有する
* フォルダーやコレクションの設定にアクセスする
* アセットをリンクとして共有する

### ゲストセッションでのアセットをダウンロードする

ゲストユーザーは、公開アセット、またはゲストユーザーのみと共有されたアセットを Brand Portal で直接ダウンロードできます。Guest users can also add assets to [!UICONTROL Lightbox] (public collection), and download the [!UICONTROL Lightbox] collection before their session expires.

アセットとコレクションをダウンロードするには、次のダウンロードアイコンを使用します。

* クイックアクションサムネール。アセットまたはコレクションの上にマウスポインターを置くと表示されます
* 上部にあるツールバー。アセットまたはコレクションの選択時に表示されます

![](assets/download-on-guest.png)

ダウンロードダイアログで「**[!UICONTROL ダウンロードアクセラレーションを有効化]**[!UICONTROL 」を選択すと、]ダウンロードパフォーマンスを強化[することができます。](../using/accelerated-download.md)

## ゲストセッションの終了 {#exit-guest-session}

To exit a guest session, use **[!UICONTROL End Session]** from the options available in the header. ただし、ゲストセッションに使用されているブラウザータブが非アクティブな場合、2時間操作がないとセッションは自動的に期限切れになります。

![](assets/end-guest-session.png)

## ゲストユーザーアクティビティの監視 {#monitoring-guest-user-activities}

管理者は、Brand Portal でのゲストユーザーの操作を監視できます。Brand Portal で生成されたレポートは、ゲストユーザーアクティビティに関する重要なインサイトを提供できます。例えばたとえば、**[!UICONTROL ダウンロード]レポートを使用すると、ゲストユーザーによってダウンロードされたアセットの数を追跡できます。****[!UICONTROL ユーザーログイン]** レポートは、指定した期間内に、ゲストユーザーが最後にポータルおよびログイン頻度にログインしたときに通知できます。
