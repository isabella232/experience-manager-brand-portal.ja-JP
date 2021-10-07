---
title: よくある質問
seo-title: null
description: Adobe Experience Manager Assets Brand Portal でのよくある質問について説明します。
seo-description: null
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 4caa4263bd74b51af7504295161c421524e51f0c
workflow-type: tm+mt
source-wordcount: '1509'
ht-degree: 57%

---

# よくある質問 {#frequently-asked-questions}

Brand Portal FAQ では、最新のExperience Manager Assets Brand Portal 6.4.6 リリース以前のバージョンで作業中に発生する可能性のあるエンドユーザー向けのクエリと問題に焦点を当てています。


## Brand Portal 6.4.6 に関する FAQ   {#faqs-bp646}

**質問：既存のレガシー OAuth エンドポイント（`https://legacy-oauth.cloud.adobe.io/login`）が機能していません。考えられる理由は何でしょうか？**

**回答：** レガシー OAuth 設定は非推奨です。Experience Manager Assetsオーサーインスタンスを最新のサービスパックにアップグレードし、Adobe開発者コンソールで設定する必要があります。 詳しくは、[Brand PortalとのExperience Manager Assetsの設定 ](configure-aem-assets-with-brand-portal.md) を参照してください。 ただし、アップグレードするまでレガシー OAuth 設定が機能するようにするには、レガシー OAuth エンドポイントを `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/` に更新します。

<!--
**Ques. I have created a collection using the asset link shared by the administrator. But I am unable to create a share link for my collection. Do I need special permissions to do this?**

**Ans.** The functionality is by design, the viewer users are not permitted to share link for collections as they have limited privileges due to which they cannot add users to create a share link. It is a known issue that the share link for collections is currently visible to the viewer users. This issue will be fixed in the upcoming release, the option to share link for the collections will not be available to the viewer users.    
-->

**質問：Adobe開発者コンソールにアップグレードした後、投稿フォルダーのアセットをBrand PortalからExperience Manager Assetsに公開できません。 オーサーインスタンスがExperience Manager Assets 6.5.4 にあります。考えられる理由は何でしょうか？**

**回答：** はい。Adobe開発者コンソールを使用してExperience Manager Assets 6.5.4 に投稿フォルダーのアセットを公開する際に発生する既知の問題があります。

