---
title: アセットをリンクとして共有
seo-title: アセットをリンクとして共有
description: AEM Assets Brand Portal 管理者は、内部のユーザーや外部の関係者（パートナーやベンダーを含む）との間で複数のアセットのリンクを共有できます。エディターは、管理者によって共有されたアセットのみを閲覧および共有できます。
seo-description: AEM Assets Brand Portal 管理者は、内部のユーザーや外部の関係者（パートナーやベンダーを含む）との間で複数のアセットのリンクを共有できます。エディターは、管理者によって共有されたアセットのみを閲覧および共有できます。
uuid: 8889ac24-c56d-4a47-b792-80c34ffb5c3f
contentOwner: bdhar
content-type: reference
topic-tags: sharing
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: f3573219-3c58-47ba-90db-62b003d8b9aa
translation-type: tm+mt
source-git-commit: 86d4d5c358ea795e35db2dce8c9529ed14e9ee2d

---


# アセットをリンクとして共有 {#share-assets-as-a-link}

AEM Assets Brand Portal 管理者は、内部のユーザーや外部の関係者（パートナーやベンダーを含む）との間で複数のアセットのリンクを共有できます。エディターは、管理者によって共有されたアセットのみを閲覧および共有できます。

受信者がBrand portalにログインしなくてもアセットにアクセスできるので、リンクを介したアセットの共有は、外部の関係者が簡単に利用できるようにする方法です。

