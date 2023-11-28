---
title: 顧客パスワードのリセット
description: 通常、ユーザーはストアフロントからパスワードをリセットしますが、ストア管理者は、管理者からパスワードのリセットを開始するか、強制的にサインインすることができます。
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# 顧客パスワードのリセット

通常、ユーザーは、 _[!UICONTROL Forgot Your Password?]_. ただし、ストア管理者は、パスワードのリセットを開始するか、管理者から強制的にログインを開始することができます。

| 関数 | 説明 |
| --- | --- |
| パスワードをリセット | パスワードリセット用の電子メールが顧客の電子メールアカウントに直接送信されます。 ストア管理者は、顧客のパスワードにアクセスできません。 |
| 強制的にサインイン | 顧客アカウントに関連付けられている OAuth アクセストークンを取り消します。 これは、Web API の一部として OAuth トークンを割り当てた顧客アカウントでのみ使用できます [統合](../systems/integrations.md). 詳しくは、 [OAuth ベースの認証](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) （開発者向けドキュメント）。 <br/><br/>ストアフロントまたは管理者から作成された標準顧客アカウントには、OAuth トークンはありません。 |

{style="table-layout:auto"}

## ストアフロントからのパスワードのリセット

1. ログインページで、顧客が **[!UICONTROL Forgot Your Password?]**.

1. プロンプトが表示されたら、 **[!UICONTROL Email Address]** アカウントおよびクリックに関連付けられている **[!UICONTROL Reset My Password]**.

   ![パスワードを忘れた場合](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >入力した電子メールアドレスがアカウントに関連付けられている電子メールアドレスと一致する場合は、パスワードリセットの確認の電子メールが顧客に届き、パスワードをリセットするためのリンクが記載されています。

1. E メールが届くと、顧客は _パスワードをリセット_ リンクし、 **[!UICONTROL New Password]** プロンプトが表示されたら、

1. 再度入力して確定し、クリックする **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >新しいパスワードは、スペースを含まない 6 文字以上の長さにする必要があります。 パスワードの更新の確認を受け取ったユーザーは、新しいパスワードを使用して自分のアカウントにサインインできます。 デフォルトでは、 _パスワードをリセット_ リンクは 24 時間有効です。

## 管理者からのパスワードのリセット

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. グリッドで顧客アカウントを見つけ、 **[!UICONTROL Edit]** （内） _アクション_ 列。

1. ページ上部の一連のオプションで、「 **[!UICONTROL Reset Password]**.

   1 時間以内に許可されるパスワードリセット要求の数は、 [設定](../configuration-reference/customers/customer-configuration.md) トピック。

## 顧客の OAuth トークンの失効

>[!IMPORTANT]
>
>API 認証について完全に理解していない限り、続行しないでください。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. グリッドで顧客アカウントを見つけ、 **[!UICONTROL Edit]** （内） _アクション_ 列。

1. ページ上部の一連のオプションで、「 **[!UICONTROL Force Sign In]**.

1. 確認するメッセージが表示されたら、「 **OK**.
