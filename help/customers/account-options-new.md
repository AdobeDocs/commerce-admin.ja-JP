---
title: 新規顧客アカウントオプション
description: ストアの新しい顧客アカウントの設定オプションについて説明します。
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: 117720d06227a9122059a1f72fa498465b8cc644
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%
---
# 新規顧客アカウントオプション

設定の&#x200B;_[!UICONTROL Create New Account Options]_&#x200B;セクションでは、基本的なアカウントオプションと、VAT ID検証とカスタム統合に関連する高度なオプションが組み合わされています。 次の手順では、最も頻繁に使用されるオプションのみを説明します。 顧客グループの自動割り当てについて詳しくは、[VAT検証](../stores-purchase/vat.md)を参照してください。

![新しいアカウントオプションを作成](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## 基本的な顧客アカウントオプションの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > **[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Customer Configuration]**&#x200B;を選択します。

1. 「**[!UICONTROL Create New Account Options]**」セクションを展開します。

   ![新しいアカウント オプションの既定の設定を作成](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. ストアフロントでサポートする必要がある顧客体験に応じて、各オプションを設定します。

   - アカウントの作成時に新規顧客に割り当てられる顧客グループに&#x200B;**[!UICONTROL Default Group]**&#x200B;を設定します。

   - _付加価値税_&#x200B;の番号があり、それを顧客に表示する場合は、**[!UICONTROL Show VAT Number on Storefront]**&#x200B;を`Yes`に設定します。

   - 顧客の管理者注文作成中に顧客の電子メールを要求するには、**[!UICONTROL Email is required field for Admin order creation]**&#x200B;を`Yes`に設定します。

   - ストアの&#x200B;**[!UICONTROL Default Email Domain]**&#x200B;を入力します（`mystore.com`など）

   - **[!UICONTROL Default Welcome Email]**&#x200B;を、新規顧客に送信されるようこそメールに使用されるテンプレートに設定します。

   - ストアでアカウントを開くリクエストを顧客に確認してもらうには、**[!UICONTROL Require Emails Confirmation]**&#x200B;を`Yes`に設定します。 次に、確認メールに使用するテンプレートに&#x200B;**[!UICONTROL Confirmation Link Email]**&#x200B;を設定します。

     >[!NOTE]
     >
     >バージョン 2.4.7以降、お客様は、ブラウザーに関係なく、メール確認後にアカウントにログインするために、メールとパスワードを再入力する必要があります。

   - アカウントの確認後に送信されるようこそメッセージに使用されるテンプレートに&#x200B;**[!UICONTROL Welcome Email]**&#x200B;を設定します。

   - パスワードを持たない顧客アカウントの作成時に使用されるテンプレートに&#x200B;**[!UICONTROL Default Welcome Email without Password]**&#x200B;を設定します。 例えば、管理者から作成された顧客アカウントには、まだパスワードが割り当てられていません。

   - ようこそ電子メールの送信者として表示されるストア連絡先に&#x200B;**[!UICONTROL Email Sender]**&#x200B;を設定します。

   - ストアでアカウントを開くリクエストを顧客に確認してもらうには、**[!UICONTROL Require Emails Confirmation]**&#x200B;を`Yes`に設定します。 次に、確認メールに使用するテンプレートに&#x200B;**[!UICONTROL Confirmation Link Email]**&#x200B;を設定します。

   ![VATが有効になっている新しいアカウント オプションを作成](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   この設定オプションセットで使用できる各オプションについて詳しくは、_新しいアカウントオプションの作成_ [設定リファレンス &#x200B;](../configuration-reference/customers/customer-configuration.md)を参照してください。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
