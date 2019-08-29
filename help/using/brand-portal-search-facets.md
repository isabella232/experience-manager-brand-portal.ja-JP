---
title: カスタム検索ファセットの使用
seo-title: カスタム検索ファセットの使用
description: 管理者は、フィルターパネルに検索用述語を追加することで、検索をカスタマイズして、多目的な検索機能を設定できます。
seo-description: 管理者は、フィルターパネルに検索用述語を追加することで、検索をカスタマイズして、多目的な検索機能を設定できます。
uuid: 986fba5a- fac5-4128- ac75- d04da5b52d45
content-type: reference
topic-tags: 管理
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
discoiquuid: 19fa028-246b-42c7-869f-97c95c7a1349
translation-type: tm+mt
source-git-commit: ea7fdd2df0696ed309227fa77e3f79d0141bcb58

---


# カスタム検索ファセットの使用 {#use-custom-search-facets}

管理者は、フィルターパネルに検索用述語を追加することで、検索をカスタマイズして、多目的な検索機能を設定できます。

[!DNL Brand Portal] は [、承認されたブランド](../using/brand-portal-searching.md#search-using-facets-in-filters-panel) アセットの詳細検索をサポートします。この検索は [**、フィルター** パネルによって可能](../using/brand-portal-searching.md#search-using-facets-in-filters-panel)です。Search facets are made available on Filters panel through **Search Form** in the admin tools. デフォルトの検索フォームはアセット管理検索レールという名前で、管理ツールの検索フォームページにあります。しかし、管理者はデフォルトのフィルターパネルをカスタマイズできます。デフォルトの検索フォーム（アセット管理検索レール）を編集し、検索用述語を追加、修正、削除することで、検索機能をカスタマイズできます。

You can use various search predicates to customize the **Filters** panel. 例えば、この述語で指定した単一のプロパティに一致するアセットを検索するには、プロパティの述語を追加します。特定のプロパティに指定した1つ以上の値に一致するアセットを検索するために、options Predicateを追加します。日付範囲の述語を追加して、指定した日付範囲内で作成されたアセットを検索します。

>[!NOTE]
>
>[!DNL AEM] 組織は、カスタマイズ [した検索フォームを[!同じフォームを再作成するのではなく、"DNL AEM"の作成者](../using/publish-schema-search-facets-presets.md#publish-search-facets-to-brand-portal) を参照 [!DNL Brand Portal][!DNL Brand Portal]してください。

## 検索用述語の追加 {#add-a-search-predicate}

**フィルター**&#x200B;パネルに検索用述語を追加するには、次のようにします。

1. To access administrative tools, click the [!DNL AEM] logo from the toolbar at the top.

   ![](assets/aemlogo.png)

2. From the administrative tools panel, click **Search Forms**.

   ![](assets/navigation-panel-1.png)

3. **検索フォーム**&#x200B;ページの「**アセット管理者の検索レール**」を選択します。

   ![](assets/search-forms-page.png)

4. 上部に表示されるツールバーの「**編集**」をクリックして、「検索フォームを編集」を開きます。

   ![](assets/edit-search-form-1.png)

5. In the **Edit Search Form** page, drag a predicate from the **Select Predicate** tab to the main pane. For example, drag **Property Predicate**.

   メインウィンドウに「**プロパティ**」フィールドが表示され、右側の「**設定**」タブにプロパティの述語が表示されます。

   ![](assets/partial-prop-predicate.png)

   >[!NOTE]
   >
   >「**設定**」タブのヘッダーラベルは、選択した述語のタイプを示します。

6. 「**設定**」タブで、そのプロパティの述語のラベル、プレースホルダーテキストおよび説明を入力します。

   * Select **Partial Search**, if you want to allow partial phrase search (and wildcard search) of assets-based on the specified property value. 述語はデフォルトでフルテキスト検索をサポートしています。
   * Select **Ignore Case**, if you want the asset search based on property value to be non-case sensitive. 検索フィルターでのプロパティ値の検索では、デフォルトで大文字と小文字が区別されます。
   >[!NOTE]
   >
   >「**部分検索**」チェックボックスを選択すると、デフォルトで「**大文字と小文字を区別しない**」がオンになります。

7. **「プロパティ名」** フィールドで、プロパティピッカーを開き、検索の実行に基づいてプロパティを選択します。または、プロパティの名前を入力します。For example, enter `  jcr :content/metadata/dc:title` or `./jcr:content/metadata/dc:title`.

   ![](assets/title-prop.png)

8. 「**完了**」をクリックして、設定を保存します。
9. **アセット** ユーザーインターフェイスで、オーバーレイアイコンをクリックし、 **「フィルター」** を選択して **フィルター** パネルに移動します。**プロパティ** の述語がパネルに追加されます。

   ![](assets/property-filter-panel.png)

10. 「**プロパティ**」テキストボックスに、検索するアセットのタイトルを入力します。例えば、「アドビ」と入力します。検索を実行すると、「アドビ」と一致するタイトルを持つアセットが検索結果に表示されます。

## 検索用述語の一覧 {#list-of-search-predicates}

**プロパティ** の述語を追加する方法と同様に、次の述語を **フィルター** パネルに追加できます。

| **述語名** | **説明** | **プロパティ** |
|-------|-------|----------|
| パスブラウザー | 特定の場所にあるアセットを検索するための検索用述語。**注意:***ログインユーザーの場合、フィルターのパスブラウザーには、ユーザーと共有されているフォルダー（およびその祖先）のコンテンツ構造のみが表示されます。*<br>管理者は、パスブラウザーを使用して目的のフォルダーまでナビゲートすることで、あらゆるフォルダー内のアセットを検索できます。<br> 管理者以外のユーザーは、パスブラウザーでフォルダに移動して、フォルダ内のアセットを（アクセス可能な）フォルダ内に検索できます。 | <ul><li>フィールドラベル</li><li>パス</li><li>説明</li></ul> |
| プロパティ | 特定のメタデータプロパティに基づいてアセットを検索します。**注意:***部分検索を選択する場合、デフォルトでは「大文字と小文字を区別しない」が選択*&#x200B;されています。 | <ul><li>フィールドラベル</li><li>プレースホルダー</li><li>プロパティ名</li><li>部分検索</li><li>大文字と小文字を区別しない</li><li> 説明</li></ul> |
| 複数値プロパティ | Similar to property predicate but allows multiple input values, separated by a delimiter (default is COMMA[,]) assets matching any of the input values are returned in results. | <ul><li>フィールドラベル</li><li>プレースホルダー</li><li>プロパティ名</li><li>区切り文字のサポート</li><li>大文字と小文字を区別しない</li><li>説明</li></ul> |
| タグ | タグに基づいてアセットを検索するための検索用述語。「パス」プロパティを設定して、「タグ」リストに様々なタグを表示できます。*注意:管理者は、パス値を変更する必要が生じる場合があります*`/etc/tags/mac/<tenant_id>/<custom_tag_namespace>`*（例えば、検索フォームを発行する[!DNL AEM]場合、パスにテナント情報が含ま*`/etc/tags/<custom_tag_namespace>`れていない場合など）。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>パス</li><li>説明</li></ul> |
| パス | 特定の場所にあるアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>パス</li><li>説明</li></ul> |  |
| 相対的な日付 | アセットの相対的な作成日に基づいてアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>相対的な日付</li></ul> |
| 範囲 | 指定したプロパティ値の範囲内に含まれるアセットを検索するための検索用述語。フィルターパネルで、範囲の最小プロパティと最大プロパティ値を指定できます。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| 日付の範囲 | 日付プロパティに対して指定した範囲内で作成されたアセットを検索するための検索用述語。フィルターパネルで、開始日と終了日を指定できます。 | <ul><li>フィールドラベル</li><li>プレースホルダー</li><li>プロパティ名</li><li>範囲テキスト (開始)</li><li>範囲テキスト (終了)</li><li>説明</li></ul> |
| 日付 | 日付プロパティに基づいて、スライダーを使用してアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| ファイルサイズ | サイズに基づいてアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>パス</li><li>説明</li></ul> |
| 最終変更アセット | 最終変更日に基づいてアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| 承認ステータス | 承認メタデータプロパティに基づいてアセットを検索するための検索用述語。デフォルトのプロパティ名は **dam:status** です。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| チェックアウトステータス | Search predicate to search assets based on the check-out status of an asset when it was published from [!DNL AEM] Assets. | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| チェックアウト実行者 | アセットをチェックアウトしたユーザーに基づいてアセットを検索するための検索用述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| 有効期限ステータス | 有効期限ステータスに基づいてアセットを検索するための検索の述語。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |
| コレクションのメンバー | アセットがコレクションの一部であるかどうかに基づいてアセットを検索するための検索用述語。 | 説明 |
| 非表示 | この述語は、エンドユーザーには明示的に表示されません。これは、一般的に検索結果のタイプを **dam:Asset** に制限する非表示の制約として使用されます。 | <ul><li>フィールドラベル</li><li>プロパティ名</li><li>説明</li></ul> |

>[!NOTE]
>
>Do not use **Options Predicate**, **Publish Status Predicate**, and **Rating Predicate** as these predicates are not functional in [!DNL Brand Portal].

## 検索用述語の削除 {#delete-a-search-predicate}

検索用述語を削除するには、次の手順に従います。

1. アドビロゴをクリックして、管理ツールにアクセスします。

   ![](assets/aemlogo.png)

2. From the administrative tools panel, click **Search Forms**.

   ![](assets/navigation-panel-2.png)

3. **検索フォーム**&#x200B;ページの「**アセット管理者の検索レール**」を選択します。

   ![](assets/search-forms-page.png)

4. 上部に表示されるツールバーの「**編集**」をクリックして、「検索フォームを編集」を開きます。

   ![](assets/edit-search-form-2.png)

5. In the **Edit Search Form** page, from the main pane, select the predicate you want to delete. For example, select **Property Predicate**.

   右側の「**設定**」タブに、「プロパティの述語」に関するフィールドが表示されます。

6. プロパティの述語を削除するには、ごみ箱アイコンをクリックします。**フィールドを削除**&#x200B;ダイアログボックスで、「**削除**」をクリックして、削除することを確認します。

   メインウィンドウから「**プロパティの述語**」フィールドが削除され、「**設定**」タブが空になります。

   ![](assets/search-form-delete-predicate.png)

7. To save the changes, click **Done** in the toolbar.
8. **アセット** ユーザーインターフェイスで、オーバーレイアイコンをクリックし、 **「フィルター」** を選択して **フィルター** パネルに移動します。**プロパティ** の述語がパネルから削除されます。

   ![](assets/property-predicate-removed.png)
