---
title: Brand Portal でのダイナミックビデオのサポート
seo-title: Dynamic video support on Brand Portal
description: Brand Portal でのダイナミックビデオのサポート
seo-description: Dynamic video support on Brand Portal
uuid: a3502a4d-3971-4ea4-953c-44ba04446269
contentOwner: mgulati
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: download-install
discoiquuid: e18d992a-a3b5-45f2-9696-8161993213ee
exl-id: 08d6a0fb-061e-4bef-b8e2-bb8522e7482e
source-git-commit: 8924ff9c78c065895dd0f8d1099a5488b34a34e2
workflow-type: tm+mt
source-wordcount: '1250'
ht-degree: 56%

---

# Brand Portal でのダイナミックビデオのサポート {#dynamic-video-support-on-brand-portal}

Dynamic Media をサポートしている Brand Portal でビデオをアダプティブにプレビューおよび再生します。また、ポータルおよび共有リンクから動的レンディションをダウンロードします。
Brand Portal を使用すると、次のことが可能になります。

* アセットの詳細ページ、カード表示、リンク共有のプレビューページでビデオをプレビューする。
* アセットの詳細ページでビデオエンコードを再生する。
* アセットの詳細ページの「レンディション」タブで動的レンディションを表示する。
* ビデオを格納したフォルダーとビデオエンコードをダウンロードする。

>[!NOTE]
>
>ビデオを操作したり Brand Portal に公開したりするには、Experience Manager オーサーインスタンスが Dynamic Media ハイブリッドモードか Dynamic Media **[!DNL Scene7]** モードのいずれかに設定されていることを確認してください。

ビデオをプレビュー、再生、ダウンロードするために、Brand Portal では次の 2 つの設定を管理者に公開しています。

