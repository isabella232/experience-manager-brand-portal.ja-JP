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
source-git-commit: 068ce845c51de48fb677f7bd09a2f6d20ff6f1a5

---


# ブランドポータルでコレクションを共有 {#share-collections-bp}

AEM Assets Brand Portal 管理者は、コレクションやスマートコレクションを承認済みユーザーと共有したり、共有を解除したりできます。エディターは、自身が作成したコレクションおよび共有が認められているコレクションと公開コレクションのみを閲覧、共有できます。ただし、エディターは公開コレクションを非公開コレクションに変更できません。

>[!NOTE]
>
>Editors cannot change a public collection to a non-public collection and, therefore, do not have [!UICONTROL Public Collection] checkbox available in [!UICONTROL Collection Settings] dialog.

## コレクションの共有 {#share-collection}

コレクションを共有するには、次のようにします。

1. Click the overlay icon on the left, and choose **[!UICONTROL Navigation]**.

   ![](assets/contenttree-1.png)

2. From the siderail on the left, click **[!UICONTROL Collections]**.

   ![](assets/access_collections.png)

3. **[!UICONTROL コレクション]コンソールで、以下のいずれかの手順を実行します。**

   * 共有するコレクションの上にマウスポインターを置きます。そのコレクションで使用できるクイックアクションサムネールから、**[!UICONTROL 設定]アイコンをクリックします。**
   ![](assets/settings_thumbnail.png)

   * 共有するコレクションを選択します。From the toolbar at the top, click **[!UICONTROL Settings]**.
   ![](assets/collection-sharing.png)

4. [!UICONTROL コレクション設定] ダイアログボックスで、コレクションを共有するユーザーまたはグループを選択し、グローバルロールに一致するユーザーまたはグループの役割を選択します。例えば、グローバルなエディターにはエディターの役割を割り当て、グローバルな閲覧者には閲覧者の役割を割り当てます。

   Alternatively, to make the collection available to all users irrespective of their group membership and role, make it public by selecting the **[!UICONTROL Public Collection]** check-box.

   >[!NOTE]
   >
   >ただし、公開コレクションが大量に作成されてシステムの容量に影響しないように、管理者以外のユーザーによる公開コレクションの作成を制限できます。Organizations can disable the **[!UICONTROL Allow public collections creation]** configuration from [!UICONTROL General] settings available in admin tools panel.

   ![](assets/collection_sharingadduser.png)

   Editors cannot change a public collection to a non-public collection and, therefore, do not have [!UICONTROL Public Collection] check-box available in [!UICONTROL Collection Settings] dialog.

   ![](assets/collection-setting-editor.png)

5. **[!UICONTROL 「追加]**」を選択し、 **[!UICONTROL 保存]**&#x200B;します。コレクションが、選択したユーザーと共有されます。

   >[!NOTE]
   >
   >コレクション内のアセットやフォルダーへのアクセスは、ユーザーの役割によって決まります。ユーザーがアセットにアクセスできない場合、空のコレクションがユーザーと共有されます。また、コレクションに対して実行できるアクションも、ユーザーの役割によって決まります。

## コレクションの共有解除 {#unshare-a-collection}

コレクションの共有を解除するには、以下の手順を実行します。

1. [!UICONTROL コレクション]コンソールで、共有を解除するコレクションを選択します。

   In the toolbar, click **[!UICONTROL Settings]**.

   ![](assets/collection_settings.png)

2. [!UICONTROL コレクション設定] ダイアログボックスの«メンバー»の下 [!UICONTROL の«メンバー]»の下の **[!UICONTROL 、コレクションを共有しているユーザーのリストから、ユーザーまたはグループの横のx]** 記号をクリックします。

   ![](assets/unshare_collection.png)

3. 警告メッセージボックスの「**[!UICONTROL 確認]」をクリックして、共有を解除することを確認します。**

   Click **[!UICONTROL Save]**.

4. 共有リストから削除したユーザーの資格情報を使用してブランドポータルにログインします。指定したコレクションが、**[!UICONTROL コレクション]コンソールから削除されています。**
