---
title: AEM Assets Brand Portal の新機能
seo-title: AEM Assets Brand Portal の新機能
description: 6.4.4 の新機能と機能強化について説明します。
seo-description: 6.4.4 の新機能と機能強化について説明します。
uuid: 2c59d738-9b53-4f25- a205-13bf75c80b77
contentOwner: bDHar
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
content-type: reference
topic-tags: introduction
discoiquuid: fec32ca3-142b-4a11-9b92-5113fc27277a
translation-type: tm+mt
source-git-commit: cbb64eb8a79480a1ccedbe5131a38ddf6eaec88d

---


# AEM Assets Brand Portal の新機能 {#what-s-new-in-aem-assets-brand-portal}

Adobe Experience Manager（AEM）アセットブランドポータルを使用すると、承認されたクリエイティブアセットを外部のパーティや社内のビジネスユーザーに容易に取得、制御およびセキュリティで配信できます。アセットの共有を効率化し、アセットの市場投入時間を短縮し、コンプライアンス違反や不正アクセスのリスクを低減できます。アドビは Brand Portal の全体的なエクスペリエンスの強化に取り組んでいます。以下に、最新機能と機能強化について簡単に紹介します。

## 6.4.4 の変更点 {#what-is-changing-in}

Brand Portal 6.4.4 リリースでは、テキスト検索の機能強化と、お客様らのご要望への対応に重点を置いています。最新 [のブランドポータルリリースノート](brand-portal-release-notes.md)を参照してください。

### 検索の機能強化 {#search-enhancements}

Brand Portal 6.4.4 以降では、フィルタリングウィンドウのプロパティの述語で部分テキスト検索がサポートされます。To allow partial text search you need to enable **Partial Search** in Property Predicate in the search form.

部分テキスト検索およびワイルドカード検索について詳しくは、以下の説明を参照してください。

#### 部分フレーズ検索 {#partial-phrase-search}

フィルタリングウィンドウで、検索対象フレーズの一部分（1 つか 2 つの単語）のみを指定してアセットを検索できます。

**使用事例**&#x200B;部分的なフレーズ検索は、検索語句で発生した単語の完全な組み合わせがわからない場合に便利です。

例えば、Brand Portal の検索フォームで、「プロパティの述語」を使用してアセットのタイトルの部分検索をおこなう場合、「**camp**」という単語を指定すると、タイトルフレーズで「camp」という単語を使用しているアセットがすべて返されます。

![](assets/partialphrasesearch.png)

#### ワイルドカード検索 {#wildcard-search}

ブランドポータルでは、検索クエリでアスタリスク（*）を検索し、検索したフレーズ内の単語の一部として使用できます。

**使用例**&#x200B;検索されたフレーズで正しい単語が不明な場合は、ワイルドカード検索を使用して検索クエリのギャップを埋めることができます。

**例えば、«flin*** »を指定すると、ブランドポータルの検索フォームで、アセットのタイトルに対する部分検索のためにプロパティPredicateを使用している場合、文字 **で始まる単語がすべてタイトルフレーズ** で増加します。

![](assets/wildcard-prop.png)

さらに、以下のような指定ができます。

* *** theming** を指定すると、すべてのアセットが、文字 **で終わる単語がタイトルフレーズ** で増加します。

* *** inch*** を指定すると、文字を構成する単語を含むすべてのアセットが、タイトルフレーズ内で **増加** します。

>[!NOTE]
>
>「**部分検索**」チェックボックスを選択すると、デフォルトで「**大文字と小文字を区別しない**」がオンになります。

