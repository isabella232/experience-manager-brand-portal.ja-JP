---
title: 管理者の一般テナント設定
seo-title: 管理者の一般テナント設定
description: ダウンロードのアクセラレーションを設定、公開スマート[!UACROL collection] creation， public[!UACROLコレクションを作成し、管理者ユーザーがテナント上のアセットを削除できるようにします。
seo-description: ダウンロードのアクセラレーションを設定、公開スマート[!UACROL collection] creation， public[!UACROLコレクションを作成し、管理者ユーザーがテナント上のアセットを削除できるようにします。
uuid: 3c46cd7c- c38b-4bc7- b566-93f977bc8227
contentOwner: ムムラティ
topic-tags: 管理
content-type: reference
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
discoiquuid: f4c237bc- f6a4-4bc4- af56-3d9c3027daf4
translation-type: tm+mt
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# 管理者の一般テナント設定 {#administer-general-tenant-configurations}

AEM Assets Brand Portal では、各組織が特定のテナントについて以下の機能を設定することができます。

* 管理者によるアセットの削除
* 管理者以外のユーザーによる公開コレクションの作成
* 管理者以外のユーザーによる公開スマートコレクションの作成
* ダウンロードアクセラレーション
* 管理者以外のユーザーが見られる共有フォルダーの親階層

These configurations have been provided as **[!UICONTROL General Settings]** configurations on the administrative tools panel.

![](assets/general-configs.png)

**管理者がブランドポータルからアセットを削除できる** ようにするための設定です。（デフォルトでは有効になっています）

**B** 設定を参照してください。（デフォルトでは有効になっています）

**C** 管理者以外のユーザーに対し、公開スマートコレクションを作成することを許可する設定。（デフォルトでは有効になっています）

**D** 設定を参照してください。（デフォルトでは無効になっています）

**E** 共有フォルダーの（ルートからの）フォルダー階層を管理者以外のユーザー（エディター、閲覧者、ゲストユーザー）に表示する設定。（デフォルトでは無効になっています）

## 一般設定の有効化／無効化 {#enable-disable-general-configurations}

これらの設定を有効化／無効化するには、次のようにします。

1. 管理者権限でログインします。
2. 管理ツールにアクセスするには、上部のツールバーにある AEM ロゴを選択します。
3. From the administrative tools panel, select **[!UICONTROL General]** to open the **[!UICONTROL General Settings]** page.
4. それぞれの切り替えスイッチを使用して一般設定を有効化／無効化します。
5. **[!UICONTROL 変更内容を保存します。]**
6. ログアウトして変更を有効にします。

## 管理者が Brand Portal からアセットを削除することを許可 {#allow-admin-users-to-delete-assets-from-brand-portal}

**[!UICONTROL ユーザーが設定を削除]** できるようにすることで、組織は、管理者権限を持つユーザーをブランドポータルから削除（または制限）することができます。

## 管理者以外による公開コレクションの作成を許可 {#allow-public-collections-creation-by-non-admins}

[[!UACROL「公開コレクションを許可」](../using/brand-portal-share-collection.md#main-pars-text-1915052376) 設定は、管理者以外のユーザーがブランドポータル上で公開コレクションを作成できるかどうかを制御します。この設定はデフォルトで有効です。この設定を無効にすると、ポータル上に多数の公開コレクションが作成されることを防止できるので、システム領域を節約できます。

## 管理者以外による公開スマートコレクションの作成を許可 {#allow-public-smart-collections-creation-by-non-admins}

[[!UACROL「公開スマートコレクションを許可」](../using/brand-portal-searching.md#main-pars-header-500620467) 設定は、管理者以外の管理者が検索をスマートコレクションとして保存し、そのテナントに対して公開できるかどうかを制御します。この設定はデフォルトで有効です。この設定を無効にすると、管理者以外のユーザーが組織の Brand Portal 上に多数の公開スマートコレクションを作成することを防止できます。

## ダウンロードアクセラレーションを許可 {#allow-download-acceleration}

[[!UACROLを許可するダウンロードアクセラレーションを](../using/accelerated-download.md) 使用すると、企業は、インストールオンデマンドアプリケーションであるIBM Avera Connectと統合して、ブランドポータルおよび共有リンクからのアセットの高速ダウンロードを許可できます。このアプリケーションは TCP オーバーヘッドをなくす独自のテクノロジを使用しています。

## フォルダー階層の有効化 {#enable-folder-hierarchy}

[[!UACROLを有効にするフォルダ階層を](../using/brand-portal-sharing-folders.md#non-admin-user-access-to-shared-folders) 使用すると、管理者は管理者以外のユーザー（エディター、ビューアおよびユーザーユーザー）がログイン後に共有フォルダーを表示する方法を制御できます。
