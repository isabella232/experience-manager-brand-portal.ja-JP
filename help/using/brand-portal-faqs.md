---
title: よくある質問
seo-title: null
description: Adobe Experience Manager Assets Brand Portal でのよくある質問について説明します。
seo-description: null
uuid: null
content-type: reference
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: tm+mt
source-git-commit: b8e252140a8e77595489682e69da8c86284a28d1

---


# よくある質問 {#frequently-asked-questions}

Brand Portal FAQ では、最新の AEM Assets Brand Portal 6.4.5 リリース以前のバージョンで作業中に発生する可能性のあるエンドユーザー向けのクエリと問題に焦点を当てています。


## Brand Portal 6.4.6に関するFAQ {#faqs-bp646}

**質問：既存のレガシーOAuthエンドポイント(`https://legacy-oauth.cloud.adobe.io/login`)が機能していません。 考えられる理由は何でしょう？**

**回答：** 従来のOAuth設定は非推奨です。 AEM Assetsの作成者インスタンスを最新のサービスパックにアップグレードし、Adobe IOを使用して設定する必要があります。 See [Configure AEM Assets with Brand Portal](configure-aem-assets-with-brand-portal.md) for details. ただし、アップグレードするまでレガシーOAuth設定が機能するようにするには、レガシーOAuthエンドポイントをに更新しま `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/`す。

**質問：Adobe I/Oにアップグレードした後、貢献度フォルダーのアセットをBrand PortalからAEM Assetsに公開できません。作成者インスタンスがAEM 6.5.4にある。考えられる理由は何でしょう？**

**回答：** はい、Adobe I/Oを使用してAEM 6.5.4上のAEM Assetsにコントリビューションフォルダーのアセットを公開する際に、既知の問題が発生しました。この問題は、次のサービスパックAEM 6.5.5で修正されます。

AEM 6.5.4の即時修正を行うには、ホットフィックスをダウンロードし [て](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041) 、AEMオーサーインスタンスにインストールすることをお勧めします。


## Brand Portal 6.4.5 FAQ {#faqs-bp645}

**質問：Brand Portal 6.4.5 リリースの主な変更点は何ですか。**

**回答：**AEM Assets Brand Portal 6.4.5 は、Brand Portal ユーザーが管理者権限を必要としないで Brand Portal インスタンス内のコンテンツをアップロードし、投稿フォルダーを AEM Assets に公開できる機能リリースです。
詳しくは、[Brand Portal でのアセットソーシング](brand-portal-asset-sourcing.md)を参照してください。



**質問：私が作成した既存のアセット、機能または設定へのアクセス権は失われますか。**

**回答：**&#x200B;既存の機能と設定はすべてそのまま残ります。エンド-ユーザーに影響はなく、コンテンツはそのまま残ります。



**質問：新しいバージョンの Brand Portal にはいつ移行しますか。**

**回答：** Brand Portal 6.4.5 は、2019 年 10 月に実稼動環境へリリースされました。Brand Portal の次期バージョンは、2020 年の第 3 四半期にリリース予定です。アップデートとバージョンの変更については、Brand Portal の[リリースノート](brand-portal-release-notes.md)と [Brand Portal の新機能](whats-new.md)を確認することをお勧めします。



**質問：私が管理しているユーザーに影響しますか。**

**回答：** Brand Portal 6.4.5 リリースは完全に Brand Portal 内にとどまるため、エンドユーザーには影響しません。



**質問：Brand Portal ユーザーとして必要なアクションはありますか。**

**回答：** Brand Portal 6.4.5 リリースには、「アセットソーシング」という新機能が含まれています。AEM 管理者は、AEM Assets でアセットソーシング機能を設定し、Brand Portal ユーザーに対して有効にする必要があります。詳しくは、「[アセットソーシングの有効化](brand-portal-configure-asset-sourcing.md)」を参照してください。



**質問：投稿フォルダーは誰が作成できますか。**

**回答：** AEM Assets に新しいフォルダーを作成する権限を持つ AEM ユーザーであれば、誰でも&#x200B;**投稿**&#x200B;フォルダーを作成できます。**投稿**&#x200B;フォルダーを作成するには、**アセット投稿**&#x200B;タイプの新しいフォルダーを作成します。このフォルダーは、投稿用として、アクティブな Brand Portal ユーザーと共有されます。



**質問：投稿フォルダーには何が含まれますか。**

**回答：****投稿**&#x200B;フォルダーには、**NEW** と **SHARED** の 2 つのサブフォルダーが含まれます。始めは、NEW フォルダーは空で、SHARED フォルダーには Brand Portal ユーザーの参照コンテンツ（再利用可能なアセット）が含まれます。
Brand Portal ユーザーは**投稿**&#x200B;フォルダーにアクセスし、**NEW** フォルダーにコンテンツをアップロードします。



**質問：既存の投稿フォルダーの名前を変更できますか。**

**回答：****いいえ**、既存の&#x200B;**投稿**&#x200B;フォルダーの名前を変更することはできません。



