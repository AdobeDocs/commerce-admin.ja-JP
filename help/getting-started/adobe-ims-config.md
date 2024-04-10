---
title: ID を使用して Commerce Admin 統合を設定する
description: Adobe Commerce管理者のユーザーアカウントのログインをAdobe IDと統合するには、次のオプション手順に従います。
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 9a9106cde5184823755fb1f44fe7eae300442abc
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Adobe IDと Commerce Admin の統合の設定

{{ee-feature}}

この統合は、Adobe IDを持ち、Adobe Commerceへのログインとビジネス製品のAdobeを効率化したい管理者ユーザーとのコマースマーチャントをサポートします。 これはオプションであり、インスタンスごとに有効になります。 有効にすると、管理ユーザーワークフローのみが影響を受けます。 

>[!IMPORTANT]
>
>管理者ユーザーは、この統合を有効にする前に、Commerce 管理者資格情報（ユーザー名とパスワード）と 2FA 資格情報を保存する必要があります。 これらの資格情報は、IMS 統合が無効な場合に必要です。

## 前提条件

* Adobe Commerce 2.4.5 以降
* にアクセスできるAdobe.com アカウント [Adobe Admin Console](https://adminconsole.adobe.com/).

この統合を設定する管理者には、モジュールのイネーブルメント時に次の資格情報が必要です。

* 組織 ID （取得元： [Adobe Admin Console](https://adminconsole.adobe.com/)）、24 文字以上にする必要があります。 認証済みユーザーは、この IMS 組織に属している必要があります。 組織 ID の検索について詳しくは、以下を参照してください。 [Experience Cloud内の組織](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* モジュールを有効にするには、Adobe Admin Consoleの組織レベルで 2FA を適用する必要があります。 チェック [認証設定](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* クライアント ID
* クライアント秘密鍵
* から API キーを取得すると、クライアント ID とクライアント秘密鍵を利用できるようになります [Adobe Developer コンソール](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Commerce 管理者ユーザーがログインするには、Adobe IDのアカウントを作成する必要があります。

## 一般的な手順

* からのAdobe組織 ID の取得 [Adobe Admin Console](https://adminconsole.adobe.com/)
* から新規プロジェクト、IMS API キーおよび秘密鍵を生成します。 [Adobe Developer コンソール](https://developer.adobe.com/)
* Adobe Admin ConsoleでのAdobe Commerce ユーザーの設定
* を有効にする `AdminAdobeIms` モジュール。

統合に成功するには、すべてのAdobe Commerce ユーザーが同じ名前とプライマリメールアドレスの管理者ユーザーアカウントを持っている必要があります。 一致する管理者ユーザーアカウントが存在しない場合、必要な権限を持つユーザー（通常は管理者の役割が割り当てられている）が手動で割り当てる必要があります [管理者ユーザーアカウントの作成](../systems/permissions-users-all.md#create-a-user) 同じ名前とメールを使用します。

## 統合の設定

システムアクセス権を持つ管理者または開発者が次の手順を完了した後、 _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_ボタンは、すべての管理者ユーザーの Commerce Admin ログインページに表示されます。

### 手順 1:Adobe組織 ID の取得

この機能を有効にするには、少なくとも 1 つの IMS 組織のメンバーシップが必要です。 Adobe IDがある場合、デフォルトで 1 つ以上のAdobe組織に属しています。 にログインします [Adobe Admin Console](https://adminconsole.adobe.com/) 組織 ID を取得します。

### 手順 2：新しいプロジェクト、IMS API キーおよび秘密鍵の生成

組織のプロジェクトを作成するには、その組織のAdobe管理者アカウントにシステム管理者または開発者のロールが必要です。 を参照してください。 [Developer Console ガイド](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. へのログイン [Adobe Developer コンソール](https://developer.adobe.com/).
1. に移動します **[!UICONTROL Projects]** tab （adobe.io/projects）を押してクリックします **[!UICONTROL Create a new project]**.
1. クリック **[!UICONTROL Add API]** 新しく作成したプロジェクトページ
1. を選択 **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. を選択 **[!UICONTROL Oauth 2.0 Web]**.
1. を指定 **[!UICONTROL Redirect URI]**: `https://<hostname>/`
1. を指定 **[!UICONTROL Redirect URI pattern]**: `https://<hostname>/.*`

   ホスト名のドットの前にを付けることで、ドットをエスケープします `\\`. URL の末尾にワイルドカードを追加すると、Adobe Commerce管理者の秘密鍵がサポートされます。

1. クリック **[!UICONTROL Save configured API]**.
1. をコピーします [!UICONTROL Client ID] および [!UICONTROL Client Secret] 作成されたプロジェクトのキー。

### 手順 3:Adobe Admin ConsoleでAdobe Commerce ユーザーを設定する

統合を有効にする前に、各Adobe Commerce管理者ユーザーアカウントが対応するAdobe IMSアカウントを持っていることを確認します。 Adobe Commerce ユーザーがAdobe IDでログインするには、特定のAdobe組織に属している必要があります。

>[!TIP]
>
>CSV ファイルからユーザー情報をアップロードすることで、複数のユーザーアカウントを作成できます。 参照： [複数ユーザーの管理](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. が含まれる [Adobe Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)に移動します。 **[!UICONTROL Users]**  > **[!UICONTROL Users]**.

1. クリック **[!UICONTROL Add User]**.

1. ユーザーのメールアドレスを入力します。

   該当する場合、推奨される ID タイプが自動的に入力されます。 この設定を、組織の購入プランに基づいた、リスト内の製品 ID のいずれかに変更できます。

   一度に 10 人までユーザーを追加できます。 さらに追加するには、変更を保存した後、上記の手順を繰り返します。

1. クリック **[!UICONTROL Save]**.

ユーザーが追加され、に表示されます [!UICONTROL Users] リスト。

### 手順 4:AdminAdobeIms モジュールを有効にする

この `AdminAdobeIms` モジュールは、Adobe CommerceとAdobe IMSの統合を担当します。 新しいプロジェクトを設定し、組織 ID、クライアント ID およびクライアント秘密鍵をコピーしたら、 `AdminAdobeIms` モジュール。

Enter `bin/magento admin:adobe-ims:enable`. 次のパラメーターを入力するよう求められます。 プロジェクトの作成時に生成された値を使用します。

* 組織 ID
* クライアント ID
* クライアント秘密鍵
* 2FA 有効

Adobe Commerceは、イネーブルメントが成功したか失敗したかを示すメッセージを表示します。

この機能を正常に有効にすると、他のAdobe Commerce Adobe IMSアカウントをユーザーアカウントに移行できます。 Adobe Commerce ユーザーがAdobe IDでログインするには、設定済みのAdobe組織に属している必要があります。
