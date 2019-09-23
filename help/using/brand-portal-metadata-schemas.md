---
title: メタデータスキーマフォームの使用
seo-title: メタデータスキーマフォームの使用
description: メタデータスキーマは、プロパティページのレイアウトと、特定のスキーマを使用するアセット用に表示されるメタデータプロパティを記述します。アセットにどのスキーマを適用するかによって、そのアセットのプロパティページに表示されるメタデータフィールドが決まります。
seo-description: メタデータスキーマは、プロパティページのレイアウトと、特定のスキーマを使用するアセット用に表示されるメタデータプロパティを記述します。アセットにどのスキーマを適用するかによって、そのアセットのプロパティページに表示されるメタデータフィールドが決まります。
uuid: 1a944a3b-5152-425f-b1ea-bfe3331de928
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: administration
discoiquuid: 500b46da-ef67-46a0-a069-192f4b1a0eca
translation-type: tm+mt
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# メタデータスキーマフォームの使用 {#use-the-metadata-schema-form}

メタデータスキーマは、プロパティページのレイアウトと、特定のスキーマを使用するアセット用に表示されるメタデータプロパティを記述します。アセットにどのスキーマを適用するかによって、そのアセットのプロパティページに表示されるメタデータフィールドが決まります。

各アセットの&#x200B;**[!UICONTROL プロパティ]ページには、そのアセットの MIME タイプに応じたデフォルトのメタデータプロパティが表示されます。**&#x200B;管理者は、メタデータスキーマエディターを使用して、既存のスキーマを変更したり、カスタムのメタデータスキーマを追加したりできます。AEM Assets Brand Portal provides default forms for assets of various MIME types. However, you can also add custom forms for such assets.

## メタデータスキーマフォームの追加 {#add-a-metadata-schema-form}

新しいメタデータスキーマフォームを作成するには、以下の手順を実行します。

1. 上部の AEM ツールバーでアドビのロゴをクリックして、管理ツールにアクセスします。

   ![](assets/aemlogo.png)

2. From the administrative tools panel, click **[!UICONTROL Metadata Schemas]**.

   ![](assets/navigation-panel.png)

3. On the **[!UICONTROL Metadata Schema Forms]** page, click **[!UICONTROL Create]**.

   ![](assets/create-metadata-schema-form.png)

4. **[!UICONTROL スキーマフォームを作成]**&#x200B;ダイアログボックスで、スキーマフォームのタイトルを指定し、「**作成[!UICONTROL 」をクリックして、フォーム作成プロセスを完了します。]**

   ![](assets/create-schema-form.png)

## メタデータスキーマフォームの編集 {#edit-a-metadata-schema-form}

新しく追加したメタデータスキーマフォームまたは既存のメタデータスキーマフォームを編集できます。メタデータスキーマフォームには、タブやタブ内のフォーム項目など、親から派生したコンテンツが含まれます。これらのフォーム項目をメタデータノード内のフィールドにマップしたり、フォーム項目を設定したりできます。

新しいタブまたはフォーム項目をメタデータスキーマフォームに追加できます。（親から）派生したタブおよびフォーム項目はロック状態です。子レベルではこれらを変更できません。

メタデータスキーマフォームを編集するには、以下の手順を実行します。

1. 上部の AEM ツールバーでアドビのロゴをクリックして、管理ツールにアクセスします。

   ![](assets/aemlogo.png)

2. From the administrative tools panel, click **[!UICONTROL Metadata Schemas]**.
3. From the **[!UICONTROL Metadata Schema Forms]** page, select a schema form to edit its properties, for example, **[!UICONTROL collection]**.

   ![](assets/metadata-schema-forms.png)

   >[!NOTE]
   >
   >Unedited templates display a lock symbol before them. テンプレートをカスタマイズすると、そのテンプレートの前にあるロック記号が消えます。

4. From the toolbar at the top, click **[!UICONTROL Edit]**.

   **[!UICONTROL メタデータスキーマエディター]**&#x200B;ページが開き、左側には「**[!UICONTROL 基本]」タブが、右側には「**&#x200B;フォームを作成&#x200B;**」タブが開きます。**

