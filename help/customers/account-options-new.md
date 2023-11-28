---
title: 新しい顧客アカウントオプション
description: ストア内の新しい顧客アカウントの設定オプションについて説明します。
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# 新しい顧客アカウントオプション

Adobe Analytics の _[!UICONTROL Create New Account Options]_設定のセクションでは、基本的なアカウントオプションと、VAT ID 検証およびカスタム統合に関連するより高度なオプションが組み合わされています。 次の手順では、最も頻繁に使用されるオプションのみを示します。 自動顧客グループ割り当てについて詳しくは、 [VAT 検証](../stores-purchase/vat.md).

{{beta-updates}}

![新しいアカウントオプションの作成](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## 基本的な顧客アカウントオプションの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Create New Account Options]** セクション：

   ![新しいアカウントオプションの作成のデフォルト設定](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. ストアフロントでサポートする必要がある顧客体験に応じて、各オプションを設定します。

   - 設定 **[!UICONTROL Default Group]** アカウントの作成時に新規顧客に割り当てられる顧客グループに割り当てます。

   - 次の場合、 _付加価値税_ 数を指定して、顧客に表示する **[!UICONTROL Show VAT Number on Storefront]** から `Yes`.

   - 顧客の管理注文作成時に顧客の電子メールを要求するには、 **[!UICONTROL Email is required field for Admin order creation]** から `Yes`.

   - 次を入力します。 **[!UICONTROL Default Email Domain]** 次のようなストアの `mystore.com`

   - 設定 **[!UICONTROL Default Welcome Email]** を、新規顧客に送信するようこそメールに使用するテンプレートに追加します。

   - 設定 **[!UICONTROL Default Welcome Email without Password]** パスワードを持たない顧客アカウントの作成時に使用されるテンプレートに追加します。 例えば、管理者から作成された顧客アカウントには、まだパスワードが割り当てられていません。

   - 設定 **[!UICONTROL Email Sender]** ようこそメールの送信者として表示されるストアの連絡先。

   - ストアでアカウントを開くためのリクエストを顧客に確認するよう求めるには、 **[!UICONTROL Require Emails Confirmation]** から `Yes`. 次に、 **[!UICONTROL Confirmation Link Email]** を確認 E メールに使用するテンプレートに追加します。

   - 設定 **[!UICONTROL Welcome Email]** を、アカウントの確認後に送信されるようこそメッセージに使用されるテンプレートに追加します。

     ![VAT を有効にした新規アカウントオプションの作成](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

     この設定オプションセットで使用できる各オプションの詳細については、 _新しいアカウントオプションの作成_ [設定リファレンス](../configuration-reference/customers/customer-configuration.md).

1. 完了したら、「 **[!UICONTROL Save Config]**.
