---
title: コレクションの共有
seo-title: コレクションの共有
description: AEM Assets Brand Portal 管理者は、コレクションやスマートコレクションを承認済みユーザーと共有したり、共有を解除したりできます。エディターは、自身が作成したコレクションおよび共有が認められているコレクションと公開コレクションのみを閲覧、共有できます。
seo-description: AEM Assets Brand Portal 管理者は、コレクションやスマートコレクションを承認済みユーザーと共有したり、共有を解除したりできます。エディターは、自身が作成したコレクションおよび共有が認められているコレクションと公開コレクションのみを閲覧、共有できます。
uuid: 965f39cd-1378-42c1- a58a-01e1bf825aa3
contentOwner: bDHar
content-type: reference
topic-tags: 共有
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
discoiquuid: f053013e-5981-419f-927e- b5bb1d47ae2
translation-type: tm+mt
source-git-commit: 0b70e82d034ce56fcfc5b49396e6d3a9da4b49d4

---


# ブランドポータルでコレクションを共有 {#share-collections-bp}

AEM Assets Brand Portal 管理者は、コレクションやスマートコレクションを承認済みユーザーと共有したり、共有を解除したりできます。エディターは、自身が作成したコレクションおよび共有が認められているコレクションと公開コレクションのみを閲覧、共有できます。ただし、エディターは公開コレクションを非公開コレクションに変更できません。

>[!NOTE]
>
>Editors cannot change a public collection to a non-public collection and, therefore, do not have **Public Collection** check box available in **Collection Settings** dialog.

## コレクションの共有 {#share-collection}

コレクションを共有するには、次のようにします。

1. 左側のオーバーレイアイコンをクリックし、「**ナビゲーション**」を選択します。

   ![](assets/contenttree-1.png)

1. From the siderail on the left, click **Collections**.

   ![](assets/access_collections.png)

1. **コレクション**&#x200B;コンソールで、以下のいずれかの手順を実行します。

   * 共有するコレクションの上にマウスポインターを置きます。そのコレクションで使用できるクイックアクションサムネールから、**設定**&#x200B;アイコンをクリックします。
   ![](assets/settings_thumbnail.png)

   * 共有するコレクションを選択します。From the toolbar at the top, click **Settings**.
   ![](assets/collection-sharing.png)

1. **コレクション設定** ダイアログボックスで、コレクションを共有するユーザーまたはグループを選択し、グローバルロールに一致するユーザーまたはグループの役割を選択します。例えば、グローバルなエディターにはエディターの役割を割り当て、グローバルな閲覧者には閲覧者の役割を割り当てます。

   Alternatively, to make the collection available to all users irrespective of their group membership and role, make it public by selecting the **Public Collection** check box.

   >[!NOTE]
   >
   >ただし、公開コレクションが大量に作成されてシステムの容量に影響しないように、管理者以外のユーザーによる公開コレクションの作成を制限できます。Organizations can disable the **Allow public collections creation** configuration from **General** settings available in admin tools panel.

   ![](assets/collection_sharingadduser.png)

   Editors cannot change a public collection to a non-public collection and, therefore, do not have **Public Collection** check box available in **Collection Settings** dialog.

   ![](assets/collection-setting-editor.png)

1. **「追加**»をクリックし、?«保存?****&#x200B;コレクションが、選択したユーザーと共有されます。

   >[!NOTE]
   >
   >コレクション内のアセットやフォルダーへのアクセスは、ユーザーの役割によって決まります。ユーザーがアセットにアクセスできない場合、空のコレクションがユーザーと共有されます。また、コレクションに対して実行できるアクションも、ユーザーの役割によって決まります。

## コレクションの共有解除 {#unshare-a-collection}

コレクションの共有を解除するには、以下の手順を実行します。

1. **コレクション**&#x200B;コンソールで、共有を解除するコレクションを選択します。

   In the toolbar, click **Settings**.

   ![](assets/collection_settings.png)

1. **コレクション設定** ダイアログボックスの«メンバー»の下 **の«メンバー**»の下の **、コレクションを共有しているユーザーのリストから、ユーザーまたはグループの横のx** 記号をクリックします。

   ![](assets/unshare_collection.png)

1. 警告メッセージボックスの「**確認**」をクリックして、共有を解除することを確認します。

   「**保存**」をクリックします。

1. 共有リストから削除したユーザーの資格情報を使用してブランドポータルにログインします。指定したコレクションが、**コレクション**&#x200B;コンソールから削除されています。
