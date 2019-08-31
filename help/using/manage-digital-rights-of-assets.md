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
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# アセットのデジタル著作権の管理 {#manage-digital-rights-of-assets}

ブランドを守るには、クリエイティブアセットやブランドマテリアルの配布および使用を適切に保護することが不可欠です。これは、有効期限日（および時間）をAEMからブランドポータルに発行された承認済みアセットに関連付けたり、条件付き使用のためにこれらのアセットをライセンスしたりすることで、組織全体で適用できます。また、Brand Portal から共有されるアセットへのリンクに有効期限日を指定することもできます。

以下では、Brand Portal 上のアセットを安全に保護する方法と、関連する使用権限について説明します。

## アセットの有効期限 {#asset-expiration}

アセットの有効期限は、Brand Portal 上の承認済みアセットの使用を組織全体にわたって制御する有効な方法です。AEM Assetsからブランドポータルに公開されたすべてのアセットに有効期限が設定されている場合があります。これにより、ユーザーの役割ごとにこれらのアセットの使用を制限できます。

### 期限切れアセットに関連する使用権限 {#usage-permissions-expired-assets}

Brand Portal では、管理者は期限切れアセットを表示したり、ダウンロードしたり、コレクションに追加したりできます。一方、エディターと閲覧者にできるのは、期限切れアセットを表示することと、コレクションに追加することだけです。

管理者は期限切れアセットを AEM Assets から Brand Portal へ公開できます。ただし、期限切れのアセットをブランドポータルから共有することはできません。If you select any expired asset from a folder containing both expired and non-expired assets, the **[!UICONTROL Share Link]** action is not available. ただし、期限切れおよび期限切れのアセットを含むフォルダを選択した場合は [!UICONTROL 、「共有リンク」アクション] と **[!UICONTROL 「共有リンク」]** アクションが使用できます。

>[!NOTE]
>
>フォルダーは、期限切れのアセットが含まれていても、リンクとして共有できます。この場合、リンクには期限切れのアセットが表示されず、期限切れのアセットのみが共有されます。

以下の表に、期限切れアセットの使用権限を示します。

|  | **[!UICONTROL リンク共有]** | **[!UICONTROL ダウンロード]** | **[!UICONTROL プロパティ]** | **[!UICONTROL コレクションに追加]** | **[!UICONTROL 削除]** |
|---|---|---|---|---|---|
| **[!UICONTROL 管理者]** | 使用不可 | 使用可 | 使用可 | 使用可 | 使用可 |
| **[!UICONTROL エディター]** | 使用不可 | 使用不可 | 使用可 | 使用可 | 使用不可 |
| **[!UICONTROL 閲覧者]** | 使用不可 | 使用不可 | 使用可 | 使用可 | 使用不可 |
| **[!UICONTROL ゲストユーザー]** | 使用不可 | 使用不可 | 使用可 | 使用可 | 使用不可 |

>[!NOTE]
>
>ビューアおよびエディターが期限切れのアセットおよび期限切れのアセットを含むフォルダをダウンロードする場合、期限切れのアセットのみがダウンロードされます。フォルダーに期限切れアセットのみが含まれている場合は、空のフォルダーがダウンロードされます。

### アセットの有効期限ステータス {#expiration-status-of-assets}

[!UICONTROL カード表示で、アセットの有効期限ステータスを表示]できます。カード上の赤いフラグは、そのアセットが期限切れであることを示しています。

![](assets/expired_assets_cardview.png)

>[!NOTE]
>
>リスト表示と列表示では、アセットの有効期限ステータスは表示されません。

## アセットのリンクの有効期限 {#asset-link-expiration}

While sharing assets through links, Administrators and Editors can set a date and time of expiration using the **[!UICONTROL Expiration]** field in the **[!UICONTROL Link Sharing]** dialog box. リンクのデフォルトの有効期限は、リンクが共有される日付から7日です。

![](assets/asset-link-sharing.png)

これにより、リンクとして共有されたアセットは Brand Portal の管理者およびエディターが設定した日時に期限切れになり、その後は表示もダウンロードもできなくなります。リンクによって共有されるアセットを外部ユーザーによって表示することもできますが、有効期限を指定することで、承認されたアセットが保護されていることを確認し、指定した時間以外の不明なエンティティに公開されないようにすることができます。

For more information about link sharing, refer to [Share assets as a link](../using/brand-portal-link-share.md).

## ライセンスで保護されたアセット {#licensed-assets}

ライセンスで保護されたアセットを Brand Portal からダウンロードするときは、事前に使用許諾契約への同意が求めらます。ライセンスで保護されたアセットの使用許諾契約は、アセットを Brand Portal から直接ダウンロードまたは共有リンクを介してダウンロードするときに表示されます。ライセンスで保護されたアセットは、期限切れの場合も期限切れでない場合も、すべてのユーザーが見ることができます。しかし、ライセンスで保護された期限切れアセットのダウンロードと使用には制限が適用されます。ライセンスで保護された期限切れアセットの動作と、ユーザーの役割に基づいて許可される活動については、[期限切れアセットの使用権限](../using/manage-digital-rights-of-assets.md#usage-permissions-expired-assets)を参照してください。

License-protected assets have [license agreement attached](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) to them, which is done by setting asset's [metadata property](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) in AEM Assets.

If you choose to download license-protected asset(s), you are redirected to [!UICONTROL Copyright Management] page.

![](assets/asset-copyright-mgmt.png)

ここでダウンロードするアセットを選択し、関連付けられた使用許諾契約に同意する必要があります。If you do not accept the license agreement, the [!UICONTROL Download] button is not enabled.

![](assets/licensed-asset-download-2.png)

選択した項目に保護されたアセットが複数含まれている場合は、アセットを 1 つずつ選択して使用許諾契約に同意し、アセットのダウンロードに進みます。

## 期限切れアセットに関するレポートの生成 {#generate-report-about-expired-assets}

管理者は、特定の期間内に期限切れになったすべてのアセットをリストするレポートを生成してダウンロードできます。このレポートには、サイズ、タイプ、アセット階層内のアセットの位置（アセットの有効期限が切れたとき、アセットが公開されたとき）のアセットが期限切れのアセットについての場合に、詳細情報が含まれます。このレポートの列はカスタマイズ可能であり、表示するデータを要件に応じて増やすことができます。

![](assets/assets-expired.png)

For more information about the reports feature, refer [Work with reports](../using/brand-portal-reports.md#work-with-reports).
