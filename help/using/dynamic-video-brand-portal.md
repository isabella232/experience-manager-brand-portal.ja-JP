---
title: Brand Portal でのダイナミックビデオのサポート
seo-title: Brand Portal でのダイナミックビデオのサポート
description: Brand Portal でのダイナミックビデオのサポート
seo-description: Brand Portal でのダイナミックビデオのサポート
uuid: a3502a4d-3971-4ea4-953c-44ba04446269
contentOwner: ムムラティ
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
content-type: reference
topic-tags: ダウンロードインストール
discoiquuid: e18d992a- a3b5-45f2-9696-8161993213ee
translation-type: tm+mt
source-git-commit: 770c353b1143d879280df310012ce9d4d30b40c9

---


# Brand Portal でのダイナミックビデオのサポート {#dynamic-video-support-on-brand-portal}

Preview and play videos adaptively on [!DNL Brand Portal] with Dynamic Media support. ポータルおよび共有リンクから動的レンディションをダウンロードします。
[!DNL Brand Portal] ユーザーは次のことができます。

* アセットの詳細ページ、カード表示、リンク共有のプレビューページでビデオをプレビューする。
* アセットの詳細ページでビデオエンコードを再生する。
* アセットの詳細ページの「レンディション」タブで動的レンディションを表示する。
* ビデオを格納したフォルダーとビデオエンコードをダウンロードする。

>[!NOTE]
>
>To work with videos and to publish them to [!DNL Brand Portal], make sure that your [!DNL AEM] Author instance is set up either on Dynamic Media Hybrid mode or Dynamic Media [!DNL Scene 7] mode.

To preview, play, and download videos, [!DNL Brand Portal] exposes the following two configurations to administrators:

