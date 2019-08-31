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
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# レポートの操作 {#work-with-reports}

レポート機能は、ブランドポータルの使用状況を評価し、社内および外部ユーザーが承認されたアセットとどのようにやりとりしたかを把握するのに役立ちます。管理者は Brand Portal 使用状況Usage レポートを表示できます。このレポートは、アセットレポートページでいつでも利用することができます。またただし、ユーザーログイン数、ダウンロードされたアセット、期限切れのアセット、公開されたアセット、およびリンクから共有されたアセットに関するレポートをアセットレポートページから生成およびしたり、表示できますしたりすることはできません。これらのレポートは、アセットのデプロイメントを分析する際に役立ちます。これにより、組織内で承認されたアセットの採用を測定するために重要な成功指標を派生させることができます。

レポート管理インターフェイスは直観的な設計になっており、保存済みレポートにアクセスするためのきめ細かいオプションとコントロールを備えています。以前生成したすべてのレポートが表示されるように、アセットレポートページからレポートを表示、ダウンロードまたは削除できます。

## レポートの表示 {#view-reports}

レポートを表示するには、以下の手順に従います。

1. 上部のツールバーの AEM ロゴをタップまたはクリックして、管理ツールにアクセスします。

   ![](assets/aemlogo.png)

2. From the administrative tools panel, click **[!UICONTROL Create/Manage Reports]** to open **[!UICONTROL Asset Reports]** page.

   ![](assets/access-asset-reports.png)

3. Access **[!UICONTROL Usage]** report and other generated reports from Asset Reports page.

   >[!NOTE]
   >
   >使用状況レポートは、デフォルトで Brand Portal に存在します。使用状況レポートは作成も削除もできません。ただし、ダウンロード、有効期限、発行、リンク共有およびユーザーログインレポートを作成し、削除することができます。

   レポートを表示するには、レポートのリンクをタップまたはクリックします。または、レポートを選択し、ツールバーの表示アイコンをタップまたはクリックします。

   [!UICONTROL 使用状況レポート]には、現在の Brand Portal ユーザーの数、すべてのアセットの占有ストレージスペースおよび Brand Portal 内の合計アセット数に関する情報が表示されます。また、それぞれの情報指標で許可されている容量も表示されます。

   ![](assets/usage-report.png)

   [!UICONTROL ユーザーログイン]レポートには、Brand Portal にログインしたユーザーについての情報が表示されます。レポートには、レポート生成時点までの、ブランドポータル6.4.2デプロイメントの表示名、電子メールID、個人（管理者、Viewer、エディター、ゲスト）、グループ、最後のログイン、アクティビティステータス、およびログインカウントが表示されます。

   ![](assets/user-logins.png)

   [!UICONTROL ダウンロード]レポートには、特定の期間内にダウンロードされたすべてのアセットと、それらの詳細情報が表示されます。

   ![](assets/download-report.png)

   >[!NOTE]
   >
   >The assets [!UICONTROL Download] report displays only the assets that were individually selected and downloaded from Brand Portal. ユーザがアセットを含むフォルダをダウンロードした場合、そのフォルダ内のフォルダまたはアセットは表示されません。

   [!UICONTROL 有効期限]レポートには、特定の期間内に有効期限が切れたすべてのアセットと、それらの詳細情報が表示されます。

   ![](assets/expiration-report.png)

   [!UICONTROL 公開]レポートには、特定の期間内に AEM から Brand Portal に公開されたすべてのアセットと、それらに関する情報が表示されます。

   ![](assets/publish-report.png)

   >[!NOTE]
   >
   >コンテンツフラグメントを Brand Portal に公開することはできないため、公開レポートにはコンテンツフラグメントに関する情報は表示されません。

   [!UICONTROL リンク共有レポート]には、特定の期間内に Brand Portal インターフェイスのリンクから共有されたすべてのアセットが一覧表示されます。また、このレポートでは、リンクによって共有されたアセット、ユーザー、リンクの有効期限が切れたときのユーザー、テナント（およびアセットのリンクを共有しているユーザー）の共有リンクの数が表示されます。リンク共有レポートの列はカスタマイズできません。

   ![](assets/link-share-report.png)

   >[!NOTE]
   >
   >リンク共有レポートには、リンク経由で共有されたアセットにアクセスしたユーザーや、リンクからアセットをダウンロードしたユーザーは表示されません。
   >
   >
   >共有リンクからのダウンロードを追跡するには、**[!UICONTROL レポートを作成]**&#x200B;ページで「**リンク共有ダウンロードのみ]」オプションを選択した後、ダウンロードレポートを生成する必要があります。[!UICONTROL **&#x200B;ただし、この場合、ユーザー（ダウンロード者）は匿名です。

