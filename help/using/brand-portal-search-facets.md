---
title: カスタム検索ファセットの使用
seo-title: カスタム検索ファセットの使用
description: 管理者は、フィルターパネルに検索用述語を追加することで、検索をカスタマイズして、多目的な検索機能を設定できます。
seo-description: 管理者は、フィルターパネルに検索用述語を追加することで、検索をカスタマイズして、多目的な検索機能を設定できます。
uuid: 986fba5a-fac5-4128-ac75-d04da5b52d45
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 19faa028-246b-42c7-869f-97c95c7a1349
translation-type: tm+mt
source-git-commit: 86d4d5c358ea795e35db2dce8c9529ed14e9ee2d

---


# カスタム検索ファセットの使用 {#use-custom-search-facets}

Administrators can add search predicates to the [!UICONTROL Filters] panel to customize search and make the search functionality versatile.

Brand Portal supports [faceted search](../using/brand-portal-searching.md#search-using-facets-in-filters-panel) for granular searches of approved brand assets, which is possible due to [**Filters** panel](../using/brand-portal-searching.md#search-using-facets-in-filters-panel). 検索ファセットは管理ツールの&#x200B;**[!UICONTROL 検索フォーム]を通じてフィルターパネルで使用可能になります。**&#x200B;デフォルトの検索フォームはアセット管理検索レールという名前で、管理ツールの検索フォームページにあります。しかし、管理者はデフォルトのフィルターパネルをカスタマイズできます。デフォルトの検索フォーム（アセット管理検索レール）を編集し、検索用述語を追加、修正、削除することで、検索機能をカスタマイズできます。

様々な検索用述語を使用して、**[!UICONTROL フィルター]パネルをカスタマイズできます。**&#x200B;例えば、プロパティの述語を使用すると、この述語内でユーザーが指定した 1 つのプロパティと一致するアセットを検索できます。オプションの述語を追加すると、特定のプロパティについてユーザーが指定した 1 つ以上の値と一致するアセットを検索できます。日付範囲の述語を追加すると、指定した期間内に作成されたアセットを検索できます。

>[!NOTE]
>
>AEM allows organizations to [publish the customized search forms from AEM Author](../using/publish-schema-search-facets-presets.md#publish-search-facets-to-brand-portal) to Brand Portal, instead of re-creating the same form on Brand Portal.

## 検索用述語の追加 {#add-a-search-predicate}

**[!UICONTROL フィルター]パネルに検索用述語を追加するには、次のようにします。**

1. 管理ツールにアクセスするには、上部のツールバーでAEMロゴをクリックします。

   ![](assets/aemlogo.png)

1. From the administrative tools panel, click **[!UICONTROL Search Forms]**.

   ![](assets/navigation-panel-1.png)

1. In the **[!UICONTROL Search Forms]** page, select **[!UICONTROL Assets Admin Search Rail]**.

   ![](assets/search-forms-page.png)

1. 上部に表示されるツールバーの「**[!UICONTROL 編集]」をクリックして、「検索フォームを編集」を開きます。**

   ![](assets/edit-search-form-1.png)

1. [!UICONTROL 検索フォームを編集]ページで、「[!UICONTROL 述語を選択]」タブからメインウィンドウに述語をドラッグします。For example, drag **[!UICONTROL Property Predicate]**.

   メインウィンドウに「**[!UICONTROL プロパティ]**」フィールドが表示され、右側の「**設定]」タブにプロパティの述語が表示されます。[!UICONTROL **

   ![](assets/partial-prop-predicate.png)

   >[!NOTE]
   >
   >「**[!UICONTROL 設定]」タブのヘッダーラベルは、選択した述語のタイプを示します。**

1. 「**[!UICONTROL 設定]」タブで、そのプロパティの述語のラベル、プレースホルダーテキストおよび説明を入力します。**

   * Select **[!UICONTROL Partial Search]**, if you want to allow partial phrase search (and wildcard search) of assets-based on the specified property value. 述語はデフォルトでフルテキスト検索をサポートしています。
   * Select **[!UICONTROL Ignore Case]**, if you want the asset search based on property value to be non-case sensitive. 検索フィルターでのプロパティ値の検索では、デフォルトで大文字と小文字が区別されます。
   >[!NOTE]
   >
   >「**[!UICONTROL 部分検索]**」チェックボックスを選択すると、デフォルトで「[!UICONTROL 大文字と小文字を区別しない]」がオンになります。

1. 「[!UICONTROL プロパティ名]」フィールドで、プロパティピッカーを開き、検索に使用するプロパティを選択します。または、プロパティの名前を入力します。For example, enter [!UICONTROL `  jcr :content/metadata/dc:title`] or [!UICONTROL `./jcr:content/metadata/dc:title`].

   ![](assets/title-prop.png)

1. 「**[!UICONTROL 完了]」をクリックして、設定を保存します。**
1. [!UICONTROL Assets] ユーザーインターフェイスで、オーバーレイアイコンをクリックし、「**[!UICONTROL フィルター]**」を選択して&#x200B;**フィルター[!UICONTROL パネルに移動します。]****[!UICONTROL プロパティ]の述語がパネルに追加されています。**

   ![](assets/property-filter-panel.png)

1. 「**[!UICONTROL プロパティ]」テキストボックスに、検索するアセットのタイトルを入力します。**&#x200B;例えば、「Adobe」とします。 検索を実行すると、「アドビ」と一致するタイトルを持つアセットが検索結果に表示されます。

## 検索用述語の一覧 {#list-of-search-predicates}

**[!UICONTROL プロパティ]**&#x200B;の述語を追加する場合と同様の手順で、**フィルター[!UICONTROL パネルに、次の述語を追加できます。]**

| **述語名** | **説明** | **プロパティ** |
|-------|-------|----------|
| [!UICONTROL パスブラウザー] | 特定の場所にあるアセットを検索するための検索用述語。**注意：***ログインしているユーザーの場合、フィルター上のパスブラウザーには、そのユーザーに共有されているフォルダー（とその上位層）のコンテンツ構造のみ表示されます。*<br>管理者は、パスブラウザーを使用して目的のフォルダーまでナビゲートすることで、あらゆるフォルダー内のアセットを検索できます。<br>それに対して、管理者以外のユーザーは、パスブラウザーで目的のフォルダーまでナビゲートすることは同じですが、自身がアクセス可能なフォルダー内のアセットのみ検索できます。 | <ul><li>フィールドラベル</li><li>パス</li><li>説明</li></ul> |
| [!UICONTROL プロパティ] | 特定のメタデータプロパティに基づいてアセットを検索します。**注意：***「部分検索」を選択すると、デフォルトで「大文字と小文字を区別しない」がオンになります。* | <ul><li>フィールドラベル</li><li>プレースホルダー</li><li>プロパティ名</li><li>部分検索</li><li>大文字と小文字を区別しない</li><li> 説明</li></ul> |
| [!UICONTROL 複数値プロパティ] | プロパティの述語と似ていますが、複数の入力値を区切り文字（デフォルトはコンマ [,]）で区切って使用でき、いずれかの入力値と一致するアセットが結果に返されます。 | <ul><li>フィールドラベル</li><li>プレースホルダー</li><li>プロパティ名</li><li>区切り文字のサポート</li><li>大文字と小文字を区別しない</li><li>説明</li></ul> |
| [!UICONTROL タグ] | タグに基づいてアセットを検索するための検索用述語。「パス」プロパティを設定して、「タグ」リストに様々なタグを表示できます。*Note: Administrators might need to change the path value, for example, [!UICONTROL `/etc/tags/mac/<tenant_id>/<custom_tag_namespace>`], if they publish the search form from AEM, where the path does not include tenant information, for example, [!UICONTROL `/etc/tags/<custom_tag_namespace>`]. | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>パス</li><li>説明</li></ul> |
| [!UICONTROL パス] | 特定の場所にあるアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>パス</li><li>説明</li></ul> |  |
| [!UICONTROL 相対的な日付] | アセットの相対的な作成日に基づいてアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>相対的な日付</li></ul> |
| [!UICONTROL 範囲] | 指定したプロパティ値の範囲内に含まれるアセットを検索するための検索用述語。フィルターパネルで、範囲の最小プロパティ値と最大プロパティ値を指定できます。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| [!UICONTROL 日付の範囲] | 指定した日付プロパティの範囲内で作成されたアセットを検索するための検索用述語。フィルターパネルで、開始日と終了日を指定できます。 | <ul><li>フィールドラベル</li><li>プレースホルダー</li><li>プロパティ名</li><li>範囲テキスト (開始)</li><li>範囲テキスト (終了)</li><li>説明</li></ul> |
| [!UICONTROL 日付] | 日付プロパティに基づいて、スライダーを使用してアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| [!UICONTROL ファイルサイズ] | サイズに基づいてアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>パス</li><li>説明</li></ul> |
| [!UICONTROL 最終変更アセット] | 最終変更日に基づいてアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| [!UICONTROL 承認ステータス] | 承認メタデータプロパティに基づいてアセットを検索するための検索用述語。デフォルトのプロパティ名は **dam:status** です。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| [!UICONTROL チェックアウトステータス] | アセットが AEM Assets から公開されたときのチェックアウトステータスに基づいてアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| [!UICONTROL チェックアウト実行者] | アセットをチェックアウトしたユーザーに基づいてアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| [!UICONTROL 有効期限ステータス] | 有効期限ステータスに基づいてアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| [!UICONTROL コレクションのメンバー] | アセットがコレクションの一部であるかどうかに基づいてアセットを検索するための検索用述語。 | 説明 |
| [!UICONTROL 非表示] | This predicate is not explicitly visible to the end users and is used for any hidden constraints typically for restricting search results type to **dam:Asset**. | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |

>[!NOTE]
>
>Do not use **[!UICONTROL Options Predicate]**, **[!UICONTROL Publish Status Predicate]**, and **[!UICONTROL Rating Predicate]** as these predicates are not functional in Brand Portal.

## 検索用述語の削除 {#delete-a-search-predicate}

検索用述語を削除するには、次の手順に従います。

1. アドビロゴをクリックして、管理ツールにアクセスします。

   ![](assets/aemlogo.png)

1. From the administrative tools panel, click **[!UICONTROL Search Forms]**.

   ![](assets/navigation-panel-2.png)

1. In the **[!UICONTROL Search Forms]** page, select **[!UICONTROL Assets Admin Search Rail]**.

   ![](assets/search-forms-page.png)

1. 上部に表示されるツールバーの「**[!UICONTROL 編集]」をクリックして、「検索フォームを編集」を開きます。**

   ![](assets/edit-search-form-2.png)

1. [!UICONTROL 検索フォームを編集]ページで、削除する述語をメインウィンドウから選択します。For example, select **[!UICONTROL Property Predicate]**.

   右側の「**[!UICONTROL 設定]」タブに、「プロパティの述語」に関するフィールドが表示されます。**

1. プロパティの述語を削除するには、ごみ箱アイコンをクリックします。**[!UICONTROL フィールドを削除]**&#x200B;ダイアログボックスで、「**削除[!UICONTROL 」をクリックして、削除することを確認します。]**

   メインウィンドウから「**[!UICONTROL プロパティの述語]**」フィールドが削除され、「**設定]」タブが空になります。[!UICONTROL **

   ![](assets/search-form-delete-predicate.png)

1. 変更を保存するには、ツールバーの「**[!UICONTROL 完了]」をクリックします。**
1. **[!UICONTROL Assets]** ユーザーインターフェイスで、オーバーレイアイコンをクリックし、「**[!UICONTROL フィルター]」を選択して**&#x200B;フィルター&#x200B;**パネルに移動します。**&#x200B;指定した&#x200B;**[!UICONTROL プロパティ]の述語が、パネルから削除されています。**

   ![](assets/property-predicate-removed.png)
