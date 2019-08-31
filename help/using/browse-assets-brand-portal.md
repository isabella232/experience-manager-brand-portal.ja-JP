---
title: Brand Portal でのアセットの参照
seo-title: Brand Portal でアセットを参照する
description: Brand Portal の様々な表示オプションや UI 要素を使用して、アセットの参照、アセット階層のトラバース、およびアセットの検索をおこないます。
seo-description: Brand Portal の様々な表示オプションや UI 要素を使用して、アセットの参照、アセット階層のトラバース、およびアセットの検索をおこないます。
uuid: 178ce217-0050-4922- a204- f4539d46f539
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
content-type: reference
topic-tags: introduction
discoiquuid: a70ce694-81d1-4829-9e61- b6412e013e5c
translation-type: tm+mt
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# Brand Portal でのアセットの参照 {#browsing-assets-on-brand-portal}

AEM Assets Brand Portal は、別の表示オプションを使用しながらリソースの参照、アセット階層のトラバース、およびアセットの検索を容易におこなえる様々な機能とユーザーインターフェイス要素を提供します。

管理者ユーザーは、上部にある AEM ツールバーの AEM ロゴから、管理ツールパネルへアクセスできます。

![](assets/aemlogo.png)

![](assets/admin-tools-panel-2.png)

![](assets/bp_subheader.png)

Brand Portal ドロップダウンの左上にあるレールセレクターを使用すると、アセット階層へ移動、検索を効率化、およびリソースを表示するオプションが表示されます。

![](assets/siderail-1.png)

Brand Portal の右上にある表示セレクターで利用可能な表示（カード、列、およびリスト）のいずれかを使用すると、アセットを表示、ナビゲーション、および選択することができます。

![](assets/viewselector.png)

## リソースの表示と選択 {#viewing-and-selecting-resources}

表示、移動、選択は、概念的にはすべてのビューで同じですが、使用しているビューに応じて、処理に小さなバリエーションがあります。

使用可能な任意の表示方法で、リソースを表示、ナビゲーションおよび（追加のアクションをおこな行うために）選択できます。

* 列表示
* カード表示
* リスト表示

### カード表示

![](assets/card-view.png)

カード表示では、現在のレベルの各項目の情報カードを表示します。これらのカードは、次の詳細を参照してください。

* アセット／フォルダーの内容を視覚的に表現したもの。
* 種類
* タイトル
* 名前
* AEM から Brand Portal にアセットが公開された日付と時刻
* サイズ
* ディメンション寸法

