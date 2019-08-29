---
title: レポートの操作
seo-title: レポートの操作
description: AEM Assets Brand Portal 管理者は、Brand Portal の使用状況に関するレポートを表示できます。また、ダウンロードされたアセット、有効期限が切れたアセット、公開されたアセット、リンクで共有されているアセットに関するレポートを、Brand Portal を介して作成、管理および表示することもできます。
seo-description: AEM Assets Brand Portal 管理者は、Brand Portal の使用状況に関するレポートを表示できます。また、ダウンロードされたアセット、有効期限が切れたアセット、公開されたアセット、リンクで共有されているアセットに関するレポートを、Brand Portal を介して作成、管理および表示することもできます。
uuid: dc4e5275- a614-4b95-8c70-2b7e470c50a7
content-type: reference
topic-tags: 管理
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
discoiquuid: 7683074f- b6ea-42e0- a411-3b13eb88d1f2
translation-type: tm+mt
source-git-commit: 32c3cdb8e3fafd74cfb36e6bcfe0811e7152b2d0

---


# レポートの操作 {#work-with-reports}

The reporting capability is instrumental in assessing [!DNL Brand Portal] usage, and knowing how internal and external users interact with approved assets. Administrators can view [!DNL Brand Portal] Usage report, which is always available on Asset Reports page. またただし、ユーザーログイン数、ダウンロードされたアセット、期限切れのアセット、公開されたアセット、およびリンクから共有されたアセットに関するレポートをアセットレポートページから生成およびしたり、表示できますしたりすることはできません。これらのレポートは、アセットのデプロイメントを分析する際に役立ちます。これにより、組織内で承認されたアセットの採用を測定するために重要な成功指標を派生させることができます。

レポート管理インターフェイスは直観的な設計になっており、保存済みレポートにアクセスするためのきめ細かいオプションとコントロールを備えています。以前生成したすべてのレポートが表示されるように、アセットレポートページからレポートを表示、ダウンロードまたは削除できます。

## レポートの表示 {#view-reports}

レポートを表示するには、以下の手順に従います。

1. From the toolbar at the top, tap/click the [!DNL AEM] logo to access administrative tools.

   ![](assets/aemlogo.png)

2. From the administrative tools panel, click **Create/Manage Reports** to open **Asset Reports **page.

   ![](assets/access-asset-reports.png)

3. Access **Usage** report and other generated reports from Asset Reports page.

   >[!NOTE]
   >
   >Usage report is present by default in [!DNL Brand Portal]. 使用状況レポートは作成も削除もできません。ただし、ダウンロード、有効期限、発行、リンク共有およびユーザーログインレポートを作成し、削除することができます。

   レポートを表示するには、レポートのリンクをタップまたはクリックします。または、レポートを選択し、ツールバーの表示アイコンをタップまたはクリックします。

   **使用状況レポート** には、現在 [!DNL Brand Portal] のユーザー数、すべてのアセットが占めているストレージ容量、および合計アセット数に関する情報が表示 [!DNL Brand Portal]されます。また、それぞれの情報指標で許可されている容量も表示されます。

   ![](assets/usage-report.png)

   **ユーザーログイン** レポートは、ログインしているユーザーに関する情報を提供 [!DNL Brand Portal]します。The report shows display names, email IDs, personas (admin, viewer, editor, guest), groups, last login, activity status, and login count of each user from [!DNL Brand Portal] 6.4.2 deployment until the time of report generation.

   ![](assets/user-logins.png)

   **ダウンロード**&#x200B;レポートには、特定の期間内にダウンロードされたすべてのアセットと、それらの詳細情報が表示されます。

   ![](assets/download-report.png)

   >[!NOTE]
   >
   >The assets** Download** report displays only the assets that were individually selected and downloaded from [!DNL Brand Portal]. ユーザがアセットを含むフォルダをダウンロードした場合、そのフォルダ内のフォルダまたはアセットは表示されません。

   **有効期限**&#x200B;レポートには、特定の期間内に有効期限が切れたすべてのアセットと、それらの詳細情報が表示されます。

   ![](assets/expiration-report.png)

   **公開**[!DNL AEM]レポートには、特定の期間内に から に公開されたすべてのアセットと、それらに関する情報が表示されます。[!DNL Brand Portal]

   ![](assets/publish-report.png)

   >[!NOTE]
   >
   >Publish Report does not display information about content fragments, as the content fragments cannot be published to the [!DNL Brand Portal].

   **リンク共有レポート**[!DNL Brand Portal]には、特定の期間内に インターフェイスのリンクから共有されたすべてのアセットが一覧表示されます。また、このレポートでは、リンクによって共有されたアセット、ユーザー、リンクの有効期限が切れたときのユーザー、テナント（およびアセットのリンクを共有しているユーザー）の共有リンクの数が表示されます。リンク共有レポートの列はカスタマイズできません。

   ![](assets/link-share-report.png)

   >[!NOTE]
   >
   >リンク共有レポートには、リンク経由で共有されたアセットにアクセスしたユーザーや、リンクからアセットをダウンロードしたユーザーは表示されません。
   >
   >
   >共有リンクからのダウンロードを追跡するには、**レポートを作成**&#x200B;ページで「**リンク共有ダウンロードのみ**」オプションを選択した後、ダウンロードレポートを生成する必要があります。ただし、この場合、ユーザー（ダウンロード者）は匿名です。

