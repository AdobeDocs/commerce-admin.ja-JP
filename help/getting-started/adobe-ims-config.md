---
title: ID を使用したコマース管理者統合の設定
description: Adobe Commerce Admin ユーザーアカウントログインとAdobe IDを統合する場合の、この手順（オプション）に従います。
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 20b2560ce2b8071c740907292544519f8b1c3ddf
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 1%

---

# コマース管理とAdobe IDの統合の設定

{{ee-feature}}

この統合は、Adobe IDを持ち、Adobe CommerceおよびAdobeビジネス製品へのログインを合理化したい管理者ユーザーとのコマースマーチャントをサポートします。 これはオプションで、インスタンスごとに有効になります。 有効になっている場合、管理者ユーザーワークフローのみが影響を受けます。 

>[!IMPORTANT]
>
>この統合を有効にする前に、管理者ユーザーは、コマース管理者の資格情報（ユーザー名とパスワード）と 2FA の資格情報を保存する必要があります。 IMS 統合が無効になっている場合は、これらの資格情報が必要です。

## 前提条件

* Adobe Commerce 2.4.5 以降
* へのアクセス権を持つAdobe.comアカウント [Adobe Admin Console](https://adminconsole.adobe.com/).

この統合を設定する管理者は、モジュールの有効化中に次の資格情報が必要です。

* 組織 ID （から取得） [Adobe Admin Console](https://adminconsole.adobe.com/)) で始まる必要があります。24 文字以上である必要があります。 認証済みユーザーはこの IMS 組織に属している必要があります。 組織 ID の検索について詳しくは、 [Experience Cloudの組織](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* モジュールを有効にするには、Adobe Admin Consoleの組織レベルで 2FA を適用する必要があります。 チェック [認証設定](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* クライアント ID
* クライアント秘密鍵
* クライアント ID とクライアント秘密鍵は、 [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Commerce の管理者ユーザーは、Adobe IDでアカウントを作成してログインする必要があります。

## 一般的な手順

* からのAdobe組織 ID の取得 [Adobe Admin Console](https://adminconsole.adobe.com/)
* から新しいプロジェクト、IMS API キーおよび暗号鍵を生成します。 [Adobe Developer Console](https://developer.adobe.com/)
* を有効にします。 `AdminAdobeIms` モジュール
* Adobe Admin ConsoleでAdobe Commerceユーザーを設定します。

統合を成功させるには、すべてのAdobe Commerceユーザーが同じ名前とプライマリ電子メールアドレスを持つ管理者ユーザーアカウントを持っている必要があります。 一致する管理者ユーザーアカウントが存在しない場合は、必要な権限（通常は管理者の役割が割り当てられる）を持つユーザーが手動で作成する必要があります [管理者ユーザーアカウントの作成](../systems/permissions-users-all.md#create-a-user) 同じ名前と E メールを持つ

## 統合の設定

システムにアクセスできる管理者または開発者が、次の手順を完了した後、 _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_ボタンが、すべての管理者ユーザーのコマース管理者ログインページに表示されます。

### 手順 1:Adobe組織 ID の取得

この機能を有効にするには、少なくとも 1 つの IMS 組織のメンバーシップが必要です。 Adobe IDを持っている場合、デフォルトで 1 つ以上のAdobe組織に属しています。 にログインします。 [Adobe Admin Console](https://adminconsole.adobe.com/) をクリックして組織 ID を取得します。

### 手順 2：新しいプロジェクト、IMS API キー、秘密鍵を生成する

組織のプロジェクトを作成するには、その組織のAdobe管理者アカウントにシステム管理者または開発者の役割が必要です。 詳しくは、 [開発者コンソールガイド](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. にログインします。 [Adobe Developer Console](https://developer.adobe.com/).
1. 次に移動： **[!UICONTROL Projects]** タブ (adobe.io/projects) をクリックし、 **[!UICONTROL Create a new project]**.
1. クリック **[!UICONTROL Add API]** をクリックします。
1. 選択 **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. 選択 **[!UICONTROL Oauth 2.0 Web]**.
1. 次を指定します。 **[!UICONTROL Redirect URI]**: `https://<hostname>/`
1. 次を指定します。 **[!UICONTROL Redirect URI pattern]**: `https://<hostname>/.*`

   ドットの前にあるホスト名のドットをエスケープします。 `\\`. URL の末尾にワイルドカードを追加すると、Adobe Commerce Admin 秘密鍵がサポートされます。

1. クリック **[!UICONTROL Save configured API]**.
1. をコピーします。 [!UICONTROL Client ID] および [!UICONTROL Client Secret] 作成したプロジェクトのキー。

### 手順 3:AdminAdobeIms モジュールの有効化

The `AdminAdobeIms` モジュールは、Adobe Commerce/Adobe IMSの統合を担当します。 新しいプロジェクトを設定し、組織 ID、クライアント ID、クライアントの秘密鍵をコピーした後、 `AdminAdobeIms` モジュール。

入力 `bin/magento admin:adobe-ims:enable`. 次のパラメーターを入力するよう求められます。 プロジェクトの作成時に生成された値を使用します。

* 組織 ID
* クライアント ID
* クライアント秘密鍵
* 2FA 有効

Adobe Commerceは、イネーブルメントが成功したか失敗したかを示すメッセージを表示します。

この機能を正常に有効にした後、他のAdobe CommerceユーザーアカウントをAdobe IMSアカウントに移行できます。 Adobe CommerceユーザーがAdobe IDを使用してログインするには、設定済みのAdobe組織に属している必要があります。

### 手順 4:Adobe Admin ConsoleでのAdobe Commerceユーザーの設定

この機能を正常に有効にした後、他のAdobe CommerceユーザーアカウントをAdobe IMSアカウントに移行できます。 Adobe CommerceユーザーがAdobe IDを使用してログインするには、1 つ以上のAdobe組織に属している必要があります。

1. Adobe Analytics の [Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)に移動します。 **[!UICONTROL Users]**  > **[!UICONTROL Users]**.

1. クリック **[!UICONTROL Add User]**.

1. ユーザーの電子メールアドレスを入力します。

   該当する場合、推奨 ID タイプが自動的に入力されます。 この設定は、組織の購入プランに基づく、リスト内の製品 ID の 1 つに変更できます。

   一度に 10 人までのユーザーを追加できます。 さらに追加するには、変更を保存した後で、上記の手順を繰り返します。

1. クリック **[!UICONTROL Save]**.

ユーザーが追加され、「 [!UICONTROL Users] リスト。
