---
title: 顧客パスワードのリセット
description: お客様は通常、ストアフロントからパスワードをリセットしますが、ストア管理者は、パスワードのリセットまたは管理者からの強制サインインを開始できます。
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 顧客パスワードのリセット

お客様は通常、次のボタンをクリックしてストアフロントからパスワードをリセットします。 _[!UICONTROL Forgot Your Password?]_. ただし、ストア管理者は、パスワードのリセットまたは管理者からの強制サインインを開始できます。

| 関数 | 説明 |
| --- | --- |
| パスワードをリセット | パスワードリセットメールが、顧客のメールアカウントに直接送信されます。 ストア管理者は、顧客のパスワードにアクセスできません。 |
| サインインを強制 | 顧客アカウントに関連付けられている OAuth アクセストークンを失効させます。 これは、Web API の一部として OAuth トークンが割り当てられているユーザーアカウントでのみ使用できます [統合](../systems/integrations.md). 詳しくは、 [OAuth ベースの認証](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) 開発者向けドキュメント <br/><br/>ストアフロントまたは管理者から作成された標準の顧客アカウントには、OAuth トークンがありません。 |

{style="table-layout:auto"}

## ストアフロントからのパスワードのリセット

1. ログインページで、をクリックします **[!UICONTROL Forgot Your Password?]**.

1. プロンプトが表示されたら、と入力します **[!UICONTROL Email Address]** これは、ユーザーのアカウントとクリックに関連付けられています **[!UICONTROL Reset My Password]**.

   ![パスワードを忘れた場合](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >入力したメールアドレスがアカウントに関連付けられているメールアドレスと一致する場合、パスワードをリセットするためのリンクが記載されたパスワードリセット確認メールが届きます。

1. メールが届いたら、顧客は _パスワードをリセット_ リンクしてユーザーに入力 **[!UICONTROL New Password]** プロンプトが表示されたら、

1. 再度入力して確認とクリックを行います **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >新しいパスワードの長さは、6 文字以上（スペースを含まない）にする必要があります。 パスワードが更新されたことを確認するメッセージが表示されたら、新しいパスワードを使用して自分のアカウントにログインできます。 デフォルトでは、 _パスワードをリセット_ リンクは 24 時間有効です。

## 管理者からのパスワードのリセット

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. グリッドで顧客アカウントを見つけて、 **[!UICONTROL Edit]** が含まれる _アクション_ 列。

1. ページ上部にある一連のオプションで、 **[!UICONTROL Reset Password]**.

   1 時間以内に許可されるパスワードリセット要求の数は、 [設定](../configuration-reference/customers/customer-configuration.md) トピック。

## 顧客の OAuth トークンの失効

>[!IMPORTANT]
>
>API 認証について完全に理解している場合以外は、続行しないでください。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. グリッドで顧客アカウントを見つけて、 **[!UICONTROL Edit]** が含まれる _アクション_ 列。

1. ページ上部にある一連のオプションで、 **[!UICONTROL Force Sign In]**.

1. 確認を求められたら、 **OK**.
