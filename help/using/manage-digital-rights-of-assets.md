---
title: アセットのデジタル著作権の管理
seo-title: アセットのデジタル著作権の管理
description: アセットのライセンスを供与したり、アセットや共有リンクの有効期限を設定することで、アセットの使用を制御し、アセットを保護できます。
seo-description: アセットのライセンスを供与したり、アセットや共有リンクの有効期限を設定することで、アセットの使用を制御し、アセットを保護できます。
uuid: ce30e398-0109-41bf- a4d2-2fcca476f499
contentOwner: bDHar
topic-tags: ダウンロードインストール
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
content-type: reference
discoiquuid: f77003ba-31fe-4a9e-96c8- dsc4c2aba79e
translation-type: tm+mt
source-git-commit: 770c353b1143d879280df310012ce9d4d30b40c9

---


# アセットのデジタル著作権の管理 {#manage-digital-rights-of-assets}

ブランドを守るには、クリエイティブアセットやブランドマテリアルの配布および使用を適切に保護することが不可欠です。This can be enforced across the organization and outside by associating an expiration date (and time) with approved assets published from [!DNL AEM] to [!DNL Brand Portal], or by licensing these assets for conditional use. Also, [!DNL Brand Portal] allows you to specify an expiration date for links to the assets shared from [!DNL Brand Portal].

Read on to know how the assets are secured on [!DNL Brand Portal] and understand the associated usage permissions.

## アセットの有効期限 {#asset-expiration}

アセットの有効期限は、Brand Portal 上の承認済みアセットの使用を組織全体にわたって制御する有効な方法です。All the assets published from [!DNL AEM] Assets to Brand Portal can have an expiration date, which restricts the usage of these assets by different user roles.

### 期限切れアセットに関連する使用権限 {#usage-permissions-expired-assets}

In [!DNL Brand Portal], Administrators can view, download, and add expired assets to collections. 一方、エディターと閲覧者にできるのは、期限切れアセットを表示することと、コレクションに追加することだけです。

Administrators can publish expired assets from [!DNL AEM] Assets to [!DNL Brand Portal]. However, expired assets cannot be shared via ink from [!DNL Brand Portal]. If you select any expired asset from a folder containing both expired and non-expired assets, the **[!UICONTROL Share Link]** action is not available. ただし、期限切れおよび期限切れのアセットを含むフォルダを選択した場合は [!UICONTROL 、「共有リンク」アクション] と **[!UICONTROL 「共有リンク」]** アクションが使用できます。

>[!NOTE]
>
>フォルダーは、期限切れのアセットが含まれていても、リンクとして共有できます。この場合、リンクには期限切れのアセットが表示されず、期限切れのアセットのみが共有されます。

以下の表に、期限切れアセットの使用権限を示します。

|  | **リンク共有** | **ダウンロード** | **プロパティ** | **コレクションに追加** | **削除** |
|---|---|---|---|---|---|
| **管理者** | 使用不可 | 使用可 | 使用可 | 使用可 | 使用可 |
| **エディター** | 使用不可 | 使用不可 | 使用可 | 使用可 | 使用不可 |
| **閲覧者** | 使用不可 | 使用不可 | 使用可 | 使用可 | 使用不可 |
| **ゲストユーザー** | 使用不可 | 使用不可 | 使用可 | 使用可 | 使用不可 |

>[!NOTE]
>
>ビューアおよびエディターが期限切れのアセットおよび期限切れのアセットを含むフォルダをダウンロードする場合、期限切れのアセットのみがダウンロードされます。フォルダーに期限切れアセットのみが含まれている場合は、空のフォルダーがダウンロードされます。

### アセットの有効期限ステータス {#expiration-status-of-assets}

アセットの有効期限ステータスはカード表示で確認できます。カード上の赤いフラグは、そのアセットが期限切れであることを示しています。

![](assets/expired_assets_cardview.png)

>[!NOTE]
>
>リスト表示と列表示では、アセットの有効期限ステータスは表示されません。

## アセットのリンクの有効期限 {#asset-link-expiration}

While sharing assets through links, Administrators and Editors can set a date and time of expiration using the **[!UICONTROL Expiration]** field in the **[!UICONTROL Link Sharing]** dialog box. リンクのデフォルトの有効期限は、リンクが共有される日付から7日です。

![](assets/asset-link-sharing.png)

It ensures that assets shared as links expire at the date and time set by [!DNL Brand Portal] Administrators and Editors, and can no longer be viewed and downloaded beyond the expiration date. リンクによって共有されるアセットを外部ユーザーによって表示することもできますが、有効期限を指定することで、承認されたアセットが保護されていることを確認し、指定した時間以外の不明なエンティティに公開されないようにすることができます。

For more information about link sharing, refer to [Share assets as a link](../using/brand-portal-link-share.md).

## ライセンスで保護されたアセット {#licensed-assets}

ライセンスで保護されたアセットを Brand Portal からダウンロードするときは、事前に使用許諾契約への同意が求めらます。This agreement for licensed assets comes when you directly download the asset from [!DNL Brand Portal] or via a shared link. ライセンスで保護されたアセットは、期限切れの場合も期限切れでない場合も、すべてのユーザーが見ることができます。しかし、ライセンスで保護された期限切れアセットのダウンロードと使用には制限が適用されます。ライセンスで保護された期限切れアセットの動作と、ユーザーの役割に基づいて許可される活動については、[期限切れアセットの使用権限](../using/manage-digital-rights-of-assets.md#usage-permissions-expired-assets)を参照してください。

License-protected assets have [license agreement attached](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) to them, which is done by setting asset's [metadata property](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) in [!DNL AEM] Assets.

If you choose to download license-protected asset(s), you are redirected to [!UICONTROL Copyright Management] page.

![](assets/asset-copyright-mgmt.png)

ここでダウンロードするアセットを選択し、関連付けられた使用許諾契約に同意する必要があります。If you do not accept the license agreement, the **[!UICONTROL Download]** button is not enabled.

![](assets/licensed-asset-download-2.png)

選択した項目に保護されたアセットが複数含まれている場合は、アセットを 1 つずつ選択して使用許諾契約に同意し、アセットのダウンロードに進みます。

## 期限切れアセットに関するレポートの生成 {#generate-report-about-expired-assets}

管理者は、特定の期間内に期限切れになったすべてのアセットをリストするレポートを生成してダウンロードできます。このレポートには、サイズ、タイプ、アセット階層内のアセットの位置（アセットの有効期限が切れたとき、アセットが公開されたとき）のアセットが期限切れのアセットについての場合に、詳細情報が含まれます。このレポートの列はカスタマイズ可能であり、表示するデータを要件に応じて増やすことができます。

![](assets/assets-expired.png)

For more information about the reports feature, refer [Work with reports](../using/brand-portal-reports.md#work-with-reports).
