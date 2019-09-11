---
title: ブランドポータルのダウンロード速度の向上
seo-title: ブランドポータルのダウンロード速度の向上
description: Brand Portal および共有リンクからのダウンロードパフォーマンスを強化します。
seo-description: Brand Portal および共有リンクからのダウンロードパフォーマンスを強化します。
uuid: 2871137e-6471-49a7-872a-841bd92543d1
contentOwner: ムムラティ
topic-tags: ダウンロードインストール
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 301f7a0b-5527-4aac- b731- bfc145ped0c0
translation-type: tm+mt
source-git-commit: fb8243ea896d39b324a69ea534271ee3015c076f

---


# ブランドポータルのダウンロード速度の向上 {#guide-to-accelerate-downloads-from-brand-portal}

ブランドポータルでは、インストールオンデマンドアプリケーションであるIBM Avera Connectと統合することで、大きなアセットファイルのダウンロードパフォーマンスを強化できます。アプリケーションは独自のテクノロジーを使用してTCPオーバーヘッドを削除し、アセットファイルの転送速度を向上させます。この統合により、拡張されたダウンロードエクスペリエンスが確保されます。

>[!NOTE]
>
>ダウンロード速度は、ネットワーク帯域幅、サーバー遅延、地理的な場所などの要因によって異なります。

この設定が有効化されている場合、Brand Portal ユーザーは、Aspera Connect クライアントをインストールして、Brand Portal または共有リンクから希望するアセットファイルをダウンロードするのにかかる時間を大幅に短縮できます。

![](assets/enable-fast-file-download.png)

## ファイルのダウンロードを高加速化するための前提条件 {#prerequisites-to-accelerate-file-download}

ファイルをすばやくダウンロードするには、次のことを確認してください。