* [動的メディアハイブリッド設定](#configure-dm-hybrid-settings)[!DNL AEM] （作成者インスタンスがダイナミックメディアハイブリッドモードで実行されている場合）
* [ダイナミックメディア[!DNL Scene7]作成者インスタンス](#configure-dm-scene7-settings)が [!DNL AEM] ダイナミックメディア[!DNL Scene 7] モードで実行されている場合に設定。
Set either of these configurations based on the configurations you set in your [!DNL AEM] Author instance with which [!DNL Brand Portal] tenant is replicated.

>[!NOTE]
>
>Dynamic videos are not supported on [!DNL Brand Portal] tenants integrated with [!DNL AEM] Author running on [!UICONTROL Scene7Connect] runmode.

## How are dynamic videos played? {#how-are-dynamic-videos-played}

![ビデオエンコードはクラウドから取得される](assets/VideoEncodes.png)

If Dynamic Media configurations ([Hybrid](../using/dynamic-video-brand-portal.md#configure-dm-hybrid-settings) or [[!DNL Scene 7]](../using/dynamic-video-brand-portal.md#configure-dm-scene7-settings) configurations) are set up on [!DNL Brand Portal], the dynamic renditions are fetched from [!DNL Scene 7] server. したがって、ビデオエンコードは遅延や品質の劣化なしにプレビューおよび再生されます。

As video encodes are not stored in [!DNL Brand Portal] repository and are fetched from [!DNL Scene 7] server, ensure that the Dynamic Media configurations on [!DNL AEM] Author Instance and [!DNL Brand Portal] are the same.

>[!NOTE]
>
>Video viewers and viewer presets are not supported in [!DNL Brand Portal]. Videos are previewed and played on the default viewers in [!DNL Brand Portal].

## 前提条件 {#prerequisites}

To work with dynamic videos on [!DNL Brand Portal], make sure to:

* **DMで[!DNL AEM]作成者を起動（ダイナミックメディア）モードで**、Dynamic [!DNL AEM][!DNL Brand Portal][Mediaハイブリッドモード](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dynamic.html#EnablingDynamicMedia) または [Dynamic Media[!DNL Scene7]モード](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dms7.html#EnablingDynamicMediainScene7mode)。
* **作成者に[!DNL AEM]よるダイナミックメディアクラウドサービスの作成作成者**&#x200B;が実行中で [!DNL AEM] あることを確認し、 [Dynamic Mediaクラウドサービス](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dynamic.html#ConfiguringDynamicMediaCloudServices) のいずれかまたは [[!ツールから作成者](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dms7.html#ConfiguringDynamicMediaCloudServices) の [!DNL AEM] DNL **Scene7]クラウドサービス** | **クラウドサービス** | **ダイナミックメディア**。
* **ダイナミックメディアの設定（作成者のダイナミックメディアクラウド設定に**&#x200B;基づく [!DNL AEM] ）、 [ダイナミックメディア設定の設定](#configure-dm-hybrid-settings) 、 [[!管理ツール](#configure-dm-scene7-settings) から [!DNL Brand Portal] のDNL Scene7の設定
[必ず個別の[!DNLブランドポータル]テナント](#separate-tenants) は、ダイナミック [!DNL AEM] メディアハイブリッドおよびダイナミックメディアS7の機能を使用している場合に、ダイナミックメディアハイブリッドモードとダイナミックメディア [!UICONTROL Scene7] モードで設定された作成者インスタンスに使用 されます。
* **ブランドポータル**&#x200B;適用 [のビデオエンコーディングに適用されたビデオエンコードを使用してフォルダーを公開](https://helpx.adobe.com/experience-manager/6-5/assets/using/video-profiles.html) し、作成者インスタンスから [!DNL AEM] リッチメディアアセットを含むフォルダーを公開 [!DNL Brand Portal]します。
* **ホワイトリストに登録されている場合、SPSで保護されたプレビュー機能**&#x200B;を有効にして[!DNL Scene 7] いる場合（会社に [セキュアプレビューを有効](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html) にした場合）、 [!DNL Scene 7] 会社管理者 [は、SPS（](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html#testing-the-secure-testing-service)[!UICONTROL Scene7] Publishing System）フラッシュUIを使用して、会社の管理者が各地域に対して公開IPアドレスをホワイトリストに登録することをお勧めします。
 エグレス IP は次のとおりです。

| **地域** | **エグレス IP** |
|--- |--- |
| NA | 192.243.237.86 |
| EMEA | 185.34.189.4 |
| APAC | 63.140.44.54 |

To whitelist either of these egress IPs, see [prepare your account for secure testing service](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html#testing-the-secure-testing-service).

## ベストプラクティス

To ensure that your dynamic video assets are successfully previewed, played, and downloaded from [!DNL Brand Portal] (and shared links), follow these practices:

### ダイナミックメディアハイブリッドモードおよびダイナミックメディアScene7モードのための個別のテナント {#separate-tenants}

ダイナミックメディア [!DNL Scene 7] とダイナミックメディアハイブリッド機能の両方を使用している場合は、ダイナミックメディアのハイブリッドモード [!DNL Brand Portal] とダイナミック [!DNL AEM] メディア [!DNL Scene 7] モードで設定された作成者インスタンスに異なるテナントを使用することをお勧めします。
![オーサーと BP が 1 対 1 に対応](assets/BPDynamicMedia.png)

### AEM作成者インスタンスおよびブランドポータルでの同じ設定の詳細

タイトル、登録ID、ビデオサービスURL（ダイナミックメディアハイブリッド）、タイトル、資格情報（電子メールとパスワード）、地域、会社（ダイナミックメディア [!DNL Scene 7]）などの設定の詳細は、クラウド [!DNL Brand Portal] 設定と [!DNL AEM] 同じです。

### Dynamic Media Scene7モード用のホワイトリストの公開IPモード

Dynamic Media Scene7で保護され [たプレビューを有効にし](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html)てビデオアセットを提供する場合、 [!DNL Brand Portal]Scene7はステージング環境または内部アプリケーション用に専用のImage Serverを確立します。このサーバーへのリクエストはすべて、発信元 IP アドレスをチェックします。受信リクエストが IP アドレスの承認済みリストに含まれていない場合は、失敗のレスポンスが返されます。したがって、Scene7会社管理者は、SPS（Scene-7Publishing System） Flash UI経由で、会社のセキュアテスト環境のIPアドレスの承認されたリストを設定します。該当するそれぞれの地域のエグレス IP（以下を参照）を、その承認済みリストに必ず追加してください。To whitelist either of these egress IPs, see [prepare your account for secure testing service](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html#testing-the-secure-testing-service).
受信者のIPアドレスは次のとおりです。

| **地域** | **エグレス IP** |
|--- |--- |
| NA | 192.243.237.86 |
| EMEA | 185.34.189.4 |
| APAC | 63.140.44.54 |

## Dynamic Media ハイブリッドの設定 {#configure-dm-hybrid-settings}

[!DNL AEM] 作成者インスタンスがダイナミックメディアのハイブリッドモードで実行されている場合は、管理ツールパネルからビデオタイルを使用して、ダイナミックメディアゲートウェイ設定を設定します。
>[!NOTE]
>
>[ビデオエンコーディングプロファイル](https://helpx.adobe.com/experience-manager/6-5/assets/using/video-profiles.html) は、 [!DNL Brand Portal]代わりにScene7サーバから取得されます。Therefore, for video encodes to be played successfully in [!DNL Brand Portal], ensure that the configuration details are the same as the [Scene7 cloud configuration](https://helpx.adobe.com/experience-manager/6-5/assets/using/config-dms7.html#ConfiguringDynamicMediaCloudServices) in your [!DNL AEM] Author instance.
To set up Dynamic Media configurations on [!DNL Brand Portal] tenants:

1. Select the [!DNL AEM] logo to access administrative tools from the toolbar at the top, in [!DNL Brand Portal].

2. From the administrative tools panel, select the **Video** tile.
   ![Brand Portal での Dynamic Media ハイブリッドの設定](assets/DMHybrid-Video.png)
   **ダイナミックメディア設定** ページが開きます。
   ![Brand Portal での Dynamic Media ハイブリッドの設定](assets/edit-dynamic-media-config.png)

3. **登録ID** および **ビデオサービスURL** （DM- Gateway URL）を指定します。Make sure these details are the same as those in **Tools** &gt; **Cloud Services** in your [!DNL AEM] Author instance.

4. 「**保存**」をクリックして、設定を保存します。

## Dynamic Media Scene7 の設定 {#configure-dm-scene7-settings}

[!DNL AEM] 作成者インスタンスがダイナミックメディア- [!UICONTROL Scene7] モードで実行されている場合は、管理ツールパネルから **ダイナミックメディア設定** タイルを使用して [!UICONTROL 、Scene7] サーバの設定を行います。

To set up Dynamic Media [!UICONTROL Scene 7] configurations on [!DNL Brand Portal] tenants:

1. Select the [!DNL AEM] logo to access administrative tools from the toolbar at the top, in [!DNL Brand Portal].

2. From the administrative tools panel, select the **Dynamic Media Configuration** tile.
   ![ダイナミックメディア設定の [!DNL Brand Portal]](assets/DMS7-Tile.png)編集ページのDM Scene7設定が開きます。
   ![Scene7の設定 [!DNL Brand Portal]](assets/S7Config.png)

3. 以下を指定します。
   * タイトル
   * Scene7 サーバーにアクセスするための認証情報（電子メール ID とパスワード）
   * 地域
Make sure these values are the same as those in your [!DNL AEM] Author instance.

4. 「**Dynamic Media に接続**」をクリックします。

5. **会社名**&#x200B;を入力し、設定 **を保存** します。