* [Dynamic Media ハイブリッド設定](#configure-dm-hybrid-settings)：Experience Manager オーサーインスタンスが Dynamic Media ハイブリッドモードで動作している場合。
* [Dynamic Media [!DNL Scene7] 設定](#configure-dm-scene7-settings)：Experience Manager オーサーインスタンスが Dynamic Media **[!DNL Scene7]** モードで動作している場合。
Brand Portal テナントの複製先となる Experience Manager オーサーインスタンスに指定した設定に基づいて、これらの設定のいずれかを指定します。

>[!NOTE]
>
>で実行されているExperience Managerオーサーとの設定済みのBrand Portalテナントでは、ダイナミックビデオはサポートされていません。 **[!UICONTROL Scene7Connect]** 実行モード。

## ダイナミックビデオの再生方法 {#how-are-dynamic-videos-played}

![ビデオエンコードはクラウドから取得される](assets/VideoEncodes.png)

Dynamic Media 設定（[ハイブリッド](../using/dynamic-video-brand-portal.md#configure-dm-hybrid-settings)設定または [[!DNL Scene7]](../using/dynamic-video-brand-portal.md#configure-dm-scene7-settings) 設定）が Brand Portal で指定されている場合、動的レンディションは **[!DNL Scene7]** サーバーから取得されます。したがって、ビデオエンコードは遅延や品質の劣化なしにプレビューおよび再生されます。

ビデオエンコードはBrand Portalリポジトリに格納されず、から取得されるので、 **[!DNL Scene7]** サーバーで、Adobe Experience ManagerオーサーインスタンスとBrand PortalのDynamic Media設定が同じであることを確認してください。

>[!NOTE]
>
>Brand Portal では、ビデオビューアとビューアプリセットはサポートされません。ビデオは Brand Portal のデフォルトのビューアでプレビューおよび再生されます。

## 前提条件 {#prerequisites}

Brand Portal 上でダイナミックビデオを操作するには、必ず以下を行ってください。

* **Dynamic MediaモードでExperience Managerオーサーを起動する**
次のいずれかで、(Brand Portalの設定に使用する )Experience Managerオーサーインスタンスを起動します。 [Dynamic Media - [!DNL Scene7] mode](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/config-dms7.html?lang=en#enabling-dynamic-media-in-scene-mode) または [Dynamic Media — ハイブリッドモード](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/config-dynamic.html?lang=ja) または
* **Experience ManagerオーサーでのDynamic MediaCloud Servicesの設定**
Dynamic Mediaモード (Scene7モードまたはハイブリッドモード ) でExperience Manager作成者が実行しているモードに応じて、 [Dynamic MediaCloud Services([!DNL Scene7] モード )](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/config-dms7.html?lang=ja?lang=en#configuring-dynamic-media-cloud-services) または [Dynamic MediaCloud Services（ハイブリッドモード）](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/config-dynamic.html?lang=en#configuring-dynamic-media-cloud-services) Experience Manager作成者： **ツール** | **Cloud Services** | **Dynamic Media**.
* **Brand PortalでのDynamic Mediaの設定**
Experience Manager作成者のDynamic Mediaクラウド設定に基づいて、を設定します。 [Dynamic Media設定](#configure-dm-hybrid-settings) または [[!DNL Scene7] 設定](#configure-dm-scene7-settings) Brand Portal管理ツールから。
必ず [独立したBrand Portalテナント](#separate-tenants) は、Dynamic Mediaで設定されたExperience Managerオーサーインスタンスに使用されます。 **[!UICONTROL Scene7]** モードとDynamic Media — ハイブリッドモード。 特にDynamic Mediaの機能を使用する場合 **[!UICONTROL S7]** Dynamic Mediaハイブリッド。
* **Brand Portalに適用されたビデオエンコードを含んだフォルダーを公開する**
適用 [ビデオエンコーディング](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/video-profiles.html?lang=ja) リッチメディアアセットを含むフォルダーをExperience ManagerオーサーインスタンスからBrand Portalに公開します。
* **セキュアプレビューが有効な場合は、SPS でエグレス IP を許可リストに登録する**：
（会社に対して[セキュアプレビューが有効 ](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html?lang=ja)な状態で）Dynamic Media -**[!DNL Scene7]** を使用する場合は、 の **[!DNL Scene7]** 会社管理者が SPS（**[!UICONTROL Scene7]** Publishing System）Flash UI を使用して、それぞれの地域の[公開エグレス IP を許可リストに登録する](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html?lang=ja#testing-the-secure-testing-service)ことをお勧めします。
エグレス IP は次のとおりです。

| **地域** | **エグレス IP** |
|--- |--- |
| 該当なし | 130.248.160.68,  20.94.203.130 |
| EMEA | 185.34.189.3,  51.132.146.75 |
| APAC | 63.140.44.54 |

これらのいずれかのエグレス IP を許可リストに登録するには、[セキュアテストサービス用アカウントの準備方法](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html#testing-the-secure-testing-service)を参照してください。

## ベストプラクティス

ダイナミックビデオアセットが Brand Portal（および共有リンク）から正常にプレビュー、再生、ダウンロードされるようにするには、次のベストプラクティスに従います。

### Dynamic Media - Scene7とDynamic Media — ハイブリッドモードでテナントが異なる {#separate-tenants}

両方のDynamic Media - **[!DNL Scene7]** モードとDynamic Media — ハイブリッドモードの機能。Dynamic Mediaで設定されたExperience Managerオーサーインスタンスには、異なるBrand Portalテナントを使用します — **[!DNL Scene7]** およびDynamic Media — ハイブリッドモード。


![オーサーと BP が 1 対 1 で対応](assets/BPDynamicMedia.png)

### Experience ManagerオーサーインスタンスとBrand Portalで同じ設定の詳細

Brand Portalと **[!UICONTROL Experience Managerクラウド設定]**. 同じ設定の詳細を次に示します。

* **[!UICONTROL タイトル]**
* **[!UICONTROL 登録 ID]**
* **[!UICONTROL ビデオサービスの URL]** in **[!UICONTROL Dynamic Media — ハイブリッドモード]**
* **[!UICONTROL タイトル]**
* 資格情報 (**[!UICONTROL 電子メール]** およびパスワード )
* **[!UICONTROL 地域]**
* **[!UICONTROL 会社]** Dynamic Media - **[!DNL Scene7]** mode

### Dynamic Media Scene7 モードの公開エグレス IP を許可リストに登録する

Dynamic Media **[!UICONTROL Scene7]**（[セキュアプレビューが有効](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html)）を使用して Brand Portal にビデオアセットを配信する場合、**[!UICONTROL Scene7]** はステージング環境または内部アプリケーション用に専用の画像サーバーを設定します。このサーバーへのリクエストはすべて、発信元 IP アドレスをチェックします。受信リクエストが IP アドレスの承認済みリストに含まれていない場合は、失敗のレスポンスが返されます。
この **[!UICONTROL Scene7]** したがって、会社の管理者が自社の **[!UICONTROL セキュアテスト]** 環境、経由 **[!UICONTROL SPS]** (Scene7 Publishing System)Flash UI 該当するそれぞれの地域のエグレス IP（以下を参照）を、その承認済みリストに必ず追加してください。
これらのいずれかのエグレス IP を許可リストに登録するには、[セキュアテストサービス用アカウントの準備方法](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html#testing-the-secure-testing-service)を参照してください。
エグレス IP は次のとおりです。

| **地域** | **エグレス IP** |
|--- |--- |
| 該当なし | 130.248.160.66、52.151.32.108 |
| EMEA | 185.34.189.1 |
| APAC | 63.140.44.54 |

## Dynamic Media ハイブリッドの設定 {#configure-dm-hybrid-settings}

Experience Managerオーサーインスタンスが Dynamic Media ハイブリッドモードで動作している場合は、 **[!UICONTROL ビデオ]** 管理ツールパネルのタイルで、Dynamic Mediaゲートウェイを設定します。

>[!NOTE]
>
>[ビデオエンコーディングプロファイル](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/video-profiles.html)は Brand Portal には公開されず、代わりに **[!UICONTROL Scene7]** サーバーから取得されます。そのため、ビデオエンコードがBrand Portalで正常に再生されるには、設定の詳細を [Dynamic MediaCloud Services([!DNL Scene7] モード )](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/config-dms7.html?lang=en#configuring-dynamic-media-cloud-services) をExperience Managerオーサーインスタンスに追加します。

Brand Portal テナントで Dynamic Media 設定をセットアップするには：

1. Brand Portalで上部のExperience Managerのツールバーから管理ツールにアクセスできるように、ツールロゴを選択します。
1. 管理ツールパネルで&#x200B;**[!UICONTROL ビデオ]**&#x200B;タイルを選択します。

   ![Brand Portal での Dynamic Media ハイブリッドの設定](assets/DMHybrid-Video.png)

   **[!UICONTROL Dynamic Media 設定を編集]**&#x200B;ページが開きます。

   ![Brand Portal での Dynamic Media ハイブリッドの設定](assets/edit-dynamic-media-config.png)

1. 「**[!UICONTROL 登録 ID]**」と「**[!UICONTROL ビデオサービスの URL]**」（DM ゲートウェイの URL）を指定します。これらの詳細が、 **[!UICONTROL ツール/Cloud Services]** をExperience Managerオーサーインスタンスに追加します。
1. 「**保存**」をクリックして、設定を保存します。

## Dynamic Media Scene7 の設定 {#configure-dm-scene7-settings}

Experience ManagerオーサーインスタンスがDynamic Media上で動作している場合 — **[!UICONTROL Scene7]** モードを選択してから、 **[!UICONTROL Dynamic Media Configuration]** 管理ツールパネルからタイルを作成して設定 **[!UICONTROL Scene7]** サーバー設定。

Brand Portal テナントで Dynamic Media **[!UICONTROL Scene7]** 設定をセットアップするには：

1. Brand Portalで上部のExperience Managerのツールバーから管理ツールにアクセスできるように、ツールロゴを選択します。

2. 管理ツールパネルで **[!UICONTROL Dynamic Media 設定]**&#x200B;タイルを選択します。

   ![Brand Portal での DM [!UICONTROL Scene7] の設定](assets/DMS7-Tile.png)

   **[!UICONTROL Dynamic Media 設定を編集]**&#x200B;ページが開きます。

   ![Brand Portal での Scene7 の設定](assets/S7Config.png)

3. 以下を指定します。

   * **[!UICONTROL タイトル]**
   * Scene7 サーバーにアクセスするための認証情報（**[!UICONTROL 電子メール ID]** と&#x200B;**[!UICONTROL パスワード]**）
   * **[!UICONTROL 地域]**

   これらの値が、Experience Managerオーサーインスタンスで見つかった値と同じであることを確認してください。

4. 「**[!UICONTROL Dynamic Media に接続]**」をクリックします。

5. **[!UICONTROL 会社名]**&#x200B;を指定し、設定を&#x200B;**[!UICONTROL 保存]**&#x200B;します。
