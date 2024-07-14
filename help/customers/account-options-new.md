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

設定の _[!UICONTROL Create New Account Options]_のセクションでは、基本的なアカウントオプションと、VAT ID 検証およびカスタム統合に関連するより高度なオプションが組み合わされています。 以下の説明は、最も頻繁に使用されるオプションに関するものです。 顧客グループの自動割当の詳細は、[VAT 検証 ](../stores-purchase/vat.md) を参照してください。

![ 新規アカウントオプションの作成 ](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## 基本的な顧客アカウントオプションの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Customer Configuration]**」を選択します。

1. **[!UICONTROL Create New Account Options]** セクションを展開します。

   ![ 新規アカウントオプションのデフォルト設定の作成 ](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. ストアフロントでサポートする必要がある顧客体験に応じて、各オプションを設定します。

   - アカウントの作成時に新規顧客に割り当てられる顧客グループに **[!UICONTROL Default Group]** を設定します。

   - _付加価値税_ 番号があり、顧客に表示する場合は、**[!UICONTROL Show VAT Number on Storefront]** を `Yes` に設定します。

   - 顧客の管理者による注文の作成時に顧客の電子メールを要求するには、**[!UICONTROL Email is required field for Admin order creation]** を `Yes` に設定します。

   - ストアの **[!UICONTROL Default Email Domain]** を入力します（例：`mystore.com`）

   - 新規顧客に送信される「ようこそ」のメールに使用するテンプレートに **[!UICONTROL Default Welcome Email]** を設定します。

   - ストアでアカウントを開くリクエストを顧客に確認させるには、**[!UICONTROL Require Emails Confirmation]** を `Yes` に設定します。 次に、確認メールに使用するテンプレートに **[!UICONTROL Confirmation Link Email]** を設定します。

     >[!NOTE]
     >
     >バージョン 2.4.7 以降、ブラウザーに関係なく、メールによる確認後にアカウントにログインするには、メールとパスワードを再入力する必要があります。

   - アカウントの確認後に送信される「ようこそ」メッセージに使用するテンプレートに **[!UICONTROL Welcome Email]** を設定します。

   - パスワードを持たない顧客アカウントを作成する際に使用されるテンプレートに **[!UICONTROL Default Welcome Email without Password]** を設定します。 例えば、管理者から作成された顧客アカウントには、まだパスワードが割り当てられていません。

   - **[!UICONTROL Email Sender]** を、ようこそメールの送信者として表示されるストアの連絡先に設定します。

   - ストアでアカウントを開くリクエストを顧客に確認させるには、**[!UICONTROL Require Emails Confirmation]** を `Yes` に設定します。 次に、確認メールに使用するテンプレートに **[!UICONTROL Confirmation Link Email]** を設定します。

   ![VAT が有効な新規口座オプションの作成 ](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   この設定オプションセットで使用できる各オプションについて詳しくは、_新しいアカウントオプションの作成_ 設定リファレンス [ を参照してください ](../configuration-reference/customers/customer-configuration.md)。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
