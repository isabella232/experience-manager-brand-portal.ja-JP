---
title: ユーザー、グループおよびユーザーの役割の管理
seo-title: ユーザー、グループおよびユーザーの役割の管理
description: 管理者は、Adobe Admin Console を使用して AEM Assets Brand Portal のユーザーおよび製品プロファイルを作成でき、それらのユーザーの役割を Brand Portal ユーザーインターフェイスで管理できます。これは閲覧者とエディターにはない権限です。
seo-description: 管理者は、Adobe Admin Console を使用して AEM Assets Brand Portal のユーザーおよび製品プロファイルを作成でき、それらのユーザーの役割を Brand Portal ユーザーインターフェイスで管理できます。これは閲覧者とエディターにはない権限です。
uuid: 0dc1867c-6d1b-4d0d- a25e-0df207c269b8
content-type: reference
topic-tags: 管理
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
discoiquuid: ba468e80- d077-4af6- b782-238fc557e22b
translation-type: tm+mt
source-git-commit: 32c3cdb8e3fafd74cfb36e6bcfe0811e7152b2d0

---


# Manage Users, Groups, and User Roles {#manage-users-groups-and-user-roles}

Administrators can use [!DNL Adobe Admin Console] to create [!DNL AEM Assets Brand Portal] users and product profiles, and manage their roles using the Brand Portal user interface. これは閲覧者とエディターにはない権限です。

