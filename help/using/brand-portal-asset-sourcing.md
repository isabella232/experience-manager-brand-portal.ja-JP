---
title: ブランドポータルでのアセットソーシング
seo-title: ブランドポータルでのアセットソーシング
description: Adobe Experience Manager Assets Brand portalでリリースされたアセットソーシング機能に関する洞察を得ます。
seo-description: Adobe Experience Manager Assets Brand portalでリリースされたアセットソーシング機能に関する洞察を得ます。
uuid: null
content-type: reference
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: tm+mt
source-git-commit: 413a6bd17d689d0af0cce20bbd7dedb6ae3cf9b5

---


# アセットソーシングの概要 {#overview-asset-sourcing-in-bp}

**Asset Sourcingを使用すると****** 、AEMユーザー（管理者/非管理者ユーザー）は、追加のアセット貢献度プロパティを使用して新しいフォルダーを作成でき、新しく作成したフォルダーは、Brand portalユーザーがアセット送信を開くことができます。 これにより、新しく作成された貢献度フォルダー内に **SHARED** と **NEW**（共有）という2つの追加のサブフォルダーを作成するワークフローが自動的にトリガ **ーされます** 。 次に、AEM管理者は、貢献度フォルダーに追加する必要のあるアセットのタイプと、ベースラインアセットのセットに関する簡単な情報を **SHARED** フォルダーにアップロードして、BPユーザーが必要な参照情報を確実に取得できるように定義します。 管理者は、新しく作成した貢献度フォルダーをBrand portalに公開する前に、アクティブなBrand portalユーザーに貢献度フォルダーへのアク **セス権を** 付与できます。 ユーザーは、 **NEW** （新規）フォルダーにコンテンツを追加し終えると、貢献度フォルダーをAEMオーサー環境に再度公開できます。 読み込みが完了し、AEM Assets内に新しく公開されたコンテンツが反映されるまでに数分かかる場合があります。

また、既存の機能はすべて変更されません。 Brand portalユーザーは、貢献度フォルダーおよび他の許可されたフォルダーから、アセットを表示、検索およびダウンロードできます。 また、管理者は貢献度フォルダーの共有、プロパティの変更、コレクションへのアセットの追加を行うこともできます。

>[!NOTE]
>
>Brand PortalでのアセットソーシングはAEM 6.5.2.0以降でサポートされています。
>
>この機能は、AEM 6.3およびAEM 6.4の以前のバージョンではサポートされていません。
>
>AEMインスタンスを最新のサポート対象AEMバージョンにアップグレードする場合は、アドビサポートにお問い合わせください。

![](assets/asset-sourcing.png)

## 関連トピック {#reference-articles}

**管理者向け**
* [AEMでのアセットソーシングの設定](brand-portal-enable-asset-sourcing.md)
* [ブランドポータルユーザリストのアップロード](brand-portal-upload-user-list.md)
* [貢献度フォルダーの設定](brand-portal-contribution-folder.md)
* [ベースラインアセットを貢献度フォルダーにアップロード](brand-portal-upload-baseline-assets.md)
* [Brand portalへの貢献度フォルダーの公開](brand-portal-publish-contribution-folder-to-brand-portal.md)

**ブランドポータルユーザー用**
* [アセット要件のダウンロード](brand-portal-download-asset-requirements.md)
* [新しいアセットを貢献度フォルダーにアップロード](brand-portal-upload-assets-to-contribution-folder.md)
* [貢献度フォルダーをAEMアセットに発行](brand-portal-publish-contribution-folder-to-aem-assets.md)