## レポートの生成 {#generate-reports}

Administrators can generate and manage the following standard reports, once generated, they are saved to be [accessed](../using/brand-portal-reports.md#main-pars-header) later:

* ユーザーログイン
* ダウンロード
* 有効期限
* 公開
* リンク共有

ダウンロード、有効期限および公開レポートの列は、カスタマイズして表示できます。レポートを生成するには、以下の手順に従います。

1. From toolbar at the top, tap/click the [!DNL AEM] logo to access administrative tools.

   ![](assets/aemlogo.png)

2. From the administrative tools panel, tap/click **Create/Manage Reports** to open **Asset Reports **page.

   ![](assets/asset-reports.png)

3. アセットレポートページで、「**作成**」をタップまたはクリックします。
4. From the **Create Report** page, select a report to create, and tap/click **Next**.

   ![](assets/crete-report.png)

5. レポートの詳細を設定します。Specify title, description, folder structure (where report needs to run and generate statistics), and date range for **Download**, **Expiration**, and **Publish** reports.

   ![](assets/create-report-page.png)

   Whereas, **Link Share Report** only needs the title, description, and date range parameters.

   ![](assets/create-link-share-report.png)

   >[!NOTE]
   >
   >レポートのタイトルの特殊文字#および%は、レポート生成のハイフン（-）に置き換えられます。

6. Tap/click **Next**, to configure the columns of Download, Expiration, and Publish reports.
7. 必要に応じて、適切なチェックボックスをオンまたはオフにします。For example, to view names of users (who downloaded assets) in **Download** report, select **Downloaded By**. 次の画像は、ダウンロードレポートのデフォルト列の選択を示しています。

   ![](assets/createdownloadreport.png)

   また、これらのレポートにカスタム列を追加して、独自の要件に応じてさらに多くのデータを表示できます。

   ダウンロードレポート、公開レポートまたは有効期限レポートにカスタム列を追加するには、以下の手順に従います:

   1. To display a custom column, tap/click **Add** within **Custom Columns**.
   2. Specify name of the column in **Column Name** field.
   3. プロパティピッカーを使用して、列と対応付ける必要があるプロパティを選択します。

      ![](assets/property-picker.png)または、プロパティパスフィールドにパスを入力します。

      ![](assets/property-path.png)

      カスタム列をさらに追加するには、「**追加**」をタップまたはクリックし、手順 2 および 3 を繰り返します。

8. 「**作成**」をタップまたはクリックします。レポート生成が開始されたことを知らせるメッセージが表示されます。

## ダウンロードレポート {#download-reports}

レポートを保存し、.csv ファイルとしてダウンロードするには、以下のいずれかの手順を実行します。

* Select a report on Asset Reports page, and tap/click **Download** from the toolbar at the top.

![](assets/download-asset-report.png)

* アセットレポートページから、レポートを開きます。Select **Download** option from the top of the report page.

![](assets/download-report-fromwithin.png)

## レポートの削除 {#delete-reports}

既存のレポートを削除するには、**アセットレポート**&#x200B;ページからレポートを選択し、上部のツールバーの「**削除**」をタップまたはクリックします。

>[!NOTE]
>
>**使用状況**&#x200B;レポートを削除することはできません。
