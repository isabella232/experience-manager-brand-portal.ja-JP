---
title: リリースノート
seo-title: リリースノート
description: Adobe Experience Manager Assets Brand Portal 6.4.6 リリースの新機能、機能強化、修正された重要な問題および既知の問題について説明します。
seo-description: Adobe Experience Manager Assets Brand Portal 6.4.6 リリースの機能強化、修正された重要な問題および既知の問題について説明します。
uuid: 3d6ffb6f-4608-4e83-8486-5c90e06cdb43
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 79ebb9fc-385c-48a8-979e-374f42517988
translation-type: ht
source-git-commit: 9bb1538165030f7f9e78af99bb89ea38897c3967

---


# リリースノート {#release-notes}

Adobe Experience Manager Assets Brand Portal 6.4.6 リリースの新機能、機能強化、修正された重要な問題および既知の問題について説明します。

## リリース情報 {#release-information}

| 製品 | Adobe Experience Manager Assets Brand Portal |
|---|---|
| バージョン | 6.4.6 |
| 日付 | 2020 年 3 月 |

## 概要 {#overview}

Adobe Experience Manager（AEM）Assets Brand Portal では、承認されたクリエイティブアセットを容易に取得、制御し、それらのアセットを、デバイスの種類を問わず、外部の関係者や内部のビジネスユーザーに安全に配布できます。アセットの共有を効率化し、アセットの市場投入までの時間を短縮し、コンプライアンス違反や不正アクセスのリスクを低減できます。Brand Portal では、アセットの参照、検索、プレビュー、ダウンロードおよび会社で承認された形式での書き出しを、いつでも、どこでも実行できます。

## 6.4.6 の新機能 {#what-s-new-in-646}

### 新機能 {#new-feature}

このリリースには、次の新機能が含まれています。

* Captcha を使用して Brand Portal にゲストとしてログインする。詳しくは、[Brand Portal へのゲストによるアクセス](../using/guest-access.md)を参照してください。

* AEM Assets Cloud Service で Brand Portal がサポートされるようになりました。AEM Assets が Brand Portal でサービスできるように設定して、Brand Portal ユーザーとアセットを共有および配布できます。
詳しくは、[AEM Assets Cloud Service と Brand Portal の設定](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html)を参照してください。

### 機能強化 {#enhancements-646}

このリリースの Brand Portal で強化された機能は次のとおりです。

* AEM 6.3 以降では、AEM Assets と Brand Portal の間の認証チャネルが変更されます。AEM Assets と Brand Portal の連携が、Adobe I/O を通じて設定されるようになりました。Adobe I/O が Brand Portal テナントの認証用の IMS トークンを取得します。

   >[!NOTE]
   >
   >旧来の OAuth を使用した設定は、2020 年 4 月 6 日以降はサポートされなくなり、Adobe I/O を使用した設定に変更されます。


>[!TIP]
>
>***既存のお客様のみ***
>
>既存のレガシー OAuth Gateway 設定を引き続き使用することをお勧めします。レガシー OAuth Gateway 設定に問題が発生した場合は、既存の設定を削除し、Adobe I/O から新しい設定を作成します。


詳しくは、[AEM Assets と Brand Portal の連携の設定](configure-aem-assets-with-brand-portal.md)を参照してください

### 修正された重要な問題 {#critical-issues-fixed}

このリリースでは、次の重要な問題が修正されています。

* メタデータスキーマのドロップダウン値が、アセットプロパティに表示されない。

* メタデータサブスキーマに、アセットプロパティの MIME タイプに基づくタブが表示されない。

* 非公開メタデータスキーマが、バックエンドでスキーマが削除されてもエラーメッセージを入力する。

* 公開済みアセットのプレビュー画像が表示されない。

* 名前に一重引用符が含まれているアセットを公開または非公開にできない。

* 複数アセットのダウンロード中に利用条件が表示されない。

* セキュリティに関する小さな脆弱性を解消。

### 既知の問題 {#known-issues}

このリリースには、次の既知の問題が含まれています。

* Brand Portal ユーザーが AEM 6.5.4 の Adobe I/O にアップグレードする際に、投稿フォルダーのアセットを AEM Assets に公開できない。

   この問題は、次のサービスパック 6.5.5 で修正されます。

   AEM 6.5.4 の即時修正をおこなうには、[ホットフィックスをダウンロード](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041)して、オーサーインスタンスにインストールすることをお勧めします。

* アセットのダウンロード中に、「システムレンディションを除く」オプションが正常に機能しない。


## 言語 {#languages}

Brand Portal ユーザーインターフェイスは次の言語で使用できます。

* 英語
* ドイツ語
* フランス語
* スペイン語
* イタリア語
* ブラジル語ポルトガル語
* 日本語
* 簡体字中国語
* 韓国語

## 認定プラットフォーム{#certified-platforms}

このリリースの Brand Portal を実行できる認定プラットフォームを確認するには、[技術要件](https://helpx.adobe.com/jp/experience-manager/6-4/sites/deploying/using/technical-requirements.html)の「**オーサリングユーザーインターフェイス向けにサポートされているブラウザー**」節に記載されている表の「**UI のサポート**」列を参照してください。

## リンク {#links}

* [Adobe Experience Manager 製品ページ（adobe.com）](http://www.adobe.com/jp/marketing-cloud/experience-manager.html)
* [Assets Brand Portal のドキュメント](https://helpx.adobe.com/jp/experience-manager/brand-portal/user-guide.html)

## 製品のアクセスとサポート（制限付きサイト）{#product-access-and-support-restricted-sites}

以下のサイトは既存ユーザーのみが参照できます。アクセス権を必要とするお客様は、アドビのアカウントマネージャーにご連絡ください。

* [https://daycare.day.com](https://daycare.day.com)

* [製品へのアクセス](https://login.marketing.adobe.com)

* [アドビカスタマーケア](https://helpx.adobe.com/jp/contact.html)
