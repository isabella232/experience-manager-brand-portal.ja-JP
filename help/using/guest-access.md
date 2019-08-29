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
source-git-commit: 770c353b1143d879280df310012ce9d4d30b40c9

---


# Brand Portal へのゲストによるアクセス {#guest-access-to-brand-portal}

[!DNL AEM Brand portal] ポータルへのゲストアクセスを許可します。ゲストユーザーは資格情報がなくてもポータルに入ることができ、ポータルの公開アセット（およびコレクション）へのアクセス権を持ちます。Users in the guest session can add assets to their lightbox (private collection) and download the same until their session lasts, which is 2 hours from the beginning of the session unless the guest user chooses to [End Session](#exit-guest-session).

Guest access functionality enables organizations to [quickly share approved assets](../using/brand-portal-sharing-folders.md#how-to-share-folders) with the intended audience at scale without having to onboard them. [!DNL Brand Portal] 6.4.2 以降には、複数の同時ゲストユーザー（組織あたりの合計ユーザークォータの 10%）に対応する機能が搭載されています。Allowing guest access saves time to manage and on-board scores of users who need to use limited functionalities on [!DNL Brand Portal].\
組織は、管理ツールパネルの「アクセス」設定の「ゲスト [!DNL Brand Portal] アクセス **を許可」** オプションを使用して、組織のアカウントに対するゲスト **アクセス** を有効（または無効）にすることができます。

<!--
Comment Type: annotation
Last Modified By: mgulati
Last Modified Date: 2018-08-17T10:42:59.879-0400
Removed the first para: "AEM Assets Brand Portal allows public users to enter the portal anonymously and have restricted access to the allowed public resources as guests. Organization users with guest role need not seek access and authentication from administrators."
-->

![](assets/enable-guest-access.png)

## ゲストセッションの開始 {#begin-guest-session}

匿名で Brand Portal に入るには、Brand Portal ようこそ画面で&#x200B;**[!UICONTROL ゲストとしてアクセスしますか？]**&#x200B;の横にある「**ここをクリックしてください**[!DNL Brand Portal] をクリックしてください。Users need not seek access and wait for the administrator to authenticate them to grant access to use the [!DNL Brand Portal].

![](assets/bp-login-screen.png)

## ゲストセッションの期間 {#guest-session-duration}

ゲストユーザーセッションは 2 時間アクティブのままになります。This means that the state of the [!UICONTROL lightbox] is preserved until 1 hour from the session start time, and after 2 hours the current guest session restarts so the lightbox state is lost.\
For example, a guest user logs in to the [!DNL Brand Portal] at 1500 hours and adds assets to lightbox for download at 16:50 hours. If the user doesn't download the [!UICONTROL lightbox collection] (or its assets) before 17:00 hours, the [!UICONTROL lightbox] will become empty as the user will have to restart the session at the end of 1 hour (that is 1700 hours).

## 許可されている同時ゲストセッション {#concurrent-guest-sessions-allowed}

同時ゲストセッション数は、組織ごとのユーザー割り当ての合計数の10%に制限されます。つまり、ユーザーの割り当てを200人にする組織では、最大20人のユーザーが同時に作業できます。21人のユーザーがアクセスを拒否され、20人のアクティブなゲストユーザーのセッションが終了したときにのみゲストとしてアクセスできるようになります。

## ゲストユーザーの Brand Portal の操作 {#guest-user-interaction-with-brand-portal}

### ゲスト UI ナビゲーション

On entering the [!DNL Brand Portal] as the guest, users are able to see all the [assets and folders shared](../using/brand-portal-sharing-folders.md#sharefolders) publicly or with guest users exclusively. これはコンテンツのみの表示であり、アセットがカード、リストまたは列レイアウトで表示されます。

![](assets/disabled-folder-hierarchy1.png)

However, Guest Users see the folder tree (starting from the root folder) and the shared folders arranged within their respective parent folders on logging in to the [!DNL Brand Portal], if administrators have enabled [Enable Folder Hierarchy](../using/brand-portal-general-configuration.md#main-pars-header-1621071021) configuration.

これらの親フォルダーは仮想フォルダーであり、これらに対してアクションを実行することはできません。仮想フォルダーは鍵のアイコン付きで表示されます。

カード表示でこれらをカーソルで指したり選択したりしても、共有フォルダーとは異なり、アクションタスクは表示されません。列表示やリスト表示で仮想フォルダーを選択すると「概要」ボタンが表示されます。

>[!NOTE]
>
>仮想フォルダーのデフォルトのサムネールは最初の共有フォルダーのサムネール画像になることに注意してください。

![](assets/enabled-hierarchy1.png) ![](assets/hierarchy1-nonadmin.png) ![](assets/hierarchy-nonadmin.png) ![](assets/hierarchy2-nonadmin.png)

「表示設定」オプションでは、ゲストユーザーは、カード表示のカードサイズや、リスト表示に表示する列を調整することができます。

![](assets/nav-guest-user.png)

コンテンツツリーを使用すると、アセット階層を移動できます。

![](assets/guest-login-ui.png)

[!DNL Brand Portal] では、 **選択した** アセット/フォルダのアセットプロパティを表示することができます。「概要」オプションは、次の場所に表示されます。

1. アセットやフォルダーを選択する際に上部に表示されるツールバー。
2. レールセレクターを選択する際のドロップダウン。

アセットやフォルダーを選択した状態で「概要」オプションを選択すると、タイトル、パス、アセット作成時間を確認できます。一方、アセットの詳細ページで「概要」オプションを選択すると、アセットのメタデータを確認できます。

![](assets/overview-option-1.png)

![](assets/overview-rail-selector-1.png)

**[!UICONTROL 左側のナビゲーションバーのナビゲーション]** オプションを使用すると、ファイルから [!UICONTROL コレクション] に移動して、ユーザーがファイルまた [!UICONTROL はコレクション内のアセットを参照できるように、ゲストセッションで戻る]ことができます。

**フィルター** オプションを使用すると、管理者が設定した検索述語を使用して、アセットファイルおよびフォルダーをフィルターできます。

### ゲストユーザーの機能

Guest users can access public assets on [!DNL Brand Portal], and also have few restrictions as discussed further.

ゲストユーザーが実行できる操作：

* access all the public folders and [!UICONTROL collections] meant for all the [!DNL Brand Portal] users.
* browse members, detail page, and have full asset view of the members of all the public folders and [!UICONTROL collections].
* search assets across public folders and [!UICONTROL collections].
* add assets to lightbox [!UICONTROL collection]. These changes to the [!UICONTROL collection] persist during the session.
* download assets directly or through lightbox [!UICONTROL collection].

ゲストユーザーが実行できない操作：

* [!UICONTROL コレクション] と保存済みの検索を作成したり、それらを共有したりできます。
* access folder and [!UICONTROL collections] settings.
* アセットをリンクとして共有する

### ゲストセッションでのアセットをダウンロードする

Guest users can directly download assets shared publically or exclusively with guest users on [!DNL Brand Portal]. Guest users can also add assets to [!UICONTROL Lightbox] (public [!UICONTROL collection]), and download the [!UICONTROL lightbox collection] before their session expires.

To download assets and [!UICONTROL collections], use the download icon from:

* quick action thumbnails, which appear on hovering over the asset or [!UICONTROL collection]
* the toolbar at the top, which appears on selecting the asset or [!UICONTROL collection]

![](assets/download-on-guest.png)

ダウンロードダイアログで「**ダウンロードアクセラレーションを有効化**」を選択すと、[ダウンロードパフォーマンスを強化](../using/accelerated-download.md)することができます。

## ゲストセッションの終了 {#exit-guest-session}

To exit a guest session, use **End Session** from the options available in the header. ただし、ゲストセッションに使用されているブラウザータブが非アクティブな場合、2時間操作がないとセッションは自動的に期限切れになります。

![](assets/end-guest-session.png)

## ゲストユーザーアクティビティの監視 {#monitoring-guest-user-activities}

Administrators can monitor guest user interaction with the [!DNL Brand Portal]. Reports generated in [!DNL Brand Portal] can provide key insights into guest user activities. 例えばたとえば、**ダウンロード**&#x200B;レポートを使用すると、ゲストユーザーによってダウンロードされたアセットの数を追跡できます。**ユーザーログイン** レポートは、指定した期間内に、ゲストユーザーが最後にポータルおよびログイン頻度にログインしたときに通知できます。
