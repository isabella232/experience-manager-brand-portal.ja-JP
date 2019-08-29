---
title: Brand Portal からのダウンロードを高速化するためのガイド
seo-title: Brand Portal からのダウンロードを高速化するためのガイド
description: Brand Portal および共有リンクからのダウンロードパフォーマンスを強化します。
seo-description: Brand Portal および共有リンクからのダウンロードパフォーマンスを強化します。
uuid: 2871137e-6471-49a7-872a-841bd92543d1
contentOwner: ムムラティ
topic-tags: ダウンロードインストール
content-type: reference
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
discoiquuid: 301f7a0b-5527-4aac- b731- bfc145ped0c0
translation-type: tm+mt
source-git-commit: 770c353b1143d879280df310012ce9d4d30b40c9

---


# Brand Portal からのダウンロードを高速化するためのガイド {#guide-to-accelerate-downloads-from-brand-portal}

ブランドポータルは、インストールオンデマンドアプリケーションであるIBM Avera Connectと統合して、大規模なアセットファイルの高速ダウンロードをサポートしています。このアプリケーションは TCP オーバーヘッドをなくす独自のテクノロジーを使用しており、ファイルの転送速度を向上させ、快適なダウンロードエクスペリエンスを実現します。地理的に離れた場所にいて長い待ち時間を経験しているユーザーも、この機能の恩恵を受けることができます。

>[!NOTE]
>
>IBM Aspera Connect を使用すると、Brand Portal および共有リンクから大きなアセットファイルをすばやくダウンロードすることができます（ダウンロード速度は、ネットワーク帯域幅や、サーバーのレイテンシ、クライアントの地理的な場所などの要因に応じて異なります）。

To configure specific tenants for accelerated file download, administrators **[!UICONTROL Enable Download Acceleration]** (which is disabled by default)from **General Settings** in the administrative tools panel.

この設定が有効化されている場合、Brand Portal ユーザーは、Aspera Connect クライアントをインストールして、Brand Portal または共有リンクから希望するアセットファイルをダウンロードするのにかかる時間を大幅に短縮できます。

![](assets/enable-fast-file-download.png)

## ファイルのダウンロードを高加速化するための前提条件 {#prerequisites-to-accelerate-file-download}

ファイルのダウンロード機能を高速化するには、次のようにします。

