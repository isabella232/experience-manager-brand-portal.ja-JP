---
title: フォルダーの共有
seo-title: フォルダーの共有
description: Brand Portal は、アセットの取り込みをサポートしていません。したがって、事前設定済みの AEM オーサーインスタンスから Brand Portal にアセットを公開する必要があります。公開されたアセットは、AEM インスタンスとのレプリケーションの設定時に特に指定しない限り、Brand Portal の管理者以外のユーザーからはアクセスできなくなります。そこで、共有するための設定をおこなう必要があります。
seo-description: Brand Portal は、アセットの取り込みをサポートしていません。したがって、事前設定済みの AEM オーサーインスタンスから Brand Portal にアセットを公開する必要があります。公開されたアセットは、AEM インスタンスとのレプリケーションの設定時に特に指定しない限り、Brand Portal の管理者以外のユーザーからはアクセスできなくなります。そこで、共有するための設定をおこなう必要があります。
uuid: 340d0a49- b708-4f0e-9fb8-99c824942f34
content-type: reference
topic-tags: 共有
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
discoiquuid: 2332c16f-40be-4673-8cc6-2360d5b74116
translation-type: tm+mt
source-git-commit: 0b70e82d034ce56fcfc5b49396e6d3a9da4b49d4

---


# ブランドポータルでフォルダーを共有 {#share-folders}

Brand Portal は、アセットの取り込みをサポートしていません。したがって、事前設定済みの AEM オーサーインスタンスから Brand Portal にアセットを公開する必要があります。

## Brand Portal でのフォルダー共有ワークフロー {#folder-sharing-workflow-in-brand-portal}

以下に、フォルダー共有のワークフローとユーザーアクセスを示します。

* AEM Assets から Brand Portal に公開されるすべてのフォルダーは、レプリケーションの設定時に「公開」として指定されていない限り、デフォルトで Brand Portal 管理者にのみ表示されます。
* The Administrator uses the **Folder Properties** console to share a folder with selective users or groups. フォルダーを共有しているこれらのユーザーとグループのみが、Brand Portal へのログイン後にフォルダーを表示できます。それ以外のユーザーにフォルダーは表示されません。
* The Administrator can also choose to make a folder public through the **Public Folder** check box in the **Folder Properties** console. 公開フォルダーはすべてのユーザーに表示されます。

* ユーザーの役割と権限に関係なく、ユーザーが Brand Portal にログインすると、すべての公開フォルダーが表示されます。また、そのユーザーと直接共有しているフォルダーや、そのユーザーの所属グループと直接共有しているフォルダーも表示されます。非公開フォルダーや、その他のユーザーと共有しているフォルダーは、すべてのユーザーには表示されません。

### Share folders with user groups on Brand Portal {#sharing-folders-with-user-groups-on-brand-portal}

