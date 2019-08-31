---
title: AEM Assets Brand Portal の概要
seo-title: AEM Assets Brand Portal の概要
description: AEM Assets Brand Portal では、承認されたクリエイティブアセットを容易に取得、制御し、それらのアセットを、様々なデバイスをまたいで、外部の関係者や内部のビジネスユーザーに安全に配布できます。
seo-description: AEM Assets Brand Portal では、承認されたクリエイティブアセットを容易に取得、制御し、それらのアセットを、様々なデバイスをまたいで、外部の関係者や内部のビジネスユーザーに安全に配布できます。
uuid: b1e54d03- eb2e-488e- af4d- bae817dd135a
content-type: reference
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
topic-tags: introduction
discoiquuid: 6aefa298-4728-4b8e- a85b- e419ee37f2f4
translation-type: tm+mt
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# AEM Assets Brand Portal の概要 {#overview-of-aem-assets-brand-portal}

マーケティング担当者として、チャネルパートナーや社内ビジネスユーザーと協力して、関連するデジタルコンテンツを迅速に作成、管理および配信することが必要になることがあります。関連するコンテンツをカスタマージャーニー全体にわたってタイミングよく配信することは、顧客のニーズやコンバージョン、エンゲージメント、ロイヤリティを促進するために不可欠です。

しかし問題は、広範囲に広がる内部チームやパートナー、リセラーとの間でブランドロゴやガイドライン、キャンペーンアセット、製品の写真を効率的かつ安全に共有できるソリューションを構築するのは容易ではないということです。

**Adobe Experience Manager（AEM）Assets Brand Portal では、承認されたクリエイティブアセットを容易に取得、制御し、それらのアセットを、様々なデバイスをまたいで、外部の関係者や内部のビジネスユーザーに安全に配布できます。**&#x200B;アセットの共有を効率化し、アセットの市場投入時間を短縮し、コンプライアンス違反や不正アクセスのリスクを低減できます。

ブラウザーベースのポータル環境を使用すると、承認された形式でアセットを簡単にアップロード、参照、検索、プレビューおよび書き出すことができます。

## ブランドポータルのユーザーの役割 {#Personas}

ブランドポータルでは、次のユーザーロールをサポートしています。

* ゲストユーザー
* 閲覧者
* エディター
* 管理者

次の表に、これらの役割を持つユーザーが実行できるタスクを示します。

|  | **参照** | **検索** | **ダウンロード** | **フォルダーの共有** | **コレクションの共有** | **アセットをリンクとして共有** | **管理ツールにアクセス** |
|--- |--- |--- |--- |--- |--- |--- |--- |
| **ゲストユーザー** | ✓* | ✓* | ✓* | x | x | x | x |
| **閲覧者** | ✓ | ✓ | ✓ | x | x | x | x |
| **エディター** | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | x |
| **管理者** | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |

* ゲストユーザーは、公開フォルダーおよび公開コレクション内にあるアセットのみを参照、アクセス、および検索できます。

### ゲストユーザー {#guest-user}

認証なしで Brand Portal 上のアセットに対する制限付きのアクセス権を持つユーザーはすべてゲストユーザーです。ゲストセッションでは、ユーザーは公開フォルダーやコレクションにアクセスできます。ユーザーは、アセットの詳細を参照し、公開フォルダーとコレクションのメンバーのアセットビューを完全に表示できます。You can search, download, and add public assets to [!UICONTROL Lightbox] collection.

ただし、ゲストセッションでは、コレクションや保存済みの検索結果を作成したり、それらを共有したりすることはできません。ゲストセッション中のユーザーはフォルダーやコレクションの設定にアクセスしたり、アセットを リンク. 以下に、ゲストユーザーが実行できるタスクのリストを示します。

[公開アセットの参照および公開アセットへのアクセス](browse-assets-brand-portal.md)

[公開アセットの検索](brand-portal-searching.md)

[公開アセットのダウンロード](brand-portal-download-users.md)

