---
title: Brand Portal でのアセットソーシング
seo-title: Brand Portal でのアセットソーシング
description: Adobe Experience Manager Assets Brand Portal でリリースされたアセットソーシング機能について説明します。
seo-description: Adobe Experience Manager Assets Brand Portal でリリースされたアセットソーシング機能について説明します。
uuid: null
content-type: reference
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: ht
source-git-commit: 413a6bd17d689d0af0cce20bbd7dedb6ae3cf9b5

---


# アセットソーシングの概要 {#overview-asset-sourcing-in-bp}

**アセットソーシング**&#x200B;を使用すると、追加の&#x200B;**アセットコントリビューション**&#x200B;プロパティを持つ新しいフォルダーを AEM ユーザー（管理者／管理者以外のユーザー）が作成できるので、この新規作成フォルダーを Brand Portal ユーザーによるアセット送信に利用することができます。これにより、新しく作成された&#x200B;**コントリビューション**&#x200B;フォルダー内に **SHARED** および **NEW** という 2 つのサブフォルダーを追加作成するワークフローが自動的にトリガーされます。次に、AEM 管理者はプロジェクトの要件を定義します。それには、コントリビューションフォルダーに追加する必要があるアセットのタイプの簡単な説明と一連のベースラインアセットを **SHARED** フォルダーにアップロードして、BP ユーザーが必要な参照情報を確実に入手できるようにします。その後、管理者は、アクティブな Brand Portal ユーザーにコントリビューションフォルダーへのアクセスを許可してから、新しく作成した&#x200B;**コントリビューション**&#x200B;フォルダーを Brand Portal に公開することができます。**NEW** フォルダーへのコンテンツの追加を完了したら、ユーザーは、コントリビューションフォルダーを AEM オーサー環境に公開できます。なお、読み込みが完了し、新しく公開したコンテンツが AEM Assets 内に反映されるまでに数分かかる場合があります。

また、既存の機能はすべてそのままで変わりません。Brand Portal ユーザーは、コントリビューションフォルダーおよび許可された他のフォルダーからアセットを表示、検索およびダウンロードできます。さらに、管理者はコントリビューションフォルダーの共有、プロパティの変更、コレクションへのアセットの追加をおこなうことができます。

>[!NOTE]
>
>Brand Portal のアセットソーシングは、AEM 6.5.2.0 以降でサポートされます。
>
>この機能は、以前のバージョン（AEM 6.3 および AEM 6.4）サポートされません。
>
>AEM インスタンスを最新のサポートされる AEM バージョンにアップグレードするには、アドビサポートにお問い合わせください。

![](assets/asset-sourcing.png)

## 関連トピック {#reference-articles}

**管理者向け**
* [AEM でのアセットソーシングの設定](brand-portal-enable-asset-sourcing.md)
* [Brand Portal ユーザーリストのアップロード](brand-portal-upload-user-list.md)
* [コントリビューションフォルダーの設定](brand-portal-contribution-folder.md)
* [コントリビューションフォルダーへのベースラインアセットのアップロード](brand-portal-upload-baseline-assets.md)
* [Brand Portal へのコントリビューションフォルダーの公開](brand-portal-publish-contribution-folder-to-brand-portal.md)

**Brand Portal ユーザー向け**
* [アセット要件のダウンロード](brand-portal-download-asset-requirements.md)
* [コントリビューションフォルダーへの新しいアセットのアップロード](brand-portal-upload-assets-to-contribution-folder.md)
* [AEM Assets へのコントリビューションフォルダーの公開](brand-portal-publish-contribution-folder-to-aem-assets.md)