[管理コンソール](http://adminconsole.adobe.com/enterprise/overview)で、組織に関連付けられているすべての製品を表示できます。製品は、任意の [!DNL Experience Cloud] ソリューション（など [!DNL Adobe Analytics]） [!DNL Adobe Target]です [!DNL AEM Brand Portal]。AEMブランドポータル製品を選択し、製品プロファイルを作成する必要があります。

<!--
Comment Type: draft

<note type="note">
<p>Product Profiles (formerly known as product configurations*). </p>
<p>* The nomenclature has changed from product configurations to product profiles in the new Adobe Admin Console.</p>
</note>
-->
![](assets/create-user-group.png)

These product profiles are synced with the [!DNL Brand Portal] user interface every 8 hours and visible as groups in [!DNL Brand Portal]. Once you add users and create product profiles, and add users to those product profiles, you can assign roles to users and groups in [!DNL Brand Portal].

>[!NOTE]
>
>To create groups in [!DNL Brand Portal], from [!DNL Adobe Admin Console], use **Products** page &gt; **Product Profiles**, instead of **User** page &gt; **User Groups**. Product profiles in [!DNL Adobe Admin Console] are used to create groups in [!DNL Brand Portal].

## ユーザーの追加 {#add-a-user}

If you are a product administrator, use [[!DNL Adobe Admin Console]](http://adminconsole.adobe.com/enterprise/overview) to create users and assign them to product profiles (*formerly known as product configurations*), which show as groups in [!DNL Brand Portal]. これにより、グループを使用して役割の管理やアセットの共有などの操作を一括して実行できます。

>[!NOTE]
New users who do not have access to [!DNL Brand Portal] can request access from the login screen of [!DNL Brand Portal]. For more information, refer to [Request access to [!DNL Brand Portal]](../using/brand-portal.md#request-access-to-brand-portal). After you receive access request notifications in your notification area, click the relevant notification and then click **Grant Access**. または、アクセス要求電子メール内のリンクに従います。Next, to add a user through [[!DNL Adobe Admin Console]](http://adminconsole.adobe.com/enterprise/overview), follow Steps 4-7 in the procedure below.

>[!NOTE]
[[!DIL Adobe Admin Consoleを](http://adminconsole.adobe.com/enterprise/overview) 直接または元 [!DNL Brand Portal]に戻します。直接ログインする場合は、以下の手順4~7に従ってユーザを追加してください。

1. From the [!DNL AEM] toolbar at the top, click the Adobe logo to access administrative tools.

   ![AEMロゴ](assets/aemlogo.png)

2. 管理ツールパネルの「**ユーザー**」をクリックします。

   ![管理ツールパネル](assets/admin-tools-panel-5.png)

3. **[ユーザの役割** ]ページで **[管理]** タブをクリックし、[管理コンソール **の起動]をクリック**&#x200B;します。

   ![管理コンソール起動のユーザーロール](assets/launch_admin_console.png)

4. Admin Console で、以下のいずれかの手順を実行して、新しいユーザーを作成します。

   * 上部のツールバーの「**概要**」をクリックします。**概要** ページで、製品カードから「ユーザー **** を割り当て」 **[!DNL AEM Brand Portal]** をクリックします。
   ![管理コンソールの概要](assets/admin_console_overviewadduser.png)

   * 上部のツールバーの「**ユーザー**」をクリックします。**ユーザー** ページでは、左側のナビゲーションバーの **ユーザー** がデフォルトで選択されています。Click **Add User**.
   ![管理コンソールユーザの追加](assets/admin_console_adduseruserpage.png)

5. ユーザーを追加ダイアログで、追加するユーザーの電子メール ID を入力するか、入力中に表示される候補リストからユーザーを選択します。

   ![ブランドポータルへのユーザーの追加](assets/add_user_to_aem_bp.png)

6. 1 つ以上の製品プロファイル（旧称：製品設定）にユーザーを割り当てます。製品プロファイルに割り当てられたユーザーは、Brand Portal にアクセスできます。「**この製品のプロファイルを選択してください**」フィールドから、適切な製品プロファイルを選択します。
7. 「**保存**」をクリックします。追加したユーザーにウェルカムメールが送信されます。The invited user can access [!DNL Brand Portal] by clicking the link in the welcome email and signing in using an [!UICONTROL Adobe ID]. 詳しくは、[初回のログイン操作](../using/brand-portal-onboarding.md)を参照してください。

   >[!NOTE]
   If a user is unable to log on to [!DNL Brand Portal], the Administrator of the organization should visit Adobe [!UICONTROL Admin Console] and check whether the user is present and has been added to at least one product profile.

   管理者権限の付与について詳しくは、[ユーザーへの管理者権限の付与](../using/brand-portal-adding-users.md#provideadministratorprivilegestousers)を参照してください。

## 製品プロファイルの追加 {#add-a-product-profile}

[!UICONTROL 管理コンソール] の製品プロファイル（以前の製品設定）を使用して、ロールの管理やアセットの共有などの一括操作を実行できる [!DNL Brand Portal] ように、グループの作成に使用 [!DNL Brand Portal]します。**[!DNL Brand Portal]** は、デフォルトで使用可能な製品プロファイルです。これとは別の製品プロファイルを作成し、その新しい製品プロファイルにユーザーを追加することもできます。

>[!NOTE]
[[!UACROL管理コンソール]を](http://adminconsole.adobe.com/enterprise/overview) 直接または元 [!DNL Brand Portal]に設定します。If you login to [!UICONTROL Admin Console] directly, follow Steps 4-7 in the procedure below to add a product profile.

1. From the [!DNL AEM] toolbar at the top, click the Adobe logo to access administrative tools.

   ![[!DNL AEM] ロゴ](assets/aemlogo.png)

2. 管理ツールパネルの「**ユーザー**」をクリックします。

   ![管理ツールパネル](assets/admin-tools-panel-6.png)

3. **[ユーザの役割** ]ページで **[管理]** タブをクリックし、[管理コンソール **の起動]をクリック**&#x200B;します。

   ![管理コンソールの起動](assets/launch_admin_console.png)

4. From the toolbar at the top, click **Products**.
5. **製品** ページでは、デフォルトで **製品プロファイル** が選択されています。Click **New Profile**.

   ![新しい製品プロファイルの追加](assets/admin_console_addproductprofile.png)

6. **新しいプロファイルを作成**&#x200B;ページで、プロファイル名、表示名およびプロファイルの説明を入力します。また、ユーザーがプロファイルに追加された場合やプロファイルから削除された場合に電子メールで通知するかどうかも選択します。

   ![製品プロファイルの作成](assets/admin_console_addaproductprofilecreatenewprofile.png)

7. 「**完了**」をクリックします。**例えば、Salesグループ**&#x200B;などの製品設定グループがブランドポータルに追加されます。

   ![製品プロファイル](assets/admin_console_productprofileadded.png)

## 製品プロファイルへのユーザーの追加 {#add-users-to-a-product-profile}

[!DNL Brand Portal] グループにユーザーを追加するには、管理コンソールの [!UICONTROL 対応する製品プロファイル（以前の製品設定）にそれらを追加]します。ユーザーは個別に追加することも、一括で追加することもできます。

>[!NOTE]
[[!DIL管理コンソール]を](http://adminconsole.adobe.com/enterprise/overview) 直接また [!DNL Brand Portal]は元に戻します。管理コンソールに直接ログインする場合は、以下の手順4~7に従ってユーザを製品プロファイルに追加してください。

1. From the [!DNL AEM] toolbar at the top, click the Adobe logo to access administrative tools.

   ![[!DNL AEM] ロゴ](assets/aemlogo.png)

2. 管理ツールパネルの「**ユーザー**」をクリックします。

   ![管理ツールパネル](assets/admin-tools-panel-7.png)

3. **[ユーザの役割** ]ページで **[管理]** タブをクリックし、[管理コンソール **の起動]をクリック**&#x200B;します。

   ![起動 [!DNL Admin Console]](assets/launch_admin_console.png)

4. From the toolbar at the top, click **Products**.
5. **製品** ページでは、デフォルトで **製品プロファイル** が選択されています。Open the product profile to which you want to add a user, for example, **Sales group**.

   ![製品プロファイル](assets/admin_console_productprofileadded.png)

6. 製品プロファイルにユーザーを個別に追加するには、以下の手順を実行します。

   * Click **Add User**.
   ![グループプロファイルをマッピングするグループ [!DNL Brand Portal]](assets/admin_console_productprofilesalesgroup.png)

   * In the **Add User to Sales group** page, type the email ID of the user you want to add or select the user from the list of suggestions that appear as you type.
   ![グループへのユーザーの追加](assets/admin_console_addusertosalesgroup.png)

   * 「**Save**」をクリックします。



7. 製品プロファイルにユーザーを一括で追加するには、以下の手順を実行します。

   * Choose ellipsis (**...**) &gt; **Add users by CSV**.
   ![ユーザーの一括追加](assets/admin_console_addbulkusers.png)

   * In the **Add Users by CSV** page, download a CSV template or drag-and-drop a CSV file.
   ![ユーザーの一括追加](assets/admin_console_addbulkuserscsv.png)

   * 「**アップロード**」をクリックします。
   If you added users to the default product profile, that is, [!DNL Brand Portal], a welcome email is sent to the email ID of the users you added. The invited users can access [!DNL Brand Portal] by clicking the link in the welcome email and signing in using an [!UICONTROL Adobe ID]. 詳しくは、[初回のログイン操作](../using/brand-portal-onboarding.md)を参照してください。

   ユーザーをカスタム製品プロファイルや新しい製品プロファイルに追加したときに、そのユーザーに電子メール通知が送信されることはありません。

## ユーザーへの管理者権限の付与 {#provide-administrator-privileges-to-users}

You can provide the system administrator or the product administrator privilege to a [!DNL Brand Portal] user. Do not provide other administrative rights available in [!UICONTROL Admin Console], such as product profile administrator, user group administrator, and support administrator. これらの役割について詳しくは、[管理ロール](https://helpx.adobe.com/enterprise/using/admin-roles.html)を参照してください。

>[!NOTE]
[[!UACROL管理コンソール]を](https://adminconsole.adobe.com/enterprise/overview) 直接または元 [!DNL Brand Portal]に設定します。If you login to [!UICONTROL Admin Console] directly, follow Steps 4-8 in the procedure below to add a user to a product profile.

1. From the [!DNL AEM] toolbar at the top, click the Adobe logo to access administrative tools.

   ![AEMLogo](assets/aemlogo.png)

2. 管理ツールパネルの「**ユーザー**」をクリックします。

   ![管理ツールパネル](assets/admin-tools-panel-8.png)

3. **[ユーザの役割** ]ページで **[管理]** タブをクリックし、[管理コンソール **の起動]をクリック**&#x200B;します。

   ![管理コンソールの起動](assets/launch_admin_console.png)

4. 上部のツールバーの「**ユーザー**」をクリックします。
5. **ユーザー** ページでは、左側のナビゲーションバーの **ユーザー** がデフォルトで選択されています。管理者権限を付与するユーザーの名前をクリックします。

   ![管理コンソールでのユーザーの追加](assets/admin_console_adduseruserpage.png)

6. In the user profile page, locate the **Administrative Rights** section at the bottom, and choose ellipsis (**...**) &gt; **Edit admin rights**.
   ![管理コンソールの管理者権限](assets/admin_console_editadminrights.png)

7. In the **Edit Admin** page, select System Administrator or Product Administrator.

   ![管理コンソールで管理者権限を編集](assets/admin_console_editadminrightsselection.png)

   >[!NOTE]
   [!DNL Brand Portal] は、システム管理者および製品管理者の役割のみをサポートしています。
   [!DNL Adobe] 組織のすべての製品に対する組織全体の管理者権限を付与するため、システム管理者ロールを使用しないことをお勧めします。例えば、3つのMarketing Cloud製品を含む組織のシステム管理者には、3つの製品すべてに対する全権限セットがあります。Only a System Administrator can configure [!DNL AEM] Assets so that assets can be published from [!DNL AEM] Assets to [!DNL Brand Portal]. For more information, see [Configure AEM Assets integration with [!DNL Brand Portal]](https://helpx.adobe.com/experience-manager/6-5/assets/using/brand-portal-configuring-integration.html).
   それに対して、製品管理者の役割は、特定の製品に対する管理者権限のみを付与します。If you want to enforce a more granular access control within [!DNL Brand Portal], use the Product Administrator role and select the product as **[!DNL AEM Brand Portal]**.

   >[!NOTE]
   [!DNL Brand Portal] は、製品プロファイル管理者（旧称：設定管理者）の権限をサポートしていません。ユーザーに製品プロファイル管理者の権限を割り当てることは避けてください。

8. 管理者タイプの選択を確認し、「**保存**」をクリックします。

   >[!NOTE]
   ユーザーの管理者権限を失効するには、**管理者を編集**&#x200B;ページで適切な変更をおこない、「**保存**」をクリックします。

## ユーザーの役割の管理 {#manage-user-roles}

An Administrator can modify roles for users in [!DNL Brand Portal].

In addition to the Administrator role, [!DNL Brand Portal] supports the following roles:

* **閲覧者**：この役割を持つユーザーは、管理者から共有されたファイルやフォルダーを表示できます。ビューアは、アセットを検索してダウンロードすることもできます。However, Viewers cannot share content (files, folders, [!UICONTROL collections]) with other users.
* **エディター**：この役割を持つユーザーは、閲覧者の権限をすべて保有します。In addition, Editors can share content (folders, [!UICONTROL collections], links) with other users.

1. From the [!DNL AEM] toolbar at the top, click the Adobe logo to access administrative tools.

   ![AEMLogo](assets/aemlogo.png)

2. 管理ツールパネルの「**ユーザー**」をクリックします。

   ![管理ツールパネル](assets/admin-tools-panel-9.png)

3. **ユーザーの役割** ページで、デフォルトで **「ユーザー」** タブが選択されています。For the user whose role you want to change, select **Editor** or **Viewer** from the **Role** drop-down.

   ![ユーザーの役割の変更](assets/modify_user_role.png)

   複数のユーザーの役割を同時に変更するには、ユーザーを選択し、**役割**&#x200B;ドロップダウンから適切な役割を選択します。

   >[!NOTE]
   管理者ユーザーの&#x200B;**役割**&#x200B;リストは無効になっています。管理者ユーザーを選択して、役割を変更することはできません。

   >[!NOTE]
   ユーザーがエディターグループのメンバーの場合は、ユーザーの役割も無効になっています。ユーザーの編集権限を失効するには、エディターグループからそのユーザーを削除するか、グループ全体の役割を「閲覧者」に変更します。

4. 「**保存**」をクリックします。ロールは、対応するユーザーに対して変更されます。複数のユーザーを選択している場合は、すべてのユーザーの役割が同時に変更されます。

   >[!NOTE]
   Changes in user permissions are reflected in the **User Roles** page only after the users re-login to Brand Portal.

## グループの役割および権限の管理 {#manage-group-roles-and-privileges}

An Administrator can associate specific privileges with a [group](../using/brand-portal-adding-users.md#main-pars-title-278567577) of users on Brand Portal. The **Groups** tab on the **User Roles** page allows administrators to:

* ユーザーグループに役割を割り当てる
* ユーザーグループが Brand Portal から画像ファイル（.jpeg、.tiff、.png、.bmp、.gif、.pjpeg、x-portable-anymap、x-portable-bitmap、x-portable-graymap、x-portable-pixmap、x-rgb、x-xbitmap、x-xpixmap、x-icon、image/photoshop、image/x-photoshop、.psd、image/vnd.adobe.photoshop）のオリジナルのレンディションをダウンロードすることを制限する

>[!NOTE]
リンクとして共有されたアセットの場合、画像ファイルのオリジナルのレンディションへのアクセス権限は、アセットを共有しているユーザーの権限に基づいて適用されます。

ロールを変更して特定のグループメンバーの元のレンディションにアクセスするには、次の手順に従います。

1. **ユーザーの役割** ページで、 **「グループ** 」タブに移動します。
2. 役割を変更するグループを選択します。
3. **役割**&#x200B;ドロップダウンリストから、適切な役割を選択します。

   To allow the members of a group to have access to original renditions of image files (.jpeg, .tiff, .png, .bmp, .gif, .pjpeg, x-portable-anymap, x-portable-bitmap, x-portable-graymap, x-portable-pixmap, x-rgb, x-xbitmap, x-xpixmap, x-icon, image/photoshop, image/x-photoshop, .psd, image/vnd.adobe.photoshop) which they download from the portal or shared link, keep the **Access to  Original** option selected for that group. By default, **Access to Original** option is selected for all the users. ユーザーグループがオリジナルのレンディションにアクセスできないようにするには、そのグループに対応するオプションの選択を解除します。

   ![ユーザーグループの役割](assets/access-original-rend.png)

   >[!NOTE]
   ユーザーが複数のグループに追加され、これらのグループのいずれかに制限がある場合、そのユーザーに制限が適用されます。
   また、管理者は、画像ファイルのオリジナルのレンディションへのアクセスに関する制約を受けません（その管理者が制約対象となるグループのメンバーである場合も、制約は適用されません）。

4. 「**保存**」をクリックします。対応するグループの役割が変更されます。

   >[!NOTE]
   The user-to-group association, or the group membership of a user, is synced to  [!DNL Brand Portal] every 8 hours. ユーザーまたはグループの役割の変更は、次回の同期ジョブの実行後に反映されます。