* **[!UICONTROL 管理ツールパネルの]**[!UICONTROL 一般設定] から、ダウンロードの加速（デフォルトでは無効）を有効にします。
* ポート33001（TCPとUDPの両方）がファイアウォールで開きます。前提条件について詳しくは [、Atla Connect Clientドキュメント](https://downloads.asperasoft.com/en/documentation/8)を参照してください。
* 管理者権限を使用してAtla Connectをインストールします。
* For platform support of Aspera transfer client, see [Aspera Connect platform support matrix](https://www.asperasoft.com/company/support/transfer-clients/).

## ドメインのダウンロード {#download-domains}

様々な地域で利用できるダウンロードドメインを以下に示します。

| 地域コード | ドメイン |
|---|---|
| NA OR1 | downloads-na1.brand-portal.adobe.com |
| NA VA5 | downloads-na2.brand-portal.adobe.com |
| EMEA LON5 | downloads-emea1.brand-portal.adobe.com |
| APAC SIN2 | downloads-apac1.brand-portal.adobe.com |

## Sample download performance using file accelerator {#expected-download-performance-using-file-accelerator}

次の表に、Avera Connectファイルのダウンロードアクセラレーターを使用した2GBのファイルのダウンロードパフォーマンスを示します。

**監視結果は、ネットワーク帯域幅、サーバー待ち時間、クライアントの場所など、ブランドポータルサーバがオレゴン（米国）にあることを考慮して異なります。*

| クライアントの場所 | クライアントとサーバー間の遅延（ミリ秒） | Atla接続ファイル転送アクセラレーター（Mbps）による速度 | Averaファイル転送アクセラレーター（秒）を使用して2GBのファイルをダウンロードする時間 |
|---------------------------|-----------------------------------|---------------------------------------------|-------------------------------------------------------------------------|
| 米国西部（北カリフォルニア） | 18 | 36 | 57 |
| 米国西部（オレゴン） | 42 | 36 | 57 |
| 米国東部（北バージニア） | 85 | 35 | 58 |
| APAC（東京） | 124 | 36 | 57 |
| Noida（India） | 275 | 13.36 | 153 |
| シドニー | 175 | 29 | 70 |
| ロンドン | 179 | 35 | 58 |
| シンガポール | 196 | 34 | 60 |

## ファイルアクセラレーターを使用したダウンロードワークフロー {#download-workflow-using-file-accelerator}

Brand Portal より早くアセットをダウンロードするには：

1. サポートされているブラウザーを使用してブランドポータルにログインします。
2. ダウンロードする目的のアセットファイル、フォルダー、またはコレクションを参照および選択します。ダウンロードオプションをタップまたはクリックします。Download dialog appears with [Enable download acceleration] option selected.
   ![](assets/download-assetsbp.png)

   >[!NOTE]
   >
   >ダウンロードしたアセットをダウンロードするためのリンクとともに電子メール通知を送信する機能は、現在はサポートされていませんが、ダウンロードが有効になっています。

   ![](assets/fast-download-emailchk.png)

3. **[!UICONTROL 「ダウンロード]** 」オプションをタップまたはクリックします。
Brand Portal テナントアカウントでのダウンロードエクスペリエンスを高速化するには、お使いのシステムに Aspera Connect クライアントアプリケーションをインストールする必要があります。

4. **Aspera Connect クライアントをダウンロードします。**
If Aspera Connect client is not installed on your system or the existing installed Aspera Connect client is out of date, a prompt is displayed on browser page from where you can download the system-specific Aspera Connect client by selecting **[!UICONTROL Download Latest Version]**.

   ![](assets/aspera-not-launched.png)

   To download the latest version of Aspera Connect from [https://downloads.asperasoft.com/connect2/](https://downloads.asperasoft.com/connect2/), select **[!UICONTROL Download Now]** and follow the instructions.

5. **Atla Connect Client**をインストールしてIBM
Avera Connectクライアントのセットアップをインストールするには、IBM Avera Connectクライアントアプリケーションの. msiファイルからセットアップを実行し、インストールウィザードに従います。

6. クライアントを正常にインストールしたら、ブラウザーページを更新してダウンロード手順を再開開始するか、アセットの&#x200B;**[!UICONTROL ダウンロード]**&#x200B;ダイアログボックスの「**再起動]」を選択します（手順 2）。[!UICONTROL ** When using Aspera Connect for the first time, the browser prompts to open the link using **[!UICONTROL IBM Aspera Connect]**. To skip this dialog in future, enable **[!UICONTROL Remember my choice for FASP links]**.

   >[!NOTE]
   >
   >実際のメッセージは、ブラウザーによって異なります。

7. 転送を続行するかどうかを確認するダイアログボックスが表示されます。**[!UICONTROL "Allow]** to beginning"を選択します。
To skip this dialog in future, enable **[!UICONTROL Use my choice for all connections with this host]**.
ダウンロードが開始します。ダイアログボックスに、ダウンロードの進行状況が表示されます。Use the dialog box to **[!UICONTROL pause]**, **[!UICONTROL resume]**, or **[!UICONTROL cancel]** the download.
Aspera Connect アプリケーションは、システム上にアクティビティウィンドウを提供します。ユーザーはこのウィンドウからすべての転送セッションを表示および管理することができます。詳しくは、[Aspera Connect Client のドキュメント](https://downloads.asperasoft.com/en/documentation/8)を参照してください。

![](assets/aspera-activity-window.png)

ダウンロードが正常に完了すると、ユーザーのシステムにアセットがダウンロードされる場所がダイアログボックスに表示されます。問題が発生した場合は、エラーが表示されます。

>[!NOTE]
>
>There is a known limitation in Aspera Connect client application that no prompt to select download location appears if **[!UICONTROL Always ask me where to save downloaded files]** is enabled under the tab [!UICONTROL Transfers] within [!UICONTROL Preferences]. Before any download begins, provide the location in the text box **[!UICONTROL Save downloaded files to]**.

## Microsoft Edge ブラウザーでのファイルアクセラレーターの使用 {#using-file-accelerator-on-microsoft-edge-browser}

Microsoft Edge は拡張保護モード（EPM）で実行され、同じプライベートネットワーク上にあるとき、または信頼済みサイトとの通信時に、Aspera Connect サーバーとの通信を防ぎます。そのため、サーバーとの接続を確立するたびにポップアップが表示されます。

![](assets/switchapps-msedge.png)

Microsoft EdgeでAccelerated Download機能を使用するには、信頼できるサイトリストからブランドポータルサイトを削除します。

1. Open the Control Panel (press **[!UICONTROL Window key + X]**, then select **[!UICONTROL Control Panel]**).
2. **[!UICONTROL ネットワークおよびインターネット/インターネットオプションに移動]**&#x200B;します。「**[!UICONTROL セキュリティ]」タブをクリックします。**
3. **[!UICONTROL 信頼できるサイトゾーンをクリック]**&#x200B;し、 **[!UICONTROL 「サイト]**」をクリックします。
4. リストから Brand Portal サイトを削除します。

## Aspera Connect クライアントの環境設定 {#aspera-connect-client-preferences}

There are a few useful preferences which can be set in IBM Aspera Connect Client preference by right clicking the icon and selecting **[!UICONTROL Preferences]**.

![](assets/download_assets_frombrandportalimg19.png)

デフォルトのダウンロード場所を設定できます。

![](assets/aspera-preferences.png)

また、接続クライアントを実行して素早くダウンロードを始められるよう、システム起動時に Aspera Connect クライアントを自動的に開始するようマークすることもできます。

![](assets/aspera-automaticallylaunch.png)

## ダウンロードアクセラレーションに関する問題のトラブルシューティング {#troubleshoot-issues-with-download-acceleration}

ダウンロードのアクセラレーションが機能しない場合は、次の手順に従ってトラブルシューティングしてください。

1. Check that ports are not blocked, by visiting [https://test-connect.asperasoft.com](https://test-connect.asperasoft.com/) from your machine.

   ポートに問題がある場合は、ネットワークチームに連絡して、ポート 33001（TCP と UDP の両方）がファイアウォールでブロックされていないことを確認します。

2. If the ports are OK then check if your network is not slow, by measuring the available bandwidth using [https://www.speedtest.net/](https://www.speedtest.net/).

   帯域幅が少ない（1～10 Mbps）または Kbps 単位の場合、Aspera の環境設定を使用して、利用可能な帯域幅と同じ帯域幅に制限してみてください。

3. To confirm whether the downloads from Aspera demo server are working, use [https://demo.asperasoft.com/aspera/user](https://demo.asperasoft.com/aspera/user).\
   （ログイン:averaweb， password:人口統計体）

4. 上記のトラブルシューティング手順がいずれも機能しない場合は、「ダウンロードアクセラレーションをの有効化」オプションの選択を解除して、通常のダウンロードを使用します。