[アセットを[!UACROL Lightbox]](brand-portal-light-box.md#add-assets-to-lightbox)

### 閲覧者 {#viewer}

Brand Portal の標準ユーザーは一般的に、閲覧者の役割を持ちます。この役割を持つユーザーは、承認されたフォルダー、コレクションおよびアセットにアクセスできます。また、アセット（元のアセットまたは特定のレンディション）を参照、プレビュー、ダウンロードおよび書き出したり、アカウント設定を指定したり、アセットを検索したりすることもできます。次に、閲覧者が実行できるタスクの一覧を示します。

[アセットの参照](browse-assets-brand-portal.md)

[アセットの検索](brand-portal-searching.md)

[アセットのダウンロード](brand-portal-download-users.md)

### エディター {#editor}

エディターの役割を持つユーザーは、閲覧者が実行できるタスクをすべて実行できます。さらに、管理者によって共有されたファイルとフォルダーを表示できます。コンテンツ（ファイル、フォルダー、コレクション）を他のユーザーと共有することもできます。

エディターは、閲覧者が実行できるタスクに加えて、次のタスクを実行できます。

[フォルダーの共有](brand-portal-sharing-folders.md)

[コレクションの共有](brand-portal-share-collection.md)

[アセットをリンクとして共有](brand-portal-link-share.md)

### 管理者 {#administrator}

An administrator includes a user marked as system administrator or Brand Portal product administrator in [!UICONTROL Admin Console]. 管理者は、システム管理者とユーザーを追加／削除したり、プリセットを定義したりできます。また、ユーザーに電子メールを送信したり、ポータルの使用状況とストレージに関するレポートを表示したりできます。

エディターでは、エディターで以下の追加タスクを実行できるすべてのタスクを実行できます。

[ユーザー、グループおよびユーザーの役割の管理](brand-portal-adding-users.md)

[壁紙、ページヘッダーおよび電子メールのカスタマイズ](brand-portal-branding.md)

[カスタム検索ファセットの使用](brand-portal-search-facets.md)

[メタデータスキーマフォームの使用](brand-portal-metadata-schemas.md)

[画像プリセットまたは動的レンディションの適用](brand-portal-image-presets.md)

[レポートの操作](brand-portal-reports.md)

AEM Assets の作成者は、上記のタスクに加えて、次のタスクを実行できます。

[AEM Assets と Brand Portal の統合の設定](https://helpx.adobe.com/experience-manager/6-5/assets/using/brand-portal-configuring-integration.html)

[Brand Portal へのフォルダーの公開](https://helpx.adobe.com/experience-manager/6-5/assets/using/brand-portal-publish-folder.html)

[Brand Portal へのコレクションの公開](https://helpx.adobe.com/experience-manager/6-5/assets/using/brand-portal-publish-collection.html)

## ブランドポータルURLの代替エイリアス {#tenant-alias-for-portal-url}

ブランドポータル6.4.3以降には、ブランドポータルテナントの既存のURLの1つの代替（エイリアス） URLを含めることができます。エイリアスURLは、URLに代替プレフィックスを付けることで作成できます。\
カスタマイズできるのは Brand Portal URL のプレフィックスのみであり、URL 全体でないことに注意してください。For example, an organization with existing domain **[!UICONTROL geomettrix.brand-portal.adobe.com]** can get **[!UICONTROL geomettrixinc.brand-portal.adobe.com]** created on request.

ただし、AEM オーサーインスタンスを[設定](https://helpx.adobe.com/experience-manager/6-5/assets/using/brand-portal-configuring-integration.html)する際にはテナント ID URL のみを使用できます。テナントエイリアス（代替）URL は使用できません。

>[!NOTE]
>
>既存のポータル URL 中のテナント名のエイリアスを取得するには、各組織からアドビサポートへ新規テナント名の作成依頼を出す必要があります。この依頼が処理される際は、まずそのエイリアスが使用可能かどうかの確認がおこなわれ、その後でエイリアスが作成されます。
>
>古いエイリアスを置き換えたり、古いエイリアスを削除するには、同じ手続きに従う必要があります。

## Brand Portal へのアクセス権の申請 {#request-access-to-brand-portal}

ユーザーは、Brand Portal へのアクセス権をログイン画面から申請できます。These requests are sent to Brand Portal administrators, who grant access to users through the Adobe [!UICONTROL Admin Console]. アクセス権が付与されると、ユーザーに通知電子メールが届きます。

アクセス権を申請するには、以下の手順を実行します。

1. From the Brand Portal login page, select **[!UICONTROL Click here]** corresponding to **[!UICONTROL Need Access?]** が表示されるまでカーソルを行の左側に移動して、行を選択します。However, to enter the guest session, select the **[!UICONTROL Click here]** corresponding to **[!UICONTROL Guest Access?]**.

   ![ブランドポータルログイン画面](assets/bp-login-requestaccess.png)

   [!UICONTROL アクセスを申請]ページが開きます。

2. To request access to an organization’s Brand Portal, you must have a valid [!UICONTROL Adobe ID], [!UICONTROL Enterprise ID], or [!UICONTROL Federated ID].

   [!UICONTROL リクエストアクセス] ページで、ID（シナリオ1）を使用してサインインするか [!UICONTROL 、Adobe ID] （シナリオ2）を作成します。
   ![[!UICONTROL アクセスの要求]](assets/bplogin_request_access_2.png)

   **シナリオ1**
   1. [!UICONTROL Adobe ID]、 [!UICONTROL Enterprise ID]または [!UICONTROL Federated ID]を持っている場合は、 **[!UICONTROL 「サインイン]**」をクリックします。
[!UICONTROL 「サインイン] 」ページが開きます。
   2. [!UICONTROL Adobe ID] 資格情報を入力し、 **[!UICONTROL 「サインイン]**」をクリックします。
      ![Adobe Sign in](assets/bplogin_request_access_3.png)
   [!UICONTROL リクエストアクセス] ページにリダイレクトされます。
   **シナリオ2**
   1. [!UICONTROL Adobe ID]を持っていない場合は、「リクエストアクセス」ページから「 **[!UICONTROL Adobe ID]** を取得」 [!UICONTROL をクリック] します。
[!UICONTROL 「サインイン] 」ページが開きます。
   2. Click **[!UICONTROL Get an Adobe ID]**.
[!UICONTROL 入会] ページが開きます。
   3. 姓と名、電子メールID、パスワードを入力します。
   4. 「入会」を選択 ****します。
      ![](assets/bplogin_request_access_5.png)
   [!UICONTROL リクエストアクセス] ページにリダイレクトされます。

3. 次のページには、アクセスのリクエストに使用する名前と電子メールIDが表示されます。Leave a comment for the administrator, and click **[!UICONTROL Submit]**.

   ![](assets/bplogin-request-access.png)

## 製品管理者がアクセス権を付与 {#grant-access-to-brand-portal}

ブランドポータル製品管理者は、ブランドポータル通知領域内のアクセス要求と、インボックス内の電子メールを受信します。

![要求された通知へのアクセス](assets/bplogin_request_access_7.png)

To grant access, product administrators need to click the relevant notification in Brand Portal notification area and then click **[!UICONTROL Grant Access]**.
Alternatively, product administrators can follow the link provided in the access request email to visit Adobe [!UICONTROL Admin Console] and add the user to the relevant product configuration.
![](assets/bplogin_request_access_8.png)

[Adobe[!UACROL管理コンソール]](https://adminconsole.adobe.com/enterprise/overview) ホームページ。Use Adobe [!UICONTROL Admin Console] to create users and assign them to product profiles (formerly known as product configurations), which show as groups in Brand Portal. For more information about adding users in [!UICONTROL Admin Console], see [Add a user](brand-portal-adding-users.md#add-a-user) (follow Steps 4-7 in the procedure to add a user).

## Brand Portal のメンテナンス通知 {#brand-portal-maintenance-notification}

Brand Portal のメンテナンスのために停止が計画されている場合は、Brand Portal にログインすると、バナー通知が表示されます。以下に通知の例を示します。

![](assets/bp_maintenance_notification.png)

この通知を解除すると、Brand Portal を引き続き使用できます。この通知は、新しいセッションごとに表示されます。

## リリースおよびシステム情報 {#release-and-system-information}

<!--* [What's new](../using/whats-new.md)-->
* [リリースノート](brand-portal-release-notes.md)
* [サポートされているファイル形式](brand-portal-supported-formats.md)

## 関連リソース {#related-resources}

* [アドビカスタマーケア](https://helpx.adobe.com/marketing-cloud/contact-support.html)
* [AEM フォーラム](https://www.adobe.com/go/aod_forums_en)