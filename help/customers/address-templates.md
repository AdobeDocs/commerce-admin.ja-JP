---
title: 顧客の住所テンプレート
description: 顧客住所テンプレートのカスタマイズ方法を説明します。
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# 顧客の住所テンプレート

{{ee-feature}}

顧客アカウントのアドレス帳だけでなく、印刷された請求書、出荷、払い戻しに表示される、顧客の請求先および出荷先の形式を制御するテンプレートを変更できます。 追加情報を含める場合は、顧客アカウントおよび [ 住所 ](attribute-properties.md) に関連付けられた [ カスタム属性 ](address-attributes.md) を作成してテンプレートに組み込むことができます。

## 例 1：ショートフォーマット

アドレステンプレート [!UICONTROL Text One Line] 場合：

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## 例 2:long 形式

[!UICONTROL Text]、[!UICONTROL HTML]、[!UICONTROL PDF] のアドレステンプレートの場合：

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![ 顧客の住所テンプレート ](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## アドレスフィールドの順序の変更

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Customer Configuration]**」を選択します。

1. 「」をクリックして「**[!UICONTROL Address Templates]**」セクションを展開します。

   この節では、次の各項目について個別の書式設定手順を説明します。

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. 必要に応じて、例を参照しながら各テンプレートを編集します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
