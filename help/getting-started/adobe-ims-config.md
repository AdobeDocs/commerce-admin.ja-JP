---
title: IDを使用したCommerce管理者統合の設定
description: Adobe Commerce管理者ユーザーアカウントのログイン情報をAdobe IDと統合するには、次のオプション手順に従います。
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/gpbB0FZxHJdlef-Xv6DIMs4ixUg1R4kZxF6Hau94n9o
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 919
ht-degree: 1%

---

# Adobe IDとのCommerce管理者統合の設定

{{ee-feature}}

この統合は、Commerceを使用している管理者ユーザーと、Adobe IDおよびAdobe Business製品へのログインを効率化したい管理者ユーザーのAdobe Commerce マーチャントをサポートします。これはオプションであり、インスタンスごとに有効になります。有効にすると、管理者ユーザーワークフローのみが影響を受けます。 

>[!IMPORTANT]
>
>AdobeIms統合はグローバルに適用されています。 有効にすると、すべてのユーザーがAdobeImsを通じて認証する必要があります。 個々のユーザーをこの設定から除外することはできず、個々のユーザーのユーザー名とパスワードログインは使用できなくなりました。
>
>管理者ユーザーは、この統合を有効にする前に、Commerce管理者の資格情報（ユーザー名とパスワード）と2FAの資格情報を保存する必要があります。 IMS統合が無効になっている場合は、これらの資格情報が必要です。

## 前提条件