You can navigate down the hierarchy by tapping/clicking cards (taking care to avoid the quick actions) or up again by using the [breadcrumbs in the header](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/basic-handling.html#TheHeader).

![](assets/cardquickactions.png)

#### 管理者以外のユーザー向けカード表示

カードのカードのカード表示では、管理者以外のユーザー（エディター、ビューアおよびゲストユーザー）にフォルダ階層情報が表示されます。この機能により、ユーザーはフォルダーの場所を把握し、親階層に関してアクセスすることができます。
フォルダー階層の情報は、別のフォルダー階層から共有されている他のフォルダーと同様に名前を持つフォルダーを区別するのに特に役立ちます。管理者以外のユーザーが、自分たちに共有されているアセットのフォルダー構造を把握していない場合、似たような名前のアセット／フォルダーは紛らわしくなります。

* カードのサイズに合わせて、それぞれのカードに表示されるパスが切り詰められます。ただし、切り詰められたパスの上にマウスポインターを置くと、フルパスがツールヒントとして表示されます。

![](assets/folder-hierarchy1.png)

**アセットのプロパティを表示する「概要」オプション**

管理者以外のユーザー（エディター、ビューア、ゲストユーザー）が、選択したアセット/フォルダのアセットプロパティを表示するための概要オプションを使用できます。「概要」オプションは、次の場所に表示されます。

* をクリックします。
* をクリックします。

On selecting the [!UICONTROL Overview] option while an asset/folder is selected, users can see the title, path, and time of asset creation. 一方、アセットの詳細ページで「概要」オプションを選択すると、ユーザーはアセットのメタデータを確認できます。

![](assets/overview-option.png)

![](assets/overview-rail-selector.png)

#### カード表示の表示設定

[!UICONTROL 表示セレクターで表示設定を選択すると、表示設定ダイアログが開き、]****&#x200B;カード表示でアセットのサムネールのサイズを変更できます。これにより、表示をパーソナライズして、表示されるサムネールの数を制御できます。

![](assets/cardviewsettings.png)

### リスト表示

![](assets/list-view.png)

リスト表示では、現在のレベルの各リソースの情報が表示されます。リスト表示は次の詳細を提供します。

* アセットのサムネール画像
* 名前
* タイトル
* ロケール
* 種類
* ディメンション
* サイズ
* 評価
* Folder path showing asset hierarchy<sup>*</sup>
* Brand Portal 上のアセットの公開日

* パス列を使用すると、フォルダー階層内のアセットの場所が特定しやすくなります。You can navigate down the hierarchy by tapping/clicking the resource name, and back up by using the [breadcrumbs in the header](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/basic-handling.html#TheHeader).

<!--
Comment Type: draft lastmodifiedby="mgulati" lastmodifieddate="2018-08-17T03:12:05.096-0400" type="annotation">Removed:- "Selecting assets in list view To select all items in the list, use the checkbox at the upper left of the list. When all items in the list are selected, this check box appears checked. To deselect all, click or tap the checkbox. When only some items are selected, it appears with a minus sign. To select all, click or tap the checkbox. To deselect all, click or tap the checkbox again. You can change the order of items using the dotted vertical bar at the far right of each item in the list. Tap/click the vertical selection bar and drag the item to a new position in the list."
 -->

### リスト表示の表示設定

List view shows asset [!UICONTROL Name] as the first column by default. Additional information, such as asset [!UICONTROL Title], [!UICONTROL Locale], [!UICONTROL Type], [!UICONTROL Dimensions], [!UICONTROL Size], [!UICONTROL Rating], publish status are also shown. However, you can select the columns to be shown using [!UICONTROL View Settings].

![](assets/list-view-setting.png)

### 列表示

![](assets/column-view.png)

列表示を使用すると、一連のカスケード列からコンテンツツリー内を移動できます。この表示は、アセット階層を視覚化およびトラバースするのに便利です。

最初（一番左）の列のリソースを選択すると、右側にある 2 列目に子リソースが表示されます。2 列目のリソースを選択すると、右側にある 3 列目に子リソースが表示されます（以降も同様です）。

リソース名かリソース名の右にある山形記号をタップまたはクリックすることで、ツリーを上下に移動できます。

* タップまたはクリックするとリソース名と山形記号がハイライト表示されます。
* サムネールをタップまたはクリックして、リソースを選択します。
* すると、チェックマークがサムネールにオーバーレイ表示され、リソース名もハイライト表示されます。
* 選択されたリソースの詳細が最後の列に表示されます。

列表示でアセットが選択されると、アセットを視覚的に表現したものが次の詳細と共に最後の列に表示されます。

* タイトル
* 名前
* ディメンション寸法
* AEM から Brand Portal にアセットが公開された日付と時刻
* サイズ
* 種類
* 詳細オプション（アセットの詳細ページへ移動する）

<!--
Comment Type: draft

<h3>Selecting Resources</h3>
-->

<!--
Comment Type: draft

<p>Selecting a specific resource depends on a combination of the view and the device:</p>
-->

<!--
Comment Type: draft

<table border="1" cellpadding="1" cellspacing="0" width="100%">
<tbody>
<tr>
<td> </td>
<td>Select</td>
<td>Deselect</td>
</tr>
<tr>
<td>Column View<br /> </td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the thumbnail</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
</tr>
<tr>
<td>Card View<br /> </td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap-and-hold the card</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the card</li>
<li>Mobile device:<br /> Tap the card</li>
</ul> </td>
</tr>
<tr>
<td>List View</td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the thumbnail</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
</tr>
</tbody>
</table>
-->

<!--
Comment Type: draft

<h4>Deselecting All</h4>
-->

<!--
Comment Type: draft

<p>In all cases, as you select items the count of the items selected is displayed at the upper right of the toolbar.</p>
<p>You can deselect all items and exit selection mode by clicking or tapping the X next to the count.</p>
-->

<!--
Comment Type: draft

<p>In all views, all items can be deselected by tapping escape on the keyboard if you are using a desktop device.</p>
-->

## コンテンツツリー {#content-tree}

これらのビューに加えて、目的のアセットまたはフォルダを表示して選択するときに、ツリービューを使用してアセット階層をドリルダウンします。

To open the tree view, tap/click the rail selector at upper left and select the **[!UICONTROL Content tree]** from the menu.

![](assets/contenttree.png)

コンテンツ階層から目的のアセットに移動します。

![](assets/content-tree.png)

## アセットの詳細 {#asset-details}

アセットの詳細ページでは、アセットを表示、ダウンロード、アセットリンクを共有、コレクションへアセットを移動させる、またはアセットのプロパティページを表示することができます。また、同じフォルダーの他のアセットの詳細ページへ続けて移動することもできます。

![](assets/asset-detail.png)

アセットのメタデータを表示したり、様々なレンディションを表示したりするには、アセットの詳細ページのパネルセレクターを使用します。

![](assets/asset-overview.png)

アセットの詳細ページでアセットの利用可能なレンディションをすべて表示し、レンディションを選択してプレビューできます。

![](assets/renditions.png)

To open the asset properties page, use **[!UICONTROL Properties (p)]** option from the top bar.

![](assets/asset-properties.png)

また、アセットの関係も AEM から Brand Portal に公開されているため、アセットのプロパティページですべての関連アセット（AEM 上のソースまたは派生アセット）のリストを表示することもできます。
