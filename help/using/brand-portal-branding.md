---
title: 壁紙、ヘッダーおよび電子メールメッセージのカスタマイズ
seo-title: 壁紙、ヘッダーおよび電子メールメッセージのカスタマイズ
description: Brand Portal 管理者は、ユーザーに表示されるインターフェイスをカスタマイズできます。Brand Portal ログインページのために固有の背景画像（壁紙）を選択できます。顧客のブランドに合わせてヘッダー画像を追加したり、アセット共有の電子メールをカスタマイズすることもできます。
seo-description: Brand Portal 管理者は、ユーザーに表示されるインターフェイスをカスタマイズできます。Brand Portal ログインページのために固有の背景画像（壁紙）を選択できます。顧客のブランドに合わせてヘッダー画像を追加したり、アセット共有の電子メールをカスタマイズすることもできます。
uuid: e078d0b9-18b5-467a- ae90-7f0b9fd0d414
content-type: reference
products: SG_ PREPERNEMENTMANAGER/Brand_ Portal
topic-tags: 管理
discoiquuid: 7b573a4f-2d4e-48d6- b259-436d0cfbdce9
translation-type: tm+mt
source-git-commit: 32c3cdb8e3fafd74cfb36e6bcfe0811e7152b2d0

---


# 壁紙、ヘッダーおよび電子メールメッセージのカスタマイズ {#customize-wallpaper-header-and-email-message}

[!DNL Brand Portal] 管理者は、ユーザーに表示されるインターフェイスをカスタマイズできます。[!DNL Brand Portal] ログインページの特定の背景画像（壁紙）を選択できます。顧客のブランドに合わせてヘッダー画像を追加したり、アセット共有の電子メールをカスタマイズすることもできます。

## ログイン画面の壁紙のカスタマイズ {#customize-the-login-screen-wallpaper}

カスタムブランドの壁紙画像がない場合、ログインページにはデフォルトの壁紙が表示されます。

1. From the [!DNL AEM] toolbar at the top, click the Adobe logo to access administrative tools.

   ![](assets/aemlogo.png)

2. From the administrative tools panel, click **Branding**.

   ![](assets/admin-tools-panel-10.png)

3. On the left rail of the **Configure Branding** page, **Wallpaper** is selected by default. ログインページに表示されるデフォルトの背景画像が表示されます。

   ![](assets/default_wallpaper.png)

4. To add a new background image, click the **Choose Image** icon from the toolbar at the top.

   ![](assets/choose_wallpaperimage.png)

   次のいずれかの操作をおこないます。

   * To upload an image from your computer, click **Upload**. 必要な画像に移動してアップロードします。
   * To use an existing Brand Portal image, click **Select from existing**. アセットピッカーを使用して画像を選択します。
   ![](assets/asset-picker.png)

5. 背景画像のヘッダーテキストと説明を指定します。To save the changes, click **Save** from the toolbar at the top.

6. From the toolbar at the top, click the **Preview** icon to generate a preview of the Brand Portal interface with the image.

   ![](assets/chlimage_1.png)

   ![](assets/custom-wallpaper-preview.png)

7. To activate or deactivate the default wallpaper, do the following in the **Configure Branding** &gt; **Wallpaper** page:

   * To display the default wallpaper image on the Brand Portal login page, click **Deactivate Wallpaper** from the toolbar at the top. カスタム画像のアクティベート解除を確認するメッセージが表示されます。
   ![](assets/chlimage_1-1.png)

   * Brand Portal ログインページにカスタム画像を再度表示するには、ツールバーの「**壁紙をアクティベート**」をクリックします。画像が復元されたことを確認するメッセージが表示されます。
   ![](assets/chlimage_1-2.png)

   * 「**保存**」をクリックして、変更を保存します。



## ヘッダーのカスタマイズ {#customize-the-header}

ブランドポータルにログインすると、様々なブランドポータルページにヘッダーが表示されます。

1. 上部のAEMツールバーから、Adobeロゴをクリックして管理ツールにアクセスします。

   ![](assets/aemlogo.png)

2. From the administrative tools panel, click **Branding**.

   ![](assets/admin-tools-panel-11.png)

3. To customize the page header for the Brand Portal interface, on the **Configure Branding** page, select **Header Image** from the left rail. デフォルトのヘッダー画像が表示されています。

   ![](assets/default-header.png)

4. To upload a header image, click the **Choose Image** icon and choose **Upload**.

   To use an existing  [!DNL Brand Portal] image, choose **Select from existing**.

   ![](assets/choose_wallpaperimage-1.png)

   アセットピッカーを使用して画像を選択します。

   ![](assets/asset-picker-header.png)

5. ヘッダー画像に URL を含めるには、「**画像 URL**」ボックスに URL を指定します。外部URLまたは内部URLを指定できます。内部リンクも相対リンク（例えば、
   `/mediaportal.html/content/dam/mac/tenant_id/tags`.
このリンクは、ユーザーをタグフォルダーに転送します。
To save the changes, click **Save** from the toolbar at the top.

   ![](assets/configure_brandingheaderimageurl.png)

6. 上部のツールバーの「**プレビュー**」アイコンをクリックして、ヘッダー画像を含む インターフェイスをプレビューします。[!DNL Brand Portal]

   ![](assets/chlimage_1-3.png)
   ![](assets/custom_header_preview.png)

7. To activate or deactivate the header image, do the following in the **Configure Branding** &gt; **Header Image** page:

   * To prevent a header image from appearing on  [!DNL Brand Portal] pages, click **Deactivate Header** from the toolbar at the top. ヘッダー画像のアクティベート解除を確認するメッセージが表示されます。
   ![](assets/chlimage_1-4.png)

   * To make the header image reappear on  [!DNL Brand Portal] pages, click **Activate Header** from the toolbar at the top. 画像がアクティブ化されていることを確認するメッセージが表示されます。
   ![](assets/chlimage_1-5.png)

   * 「**保存**」をクリックして、変更を保存します。



## 電子メールメッセージのカスタマイズ {#customize-the-email-messaging}

アセットをリンクとして共有すると、そのリンクを含む電子メールがユーザーに届きます。管理者は、これらの電子メールのメッセージ内容、つまりロゴ、説明およびフッターをカスタマイズできます。

1. From the  [!DNL AEM] toolbar at the top, click the Adobe logo to access administrative tools.

   ![](assets/aemlogo.png)

2. From the administrative tools panel, click **Branding**.

   ![](assets/admin-tools-panel-12.png)

3. When assets are shared as links or downloaded through emails, and when  [!UICONTROL collections] are shared, email notifications are sent to users. To customize the email message, on the **Configure Branding** page, select **Email Message** from the left rail.

   ![](assets/configure-branding-page-email.png)

4. To add a logo to outgoing emails, click **Upload** from the toolbar at the top.

5. 「**説明**」セクションで、電子メールのヘッダーとフッターのテキストを指定します。To save the changes, click **Save** from the toolbar at the top.

   >[!NOTE]
   >
   >ロゴに推奨サイズを使用しない場合、またはヘッダーとフッターのテキストが推奨ワード数を超えた場合は、電子メールメッセージのコンテンツが文字化けすることがあります。
