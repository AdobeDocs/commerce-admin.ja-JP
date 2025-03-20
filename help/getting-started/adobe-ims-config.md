---
title: ID を使用したCommerce Admin Integration の設定
description: Adobe Commerce管理者のユーザーアカウントのログインをAdobe IDと統合するには、次のオプション手順に従います。
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 8589444a126c82f033c5b852b20493d1cf83c338
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Commerce Admin とAdobe IDの統合の設定

{{ee-feature}}

この統合は、Adobe IDを持ち、Adobe CommerceおよびAdobe Business 製品へのログインを効率化したい管理者ユーザーを持つCommerce マーチャントをサポートします。 これはオプションであり、インスタンスごとに有効になります。 有効にすると、管理ユーザーワークフローのみが影響を受けます。 

>[!IMPORTANT]
>
>管理者ユーザーは、この統合を有効にする前に、Commerce管理者資格情報（ユーザー名とパスワード）と 2FA 資格情報を保存する必要があります。 これらの資格情報は、IMS 統合が無効な場合に必要です。

## 前提条件

* Adobe Commerce 2.4.5 以降
* [Adobe Admin Console](https://adminconsole.adobe.com/) にアクセスできるAdobe.com アカウント。

この統合を設定する管理者には、モジュールのイネーブルメント時に次の資格情報が必要です。

* 組織 ID （[Adobe Admin Console](https://adminconsole.adobe.com/) から取得）。24 文字以上にする必要があります。 認証済みユーザーは、この IMS 組織に属している必要があります。 組織 ID の検索について詳しくは、[Experience Cloudの組織 ](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html) を参照してください。
* モジュールを有効にするには、Adobe Admin Consoleの組織レベルで 2FA を適用する必要があります。 [ 認証設定 ](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification) をオンにします。
* クライアント ID
* クライアント秘密鍵
* クライアント ID およびクライアント秘密鍵は、[Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/) から API キーを取得した後に利用できます。

Commerce管理者ユーザーがログインするには、Adobe IDのアカウントを作成する必要があります。

## 一般的な手順

* [Adobe Admin Console](https://adminconsole.adobe.com/) からAdobe組織 ID を取得
* [Adobe Developer Console](https://developer.adobe.com/) から新規プロジェクト、IMS API キーおよび秘密鍵を生成します
* Adobe Admin ConsoleでのAdobe Commerce ユーザーの設定
* `AdminAdobeIms` モジュールを有効にします。

統合に成功するには、すべてのAdobe Commerce ユーザーが同じ名前とプライマリメールアドレスの管理者ユーザーアカウントを持っている必要があります。 一致する管理者ユーザーアカウントが存在しない場合、必要な権限を持つユーザー（通常は管理者の役割が割り当てられている）が、同じ名前とメールアドレスで手動で [ 管理者ユーザーアカウントを作成 ](../systems/permissions-users-all.md#create-a-user) する必要があります。

## 統合の設定

システムアクセス権を持つ管理者または開発者が次の手順を完了すると、すべての管理者ユーザーのCommerce Admin ログインページに「_[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_」ボタンが表示されます。

### 手順 1:Adobe組織 ID の取得

この機能を有効にするには、少なくとも 1 つの IMS 組織のメンバーシップが必要です。 Adobe IDがある場合、デフォルトで 1 つ以上のAdobe組織に属しています。 組織 ID を取得するには、[Adobe Admin Console](https://adminconsole.adobe.com/) にログインします。

### 手順 2：新しいプロジェクト、IMS API キーおよび秘密鍵の生成

組織用のプロジェクトを作成するには、その組織のAdobe管理者アカウントにシステム管理者または開発者のロールが必要です。 [Developer Console ガイド ](https://developer.adobe.com/developer-console/docs/guides/projects/) を参照してください。

1. [Adobe Developer Console](https://developer.adobe.com/) にログインします。
1. 「**[!UICONTROL Projects]**」タブ（adobe.io/projects）に移動し、「**[!UICONTROL Create a new project]**」をクリックします。
1. 新しく作成されたプロジェクトページで「**[!UICONTROL Add API]**」をクリックします。
1. **[!UICONTROL Adobe Services]**/**[!UICONTROL Adobe Commerce with Adobe ID]** を選択します。
1. 「**[!UICONTROL Oauth 2.0 Web]**」を選択します。
1. **[!UICONTROL Redirect URI]** を指定します。`https://<commerce_base_url>/`
1. **[!UICONTROL Redirect URI pattern]** を指定します。`https://<commerce_base_url>/.*`

   ホスト名のドットの前に `\\` を付けることで、ドットをエスケープします。 URL の末尾にワイルドカードを追加すると、Adobe Commerce管理者の秘密鍵がサポートされます。

1. 「**[!UICONTROL Save configured API]**」をクリックします。
1. 作成したプロジェクトから [!UICONTROL Client ID] キーと [!UICONTROL Client Secret] キーをコピーします。

### 手順 3:Adobe Admin ConsoleでAdobe Commerce ユーザーを設定する

統合を有効にする前に、各Adobe Commerce管理者ユーザーアカウントが対応するAdobe IMSアカウントを持っていることを確認します。 Adobe Commerce ユーザーがAdobe IDでログインするには、特定のAdobe組織に属している必要があります。

>[!TIP]
>
>CSV ファイルからユーザー情報をアップロードすることで、複数のユーザーアカウントを作成できます。 [ 複数のユーザーの管理 ](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) を参照してください。

1. [Adobe Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html) で、**[!UICONTROL Users]**/**[!UICONTROL Users]** に移動します。

1. 「**[!UICONTROL Add User]**」をクリックします。

1. ユーザーのメールアドレスを入力します。

   該当する場合、推奨される ID タイプが自動的に入力されます。 この設定を、組織の購入プランに基づいた、リスト内の製品 ID のいずれかに変更できます。

   一度に 10 人までユーザーを追加できます。 さらに追加するには、変更を保存した後、上記の手順を繰り返します。

1. 「**[!UICONTROL Save]**」をクリックします。

ユーザーが追加され、[!UICONTROL Users] リストに表示されます。

### 手順 4:AdminAdobeIms モジュールを有効にする

`AdminAdobeIms` モジュールは、Adobe CommerceとAdobe IMSの統合を行います。 新しいプロジェクトを設定し、組織 ID、クライアント ID およびクライアント秘密鍵をコピーしたら、`AdminAdobeIms` モジュールを有効にできます。

`bin/magento admin:adobe-ims:enable` と入力します。 次のパラメーターを入力するよう求められます。 プロジェクトの作成時に生成された値を使用します。

* 組織 ID
* クライアント ID
* クライアント秘密鍵
* 2FA 有効

Adobe Commerceは、イネーブルメントが成功したか失敗したかを示すメッセージを表示します。

この機能を正常に有効にすると、他のAdobe Commerce Adobe IMSアカウントをユーザーアカウントに移行できます。 Adobe Commerce ユーザーがAdobe IDでログインするには、設定済みのAdobe組織に属している必要があります。
