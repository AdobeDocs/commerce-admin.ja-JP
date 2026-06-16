---
title: 顧客ログイン
description: ストアフロントの顧客ログイン機能により、顧客のアカウントに簡単にアクセスできます。
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/WuMuGVXByzb0PlpkKHnJCT-s7ToHtb1odvTu18LxB-I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 383
ht-degree: 0%

---

# 顧客ログイン

顧客は、ストアのあらゆるページから自分のアカウントに簡単にアクセスできます。 [設定](../customers/account-options-new.md)に応じて、お客様はアカウント ダッシュボードにリダイレクトするか、アカウントにログインした後にショッピングを続行できます。

設定で[CAPTCHA](../systems/security-captcha.md)が有効になっている場合、ユーザーはアカウントにアクセスする前に、人間であることを確認するテストを正しく完了する必要があります。

お客様がパスワードを忘れた場合、アカウントに関連付けられているメールアドレスにリセットリンクが送信されます。 [&#x200B; パスワードオプション &#x200B;](../customers/password-options.md)設定は、ログイン試行の顧客体験を制御します。

- 顧客がパスワードを入力しようとする回数
- 試行の間隔（分）
- アカウントがロックされるまでの合計試行回数
- ロックアウトの長さ

![&#x200B; ストアフロントヘッダーのサインインリンク &#x200B;](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## 顧客アカウントにログイン

1. ストアのヘッダーで、顧客は&#x200B;**[!UICONTROL Sign in]**&#x200B;をクリックします。

   ![お客様のログイン &#x200B;](assets/login.png){width="700" zoomable="yes"}

1. **[!UICONTROL Email]** アドレスと&#x200B;**[!UICONTROL Password]**&#x200B;を入力します。

1. **[!UICONTROL Sign in]**&#x200B;をクリックします。

   >[!IMPORTANT]
   >
   >パスワードを記憶できない場合、お客様は&#x200B;**[!UICONTROL Forgot Your Password?]**&#x200B;をクリックし、[手順](../customers/password-reset.md)に従ってパスワードをリセットできます。

## 顧客ログイン後にアカウントダッシュボードへのリダイレクトを設定する

ログイン後に顧客をアカウントダッシュボードにリダイレクトするか、ショッピングを続行するようにストアを設定できます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Customer Configuration]**&#x200B;を選択します。

1. **[!UICONTROL Login Options]** セクションを展開します。

1. **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]**&#x200B;を次のいずれかに設定します：

   - `Yes` – 顧客がアカウントにログインすると、アカウントダッシュボードが表示されます。
   - `No` – お客様は、アカウントにログインした後もショッピングを続けることができます。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## Amazonでログイン

[!DNL Amazon Pay]と[!DNL Login with Amazon]の統合が設定されているストアの場合、お客様はAmazon バイヤーアカウントにログインできます。

1. ストアのヘッダーで、顧客は&#x200B;**[!UICONTROL Sign in]**&#x200B;をクリックします。

1. **[!UICONTROL Login with Amazon]**&#x200B;をクリックします。

   ![Amazonでログイン &#x200B;](assets/amazon-pay.png){width="700" zoomable="yes"}

1. ログインを求められると、お客様はAmazon バイヤーアカウントの&#x200B;**[!UICONTROL email address]**&#x200B;と&#x200B;**[!UICONTROL password]**&#x200B;を入力します。

   ![Amazon資格情報を入力しています](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. 購入処理時にAmazonのアカウントから以下の情報を店舗と共有する権限を付与するには、**OK**&#x200B;をクリックします。

   - 名前
   - メールアドレス
   - 輸送先住所

   ![&#x200B; データを共有する権限を付与](assets/amazon-popup2.png){width="700" zoomable="yes"}

## 顧客アカウントからログアウトする

1. _[!UICONTROL Welcome, Customer Name!]_&#x200B;の横の右上隅で、顧客は&#x200B;**[!UICONTROL v]**&#x200B;メニューセレクターをクリックします。

1. **[!UICONTROL Sign Out]**&#x200B;を選択してください。

サインアウト後、お客様はホームページにリダイレクトされます。
