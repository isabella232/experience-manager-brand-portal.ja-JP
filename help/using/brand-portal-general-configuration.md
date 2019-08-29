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
source-git-commit: ea7fdd2df0696ed309227fa77e3f79d0141bcb58

---


# 管理者の一般テナント設定 {#administer-general-tenant-configurations}

[!DNL AEM] アセット [!DNL Brand Portal] を使用すると、組織は特定のテナントに次の機能を設定できます。

* 管理者によるアセットの削除
* Public [!UICONTROL collection] creation by non-admin users
* Public smart [!UICONTROL collection] creation by non-admin users
* ダウンロードアクセラレーション
* 管理者以外のユーザーが見られる共有フォルダーの親階層

These configurations have been provided as **General Settings** configurations on the administrative tools panel.

![](assets/general-configs.png)

**管理者がアセットを削除できる** 設定 [!DNL Brand Portal]。（デフォルトでは有効になっています）

**B** 設定 を参照してください。（デフォルトは有効です）

**C** 設定 を参照してください。（デフォルトは有効です）

**D** 設定を参照してください。（デフォルトでは無効になっています）

**E** 共有フォルダーの（ルートからの）フォルダー階層を管理者以外のユーザー（エディター、閲覧者、ゲストユーザー）に表示する設定。（デフォルトでは無効になっています）

## 一般設定の有効化／無効化 {#enable-disable-general-configurations}

これらの設定を有効化／無効化するには、次のようにします。

1. 管理者権限でログインします。
2. Select the [!DNL AEM] logo to access administrative tools, from the toolbar at the top.
3. From the administrative tools panel, select **General** to open the **General Settings** page.
4. それぞれの切り替えスイッチを使用して一般設定を有効化／無効化します。
5. **変更内容を保存します。**
6. ログアウトして変更を有効にします。

## Allow admin users to delete assets from [!DNL Brand Portal] {#allow-admin-users-to-delete-assets-from-brand-portal}

**ユーザーが設定を削除** できるようにすることで、管理者権限を持つユーザーがアセットやフォルダを削除する（または制限する）ことができ [!DNL Brand Portal]ます。

## 管理者以外による公開コレクションの作成を許可 {#allow-public-collections-creation-by-non-admins}

[公開 [!UICONTROL コレクション]の作成を許可]（./using/brand- portal- share-[!UICONTROL collection]. md# main- pars- text-1915052376）設定で、管理者以外のユーザーが公開 [!UICONTROL コレクション]を作成できるかどうかを制御 [!DNL Brand Portal]します。この設定はデフォルトで有効です。By disabling the configuration organizations can prevent having numerous public [!UICONTROL collection]s on their portal so that system space can be saved.

## 管理者以外による公開スマートコレクションの作成を許可 {#allow-public-smart-collections-creation-by-non-admins}

[公開スマートコレクションの作成](../using/brand-portal-searching.md#main-pars-header-500620467) を許可すると、管理者以外の管理者が検索をスマート [!UICONTROL コレクション] として保存し、そのテナントに対して公開することができます。この設定はデフォルトで有効です。By disabling the configuration organizations can prevent having a huge number of public smart [!UICONTROL collections] created by non-admin users on organization's [!DNL Brand Portal].

## ダウンロードアクセラレーションを許可 {#allow-download-acceleration}

「[ダウンロードアクセラレーションを許可](../using/accelerated-download.md)[!DNL Brand Portal]」設定では、 や共有リンクからのアセットの高速ダウンロードを許可できます。これはインストールオンデマンドアプリケーションである IBM Aspera Connect との連携によって実現されます。このアプリケーションは TCP オーバーヘッドをなくす独自のテクノロジを使用しています。

## フォルダー階層の有効化 {#enable-folder-hierarchy}

「[フォルダー階層を有効化](../using/brand-portal-sharing-folders.md#non-admin-user-access-to-shared-folders)」設定では、管理者以外のユーザー（エディター、閲覧者、ゲストユーザー）がログイン後に目にする共有フォルダーの表示を管理者が制御できます。
