---
title: ユーザーによるログイン
description: ストアフロントのカスタマーログイン機能により、お客様のアカウントに簡単にアクセスできます。
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# ユーザーによるログイン

顧客は、ストア内のすべてのページから自分のアカウントに簡単にアクセスできます。 応じて [設定](../customers/account-options-new.md)の場合、顧客はアカウントダッシュボードにリダイレクトしたり、アカウントにログインした後で買い物を続行したりできます。

次の場合 [CAPTCHA](../systems/security-captcha.md) が有効になっている設定では、ユーザーはアカウントにアクセスする前に、自分が人間であることを確認するテストを正しく完了する必要があります。

顧客がパスワードを忘れると、リセットリンクがそのアカウントに関連付けられているメールアドレスに送信されます。 この [パスワードオプション](../customers/password-options.md) 設定は、ログイン試行のカスタマーエクスペリエンスを制御します。

- 顧客がパスワードの入力を試みる回数
- 試行間隔（分）
- アカウントがロックされるまでの合計試行回数
- ロックアウトの長さ

![ストアフロントヘッダーのサインインリンク](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## 顧客アカウントにサインイン

1. ストアのヘッダーで、顧客は次をクリックします **[!UICONTROL Sign in]**.

   ![カスタマーログイン](assets/login.png){width="700" zoomable="yes"}

1. エントリ数 **[!UICONTROL Email]** 住所と **[!UICONTROL Password]**.

1. クリック数 **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >パスワードを思い出せない場合は、 **[!UICONTROL Forgot Your Password?]** およびフォロー [指示](../customers/password-reset.md) ：パスワードをリセットします。

## カスタマーログイン後のアカウントダッシュボードへのリダイレクトの設定

ログイン後に顧客を自分のアカウントダッシュボードにリダイレクトしたり、買い物を続行させたりするように、ストアを設定できます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Login Options]** セクション。

1. を設定 **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** を次のいずれかに変更します。

   - `Yes`  – 顧客が自分のアカウントにログインすると、アカウントダッシュボードが表示されます。
   - `No`  – 顧客はアカウントにログインした後も買い物を続けることができます。

1. 完了したら、 **[!UICONTROL Save Config]**.

## Amazonでログイン

が設定されているストアの場合 [!DNL Amazon Pay] および [!DNL Login with Amazon] 統合により、お客様はAmazonのバイヤーアカウントにログインできます。

1. ストアのヘッダーで、顧客は次をクリックします **[!UICONTROL Sign in]**.

1. クリック数 **[!UICONTROL Login with Amazon]**.

   ![Amazonでログイン](assets/amazon-pay.png){width="700" zoomable="yes"}

1. ログインを求めるメッセージが表示されたら、顧客は **[!UICONTROL email address]** および **[!UICONTROL password]** Amazonのバイヤーアカウント用。

   ![Amazon資格情報の入力](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. 購入処理時にAmazonに以下の情報をストアと共有する権限を付与するには、をクリックします **分かった**.

   - 名前
   - メールアドレス
   - 発送先住所

   ![データ共有の権限を付与](assets/amazon-popup2.png){width="700" zoomable="yes"}

## 顧客アカウントからのログアウト

1. の右上隅にある  _[!UICONTROL Welcome, Customer Name!]_顧客が&#x200B;**[!UICONTROL v]**メニューセレクター。

1. を選択 **[!UICONTROL Sign Out]**.

ログアウト後、顧客はホームページにリダイレクトされます。
