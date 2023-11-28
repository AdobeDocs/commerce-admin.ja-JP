---
title: 電子メールリマインダー
description: 特定の条件が満たされた場合に顧客に自動的に送信される電子メールリマインダーについて説明します。
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# 電子メールリマインダー

{{ee-feature}}

電子メールのリマインダーの目的は、店舗を訪問した人にプロモーションを活用して購入を促すことです。 特定の条件が満たされた場合に、電子メールのリマインダーを自動的に顧客に送信できます。 例えば、買い物かごやウィッシュリストに何かを追加したがまだ購入していない顧客にリマインダーを送信できます。 電子メールのリマインダーを使用して、顧客がストアに戻るよう促したり、 [クーポンコード](price-rules-cart-coupon.md) インセンティブとして。 クーポンコードは、電子メールのリマインダーの各バッチに対して自動的に生成され、各バッチに関連付けられるオファーを制御できます。

電子メールリマインダーは、買い物かごが破棄されてから特定の日数が経過した後、または定義する他の条件に対してトリガーできます。 一般的な条件には、合計買い物かごの値、数量、買い物かご内の品目などがあります。

>[!NOTE]
>
>顧客に対して、一致しなかった買い物かご、ウィッシュリストまたはその両方の組み合わせが複数ある場合、その顧客に対して電子メールリマインダーが 1 回だけトリガーされます。 同じ電子メールリマインダーを再度トリガーするには、 _[!UICONTROL Repeat Schedule]_フィールドを使用してメール間の日数を設定します。

![電子メールリマインダー](./assets/email-reminders.png){width="700" zoomable="yes"}

## 電子メールリマインダーの設定

電子メールリマインダールールは、分、時間または日単位で一定の間隔で送信できます。 この設定によって、1 回のバッチで送信される E メールの数と、メッセージの送信者として表示されるストア ID が決まります。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Promotions]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Automated Email Reminder Rules]** 」セクションで次の操作を実行します。

   ![顧客設定 — 自動電子メールリマインダールール](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Enable Reminder Emails]** から `Yes`.

   - 自動電子メールリマインダーを検証する新規顧客のチェックを実行する頻度を設定するには、 **[!UICONTROL Frequency]** を次のいずれかに変更します。

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - 適切な **[!UICONTROL Interval]**、 _[!UICONTROL Frequency]_設定。

   - 設定 **[!UICONTROL Start Time]** を時、分、秒の間に 24 時間形式で電子メールが送信されます。

   - バッチで送信できる E メールの数を制限するには、 **[!UICONTROL Maximum Emails per One Run]** フィールドに入力します。

   - 失敗した E メールを繰り返し送信しないようにするには、 **[!UICONTROL Email Send Failure Threshold]** フィールドに入力します。

   - 設定 **[!UICONTROL Reminder Email Sender]** から [ストア連絡先](../getting-started/store-details.md#store-email-addresses) リマインダーの E メールの送信者として表示される

   これらのオプションの詳細なリストについては、 [自動電子メールリマインダールール](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) （内） _設定リファレンス_.

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 電子メールリマインダーテンプレート

デフォルトの電子メールリマインダーテンプレートをカスタマイズしたり、様々なプロモーション用に追加のテンプレートを作成したりできます。 電子メールのリマインダーには、メッセージに組み込むことのできる様々な変数があります。 これらの変数の情報は、設定した電子メールリマインダールールと、クーポンに関連付けられた買い物かごの価格ルールによって決定されます。 「変数を挿入」ボタンを使用すると、変数を含むマークアップタグをテンプレートに挿入できます。 詳しくは、 [電子メール](../systems/email-templates.md).

![電子メールリマインダーのプレビュー](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### 電子メールリマインダーテンプレートのカスタマイズ

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. クリック **[!UICONTROL Add New Template]**.

1. Adobe Analytics の **[!UICONTROL Template]** の下のリスト `Magento_Reminder`、選択 **[!UICONTROL Promotion Notification/Reminder]** テンプレート。

1. クリック **[!UICONTROL Load Template]**.

標準に従う [instructions](../systems/email-template-custom.md) をクリックして、テンプレートをカスタマイズします。

### 電子メールリマインダー変数

#### クーポンコード

```
{{var coupon.getCode()|escape}}
```

#### クーポン使用制限

```
{{var coupon.usage_limit|escape}}
```

#### 顧客ごとのクーポン使用状況

```
{{var coupon.usage_per_customer|escape}}
```

#### 顧客アカウント URL

```
{{var this.getUrl($store,'customer/account/',[_nosid:1])}}
```

#### 顧客名

```
{{var customer_data.name|escape}}
```

#### 電子メールフッターテンプレート

```
{{template config_path="design/email/footer_template"}}
```

#### メールヘッダーテンプレート

```
{{template config_path="design/email/header_template"}}
```

#### メールロゴ画像 Alt

```
{{var logo_alt}}
```

#### メールロゴ画像 URL

```
{{var logo_url}}
```

#### プロモーションの説明

```
{{var promotion_description|escape|nl2br}}
```

#### プロモーション名

```
{{var promotion_name|escape}}
```

#### ストア名

```
{{var store.frontend_name}}
```

#### ストア URL

```
{{store url=""}}
```