[![](https://helpx.adobe.com/content/dam/help/en/experience-manager/brand-portal/images/see-the-guide.png)](../using/brand-portal-searching.md#facetedsearchbyapplyingfilterstosearch)

## 6.4.3 の変更点 {#what-changed-in}

Brand Portal 6.4.3 リリースでは、様々な機能が強化されています。具体的には、Brand Portal のアクセス URL にテナント ID だけでなく代替エイリアスを指定できる機能、新しいフォルダー階層の設定、ビデオサポートの機能強化、AEM オーサーインスタンスから Brand Portal への公開の日時指定、運用上の機能強化、顧客リクエストへの対応などがあります。

### 管理者以外のユーザーに表示するフォルダー階層のナビゲーション

管理者以外のユーザー（エディター、閲覧者、ゲストユーザー）がログインしたときにフォルダーをどのように表示するかを管理者が設定できるようになりました。[フォルダ階層](../using/brand-portal-general-configuration.md) の設定を、管理ツールパネルの **「一般設定**」に追加します。この設定は次のように動作します。

* **有効**&#x200B;にした場合は、ルートフォルダーから始まるフォルダーツリーが管理者以外のユーザーに表示されます。これにより、管理者と同じようなナビゲーション体験を提供できます。
* **が無効**&#x200B;になっている場合、共有フォルダーのみがランディングページに表示されます。

![](assets/enable-folder-hierarchy.png)
**使用事例**

The [Enable Folder Hierarchy](../using/brand-portal-general-configuration.md) functionality (when enabled) helps you differentiate the folders with the same names shared from different hierarchies. On logging in, non-admin users now see the virtual parent (and ancestor) folders of the shared folders.
![](assets/disabled-folder-hierarchy1-2.png) ![](assets/enabled-hierarchy1-2.png)

共有フォルダーは、仮想フォルダー内のそれぞれのディレクトリ内で整理されます。仮想フォルダーは鍵のアイコン付きで表示されます。

仮想フォルダーのデフォルトのサムネールは最初の共有フォルダーのサムネール画像になることに注意してください。

![](assets/hierarchy1-nonadmin-2.png)

[![](https://helpx.adobe.com/content/dam/help/en/experience-manager/brand-portal/images/see-the-guide.png)](../using/brand-portal-general-configuration.md)

### 特定のフォルダー階層またはパス内での検索

**パスブラウザー** の述語は、特定のディレクトリ内のアセットを検索できるように、Search Formで導入されています。The default search path of search predicate for Path Browser is */content/dam/mac/&lt;tenant-id&gt;/*, which can be configured by editing the default search form.

* 管理者は、パスブラウザーを使用して、Brand Portal 上の任意のフォルダーディレクトリへ移動できます。
* 管理者以外のユーザーは、パスブラウザーを使用して、共有されているフォルダにのみ移動できます（親フォルダに移動することもできます）。
例えば、 */content/dam/mac/&lt; tandy- id&gt;/Folio/folderB/folderC* は管理者以外のユーザーと共有されます。ユーザはパスブラウザーを使用して、folderC内のアセットを検索できます。このユーザーは、folderBおよびFolioに移動することもできます（ユーザーと共有されるfolderCの祖先です）。

![](assets/edit-search-form.png)

**使用事例**

ルートフォルダーから始まる階層ではなく、参照した特定のフォルダー内でのみアセットを検索することができます。

これらのフォルダーで検索をおこなうと、ユーザーに共有されているアセットの中で検索した結果が返されることに注意してください。

![](assets/filter-panel.png)

[![](https://helpx.adobe.com/content/dam/help/en/experience-manager/brand-portal/images/see-the-guide.png)](../using/brand-portal-search-facets.md#listofsearchpredicates)

### Dynamic Media ビデオレンディションのサポート

AEM作成者インスタンスがダイナミックメディアのハイブリッドモードにあるユーザーは、元のビデオファイルに加えて、ダイナミックメディアレンディションをプレビューしてダウンロードできます。

To allow preview and download of dynamic media renditions on specific tenant accounts, administrators need to specify **Dynamic Media Configuration** (video service URL (DM-Gateway URL) and registration ID to fetch the dynamic video) in **Video** configuration from admin tools panel.

**ダイナミックメディアビデオの使用例**&#x200B;は次のとおりです。

* アセットの詳細ページ
* アセットのカード表示
* リンク共有のプレビューページ

Dynamic Media ビデオエンコードは以下の場所からダウンロードできます。

* Brand Portal
* 共有リンク

![](assets/edit-dynamic-media-config.png)

[![](https://helpx.adobe.com/content/dam/help/en/experience-manager/brand-portal/images/see-the-guide.png)](../using/brand-portal.md#tenantaliasforportalurl)

### Brand Portal への公開のスケジュール設定

[AEM（6.4.2.0）](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html#main-pars_header_9658011) 作成者インスタンスからブランドポータルへのアセット（およびフォルダー）の投稿ワークフローは、後での日付、時間をスケジュールできます。

同様に、「Brand Portal で非公開」ワークフローのスケジュールを設定することで、公開されているアセットを未来の特定の日時にポータルから取り下げることができます。

![](assets/schedule-publish.png)
![](assets/publishlater-workflow.png)

[![](https://helpx.adobe.com/content/dam/help/en/experience-manager/brand-portal/images/see-the-guide.png)](../using/brand-portal.md#tenantaliasforportalurl)

### URL 中の設定可能なテナントエイリアス

組織のポータル URL に代替プレフィックスを含めて、カスタマイズされたポータル URL を取得することができます。既存のポータル URL 中のテナント名のエイリアスを取得するには、各組織からアドビサポートへ依頼する必要があります。

カスタマイズできるのは Brand Portal URL のプレフィックスのみであり、URL 全体でないことに注意してください。\
For example, an organization with existing domain **geomettrix.brand-portal.adobe.com** can get **geomettrixinc.brand-portal.adobe.com** created on request.

ただし、AEM オーサーインスタンスを[設定](https://helpx.adobe.com/experience-manager/6-5/assets/using/brand-portal-configuring-integration.html)する際にはテナント ID URL のみを使用できます。テナントエイリアス（代替）URL は使用できません。

**使用事例**&#x200B;アドビから提供された URL をそのまま使用するのではなく、カスタマイズされたポータル URL を取得して、ブランドのニーズを満たすことができます。

[![](https://helpx.adobe.com/content/dam/help/en/experience-manager/brand-portal/images/see-the-guide.png)](../using/brand-portal.md#tenantaliasforportalurl)

### ダウンロードエクスペリエンスの強化

このリリースでは、以下の状況におけるクリックや警告の数を低減し、シンプルなダウンロードエクスペリエンスを実現しています。

* レンディションのみをダウンロードする（オリジナルのアセットはダウンロードしない）ことの選択
* オリジナルのレンディションへのアクセスが制限されているときのアセットのダウンロード

## 6.4.2 の変更点 {#what-changed-in-1}

ブランドポータル6.4.2リリースでは、組織のアセット配布ニーズに対処するための機能の範囲が提供されています。また、高速化のダウンロードを通じて、ゲストアクセスや最適なエクスペリエンスを通じて、グローバルに配布された多数のユーザーに提供できます。また、Brand Portal は、管理者向けの新しい設定や新しく追加されたレポートを通じてきめ細かな制御を実現し、お客様の要求に応じます。

### ゲストによるアクセス

![](assets/bp-login-screen-1.png)

AEM Brand Portal は、ゲストによるポータルへのアクセスを許可します。ゲストユーザーは資格情報がなくてもポータルに入ることができます。また、すべての公開フォルダーおよび公開コレクションにアクセスしたり、それらをダウンロードしたりすることができます。ゲストユーザーは、アセットをライトボックス（プライベートコレクション）に追加し、同じダウンロードを行うことができます。また、管理者によって定められたスマートタグ検索や検索用述語を表示することもできます。ゲストセッションでは、ユーザーはコレクションや保存済みの検索を作成または共有したり、フォルダーやコレクションの設定にアクセスしたり、アセットをリンクとして共有したりすることはできません。

組織では、複数の同時ゲストセッションが許可されます（同時ゲストセッションの数は、組織あたりの合計ユーザークォータの 10 ％に制限されます）。

ゲストセッションは 2 時間アクティブのままになります。そのため、Lightbox の状態も、セッション開始時刻から 2 時間保持されます。2 時間後、ゲストセッションは再起動する必要があるので、Lightbox の状態も失われます。

### ダウンロードの高速化

Brand Portal ユーザーは、最大 25 倍の速度を実現できる IBM Aspera Connect の高速ダウンロードを利用して、世界中のどこにいてもシームレスにダウンロードをおこなうことができます。Brand Portal または共有リンクからアセットを高速にダウンロードするには、ダウンロードダイアログで「**ダウンロードアクセラレーションを有効化**」オプションを選択する必要があります（その組織で高速ダウンロードが有効になっていることが前提です）。

![](assets/donload-assets-dialog-2.png)

To enable IBM Aspera based accelerated download for the organization, administrators **Enable Download Acceleration** option (which is disabled by default) from [General Settings](brand-portal-general-configuration.md#allow-download-acceleration) in the administrative tools panel. Brand Portal および共有リンクからのアセットファイルのダウンロードを高速化するための前提条件とトラブルシューティング手順について詳しくは、[Brand Portal からのダウンロードを高速化するためのガイド](../using/accelerated-download.md#main-pars-header)を参照してください。

### ユーザーログインレポート

ユーザーのログインを追跡するための新しいレポートが導入されました。**ユーザーログイン**&#x200B;レポートは、組織が Brand Portal の委任管理者やその他のユーザーを監査および監視するし、目を光らせるのに便利です。

レポートでは、レポートの生成時点まで、ブランドポータル6.4.2のデプロイメントにより、各ユーザの表示名、電子メールID、個人（管理者、Viewer、エディター、ユーザー、Viewer、エディター、ゲスト）、ログイン数がログに記録されます。管理者は、レポートを .csv 形式で書き出すことができます。ユーザーログインレポートを他のレポートと併用すれば、組織はユーザーによる承認済みのブランドリソースの操作をより厳しく監視できるので、企業コンプライアンスオフィスへの適合性を確保することができます。

![](assets/user-logins-1.png)

### オリジナルのレンディションへのアクセス

管理者が、オリジナルの画像ファイル（.jpeg、.tiff、.png、.bmp、.gif、.pjpeg、x-portable-anymap、x-portable-bitmap、x-portable-graymap、x-portable-pixmap、x-rgb、x-xbitmap、x-xpixmap、x-icon、image/photoshop、image/x-photoshop、.psd、image/vnd.adobe.photoshop）へのユーザーアクセスを制限する一方で、Brand Portal または共有リンクからダウンロード可能な低解像度のレンディションへのアクセスを許可することができます。このアクセス権は、管理ツールパネルのユーザーの役割ページの「グループ」タブからユーザーグループレベルで制御できます。

![](assets/access-original-rend-1.png)

* デフォルトでは、すべてのユーザーがオリジナルのレンディションを「オリジナルへのアクセス」としてダウンロードできます。
* ユーザーのグループがオリジナルのレンディションにアクセスできないようにするには、管理者は各チェックボックスを選択解除する必要があります。
* ユーザーが複数のグループのメンバーであり、グループのひとつのみに制約がある場合、制約はそのユーザーに適用されます。
* 制約は管理者には適用されません（管理者が制約されたメンバーである場合を含む）。
* ユーザー共有アセットをリンクとして共有する権限は、共有リンクを使用してアセットをダウンロードするユーザーに適用されます。

### カード表示およびリスト表示のフォルダー階層パス

カード表示でフォルダーのカードが、管理者以外のユーザー（エディター、ビューア、およびゲストユーザー）にフォルダ階層情報が表示されるようになりました。この機能により、ユーザーはフォルダーの場所を把握し、親階層に関してアクセスすることができます。

フォルダー階層の情報は、別のフォルダー階層から共有されている他のフォルダーと同様に名前を持つフォルダーを区別するのに特に役立ちます。管理者以外のユーザーが、自分たちに共有されているアセットのフォルダー構造を把握していない場合、似たような名前のアセット／フォルダーは紛らわしくなります。

* カードのサイズに合わせて、それぞれのカードに表示されるパスが切り詰められます。ただし、切り詰められたパスの上にマウスポインターを置くと、フルパスがツールチップとして表示されます。

![](assets/folder-hierarchy1-1.png)

リスト表示では、Brand Portal のすべてのユーザーに対し、列内のアセットのフォルダーパスを示します。

![](assets/list-view-1.png)

### アセットのプロパティを表示する「概要」オプション

Brand Portal には、選択したアセット／フォルダーのアセットプロパティを管理者以外のユーザー（エディター、閲覧者、ゲストユーザー）が表示できる「概要」オプションがあります。「概要」オプションは、次の場所に表示されます。

1. アセットやフォルダーを選択する際に上部に表示されるツールバー。
2. レールセレクターを選択する際のドロップダウン。

アセットやフォルダーを選択した状態で「概要」オプションを選択すると、タイトル、パス、アセット作成時間を確認できます。一方、アセットの詳細ページで「概要」オプションを選択すると、アセットのメタデータを確認できます。

![](assets/overview-option-2.png)

![](assets/overview-rail-selector-2.png)

## 新しい設定

管理者が特定のテナントで次の機能を有効化／無効化できるよう、6 つの新しい設定が追加されました。

* ゲストによるアクセスを許可
* ユーザーによる Brand Portal へのアクセス要求を許可
* 管理者が Brand Portal からアセットを削除することを許可
* 公開コレクションの作成を許可
* 公開スマートコレクションの作成を許可
* ダウンロードアクセラレーションを許可

上記の設定は、管理ツールパネルのアクセスおよび一般設定にあります。

![](assets/access-configs-1.png)
![](assets/general-configs-1.png)
![](assets/admin-tools-panel-13.png)

### Adobe.io は OoAuth 統合を設定するための UI をホストする

Brand Portal 6.4.2 onwards uses Adobe.io [https://legacy-oauth.cloud.adobe.io/](https://legacy-oauth.cloud.adobe.io/) interface to create JWT application, which enables configuring oAuth integrations to allow AEM Assets integration with Brand Portal. Previously, the UI for configuring OAuth integrations was hosted in [https://marketing.adobe.com/developer/](https://marketing.adobe.com/developer/). To know more about integrating AEM Assets with Brand Portal for publishing assets and collections to Brand Portal refer [Configure AEM Assets integration with Brand Portal](https://helpx.adobe.com/in/experience-manager/6-4/assets/using/brand-portal-configuring-integration.html).

## 検索の機能強化

管理者は、更新されたプロパティの述語を使用して、大文字と小文字を区別しないプロパティを作成できます。これには、「大文字と小文字を無視」のチェックがあります。このオプションは、プロパティの述語と複数値プロパティの述語で使用できます。\
ただし、大文字と小文字を区別しない検索では、プロパティの述語のデフォルト検索よりも時間がかかります。検索フィルターに大文字と小文字が区別されない文字数が多すぎる場合、検索が遅くなる可能性があります。そのため、大文字と小文字を区別しない検索は、賢く使用することをお勧めします。

## 6.4.1 の変更点 {#what-changed-in-2}

Brand Portal 6.4.1 はプラットフォームのアップグレードリリースであり、より充実した顧客エクスペリエンスを実現するために、いくつかの新機能と、閲覧、検索、パフォーマンスなどの重要な機能強化を提供します。

### 閲覧の機能強化

* 新しいコンテンツツリーレールでアセット階層内をすばやく移動できるようになりました。

![](assets/contenttree-2.png)

* Introduced new keyboard shortcuts, for example _(p)_ for navigation to properties page, _(e)_ for Edit, and _(ctrl+c)_ for copy operations.
* 多数のアセットの閲覧に対応するように、カードおよびリスト表示でのスクロールが改善され、遅延読み込みがおこなわれるようになりました。
* カード表示の機能が強化され、表示設定に基づいて様々なサイズのカードがサポートされるようになりました。

![](assets/cardviewsettings-1.png)

* カード表示で日付ラベルにマウスポインターを置くと、日時が表示されるようになりました。

* Enhanced Column view with **More Details** under the asset snapshot, which lets you navigate to details page of an asset.

![](assets/columnmoredetail.png)

* リストビューで、ロケール、アセットタイプ、サイズ、サイズ、レーティングおよびパブリケーション情報に加えて、初期設定でアセットのファイル名が表示されるようになりました。New **View Settings** can be used to configure the amount of detail to display in List view.

* アセットの詳細が強化され、新しいナビゲーションボタンを使用してアセット間を行き来し、アセット数を表示できるようになりました。

![](assets/navbtn.png)

* AEM からアップロードされたオーディオファイルをアセットの詳細ページでプレビューできるようになりました。
* アセットのプロパティに新しい関連アセット機能が追加されました。AEM上の他のソース/派生アセットに関連するアセットをブランドポータルで公開すると、ブランドポータルで関連性が維持されるようになり、プロパティページの関連アセットへのリンクが維持されるようになりました。
* 管理者以外のユーザーによる公開コレクションの作成を制限する新しい設定が追加されました。組織は、アドビサポートチームと協力して、特定のアカウントでこの機能を設定できます。

### 検索の機能強化

* 検索クエリを再度実行せずに検索項目に移動した後、検索結果の同じ位置に戻ってきた機能。
* 検索結果数が表示されるようになりました。
* ファイルタイプによる検索フィルターが強化され、以前の「画像」、「ドキュメント」、「マルチメディア」などのオプションではなく、.jpg、.png、.psd などの詳細な MIME タイプに基づいてきめ細かくフィルター処理できるようになりました。
* コレクションの検索フィルターが強化され、以前の時間スライダー機能ではなく、正確なタイムスタンプで処理できるようになりました。
* 新しいアクセスタイプフィルターが追加され、公開または非公開コレクションを検索できるようになりました。

![](assets/accesstypefilter.png)

### ダウンロードの最適化

* zipファイルを作成せずに単一の大きなファイルが直接ダウンロードされるので、速度とスループットが向上します。
* リンク共有機能の Zip ダウンロード制限が 1 GB から 5 GB に増えました。

* アセットを Brand Portal から、または共有リンク機能を利用してダウンロードするときに、カスタムファイルと元のファイルのみを選択してを使用して、ブランドポータルからアセットをダウンロードしたり、共有リンク機能を使用してアセットをダウンロードしたりできます。

![](assets/excludeautorendition.png)

### パフォーマンスの強化

* アセットのダウンロード速度が最大 100％向上しました。
* アセットの検索応答が最大 40％向上しました。
* 閲覧パフォーマンスが最大 40％向上しました。

**注意**：ここに記した向上率は、ラボテスト実施時点でのものです。

### レポート機能の強化

**リンク共有レポートの追加**&#x200B;共有リンクの情報を提供する新しいレポートが追加されました。リンク共有レポートには、指定期間内に組織全体にわたって内部および外部のユーザーと共有されるすべてのアセットへの URL が示されます。さらに、リンクがいつ共有されたか、誰と共有されたか、いつ期限が切れるかという情報も示されます。

![](assets/navigatereport.png)

**使用状況レポートへのアクセスエントリポイントの変更**&#x200B;使用状況レポートは他のレポートと統合され、アセットレポートコンソールから表示できるようになりました。To reach Asset Reports console, navigate to **Create/Manage Reports** from administrative tools panel.

![](assets/accessassetreport.png)

**ブランドポータルでレポート**&#x200B;レポートインターフェイスのユーザーエクスペリエンスが改善され、より直感的になり、組織の制御がより多くなりました。これらのレポートはブランドポータルに保存されるので、様々なレポートを作成することで、生成されたレポートを再訪問して、ダウンロードまたは削除することができます。

デフォルトの列を追加または削除することで、各レポートを作成中にカスタマイズできるようになりました。また、ダウンロード、有効期限および公開レポートにカスタム列を追加して、精度を制御することもできます。

### 管理ツールの強化

メタデータ、検索およびレポートの管理ツールに用意されているプロパティピッカーが強化され、オートコンプリート機能や閲覧機能により管理操作が簡単になりました。

### その他の機能強化

* AEM6.3.2.1および6.4からブランドポータルに公開されたアセットを、AEM Assetsブランドポータルレプリケーションダイアログの「公開フォルダー公開」チェックボックスをマークして、ブランドポータルの一般ユーザーに公開できるようになりました。

![](assets/public-folder-publish.png)

* Brand Portal へのアクセス権が申請されると、Brand Portal の通知領域に通知が届くほか、アクセス権の申請があったことを知らせる電子メールが管理者に送信されます。

## 6.3.2 の変更点 {#what-changed-in-3}

Brand Portal 6.3.2 は、顧客からの強い要望に応える新機能や拡張機能と、全般的なパフォーマンス向上を提供します。

### Brand Portal へのアクセス権の申請 {#request-access-to-brand-portal}

ユーザーは、新しい****を使用してブランドポータルへのアクセスを要求できるようになりました。これにより、ブランドポータルのログイン画面で利用できるアクセス機能が必要になります。

![](assets/bplogin_request_access.png)

Adobe ID を持っている場合と、Adobe ID を作成する必要がある場合のそれぞれに応じて、適切なワークフローに従って申請を送信できます。Brand Portal の製品管理者は、ユーザーからの申請が通知領域に届いたら、Adobe Admin Console からアクセスを付与します。

詳しくは、[Brand Portal へのアクセス権の申請](../using/brand-portal.md#requestaccesstobrandportal)を参照してください。

### ダウンロードされたアセットのレポートの機能強化 {#enhancement-in-the-assets-downloaded-report}

ダウンロードされたアセットのレポートに、指定期間中のユーザー別のアセットダウンロード回数が含まれるようになりました。このレポートを .csv 形式でダウンロードすると、ライセンスが必要なアセットの合計ダウンロード数などのデータを集計できます。

![](assets/reports_download_downloaded_by.png)

詳しくは、[追加レポートの作成と管理](../using/brand-portal-reports.md#createandmanageadditionalreports)の手順 3 および 6 を参照してください。

### Brand Portal のメンテナンス通知 {#brand-portal-maintenance-notification}

次回のメンテナンス作業の 2～3 日前に通知バナーが表示されるようになりました。以下に通知の例を示します。

![](assets/bp_maintenance_notification-1.png)

For more information, see [Brand Portal maintenance notification](https://helpx.adobe.com/experience-manager/brand-portal/using/brand-portal.html#BrandPortalmaintenancenotification).

### リンク共有機能で共有される要ライセンスアセットの機能強化 {#enhancement-for-licensed-assets-shared-using-the-link-share-feature}

ライセンスが必要なアセットをリンク共有機能でダウンロードするときに、そのアセットの使用許諾契約書への同意が求められるようになりました。

![](assets/copyright_management.png)

For more information, see Step 12 in [Share assets as a link](../using/brand-portal-link-share.md#shareassetsasalink).

### ユーザーピッカーの機能強化 {#user-picker-enhancement}

ユーザーピッカーのパフォーマンスが向上し、ユーザーを膨大に抱える顧客のニーズに対応できるようになりました。

### Adobe Experience Cloud ブランディングの変更 {#experience-cloud-branding-changes}

Brand Portal は、新しい Adobe Experience Cloud ブランディングに準拠するようになりました。

![](assets/bp_solution_switcher.png)

## 6.3.1 の変更点 {#what-changed-in-4}

Brand Portal 6.3.1 は、Brand Portal と AEM の統合に向けた新機能と拡張機能を含みます。

### ユーザーインターフェイスのアップグレード {#upgraded-user-interface}

現在、Brand Portal のユーザーエクスペリエンスを AEM と統合するために、Coral 3 ユーザーインターフェイスへの移行を進めています。この変更により、ナビゲーションや外観を含む全体的な操作性が向上します。

#### ナビゲーションの強化 {#enhanced-navigational-experience}

* 以下に示す新しいアドビロゴから、管理ツールにすばやくアクセスできます。

![](assets/aemlogo-3.png)

* オーバーレイから製品のナビゲーションができます。

![](assets/overlay_navigation.png)

* 親フォルダーにすばやく移動できます。

![](assets/navigationparentfolders.png)

* 必要なコンテンツとツールをすばやく検索して移動できます。

![](assets/omnisearchicon.png)

### 閲覧の強化 {#enhanced-browsing-experience}

* 新しい列表示で、ネストされたフォルダーを参照できます。

![](assets/millercolumnnavigation.png) ![](assets/multi-columnview.png)

* アップロードされた最新のアセットは、フォルダー内のアセットの一覧の一番上に表示されます。

### 検索の強化 {#enhanced-search-experience}

* 新しいオムニサーチ機能により、検索キーワードを入力すると自動的に検索候補が表示されるので、その中から関連するコンテンツや機能、タグにすばやくアクセスできます。オムニサーチは、すべての検索機能で使用できます。

![](assets/omnisearch_whatsnew.png)

* オムニサーチに検索フィルターを追加すれば、検索結果をより細かく絞り込んで、検索を効率化できます。

![](assets/omnisearch_withfilters.png)

* 新しい評価ベースのアセット検索を使用すると、アセットを評価に基づいて検索できます（AEM Assets から公開されている場合）。
* 新しい複数値検索では、AND 演算子で複数のキーワードを指定して、アセットをすばやく検出できます。
* 新しい検索ブースト機能を使用すると、検索関連性を向上させて、特定のアセットを検索結果の一番上に表示できます。
* 新しいパスベースの検索機能を使用すると、アセットを検索できるネストされたフォルダーへのパスが見つかります。

#### 新しいスマートタグベースの検索 {#new-smart-tags-based-search}

スマートタグ付きの画像が AEM Assets から Brand Portal に公開されている場合は、Brand Portal 内で、スマートタグの名前を検索キーワードとして使用して、これらの画像を検索できます。この機能は、ファイルに対してのみ使用できます。

### ダウンロードの強化 {#enhanced-downloading-experience}

ネストされたフォルダーをダウンロードした後も、元のフォルダー階層を保持できます。ネストされたフォルダー内のアセットを、それぞれのフォルダーではなく、単一のフォルダーにダウンロードすることも可能です。

### パフォーマンスの強化 {#improved-performance}

参照、検索およびダウンロード機能が強化され、Brand Portal のパフォーマンスが大幅に向上しています。

### アセットの新しい Digital Rights Management {#new-digital-rights-management-for-assets}

管理者は、アセットを共有する前に、そのアセットの有効期限（日時）を設定できます。有効期限が切れたアセットは、閲覧者とエディターが見ることはできますが、ダウンロードはできません。アセットの有効期限が切れると、管理者に通知されます。

### アセットの並べ替えの強化 {#enhanced-asset-sorting}

リスト表示でのフォルダー内アセットの並べ替えを、最初のページに表示されるアセットの数に関係なく実行できるようになりました。フォルダー内のすべてのアセットが最初のページに表示されるかどうかに関係なく、すべてのアセットが並べ替えられます。

### レポートの強化 {#reporting-capabilities}

管理者は、アセットのダウンロード、期限切れ、公開に関する 3 種類のレポートを作成および管理できます。レポート内に列を設定したり、レポートを CSV 形式で書き出したりすることも可能です。

![](assets/newreport.png)

### 追加のメタデータ {#additional-metadata}

Brand Portal 6.3.1 には、AEM Assets 6.3 と同じメタデータが追加されています。スキーマエディターフォームを使用して、アセットのプロパティページに表示するメタデータを制御できます。アセットメタデータは外部リンク共有ユーザーには表示されません。このユーザーは、リンク共有URLを使用してアセットをプレビューおよびダウンロードできます。

![](assets/additionsinmetadata.png)

### 管理者用機能の追加 {#additional-capabilities-for-administrators}

* 管理者は、ログイン画面の壁紙のカスタマイズを最終決定する前に、変更内容をプレビューできます。

![](assets/wallpaperpreview.png)

* 管理者が追加する新しいユーザーは、Brand Portal に自動的に追加されるので、Brand Portal への招待に同意する必要はありません。

### AEM Assets 6.3 の新しい公開機能 {#new-publishing-capabilities-in-aem-assets}

* AEM 管理者は、2017 年 Q4 に提供される AEM 6.3 SP 1-CFP 1 (6.3.1.1) を使用して、AEM Assets から Brand Portal にメタデータスキーマを公開できます。

![](assets/publish_metadataschemaaemassets.png)

* AEM管理者は、AEM6.2SP1- CFP7およびAEM6.3SP1- CFP1（6.3.1.1）を使用して、AEM Assetsからブランドポータルにすべてのタグを公開できます。

![](assets/publish_tags_aemassets.png)

* AEM Assets から、タグ（スマートタグを含む）を持つアセットとコレクションを公開できます。その後、Brand Portal 内でこれらのタグを検索キーワードとして使用して、アセットやコレクションを検索できます。

## よくある質問 {#frequently-asked-questions}

**Qus.私が作成した既存のアセット、機能または設定へのアクセス権は失われますか。****人。**&#x200B;既存の機能と設定はすべてそのまま残ります。エンドユーザーに影響はなく、コンテンツはそのまま残ります。

**お問い合わせ。新しいバージョンの Brand Portal にはいつ移行しますか。****人。** ブランドポータル6.4.4が2019年2月に製造にリリースされました。Brand Portal の次期バージョンは、2019 年の第 3 四半期にリリース予定です。

>[!NOTE]
>
>リリース日程は暫定的なものであり、変更の可能性があります。最新のリリース日程についてアドビのアカウントマネージャーまたはカスタマーサポートにお問い合わせください。

**お問い合わせ。私が管理しているユーザーに影響しますか。****人。**&#x200B;この変更は Brand Portal に限定されたものなので、エンドユーザーには影響しません。

**お問い合わせ。管理者側で何かすることはありますか。****人。**&#x200B;管理者にしていただく作業はありません。新しい Brand Portal にアクセスできるようになったら、ドキュメントを参照して、すべてのオプション機能を確認してください。

**お問い合わせ。質問は誰に問い合わせればいいですか。****人。**&#x200B;アドビのアカウントマネージャーか、カスタマーサポートまでお願いします。
