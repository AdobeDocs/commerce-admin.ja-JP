---
title: 顧客アドレステンプレート
description: 顧客アドレステンプレートをカスタマイズする方法を説明します。
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# 顧客アドレステンプレート

{{ee-feature}}

印刷された請求書、出荷、返金に表示される顧客請求および配送先住所の形式、および顧客アカウントの住所帳を制御するテンプレートを変更できます。 追加情報を含める場合は、 [カスタム属性](attribute-properties.md) 顧客アカウントに関連付けられている [住所](address-attributes.md)を作成し、テンプレートに組み込みます。

## 例 1：短い形式

の場合 [!UICONTROL Text One Line] アドレステンプレート：

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## 例 2：長い形式

の場合 [!UICONTROL Text], [!UICONTROL HTML]、および [!UICONTROL PDF] アドレステンプレート：

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![顧客アドレステンプレート](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## 住所フィールドの順序を変更する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択し、 **[!UICONTROL Customer Configuration]**.

1. をクリックして、 **[!UICONTROL Address Templates]** 」セクションに入力します。

   このセクションには、次の各項目に対して個別の書式設定手順が含まれています。

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. 必要に応じて、参照用の例を使用して各テンプレートを編集します。

1. 完了したら、「 **[!UICONTROL Save Config]**.