## レポートの生成 {#generate-reports}

Administrators can generate and manage the following standard reports, once generated, they are saved to be [accessed](../using/brand-portal-reports.md#main-pars-header) later:

* ユーザーログイン
* ダウンロード
* 有効期限
* 公開
* リンク共有

ダウンロード、有効期限および公開レポートの列は、カスタマイズして表示できます。レポートを生成するには、以下の手順に従います。

1. 上部のツールバーの AEM ロゴをタップまたはクリックして、管理ツールにアクセスします。

   ![](assets/aemlogo.png)

2. From the administrative tools panel, tap/click **[!UICONTROL Create/Manage Reports]** to open **Asset Reports **page.

   ![](assets/asset-reports.png)

3. In the Asset Reports page, tap/click **[!UICONTROL Create]**.
4. From the **[!UICONTROL Create Report]** page, select a report to create, and tap/click **[!UICONTROL Next]**.

   ![](assets/crete-report.png)

5. レポートの詳細を設定します。Specify title, description, folder structure (where report needs to run and generate statistics), and date range for [!UICONTROL Download], [!UICONTROL Expiration], and [!UICONTROL Publish] reports.

   ![](assets/create-report-page.png)

   Whereas, [!UICONTROL Link Share Report] only needs the title, description, and date range parameters.

   ![](assets/create-link-share-report.png)

   >[!NOTE]
   >
   >レポートのタイトルの特殊文字#および%は、レポート生成のハイフン（-）に置き換えられます。

6. Tap/click **[!UICONTROL Next]**, to configure the columns of Download, Expiration, and Publish reports.
7. 必要に応じて、適切なチェックボックスをオンまたはオフにします。For example, to view names of users (who downloaded assets) in [!UICONTROL Download] report, select **[!UICONTROL Downloaded By]**. 次の画像は、ダウンロードレポートのデフォルト列の選択を示しています。

   ![](assets/createdownloadreport.png)

   また、これらのレポートにカスタム列を追加して、独自の要件に応じてさらに多くのデータを表示できます。

   ダウンロードレポート、公開レポートまたは有効期限レポートにカスタム列を追加するには、以下の手順に従います:

   1. To display a custom column, tap/click **[!UICONTROL Add]** within [!UICONTROL Custom Columns].
   2. Specify name of the column in **[!UICONTROL Column Name]** field.
   3. プロパティピッカーを使用して、列と対応付ける必要があるプロパティを選択します。

      ![](assets/property-picker.png)または、プロパティパスフィールドにパスを入力します。

      ![](assets/property-path.png)

      カスタム列をさらに追加するには、「**追加**」をタップまたはクリックし、手順 2 および 3 を繰り返します。

8. Tap/click **[!UICONTROL Create]**. レポート生成が開始されたことを知らせるメッセージが表示されます。

## ダウンロードレポート {#download-reports}

レポートを保存し、.csv ファイルとしてダウンロードするには、以下のいずれかの手順を実行します。

* Select a report on Asset Reports page, and tap/click **[!UICONTROL Download]** from the toolbar at the top.

![](assets/download-asset-report.png)

* アセットレポートページから、レポートを開きます。Select **[!UICONTROL Download]** option from the top of the report page.

![](assets/download-report-fromwithin.png)

## レポートの削除 {#delete-reports}

既存のレポートを削除するには、**[!UICONTROL アセットレポート]**&#x200B;ページからレポートを選択し、上部のツールバーの「**削除[!UICONTROL 」をタップまたはクリックします。]**

>[!NOTE]
>
>[!UICONTROL 使用状況]レポートを削除することはできません。