5. **[!UICONTROL メタデータスキーマエディター]**&#x200B;ページで、アセットの&#x200B;**[!UICONTROL プロパティ]**&#x200B;ページをカスタマイズします。それには、「**フォームを作成[!UICONTROL 」タブのコンポーネントタイプのリストから「]基本**」タブに、1 つ以上のコンポーネントをドラッグします。****

   ![](assets/metadata-schemaeditor-page.png)

6. コンポーネントを設定するには、コンポーネントを選択して、「**[!UICONTROL 設定]」タブでそのプロパティを変更します。**

### 「フォームを作成」タブのコンポーネント{#components-in-the-build-form-tab}

「**[!UICONTROL フォームを作成]」タブには、スキーマフォーム内で使用できるフォーム項目が表示されます。**「**[!UICONTROL 設定]**」タブに、「**フォームを作成[!UICONTROL 」タブで選択した各項目の属性が表示されます。]**「**[!UICONTROL フォームを作成]」タブで使用できるフォーム項目を次の表に示します。**

| コンポーネント名 | 説明 |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL セクションヘッダー] | 共通コンポーネントのリストに対してセクションヘッダーを追加します。 |
| [!UICONTROL 1 行のテキスト] | 1 行のテキストプロパティを追加します。これは文字列として保存されます。 |
| [!UICONTROL 複数値テキスト] | 複数値テキストプロパティを追加します。これは文字列の配列として保存されます。 |
| [!UICONTROL 番号] | 数値コンポーネントを追加します。 |
| [!UICONTROL 日付] | 日付コンポーネントを追加します。 |
| [!UICONTROL ドロップダウン] | ドロップダウンリストを追加します。 |
| [!UICONTROL 標準タグ] | タグを追加します。**** 注意：管理者は、例えば、AEMからメタデータスキーマフォームを発行する場合、パスの値を変更する必要がある場合があります。この場合、パスにテナント情報が含まれない `/etc/tags/mac/<tenant_id>/<custom_tag_namespace>`(例えば、 `/etc/tags/<custom_tag_namespace>`)。 |
| [!UICONTROL スマートタグ] | AEMスマートタグアドオンを購入して設定した場合、自動検出されたタグ。 |
| [!UICONTROL 非表示のフィールド] | 非表示のフィールドを追加します。このフィールドは、アセットの保存時に POST パラメーターとして送信されます。 |
| [!UICONTROL アセットの参照元] | このアセットが参照しているアセットのリストを表示するには、このコンポーネントを追加します。 |
| [!UICONTROL アセットの参照] | このアセットを参照しているアセットのリストを表示するには、このコンポーネントを追加します。 |
| [!UICONTROL アセット評価] | AEM AssetsからBrand portalに発行される前に追加されたアセットの評価の平均。 |
| [!UICONTROL コンテキストメタデータ] | アセットのプロパティページにある他のメタデータタブの表示を制御するために追加します。 |

>[!NOTE]
>
>Do not use **[!UICONTROL Product References]**, as it is not functional.

#### メタデータコンポーネントの編集 {#edit-the-metadata-component}

フォームのメタデータコンポーネントのプロパティを編集するには、コンポーネントをクリックし、「**[!UICONTROL 設定]」タブでプロパティを編集します。**

* **[!UICONTROL フィールドラベル]**：アセットのプロパティページに表示されるメタデータプロパティの名前。

