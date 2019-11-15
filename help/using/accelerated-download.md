---
title: Brand Portal のダウンロードの高速化
seo-title: Brand Portal のダウンロードの高速化
description: Brand Portal および共有リンクからのダウンロードパフォーマンスを強化します。
seo-description: Brand Portal および共有リンクからのダウンロードパフォーマンスを強化します。
uuid: 2871137e-6471-49a7-872a-841bd92543d1
contentOwner: mgulati
topic-tags: download-install
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 301f7a0b-5527-4aac-b731-bfc145fed0c0
translation-type: ht
source-git-commit: 5a4d31622a5dee95045ee377e07c0c53f982aad3

---


# Brand Portal のダウンロードの高速化 {#guide-to-accelerate-downloads-from-brand-portal}

Brand Portal では、インストールオンデマンドアプリケーションである IBM Aspera Connect との連携により、大きなアセットファイルのダウンロードパフォーマンスを強化できます。このアプリケーションは、TCP オーバーヘッドをなくす独自のテクノロジーを使用し、アセットファイルの転送速度を向上させます。この連携により、ダウンロードエクスペリエンスを確実に強化できます。

>[!NOTE]
>
>ダウンロード速度は、ネットワーク帯域幅、サーバーのレイテンシ、クライアントの所在地などの要因によって異なるので、ユーザーごとに異なります。

この設定が有効化されている場合、Brand Portal ユーザーは、Aspera Connect クライアントをインストールして、Brand Portal または共有リンクから希望するアセットファイルをダウンロードするのにかかる時間を大幅に短縮できます。

![](assets/enable-fast-file-download.png)

## ファイルのダウンロードを高加速化するための前提条件{#prerequisites-to-accelerate-file-download}

ファイルのダウンロードを高速化するには、必ず以下をおこないます。