**質問：投稿に関するアセットの要件とは何ですか。**

**回答：****投稿**&#x200B;フォルダーに添付された&#x200B;**概要**&#x200B;ドキュメント、および&#x200B;**SHARED** フォルダーにアップロードされた参照コンテンツ（再利用可能なアセット）は、Brand Portal ユーザーが投稿の必要性と寄稿者に期待されること（総称して「アセット要件」と呼びます）を理解するのに役立ちます。



**質問：アセットは許可されているすべてのフォルダーにアップロードできますか。**

**回答：**&#x200B;いいえ。アップロードできないフォルダーもあります。Brand Portal ユーザーは、AEM または Brand Portal 管理者が共有する&#x200B;**投稿**&#x200B;フォルダーにのみコンテンツをアップロードできます。



**質問：投稿フォルダーにアクセスする方法を教えてください。**

**回答：****投稿**&#x200B;フォルダーには、自分と共有されている場合にアクセスすることができます。投稿フォルダーが共有されるたびに、電子メール／パルス通知が送信されます。電子メールで共有されたリンクを介して投稿フォルダーにアクセスするか、Brand Portal インスタンスにログインしてベルのアイコンに移動し、投稿フォルダーにアクセスする通知を受け取ることができます。

>[!NOTE]
>
>既存の Brand Portal ユーザーでない場合は、AEM 管理コンソールでユーザーを作成して Brand Portal ユーザーリストのユーザー設定ファイルにプロファイルを追加するように AEM 管理者に依頼します。「[Brand Portal ユーザーの追加](brand-portal-configure-asset-sourcing.md)」を参照してください。



**質問：ユーザー読み込み用の CSV ファイルの形式は何ですか。**

**回答：** 管理コンソールでの一括ユーザー読み込みでサポートされている形式と同じです。電子メールと氏名は必須です。



**質問：「アセット投稿」ユーザードロップダウンのユーザー（Brand Portal 寄稿者）のリストに入力される項目を教えてください。**

**回答：**&#x200B;ドロップダウンのユーザーは、AEM にアップロードされた Brand Portal のユーザー設定（.csv）ファイルから入力されます。



**質問：読み込みジョブと公開ジョブのステータスはどこで確認できますか。**

**回答：** AEM では、読み込みの状態を&#x200B;**非同期**&#x200B;ジョブページで確認できます。Brand Portal では、**[!UICONTROL ツール／アセット投稿のステータス]**&#x200B;で公開ジョブのステータスを確認できます。



**質問：AEM で定期的に実行される読み込みジョブの頻度はどれくらいですか。**

**回答：** AEMでは、ポーリングは 5 分ごとに実行されます。



**質問：Brand Portal から AEM Assets にフォルダーを公開できる回数にしきい値はありますか。**

**回答：**&#x200B;いいえ。**NEW** フォルダー内のすべてのアセットは、以前に公開されたかどうかとは関係なく、AEM Assets に公開されます。**投稿**&#x200B;フォルダーが Brand Portal から AEM Assets に公開されるたびに、**NEW** フォルダーのコンテンツが上書きされます。



**質問：新しいアセットを投稿フォルダーにアップロードする方法を教えてください。**

**回答：**&#x200B;詳しくは、[アセットを投稿フォルダーにアップロードする](brand-portal-upload-assets-to-contribution-folder.md)方法についてのドキュメントを参照してください。



**質問：Brand Portal ユーザーが NEW フォルダーにアップロードしたアセットにサムネールやプレビューが表示されません**

**回答：** Brand Portal 側でワークフローが実行されていないため、これは設計のとおりです。



**質問：AEM Assets から不安定な Brand Portal にフォルダーが公開されるとどうなりますか。**

**回答：** AEMでは、フォルダーが Brand Portal に公開されるたびにログが保持されます。公開時に、Brand Portal に公開されていないすべてのアセットが複製キューに入れられます。公開ジョブがトリガーされた後にフォルダーに追加されたアセットは、Brand Portal に公開されません。AEM ユーザーがフォルダーを再度公開すると、以前に発行されなかった（複製キューに存在する）アセットのみが Brand Portal に発行されます。
これは、AEM Assets から Brand Portal に公開されたフォルダー、および投稿フォルダー内の SHARED フォルダーに対しても同じです。



**質問：質問は誰に問い合わせればいいですか。**

**回答：**&#x200B;アドビのアカウントマネージャーか、カスタマーサポートまでお願いします。


>[!NOTE]
>
>リリース日程は暫定的なものであり、変更の可能性があります。最新のリリース日程についてアドビのアカウントマネージャーまたはカスタマーサポートにお問い合わせください。




## 製品のアクセスとサポート（制限付きサイト）{#product-access-and-support-restricted-sites}

以下のサイトは既存ユーザーのみが参照できます。アクセス権を必要とするお客様は、アドビのアカウントマネージャーにご連絡ください。

* [](https://daycare.day.com) [製品へのアクセス](https://login.marketing.adobe.com)

* [アドビカスタマーケア](https://helpx.adobe.com/contact.html)