リンク共有を利用したアクセスは、エディターと管理者に制限されています。詳しくは、[ユーザー、グループ、ユーザーの役割の管理](../using/brand-portal-adding-users.md#manage-user-roles)を参照してください。

>[!NOTE]
>
>Brand portalでのリンク共有機能を使用したZIPダウンロードは、最大5 GBで可能です。

アセットをリンクとして共有するには、次の手順に従います。

1. Click the overlay icon on the left, and choose **[!UICONTROL Navigation]**.

   ![](assets/siderail.png)

1. 左側のサイドレールで「**[!UICONTROL ファイル]」をクリックして、フォルダーや画像を共有します。**&#x200B;コレクションを共有するには、「**[!UICONTROL コレクション]**」をクリックします。

   ![](assets/navigationrail.png)

1. リンクとして共有するフォルダーやコレクションを選択します。

   ![](assets/asset-link-share.png)

1. 上部のツールバーで&#x200B;**[!UICONTROL リンクを共有]アイコンをクリックします。**

   **[!UICONTROL リンク共有]ダイアログボックスが表示されます。**

   ![](assets/link-sharing.png)

   >[!NOTE]
   >
   >自動的に作成されたアセットリンクが「**[!UICONTROL リンクを共有]」フィールドに表示されます。**&#x200B;このリンクのデフォルトの有効期限は 7 日間です。リンクをコピーして、別途ユーザーと共有できます。また、**[!UICONTROL リンク共有]ダイアログボックスからもリンクを共有できます。**

1. 「電子メールアドレス」ボックスに、リンクを共有するユーザーの電子メール ID を入力します。リンクを複数のユーザーと共有できます。

   ユーザーが組織のメンバーの場合は、ドロップダウンリストに表示される候補の中から電子メール ID を選択します。If the user is external, type the complete email ID and press **[!UICONTROL Enter]**; the email ID is added to the list of users.

   ![](assets/link-sharing-text.png)

1. 「**[!UICONTROL 件名]」ボックスに、共有するアセットの件名を入力します。**
1. 必要に応じて、「**[!UICONTROL メッセージ]」ボックスにメッセージを入力します。**
1. 「**[!UICONTROL 有効期限]」フィールドに、日付選択を使用して、リンクの有効期限を指定します。**&#x200B;デフォルトの有効期限は、リンクを共有した日から 7 日間です。

   リンク共有されるアセットは、「**[!UICONTROL 有効期限]」フィールドに指定した日時を過ぎると有効期限が切れます。** For information about the behavior of expired assets and changes in the permissible activities based on user roles in Brand Portal, see [Manage digital rights of assets](../using/manage-digital-rights-of-assets.md#asset-expiration).

1. Click **[!UICONTROL Share]**. リンクをユーザーと共有することを確認するメッセージが表示されます。リンクを含む電子メールがユーザーに届きます。

   ![](assets/link-sharing-email.png)

   >[!NOTE]
   >
   >管理者は、[ブランディング](../using/brand-portal-branding.md)機能を使用してロゴ、説明、フッターをカスタマイズするなど、電子メールメッセージをカスタマイズできます。

## 共有リンクからアセットをダウンロードする {#download-assets-from-shared-links}

電子メールのリンクをクリックし、共有アセットを表示します。AEM リンク共有ページが開きます。

共有アセットをダウンロードするには：

1. アセットをクリックしてから、ツールバーの&#x200B;**[!UICONTROL ダウンロード]アイコンをクリックします。**

   ![](assets/assets-shared-link.png)

   >[!NOTE]
   >
   >現時点では、特定のファイル形式のアセットについてのみ、プレビューとサムネールを生成できます。サポートされているファイル形式について詳しくは、[プレビューおよびサムネールをサポートするアセット形式](#preview-thumbnail-support)を参照してください。

   >[!NOTE]
   >
   >ダウンロードするアセットに、ライセンスが必要なアセットが含まれている場合は、**[!UICONTROL 著作権管理]ページにリダイレクトされます。** In this page, select the licensed assets, click **[!UICONTROL Agree]**, and then click **[!UICONTROL Download]**. 「同意しない」を選択した場合は、ライセンスが不要なアセットのみがダウンロードされます。\
   >License-protected assets have [license agreement attached](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) to them, which is done by setting asset's [metadata property](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) in [!DNL AEM Assets].

   ![](assets/licensed-asset-download.png)

   [!UICONTROL ダウンロード]ダイアログボックスが開きます。<br />
   ![](assets/download-linkshare.png)

   * リンクとして共有されたアセットファイルのダウンロードをスピードアップさせるには、「**[!UICONTROL ダウンロードアクセラレーションを有効化]**」オプションを選択し、[ウィザードに従います](../using/accelerated-download.md#download-workflow-using-file-accelerator)。To know more about the fast download of assets on Brand Portal refer [Guide to accelerate downloads from Brand Portal](../using/accelerated-download.md).
[!UICONTROL
1. 共有リンクのアセットに加えて、アセットのレンディションもダウンロードするには、「**[!UICONTROL レンディション]」オプションを選択します。** When you do so, **Exclude System Renditions]** option appears that is selected by default. これによって、承認済みのアセットレンディションやカスタムレンディションとともに、既製のレンディションがダウンロードされるのを防ぎます。

   ただし、カスタムレンディションと共に自動生成レンディションをダウンロードすることを許可する場合は、「**[!UICONTROL システムレンディションを除く]」オプションの選択を解除します。**

   >[!NOTE]
   >
   >アセットをリンクとして共有したユーザーが、[オリジナルレンディションへのアクセスを管理者によって許可](../using/brand-portal-adding-users.md#manage-group-roles-and-privileges)されていない場合、共有リンクを使用してオリジナルレンディションのダウンロードをおこなうことはできません。

   ![](assets/download-linkshare-autoren.png)

1. Tap/ click **[!UICONTROL Download]**. アセット（および選択されている場合はレンディション）が ZIP ファイルとしてローカルフォルダーにダウンロードされます。ただし、レンディションなしで 1 つのアセットをダウンロードした場合、zip ファイルは作成されないので、すばやくダウンロードを行うことができます。

>[!NOTE]
>
>Brand Portal では、ファイルサイズが 5 GB を超えるアセットのダウンロードは制限されています。

## プレビューおよびサムネールをサポートするアセット形式 {#preview-thumbnail-support}

以下の表に、Brand Portal における様々なアセット形式のサムネールおよびプレビューのサポート状況を示します。

| アセット形式 | サムネールのサポート | プレビューのサポート |
|--------------|-------------------|-----------------|
| PNG | ✓ | ✓ |
| GIF | ✓ | ✓ |
| TIFF | ✓ | ✕ |
| JPEG | ✓ | ✓ |
| BMP | ✓ | ✕ |
| PNM* | 該当なし | 該当なし |
| PGM* | 該当なし | 該当なし |
| PBM* | 該当なし | 該当なし |
| PPM* | 該当なし | 該当なし |
| PSD | ✓ | ✕ |
| EPS | 該当なし | ✕ |
| DNG | ✓ | ✕ |
| PICT | ✓ | ✕ |
| PSB* | ✓ | ✕ |
| JPG | ✓ | ✓ |
| AI | ✓ | ✕ |
| DOC | ✕ | ✕ |
| DOCX | ✕ | ✕ |
| ODT* | ✕ | ✕ |
| PDF | ✓ | ✕ |
| HTML | ✕ | ✕ |
| RTF | ✕ | ✕ |
| TXT | ✓ | ✕ |
| XLS | ✕ | ✕ |
| XLSX | ✕ | ✕ |
| ODS | ✕ | ✕ |
| PPT | ✓ | ✕ |
| PPTX | ✕ | ✕ |
| ODP | ✕ | ✕ |
| INDD | ✓ | ✕ |
| PS | ✕ | ✕ |
| QXP | ✕ | ✕ |
| EPUB | ✓ | ✕ |
| AAC | ✕ | ✕ |
| MIDI | ✕ | ✕ |
| 3GP | ✕ | ✕ |
| MP3 | ✕ | ✕ |
| MP4 | ✕ | ✕ |
| OGA | ✕ | ✕ |
| OGG | ✕ | ✕ |
| RA | ✕ | ✕ |
| WAV | ✕ | ✕ |
| WMA | ✕ | ✕ |
| DVI | ✕ | ✕ |
| FLV | ✕ | ✕ |
| M4V | ✕ | ✕ |
| MPG | ✕ | ✕ |
| OGV | ✕ | ✕ |
| MOV | ✕ | ✕ |
| WMV | ✕ | ✕ |
| SWF | ✕ | ✕ |
| TGZ | 該当なし | ✕ |
| JAR | ✓ | ✕ |
| RAR | 該当なし | ✕ |
| TAR | 該当なし | ✕ |
| ZIP | ✓ | ✕ |

以下に、この表で使用する記号の意味を示します。

| 記号 | 意味 |
|---|---|
| ✓ | この機能はサポートされています。 |
| ✕ | この機能はサポートされていません。 |
| 該当なし | この機能は適用されません。 |
| * | この機能を AEM オーサーインスタンスで使用するには、このファイル形式用のアドオンサポートが必要です。ただし、アセットが Brand Portal に公開された後、Brand Portal で使用する際には不要です。 |

## リンクとして共有されているアセットの共有解除 {#unshare-assets-shared-as-a-link}

リンクとして共有されているアセットの共有を解除するには、以下の手順を実行します。

1. To view the assets you shared as links, click the overlay icon on the left, and choose **[!UICONTROL Navigation]**.

   ![](assets/siderail.png)

1. From the siderail, click **[!UICONTROL Shared Links]**.

   ![](assets/navigationrail.png)

1. 表示された一覧で、共有されているリンクを確認します。
1. この一覧からリンクの共有を解除するには、リンクを選択し、リンク項目の横にあるごみ箱アイコンをクリックするか、上部のツールバーの「**[!UICONTROL 共有しない]」アイコンをクリックします。**

   ![](assets/unshare-links.jpg)

   >[!NOTE]
   >
   >共有されているリンクの表示は、ユーザーごとに異なります。この機能は、テナントのすべてのユーザーが共有するすべてのリンクを表示するものではありません。

1. 警告メッセージボックスで「**[!UICONTROL 続行]」をクリックして、共有を解除することを確認します。**&#x200B;指定したリンク項目が、共有リンクの一覧から削除されます。