* **[!UICONTROL プロパティにマッピング]**：このプロパティの値には、CRX リポジトリに保存される場所にあるアセットノードへの相対パスまたは名前を指定します。この値は、パスがアセットのノード以下にあることを示すように、「**./**」から始めます。

このプロパティの有効な値は次のとおりです。

-- [!UICONTROL `./jcr:content/metadata/dc:title`]: Stores the value at the asset's metadata node as the property [!UICONTROL `dc:title`].

-- [!UICONTROL `./jcr:created`]: Displays the jcr property at the asset's node. 表示プロパティ上でこれらのプロパティを設定する場合は、これらのプロパティは保護されているので、「編集を無効にする」としてマークすることをお勧めします。そうしない場合、アセットのプロパティを保存したときに、「アセットの変更に失敗しました」というエラーが発生します。

* **[!UICONTROL プレースホルダー]**：メタデータプロパティに関する関連情報をユーザーに示すには、このプロパティを使用します。
* **[!UICONTROL 必須]**：プロパティページでメタデータプロパティを必須としてマークするには、このプロパティを使用します。
* **[!UICONTROL 編集を無効にする]**：プロパティページでメタデータプロパティを編集不可にするには、このプロパティを使用します。
* **[!UICONTROL 空白のフィールドを読み取り専用として表示]**：プロパティページでメタデータプロパティに値がなくても表示するには、このプロパティをオンにします。デフォルトでは、メタデータプロパティに値がない場合、プロパティページには表示されません。
* **[!UICONTROL 説明]**：メタデータコンポーネントの短い説明を追加するには、このプロパティを使用します。
* **[!UICONTROL 削除アイコン]**：スキーマフォームからコンポーネントを削除するには、このアイコンをクリックします。

![](assets/delete_icon_editmetadataschemaform.png)

>[!NOTE]
>
>アセットのメタデータエディターフォームでは、すべてのメタデータフィールドが読み取り専用です。これは、Brand Portal にアセットを公開する前に、そのアセットのメタデータを AEM Assets で編集する必要があるからです。

#### スキーマフォームでのタブの追加または削除 {#add-or-delete-a-tab-in-the-schema-form}

デフォルトスキーマフォームには、「**[!UICONTROL 基本]**」タブと「**詳細]」タブが含まれています。[!UICONTROL **&#x200B;スキーマエディターで、タブを追加または削除できます。

![](assets/add_delete_tabs_metadataschemaform.png)

* To add a new tab on a schema form, click **[!UICONTROL +]**. 新しいタブにはデフォルトで「名前なし-1」という名前が付けられます。この名前は、「**[!UICONTROL 設定]」タブから編集できます。**

![](assets/add-tab-metadata-form.png)

* To delete a tab, click **[!UICONTROL x]**. 「**[!UICONTROL 保存]」をクリックして、変更を保存します。**

## フォルダーへのメタデータスキーマの適用 {#apply-a-metadata-schema-to-a-folder}

Brand Portal では、選択した特定の情報のみをアセットの[!UICONTROL プロパティ]ページに表示するように、メタデータスキーマをカスタマイズして制御できます。[!UICONTROL プロパティ]ページに表示するメタデータを制御するには、メタデータスキーマフォームから必要なメタデータを削除し、そのメタデータスキーマフォームを特定のフォルダーに適用します。

フォルダーにメタデータスキーマフォームを適用するには、以下の手順を実行します。

1. 上部の AEM ツールバーでアドビのロゴをクリックして、管理ツールにアクセスします。

   ![](assets/aemlogo.png)

2. From the administrative tools panel, click **[!UICONTROL Metadata Schemas]**.

3. **[!UICONTROL メタデータスキーマフォーム]**&#x200B;ページで、アセットに適用するスキーマフォーム（例：[!UICONTROL clothing]）を選択します。

   ![](assets/apply-metadata-schema-form-to-folder.png)

4. From the toolbar at the top, click **[!UICONTROL Apply to Folder(s)]**.

5. From the **[!UICONTROL Select Folder(s)]** page, navigate to the folder to which you want to apply the **[!UICONTROL clothing]** metadata schema, for example, **[!UICONTROL Gloves]**.

   ![](assets/apply_metadata_schemaformtofoldergloves.png)

6. 「**[!UICONTROL 適用]」をクリックして、フォルダーにメタデータスキーマフォームを適用します。**

   **[!UICONTROL clothing]** メタデータスキーマフォームで使用できるメタデータが **[!UICONTROL Gloves]フォルダーに適用され、そのフォルダーの**&#x200B;プロパティ&#x200B;**ページに表示されます。**

   ![](assets/folder_metadata_properties.png)

>[!NOTE]
>
>ネストされたスキーマを含むスキーマを、ビデオファイルを含むフォルダーに適用すると、そのビデオファイルのメタデータプロパティが適切にレンダリングされない場合があります。メタデータプロパティを適切にレンダリングするには、ネストされたスキーマを削除し、フォルダーに親スキーマのみを適用します。

## メタデータスキーマフォームの削除 {#delete-a-metadata-schema-form}

Brand Portal では、カスタムのスキーマフォームのみを削除できます。デフォルトのスキーマフォームまたはテンプレートを削除することはできません。ただし、これらのフォームでのカスタムの変更内容は削除できます。

フォームを削除するには、フォームを選択して&#x200B;**[!UICONTROL 削除]アイコンをクリックします。**

![](assets/delete_icon_metadataschemaeditorform.png)

>[!NOTE]
>
>デフォルトフォームに加えたカスタムの変更を削除すると、**[!UICONTROL ロック]記号がメタデータスキーマインターフェイスのフォーム名の前に再度表示され、フォームがデフォルトの状態に戻ったことが示されます。**

## MIME タイプ用のスキーマフォーム {#schema-forms-for-mime-types}

### MIME タイプ用の新しいフォームの追加 {#adding-new-forms-for-mime-types}

デフォルトのフォームに加えて、様々な MIME タイプのアセット用のカスタムフォームを追加したり、適切なフォームタイプの下に新しいフォームを作成したりできます。例えば、**[!UICONTROL image/png]サブタイプの新しいテンプレートを追加するには、「image」フォームの下にフォームを作成します。**&#x200B;スキーマフォームのタイトルはサブタイプ名です。この場合、タイトルは「png」です。

#### 様々な MIME タイプ用の既存のスキーマテンプレートの使用 {#using-an-existing-schema-template-for-various-mime-types}

各種 MIME タイプ用の既存のテンプレートを使用できます。例えば、MIME タイプが **image/png** のアセットには、**image/jpeg** フォームを使用します。

この場合は、CRX リポジトリ内の [!UICONTROL  に新しいノードを作成します。`/etc/dam/metadataeditor/mimetypemappings`]そのノードの名前を指定し、次のプロパティを定義します。

| **名前** | **種類** | **値** |
|---|---|---|
| exposedmimetype | String | image/jpeg |
| mimetypes | String[] | image/png |

* **exposedmimetype**：マッピングする既存フォームの名前
* **mimetypes**：**exposedmimetype** 属性で定義したフォームを使用する MIME タイプのリスト

Brand Portal では、次の MIME タイプとスキーマフォームがマッピングされます。

| **スキーマフォーム** | **MIME タイプ** |
|---|---|
| image/jpeg | image/pjpeg |
| image/tiff | image/x-tiff |
| application/pdf | application/postscript |
| application/x-ImageSet | Multipart/Related; type=application/x-ImageSet |
| application/x-SpinSet | Multipart/Related; type=application/x-SpinSet |
| application/x-MixedMediaSet | Multipart/Related; type=application/x-MixedMediaSet |
| video/quicktime | video/x-quicktime |
| video/mpeg4 | video/mp4 |
| video/avi | video/avi, video/msvideo, video/x-msvideo |
| video/wmv | video/x-ms-wmv |
| video/flv | video/x-flv |

以下に、デフォルトのメタデータプロパティの一覧を示します。

* jcr:content/metadata/cq:tags
* jcr:content/metadata/dc:format
* jcr:content/metadata/dam:status
* jcr:content/metadata/videoCodec
* jcr:content/metadata/audioCodec
* jcr:content/metadata/dc:title
* jcr:content/metadata/dc:description
* jcr:content/metadata/xmpMM:InstanceID
* jcr:content/metadata/xmpMM:DocumentID
* jcr:content/metadata/dam:sha1
* jcr:content/metadata/dam:solutionContext
* jcr:content/metadata/videoBitrate
* jcr:content/metadata/audioBitrate
* jcr:content/usages/usedBy
* jcr:content/jcr:lastModified
* jcr:content/metadata/prism:expirationDate
* jcr:content/onTime
* jcr:content/offTime
* jcr:content/metadata/dam:size
* jcr:content/metadata/tiff:ImageWidth
* jcr:content/metadata/tiff:ImageLength