この問題はExperience Manager Assets 6.5.5 で修正されました。Experience Manager Assetsインスタンスを最新のサービスパックにアップグレードし、Adobe開発者コンソールで設定 ](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) をアップグレードしてください。[

<!--
Broken link of download hotfix, comment out this section until we have the latest URL.

For immediate fix on AEM 6.5.4, it is recommended to [download the hotfix](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041) and install on your AEM author instance.
-->

**質問：Brand Portalから公開された投稿フォルダーのコンテンツがExperience Manager Assetsに表示されません。 考えられる理由は何でしょうか？**

**回答：** Experience Manager Assets管理者に設定を問い合わせて、Brand Portalテナントが 1 つのExperience Manager Assetsオーサーインスタンスでのみ設定されていることを確認してください。

この問題は、複数のExperience Manager AssetsオーサーインスタンスにBrand Portalテナントを設定した場合に発生する可能性があります。 例えば、管理者が、ステージング環境と実稼動環境のExperience Manager Assetsオーサーインスタンスに同じBrand Portalテナントを設定するとします。 この場合、Brand Portalでアセットの公開トリガーはおこなわれますが、レプリケーションエージェントが要求トークンを受け取らないので、Experience Manager Assetsオーサーインスタンスはアセットを読み込めません。


**質問：Experience Manager AssetsからBrand Portalにアセットを公開できません。 レプリケーションログには、接続がタイムアウトしたことが記録されています。クイックフィックスはありますか？**

**回答：**&#x200B;通常、公開がタイムアウトエラーで失敗する場合は、レプリケーションキューに保留中のリクエストが複数あります。この問題を解決するには、タイムアウトを回避するようにレプリケーションエージェントを設定します。

レプリケーションエージェントを設定するには、次の手順を実行します。

1. Experience Manager Assetsオーサーインスタンスにログインします。
1. **ツール**&#x200B;パネルで、**[!UICONTROL デプロイメント]**／**[!UICONTROL レプリケーション]**&#x200B;に移動します。
1. レプリケーションページで、「**[!UICONTROL 作成者のエージェント]**」をクリックします。Brand Portal テナントの 4 つのレプリケーションエージェントを表示できます。
1. レプリケーションエージェントの URL をクリックして、エージェントの詳細を開きます。
1. 「**[!UICONTROL 編集]**」をクリックして、レプリケーションエージェントの設定を変更します。
1. エージェントの設定で「**[!UICONTROL 拡張]**」タブをクリックします。
1. 「**[!UICONTROL 接続を閉じる]**」チェックボックスをオンにします。
1. 手順 4～7 を繰り返して、4 つのレプリケーションエージェントをすべて設定します。
1. サーバーを再起動し、接続を確認します。


## Brand Portal 6.4.5 に関する FAQ   {#faqs-bp645}

**質問：Brand Portal 6.4.5 リリースの主な変更点は何ですか。**

**回答：** Experience Manager Assets Brand Portal 6.4.5 は、Brand Portalユーザーが、管理者権限を必要とせずに、Brand Portalインスタンス内のコンテンツをアップロードし、投稿フォルダーをExperience Manager Assetsに公開できる機能リリースです。詳しくは、[Brand Portal でのアセットソーシング](brand-portal-asset-sourcing.md)を参照してください。



**質問：私が作成した既存のアセット、機能または設定へのアクセス権は失われますか。**

**回答：**&#x200B;既存の機能と設定はすべてそのまま残ります。エンドユーザーに影響はなく、コンテンツはそのまま残ります。



**質問：新しいバージョンの Brand Portal にはいつ移行しますか。**

**回答：**Brand Portal 6.4.5 は、2019 年 10 月に実稼動環境へリリースされました。Brand Portal の次期バージョンは、2020 年の第 3 四半期にリリース予定です。
アップデートとバージョンの変更については、Brand Portal の[リリースノート](brand-portal-release-notes.md)と [Brand Portal の新機能](whats-new.md)を確認することをお勧めします。



**質問：私が管理しているユーザーに影響しますか。**

**回答：** Brand Portal 6.4.5 リリースは完全に Brand Portal 内にとどまるため、エンドユーザーには影響しません。



**質問：Brand Portal ユーザーとして必要なアクションはありますか。**

**回答：** Brand Portal 6.4.5 リリースには、「アセットソーシング」という新機能が含まれています。管理者は、Experience Manager Assetsでアセットソーシング機能を設定して、Brand Portalユーザーに対してこの機能を有効にする必要があります。 詳しくは、「[アセットソーシングの有効化](brand-portal-asset-sourcing.md)」を参照してください。



**質問：投稿フォルダーは誰が作成できますか。**

**回答：** Experience Manager Assetsで新しいフォルダーを作成する権限を持つExperience Manager Assetsユーザーであれば、誰でも投稿フォルダーを作成 **** できます。**投稿**&#x200B;フォルダーを作成するには、**アセット投稿**タイプの新しいフォルダーを作成します。
このフォルダーは、投稿用として、アクティブな Brand Portal ユーザーと共有されます。



**質問：投稿フォルダーには何が含まれますか。**

**回答：** **投稿**&#x200B;フォルダーには、**NEW** と **SHARED** の 2 つのサブフォルダーが含まれます。始めは、NEW フォルダーは空で、SHARED フォルダーには Brand Portal ユーザーの参照コンテンツ（再利用可能なアセット）が含まれます。
Brand Portal ユーザーは**投稿**&#x200B;フォルダーにアクセスし、**NEW** フォルダーにコンテンツをアップロードします。



**質問：既存の投稿フォルダーの名前を変更できますか。**

**回答：** **いいえ**、既存の&#x200B;**投稿**&#x200B;フォルダーの名前を変更することはできません。



**質問：投稿に関するアセットの要件とは何ですか。**

**回答：** **投稿**&#x200B;フォルダーに添付された&#x200B;**概要**&#x200B;ドキュメント、および **SHARED** フォルダーにアップロードされた参照コンテンツ（再利用可能なアセット）は、Brand Portal ユーザーが投稿の必要性と投稿者に期待されること（総称して「アセット要件」と呼びます）を理解するのに役立ちます。



**質問：アセットは許可されているすべてのフォルダーにアップロードできますか。**

**回答：**&#x200B;いいえ。アップロードできないフォルダーもあります。Brand Portalユーザーは、コンテンツをアップロードできるのは、Experience Manager AssetsまたはBrand Portal管理者が共有する **投稿** フォルダーのみです。



**質問：投稿フォルダーにアクセスする方法を教えてください。**

**回答：** **投稿**&#x200B;フォルダーには、自分と共有されている場合にアクセスすることができます。投稿フォルダーが共有されるたびに、電子メール／パルス通知が送信されます。電子メールで共有されたリンクを介して投稿フォルダーにアクセスするか、Brand Portal インスタンスにログインしてベルのアイコンに移動し、投稿フォルダーにアクセスする通知を受け取ることができます。

>[!NOTE]
>
>既存のBrand Portalユーザーでない場合は、Experience Manager Assets管理者に、Admin Console でユーザーを作成し、Brand Portalユーザーリストのユーザー設定ファイルにプロファイルを追加するよう依頼します。

**質問：ユーザー読み込み用の CSV ファイルの形式は何ですか。**

**回答：** Admin Console での一括ユーザー読み込みでサポートされている形式と同じです。電子メールと氏名は必須です。



**質問：「アセット投稿」ユーザードロップダウンのユーザー（Brand Portal 投稿者）のリストに入力される項目を教えてください。**

**回答：** ドロップダウンのユーザーは、Experience Manager AssetsにアップロードされたBrand Portalのユーザー設定 (.csv) ファイルから入力されます。



**質問：読み込みジョブと公開ジョブのステータスはどこで確認できますか。**

**回答：** Experience Manager Assetsでは、非同期ジョブページでインポートのステータスを確 **** 認できます。Brand Portal では、**[!UICONTROL ツール／アセット投稿のステータス]**&#x200B;で公開ジョブのステータスを確認できます。



**質問：Experience Managerで定期的に実行されるインポートジョブの頻度は？**

**回答：** Experience Manager Assetsでは、ポーリングは 5 分ごとに実行されます。



**質問：Brand PortalからExperience Manager Assetsにフォルダーを公開できる回数にしきい値はありますか？**

**回答：** いいえ。 NEW フォルダー内のすべてのア **** セットは、以前に公開されたかどうかに関係なく、Experience Manager Assetsに公開されます。Brand PortalからExperience Manager Assetsに **投稿** フォルダーが公開されるたびに、**NEW** フォルダーのコンテンツが上書きされます。



**質問：新しいアセットを投稿フォルダーにアップロードする方法を教えてください。**

**回答：**&#x200B;詳しくは、[アセットを投稿フォルダーにアップロードする](brand-portal-publish-contribution-folder-to-brand-portal.md)方法についてのドキュメントを参照してください。



**質問：Brand Portal ユーザーが NEW フォルダーにアップロードしたアセットにサムネールやプレビューが表示されません**

**回答：** Brand Portal 側でワークフローが実行されていないため、これは設計のとおりです。



**質問：フォルダーが不安定なExperience Manager AssetsからBrand Portalに公開されるとどうなりますか？**

**回答：** Experience Manager Assetsでは、フォルダーがBrand Portalに公開されるたびにログが保持されます。公開時に、Brand Portal に公開されていないすべてのアセットが複製キューに入れられます。公開ジョブがトリガーされた後にフォルダーに追加されたアセットは、Brand Portal に公開されません。Experience Manager Assetsユーザーがフォルダーを再度公開すると、以前に公開されていない（レプリケーションキューに存在する）アセットのみがBrand Portalに公開されます。
これは、Experience Manager AssetsからBrand Portalに公開されたフォルダー、および投稿フォルダー内の SHARED フォルダーに対しても同じです。

**質問：質問は誰に問い合わせればいいですか。**

**回答：**&#x200B;アドビのアカウントマネージャーか、カスタマーサポートまでお願いします。

>[!NOTE]
>
>リリース日程は暫定的なものであり、変更の可能性があります。最新のリリース日程についてアドビのアカウントマネージャーまたはカスタマーサポートにお問い合わせください。


## 製品のアクセスとサポート（制限付きサイト） {#product-access-and-support-restricted-sites}

以下のサイトは既存ユーザーのみが参照できます。アクセス権を必要とするお客様は、アドビのアカウントマネージャーにご連絡ください。

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