フォルダーのアセットに対するアクセス権は、その親フォルダーに対するアクセス権に依存します。子フォルダーの設定には関係ありません。この動作は AEM 内の [ACL](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/security.html#PermissionsinAEM) によって制御されます。子フォルダーは親フォルダーの ACL を継承するためです。例えば、フォルダー A の中にフォルダー B があり、その中にフォルダー C がある場合、フォルダー A に対するアクセス権を持つユーザーグループ（またはユーザー）は、フォルダー B および C に対しても同じアクセス権を持ちます。フォルダー B は A の子フォルダーであるため A の ACL を継承し、フォルダー C はフォルダー B の子フォルダーであるため B の ACL を継承します。

同様に、フォルダーBにアクセスする権限を持つユーザーグループ（またはユーザー）は、フォルダーCに対しては同じアクセス権限を持ちますが、フォルダーAにはアクセス権限がありません。したがって、組織では、最も公開されたアセットが子フォルダに配置され、子からルートフォルダへのアクセスが制限されるように、組織がコンテンツを配置することをお勧めします。

### 公開フォルダーの公開 {#public-folder-publish}

Unless the **Public Folder Publish** option is selected while configuring Brand Portal replication, non-admin users (such as Editors and Viewers) do not have access to assets published from AEM Assets to Brand Portal.

![](assets/assetbpreplication.png)

**「公開フォルダー公開** 」オプションが無効になっている場合、管理者は共有機能を使用して、管理者以外のユーザーとこれらのアセットを具体的に共有する必要があります。

>[!NOTE]
>
>**公開フォルダの公開** を有効にするオプションは、AEM6.3.2.1以降で使用できます。

## 共有フォルダーへのアクセス {#access-to-shared-folders}

以下の表に、様々なユーザーの役割が持つアクセス権と、アセットを共有／共有解除する権限を示します。

|  | AEM Assets から Brand Portal に公開されたすべてのフォルダーへのアクセス | 共有フォルダーへのアクセス | フォルダーを共有／共有解除する権限 |
|---------------|-----------|-----------|------------|
| 管理者 | 可 | 可 | 可 |
| エディター | 不可* | 可。ただし、そのユーザーと共有されている場合、またはそのユーザーの所属グループと共有されている場合のみです。 | 共有するフォルダー、または所属するグループのフォルダーのみ |
| 閲覧者 | 不可* | 可。ただし、そのユーザーと共有されている場合、またはそのユーザーの所属グループと共有されている場合のみです。 | 不可 |
| ゲストユーザー | 不可* | 可。ただし、そのユーザーと共有されている場合、またはそのユーザーの所属グループと共有されている場合のみです。 | 不可 |

**デフォルトでは、AEM Authorを使用してブランドポータルのレプリケーションを設定する際に&#x200B;**、「公開フォルダー公開**」オプションは無効になります。このオプションが有効になっている場合は、Brand Portal に公開されているフォルダーが、デフォルトですべてのユーザー（管理者以外のユーザーも含む）にアクセス可能になります。*

### 管理者以外のユーザーによる共有フォルダーへのアクセス {#non-admin-user-access-to-shared-folders}

管理者以外のユーザーは、Brand Portal 上でそのユーザーに共有されているフォルダーにのみアクセスできます。ただし、ポータルにログインしたときにこれらのフォルダーがどのように表示されるかは、「フォルダー階層を有効化」の設定によって異なります。

**この設定が無効な場合**

管理者以外のユーザーが Brand Portal にログインすると、自身に共有されているすべてのフォルダーがランディングページを参照してください。

![](assets/disabled-folder-hierarchy1-1.png)

**この設定が有効な場合**

管理者以外のユーザーが Brand Portal にログインすると、ルートフォルダーから始まるフォルダーツリーと、それぞれの親フォルダー内に含まれる共有フォルダーが表示されます。

これらの親フォルダーは仮想フォルダーであり、これらに対してアクションを実行することはできません。仮想フォルダーは鍵のアイコン付きで表示されます。

カード表示でこれらをカーソルで指したり選択したりしても、共有フォルダーとは異なり、アクションタスクは表示されません。列表示やリスト表示で仮想フォルダーを選択すると「概要」ボタンが表示されます。

>[!NOTE]
>
>仮想フォルダーのデフォルトのサムネールは最初の共有フォルダーのサムネール画像になることに注意してください。

![](assets/enabled-hierarchy1-1.png) ![](assets/hierarchy1-nonadmin-1.png) ![](assets/hierarchy-nonadmin-1.png) ![](assets/hierarchy2-nonadmin-1.png)

## フォルダーの共有 {#how-to-share-folders}

フォルダーを Brand Portal 上でユーザーと共有するには、次の手順を実行します。

1. 左側のオーバーレイアイコンをクリックし、「**ナビゲーション**」を選択します。

   ![](assets/selectorrail.png)

2. From the siderail on the left, select **Files**.

   ![](assets/access_files.png)

3. ブランドポータルインターフェイスから、共有するフォルダを選択します。

   ![](assets/share-folders.png)

4. From the toolbar at the top, select **Share**.

   ![](assets/share_icon.png)

   **フォルダーのプロパティ**&#x200B;コンソールが表示されます。

   ![](assets/folder_properties.png)

5. デフォルトの名前をユーザーに表示しないようにする場合は、**フォルダーのプロパティ**&#x200B;コンソールで、「**フォルダーのタイトル**」フィールドにフォルダーのタイトルを指定します。
6. 「**ユーザーを追加**」リストで、フォルダーを共有するユーザーまたはグループを選択して、「**追加**」をクリックします。To share the folder with guest users only, and no other users, select **Anonymous Users** from the **Members** dropdown.

   ![](assets/only-anonymous.png)

   >[!NOTE]
   >
   >To make the folder available to all users irrespective of their group membership and role, make it public by selecting the **Public Folder** check box.

7. 必要であれば、「**サムネールを変更**」をクリックしてフォルダーのサムネール画像を変更します。
8. 「**保存**」をクリックします。
9. 共有フォルダーにアクセスするには、フォルダーを共有しているユーザーの資格情報を使用してブランドポータルにログインします。インターフェイスで共有フォルダーを確認します。

## フォルダーの共有解除 {#unshare-the-folders}

以前共有したフォルダーの共有を解除するには、次の手順に従います。

1. ブランドポータルインターフェイスから、共有解除するフォルダを選択します。

   ![](assets/share-folders-1.png)

2. From the toolbar at the top, click **Share**.
3. **Folder Properties** コンソールの **"Members**」で、ユーザーの横の **x** 記号をクリックして、フォルダーを共有しているユーザーのリストから削除します。

   ![](assets/folder_propertiesunshare.png)

4. 警告メッセージボックスの「**確認**」をクリックして、共有を解除することを確認します。「**Save**」をクリックします。

5. 共有リストから削除したユーザーの資格情報を使用してブランドポータルにログインします。このフォルダーは、ユーザーのブランドポータルインターフェイスでは使用できません。
