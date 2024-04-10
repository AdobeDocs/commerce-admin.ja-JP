---
title: 新しい顧客アカウントのオプション
description: ストア内の新しいカスタマーアカウントの設定オプションについて説明します。
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# 新しい顧客アカウントのオプション

が含まれる _[!UICONTROL Create New Account Options]_設定のセクションでは、基本的なアカウントオプションは、VAT ID 検証とカスタム統合に関連するより高度なオプションと組み合わされています。 以下の説明は、最も頻繁に使用されるオプションに関するものです。 顧客グループの自動割り当てについては、を参照してください。 [VAT 検証](../stores-purchase/vat.md).

![新しいアカウントオプションを作成](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## 基本的な顧客アカウントオプションの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Create New Account Options]** セクション：

   ![新しいアカウントオプションのデフォルト設定の作成](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. ストアフロントでサポートする必要がある顧客体験に応じて、各オプションを設定します。

   - を設定 **[!UICONTROL Default Group]** 新規アカウントの作成時に新規顧客に割り当てられる顧客グループ。

   - 次がある場合： _付加価値税_ 数値を入力し、顧客に表示する、と設定します **[!UICONTROL Show VAT Number on Storefront]** 対象： `Yes`.

   - 顧客の管理者による注文を作成する際に顧客のメールを要求するには、次のように設定します **[!UICONTROL Email is required field for Admin order creation]** 対象： `Yes`.

   - を入力 **[!UICONTROL Default Email Domain]** ストア用（例：） `mystore.com`

   - を設定 **[!UICONTROL Default Welcome Email]** 新規のお客様に送信されるお知らせメールに使用されるテンプレート。

   - ストアでアカウントを開設するリクエストを顧客に確認してもらうには、次のように設定します。 **[!UICONTROL Require Emails Confirmation]** 対象： `Yes`. 次に、を設定します **[!UICONTROL Confirmation Link Email]** を確認メールに使用されるテンプレートに追加します。

     >[!NOTE]
     >
     >バージョン 2.4.7 以降、ブラウザーに関係なく、メールによる確認後にアカウントにログインするには、メールとパスワードを再入力する必要があります。

   - を設定 **[!UICONTROL Welcome Email]** を、アカウントの確認後に送信されるようこそメッセージに使用されるテンプレートに追加します。

   - を設定 **[!UICONTROL Default Welcome Email without Password]** を、パスワードのない顧客アカウントの作成時に使用されるテンプレートに変更します。 例えば、管理者から作成された顧客アカウントには、まだパスワードが割り当てられていません。

   - を設定 **[!UICONTROL Email Sender]** ウェルカムメールの送信者として表示される店舗連絡先に送信されます。

   - ストアでアカウントを開設するリクエストを顧客に確認してもらうには、次のように設定します。 **[!UICONTROL Require Emails Confirmation]** 対象： `Yes`. 次に、を設定します **[!UICONTROL Confirmation Link Email]** を確認メールに使用されるテンプレートに追加します。

   ![VAT が有効な新規口座オプションの作成](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   このコンフィギュレーションオプションセットで使用できる各オプションの詳細については、 _新しいアカウントオプションを作成_ [設定リファレンス](../configuration-reference/customers/customer-configuration.md).

1. 完了したら、 **[!UICONTROL Save Config]**.