* Adobe Commerce 2.4.5以降
* [Adobe Admin Console](https://adminconsole.adobe.com/)にアクセスできるAdobe.com アカウント。

  >[!NOTE]
  >
  >Adobe Commerce管理コンソールへのアクセス権がない場合は、アカウントチームにアクセス権のプロビジョニングをリクエストします。

この統合を設定する管理者は、モジュールのイネーブルメント時に次の資格情報を必要とします。

* 組織ID （[Adobe Admin Console](https://adminconsole.adobe.com/)から取得）。24文字以上にする必要があります。 認証されたユーザーは、このIMS組織に属している必要があります。 組織IDの検索について詳しくは、[Experience Cloudの組織](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html)を参照してください。
* 2FAをAdobe Admin Consoleの組織レベルで適用して、モジュールを有効にする必要があります。 [認証設定](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification)を確認してください。
* クライアント ID
* クライアント秘密鍵
* クライアント IDとクライアント シークレットは、[Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials)からAPI キーを取得した後に使用できます。

Commerce管理者ユーザーがログインするには、Adobe IDでアカウントを作成する必要があります。

## 一般的な手順

* [Adobe Admin Console](https://adminconsole.adobe.com/)からAdobe組織IDを取得
* [Adobe Developer Console](https://developer.adobe.com/)から新しいプロジェクト、IMS API キー、およびシークレットを生成します
* Adobe Admin ConsoleでのAdobe Commerce ユーザーの設定
* `AdminAdobeIms` モジュールを有効にします。

統合を成功させるには、すべてのAdobe Commerce ユーザーが同じ名前とプライマリメールアドレスの管理者ユーザーアカウントを持っている必要があります。 一致する管理者ユーザーアカウントが存在しない場合、必要な権限を持つユーザー（通常は管理者の役割が割り当てられている）は、同じ名前と電子メールで[管理者ユーザーアカウント &#x200B;](../systems/permissions-users-all.md#create-a-user)を手動で作成する必要があります。

## 統合の設定

次の手順がシステム アクセス権を持つ管理者または開発者によって完了すると、すべての管理者ユーザーのCommerce管理者ログインページに「_[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_」ボタンが表示されます。

### 手順1:Adobe組織IDの取得

この機能を有効にするには、少なくとも1つのIMS組織のメンバーシップが必要です。 Adobe IDをお持ちの場合は、デフォルトで少なくとも1つのAdobe組織に属しています。 [Adobe Admin Console](https://adminconsole.adobe.com/)にログインして、組織IDを取得します。

### 手順2：新しいプロジェクト、IMS API キー、秘密鍵の生成

組織のプロジェクトを作成するには、その組織のAdobe管理者アカウントにシステム管理者または開発者の役割が必要です。 [Developer Console ガイド &#x200B;](https://developer.adobe.com/developer-console/docs/guides/projects/)を参照してください。

1. [Adobe Developer Console](https://developer.adobe.com/)にログインします。
1. **[!UICONTROL Projects]** タブ （adobe.io/projects）に移動し、**[!UICONTROL Create a new project]**&#x200B;をクリックします。
1. 新しく作成したプロジェクト ページで「**[!UICONTROL Add API]**」をクリックします。
1. **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**&#x200B;を選択します。
1. **[!UICONTROL Oauth 2.0 Web]**&#x200B;を選択します。
1. **[!UICONTROL Redirect URI]**&#x200B;を指定：`https://<commerce_base_url>/`
1. **[!UICONTROL Redirect URI pattern]**&#x200B;を指定：`https://<commerce_base_url>/.*`

   ホスト名のドットの前に`\\`を付けてエスケープします。 URLの末尾にワイルドカードを追加すると、Adobe Commerce管理者の秘密鍵がサポートされます。

1. **[!UICONTROL Save configured API]**&#x200B;をクリックします。
1. 作成したプロジェクトから[!UICONTROL Client ID]と[!UICONTROL Client Secret]個のキーをコピーします。

### 手順3:Adobe Admin ConsoleでのAdobe Commerce ユーザーの設定

統合を有効にする前に、各Adobe Commerce管理者ユーザーアカウントに対応するAdobe IMSアカウントがあることを確認します。 Adobe Commerce ユーザーは、Adobe IDを使用してログインするには、特定のAdobe組織に属している必要があります。

>[!TIP]
>
>CSV ファイルからユーザー情報をアップロードすることで、複数のユーザーアカウントを作成できます。 [複数のユーザーの管理](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html)を参照してください。

1. [Adobe Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)で、**[!UICONTROL Users]** > **[!UICONTROL Users]**&#x200B;に移動します。

1. **[!UICONTROL Add User]**&#x200B;をクリックします。

1. ユーザーのメールアドレスを入力します。

   該当する場合、推奨ID タイプは自動的に入力されます。 この設定は、組織の購入計画に基づいて、リスト内の製品IDのいずれかに変更できます。

   一度に最大10人のユーザーを追加できます。 さらに追加するには、変更を保存した後で、上記の手順を繰り返します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

ユーザーが追加され、[!UICONTROL Users] リストに表示されます。

### 手順4:AdminAdobeIms モジュールの有効化

`AdminAdobeIms` モジュールは、Adobe CommerceとAdobe IMSの統合を担当します。 新しいプロジェクトを設定し、組織ID、クライアント ID、およびクライアント秘密鍵をコピーしたら、`AdminAdobeIms` モジュールを有効にできます。

`bin/magento admin:adobe-ims:enable`と入力します。 次のパラメーターを入力するよう求められます。 プロジェクトの作成中に生成された値を使用します。

* 組織ID
* クライアント ID
* クライアント秘密鍵
* 2FA有効

Adobe Commerceには、イネーブルメントが成功したか失敗したかを示すメッセージが表示されます。

この機能を正常に有効にした後、他のAdobe Commerce ユーザーアカウントをAdobe IMSアカウントに移行できます。 Adobe IDを使用してログインするには、Adobe Commerce ユーザーが設定済みのAdobe組織に属している必要があります。

## IDとシングルサインオン

Adobe ID、Enterprise ID、Federated IDなどのID設定オプションと、Adobe アプリへの安全なアクセス用にシングルサインオン（SSO）を設定する手順について詳しくは、*Enterprise Admin Console* ドキュメントの[IDとシングルサインオンの設定](https://helpx.adobe.com/enterprise/using/set-up-identity.html)を参照してください。