* 管理ツールパネルの[!UICONTROL 一般設定]で「**[!UICONTROL ダウンロードアクセラレーションを有効化]**」をオンにします（デフォルトでは無効になっています）。
* ファイアウォールのポート 33001（TCP と UDP の両方）を開きます。前提条件について詳しくは、[Aspera Connect Client のドキュメント](https://downloads.asperasoft.com/en/documentation/8)を参照してください。
* 管理者権限を使用して Aspera Connect をインストールします。
* Aspera 転送クライアントのプラットフォームサポートについては、[Aspera Connect プラットフォームサポート一覧表](https://www.asperasoft.com/company/support/transfer-clients/)/を参照してください。

## ダウンロードドメイン {#download-domains}

様々な地域で利用できるダウンロードドメインを以下に示します。

| 地域コード | ドメイン |
|---|---|
| NA OR1 | downloads-na1.brand-portal.adobe.com |
| NA VA5 | downloads-na2.brand-portal.adobe.com |
| EMEA LON5 | downloads-emea1.brand-portal.adobe.com |
| APAC SIN2 | downloads-apac1.brand-portal.adobe.com |

## ファイルアクセラレーターを使用した場合のダウンロードパフォーマンス例 {#expected-download-performance-using-file-accelerator}

ファイルダウンロードアクセラレーター Aspera Connect を使用した場合の 2 GB ファイルのダウンロードパフォーマンスを次の表に示します。

**Brand Portal サーバーがオレゴン州（米国）にあることを考慮すると、ネットワーク帯域幅、サーバーのレイテンシ、クライアントの所在地などの要因によって測定結果は異なります。*

| クライアントの場所 | クライアントとサーバーの間のレイテンシ（ミリ秒） | Aspera Connect ファイル転送アクセラレーターを使用した場合の速度（MBps） | Aspera ファイル転送アクセラレーターを使用した場合の 2 GB ファイルのダウンロード所要時間（秒） |
|---------------------------|-----------------------------------|---------------------------------------------|-------------------------------------------------------------------------|
| 米国西部（北カリフォルニア） | 18 | 36 | 57 |
| 米国西部（オレゴン） | 42 | 36 | 57 |
| 米国東部（北バージニア） | 85 | 35 | 58 |
| APAC（東京） | 124 | 36 | 57 |
| ノイダ（インド） | 275 | 13.36 | 153 |
| シドニー | 175 | 29 | 70 |
| ロンドン | 179 | 35 | 58 |
| シンガポール | 196 | 34 | 60 |

## ファイルアクセラレーターを使用したダウンロードワークフロー {#download-workflow-using-file-accelerator}

Brand Portal より早くアセットをダウンロードするには：

1. サポートされているブラウザーを使用して Brand Portal にログインします。
1. ダウンロードする目的のアセットファイル、フォルダー、またはコレクションを参照および選択します。ダウンロードオプションをタップまたはクリックします。「[ダウンロードアクセラレーションを有効化]」オプションが選択されたダウンロードダイアログが表示されます。
   ![](assets/download-assetsbp.png)

   >[!NOTE]
   >
   >高速ダウンロードが有効になっているときに、アセットをダウンロードするためのリンクが入った電子メールを送信する機能は、現在サポートされていません。

   ![](assets/fast-download-emailchk.png)

1. 「**[!UICONTROL ダウンロード]**」オプションをタップまたはクリックします。Brand Portal テナントアカウントでのダウンロードエクスペリエンスを高速化するには、お使いのシステムに Aspera Connect クライアントアプリケーションをインストールする必要があります。

1. **Aspera Connect クライアントをダウンロードします。**
お使いのシステムに Aspera Connect クライアントがインストールされていない場合や、インストールされている既存の Aspera Connect クライアントが古い場合は、ブラウザーページに表示されるメッセージから「**[!UICONTROL 最新バージョンのダウンロード]**」を選択してシステム固有の Aspera Connect をダウンロードします。

   ![](assets/aspera-not-launched.png)

   最新バージョンの Aspera Connect を [https://downloads.asperasoft.com/connect2/](https://downloads.asperasoft.com/connect2/) からダウンロードするには、「**[!UICONTROL 今すぐダウンロード]**」をクリックして画面の指示に従います。

1. **Aspera Connect クライアントのインストール**
IBM Aspera Connect クライアントセットアップをインストールするには、IBM Aspera Connect クライアントアプリケーションの .msi ファイルからセットアップを実行し、インストールウィザードに従います。

1. クライアントを正常にインストールしたら、ブラウザーページを更新してダウンロード手順を再開するか、アセットの&#x200B;**[!UICONTROL ダウンロード]**&#x200B;ダイアログボックスの「**[!UICONTROL 再起動]**」を選択します（手順 2）。Aspera Connect を初めて使用する場合、ブラウザーには、**[!UICONTROL IBM Aspera Connect]** を使用してリンクを開くように促すメッセージが表示されます。今後このダイアログをスキップするには、「**[!UICONTROL Remember my choice for FASP links]**」を有効にします。

   >[!NOTE]
   >
   >実際のメッセージは、ブラウザーによって異なります。

1. 転送を続けるかどうかを確認するダイアログボックスが表示されます。「**[!UICONTROL Allow]**」を選択して開始します。
今後このダイアログをスキップするには、「**[!UICONTROL Use my choice for all connections with this host]**」を有効にします。ダウンロードが開始します。ダイアログボックスに、ダウンロードの進行状況が表示されます。このダイアログボックスを使用すると、ダウンロードの&#x200B;**[!UICONTROL 一時停止]**、**[!UICONTROL 再開]**、**[!UICONTROL キャンセル]**をおこなえます。
Aspera Connect アプリケーションは、システム上にアクティビティウィンドウを提供します。ユーザーはこのウィンドウからすべての転送セッションを表示および管理することができます。詳しくは、[Aspera Connect Client のドキュメント](https://downloads.asperasoft.com/en/documentation/8)を参照してください。

![](assets/aspera-activity-window.png)

ダウンロードが正常に完了すると、ユーザーのシステム上にある、アセットのダウンロード先がダイアログボックスに表示されます。問題が発生した場合は、エラーが表示されます。

>[!NOTE]
>
>Aspera Connect クライアントアプリケーションには、[!UICONTROL 設定]の「[!UICONTROL 転送]」タブで「**[!UICONTROL ダウンロードしたファイルの保存先を毎回確認する]**」が有効になっている場合、ダウンロード場所を選択するプロンプトが表示されないという既知の制限があります。ダウンロードを開始する前に、「**[!UICONTROL ダウンロードしたファイルを以下の場所に保存する]**」テキストボックスに場所を指定してください。

## Microsoft Edge ブラウザーでのファイルアクセラレーターの使用 {#using-file-accelerator-on-microsoft-edge-browser}

Microsoft Edge は拡張保護モード（EPM）で実行され、同じプライベートネットワーク上にあるとき、または信頼済みサイトとの通信時に、Aspera Connect サーバーとの通信を防ぎます。そのため、サーバーとの接続を確立するたびにポップアップが表示されます。

![](assets/switchapps-msedge.png)

Microsoft Edge で高速ダウンロード機能を使用するには、信頼済みサイトのリストゾーンから Brand Portal サイトを削除します。

1. コントロールパネルを開きます（**[!UICONTROL Windows キー + X]** を押して「**[!UICONTROL コントロールパネル]**」を選択します）。
1. **[!UICONTROL ネットワークとインターネット／インターネットオプション]**&#x200B;に移動します。「**[!UICONTROL セキュリティ]**」タブをクリックします。
1. **[!UICONTROL 信頼済みサイトゾーン]**、**[!UICONTROL サイト]**&#x200B;の順にクリックします。
1. リストから Brand Portal サイトを削除します。

## Aspera Connect クライアントの環境設定{#aspera-connect-client-preferences}

アイコンを右クリックし、「**[!UICONTROL 設定]**」を選択すると、IBM Aspera Connect クライアント環境設定で指定できる、便利な環境設定がいくつかあります。

![](assets/download_assets_frombrandportalimg19.png)

デフォルトのダウンロード場所を設定できます。

![](assets/aspera-preferences.png)

また、接続クライアントを実行して素早くダウンロードを始められるよう、システム起動時に Aspera Connect クライアントを自動的に開始するようマークすることもできます。

![](assets/aspera-automaticallylaunch.png)

## ダウンロードアクセラレーションに関する問題のトラブルシューティング{#troubleshoot-issues-with-download-acceleration}

ダウンロードアクセラレーションが機能しない場合は、次の手順に従ってトラブルシューティングをおこなってください。

1. お使いのコンピューターから [https://test-connect.asperasoft.com/](https://test-connect.asperasoft.com/) にアクセスして、そのポートがブロックされていないことを確認します。

   ポートに問題がある場合は、ネットワークチームに連絡して、ポート 33001（TCP と UDP の両方）がファイアウォールでブロックされていないことを確認します。

1. ポートに問題がない場合は、[/](https://www.speedtest.net/)https://www.speedtest.net/ を使用して使用可能な帯域幅を測定し、ネットワークが低速になっていないかどうかを確認します。

   帯域幅が少ない（1～10 Mbps）または Kbps 単位の場合、Aspera の環境設定を使用して、利用可能な帯域幅と同じ帯域幅に制限してみてください。

1. Aspera デモサーバーからのダウンロードが機能しているかどうかを確認するには、[](https://demo.asperasoft.com/aspera/user)https://demo.asperasoft.com/aspera/user を使用します。\
   （ログイン名：asperaweb、パスワード：demoaspera）

1. 上記のトラブルシューティング手順がいずれも機能しない場合は、「ダウンロードアクセラレーションを有効化」オプションの選択を解除して、通常のダウンロードを使用します。