* 管理者がファイアウォールのポート 33001（TCP と UDP の両方）を開放解放している。For more information on the prerequisites to using IBM Aspera Connect, see [Aspera Connect Client documentation](https://downloads.asperasoft.com/en/documentation/8).

   様々な地域で利用できるダウンロードドメインを以下に示します。

   | 地域 | ドメイン |
   |---|---|
   | NA OR1 | downloads-na1.brand-portal.adobe.com |
   | NA VA5 | downloads-na2.brand-portal.adobe.com |
   | EMEA LON5 | downloads-emea1.brand-portal.adobe.com |
   | APAC SIN2 | downloads-apac1.brand-portal.adobe.com |

* IBM Aspera Connect のインストーラーパッケージをダウンロードするには、管理者権限を使用します。Aspera Connect をゲストアカウントでインストールすることはできません。

### システムとブラウザーの要件 {#system-and-browser-requirements}

Aspera Connect 3.8.0 のシステムおよびブラウザー要件は次のとおりです。

| ﻿OS | OS バージョン | ブラウザー |  | 必須ライブラリ |
|----------------|----------------------------------------|-------------------|-------|--------------------------|
| Windows | Windows 7、8、10 | Chrome | 64 ～ 66 |  |
|  | Windows Server 2008、R2、2012 R2、2016 | Firefox 以降 | 57 ～ 60 |  |
|  |  | Firefox ESR | 52 |  |
|  |  | Internet Explorer | 11 |  |
|  |  | Microsoft Edge | 39 ～ 42 |  |
| MacOS | 10.11 ～ 10.13 | Chrome | 64 ～ 66 |  |
|  |  | Firefox 以降 | 57 ～ 60 |  |
|  |  | Firefox ESR | 52 |  |
|  |  | Safari | 11 |  |
| Linux（64 ビット） | RHEL 6 ～ 7 | Chrome | 64 ～ 66 | OpenSSL 1.0.2g 以降 |
|  | CentOS 6 ～ 7 |  |  | Mesa EGL |
|  | Debian 7 ～ 9 |  |  | glib2 2.28 以降 |
|  | SLES 11 ～ 12 |  |  |  |
|  | Fedora 26 ～ 27 |  |  |  |
|  | OpenSUSE 42.3 | Firefox 以降 | 57 ～ 60 |  |
|  | Ubuntu 14 ～ 17 | Firefox ESR | 52 |  |

様々なバージョンの Aspera 転送クライアントのプラットフォームサポート一覧表については、[Aspera Connect プラットフォームサポート一覧表](https://www.asperasoft.com/company/support/transfer-clients/)を参照してください。

## ファイルアクセラレーターの使用によって想定されるダウンロードパフォーマンス {#expected-download-performance-using-file-accelerator}

様々なクライアント場所におけるAvera Connectファイルのダウンロードアクセラレーターを使用して、2GBのファイルに対して予想されるダウンロードパフォーマンスは、次のとおりです。例えば、米国のオレゴンのブランドポータルサーバーを考えます。

| クライアントの場所 | クライアントとサーバー間の遅延 | Aspera File Transfer Accelerator を使用した場合の速度 | Averaファイル転送アクセラレーターを使用して2GBのファイルのダウンロードに要した時間 |
|---------------------------|-----------------------------------|---------------------------------------------|-------------------------------------------------------------------------|
| 米国西部（北カリフォルニア） | 18 ミリ秒 | 36 MB/秒 | 57 秒 |
| 米国西部（オレゴン） | 42 ミリ秒 | 36 MB/秒 | 57 秒 |
| 米国東部（北バージニア） | 85 ミリ秒 | 35 MB/秒 | 58 秒 |
| APAC（東京） | 124 ミリ秒 | 36 MB/秒 | 57 秒 |
| ノイダ | 275 ミリ秒 | 13.36 MB/秒 | 153 秒 |
| シドニー | 175 ミリ秒 | 29 MB/秒 | 70 秒 |
| ロンドン | 179 ミリ秒 | 35 MB/秒 | 58 秒 |
| シンガポール | 196 ミリ秒 | 34 MB/秒 | 60 秒 |

>[!NOTE]
>
>メンションされたデータは、ラボで実行されたテストに従い、表示されます。監視結果は、ネットワーク帯域幅、サーバー遅延、クライアントの場所などの要因によって異なります。

## ファイルアクセラレーターを使用したダウンロードワークフロー {#download-workflow-using-file-accelerator}

Brand Portal より早くアセットをダウンロードするには：

1. お好きなブラウザーから Brand Portal にログインします。
2. ダウンロードする目的のアセットファイル、フォルダー、またはコレクションを参照および選択します。ダウンロードオプションをタップまたはクリックします。Download dialog appears with [Enable download acceleration] option selected.
   ![](assets/download-assetsbp.png)

   >[!NOTE]
   >
   >ダウンロードしたアセットをダウンロードするためのリンクとともに電子メール通知を送信する機能は、現在はサポートされていませんが、ダウンロードが有効になっています。

   ![](assets/fast-download-emailchk.png)

3. **「ダウンロード**」をタップまたはクリックします。
Brand Portal テナントアカウントでのダウンロードエクスペリエンスを高速化するには、お使いのシステムに Aspera Connect クライアントアプリケーションをインストールする必要があります。

4. **Aspera Connect クライアントをダウンロードします。**&#x200B;お使いのシステムに Aspera Connect クライアントがインストールされていない場合や、インストールされている既存の Aspera Connect クライアントが古い場合は、ブラウザーページに表示されるメッセージから「**最新バージョンのダウンロード**」を選択してシステム固有の Aspera Connect をダウンロードします。

   ![](assets/aspera-not-launched.png)

   To download the latest version of Aspera Connect from [https://downloads.asperasoft.com/connect2/](https://downloads.asperasoft.com/connect2/), select **Download Now** and follow the instructions.

5. **Atla Connect Client**をインストールしてIBM
Avera Connectクライアントのセットアップをインストールするには、IBM Avera Connectクライアントアプリケーションの. msiファイルからセットアップを実行し、インストールウィザードに従います。

6. クライアントを正常にインストールしたら、ブラウザーページを更新してダウンロード手順を再開開始するか、アセットの&#x200B;**ダウンロード**&#x200B;ダイアログボックスの「**再起動**」を選択します（手順 2）。When using Aspera Connect for the first time, the browser prompts to open the link using **IBM Aspera Connect**. To skip this dialog in future, enable **Remember my choice for FASP links**.

   >[!NOTE]
   >
   >実際のメッセージは、ブラウザーによって異なります。

7. 転送を続行するかどうかを確認するダイアログボックスが表示されます。**"Allow** to beginning"を選択します。
To skip this dialog in future, enable **Use my choice for all connections with this host**.
ダウンロードが開始します。ダイアログボックスに、ダウンロードの進行状況が表示されます。Use the dialog box to **pause**, **resume**, or **cancel** the download.
Aspera Connect アプリケーションは、システム上にアクティビティウィンドウを提供します。ユーザーはこのウィンドウからすべての転送セッションを表示および管理することができます。詳しくは、[Aspera Connect Client のドキュメント](https://downloads.asperasoft.com/en/documentation/8)を参照してください。

![](assets/aspera-activity-window.png)

ダウンロードが正常に完了すると、ユーザーのシステムにアセットがダウンロードされる場所がダイアログボックスに表示されます。問題が発生した場合は、エラーが表示されます。

>[!NOTE]
>
>There is a known limitation in Aspera Connect client application that no prompt to select download location appears if **Always ask me where to save downloaded files** is enabled under the tab **Transfers **within **Preferences**. Before any download begins, provide the location in the text box **Save downloaded files to**.

## Microsoft Edge ブラウザーでのファイルアクセラレーターの使用 {#using-file-accelerator-on-microsoft-edge-browser}

Microsoft Edge は拡張保護モード（EPM）で実行され、同じプライベートネットワーク上にあるとき、または信頼済みサイトとの通信時に、Aspera Connect サーバーとの通信を防ぎます。そのため、サーバーとの接続を確立するたびにポップアップが表示されます。

![](assets/switchapps-msedge.png)

Microsoft EdgeでAccelerated Download機能を使用するには、信頼できるサイトリストからブランドポータルサイトを削除します。

1. Open the Control Panel (press **Window key + X**, then select **Control Panel**).
2. **ネットワークとインターネット／インターネットオプション**&#x200B;に移動します。「**セキュリティ**」タブをクリックします。
3. **信頼済みサイトゾーン**、**サイト**&#x200B;の順にクリックします。
4. リストから Brand Portal サイトを削除します。

## Aspera Connect クライアントの環境設定 {#aspera-connect-client-preferences}

アイコンを右クリックし、「**環境設定**」を選択して IBM Aspara Connect クライアント環境設定で指定できる、便利な環境設定がいくつかあります。

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
