---
title: メールのリマインダー
description: 特定の条件のセットを満たした場合に、顧客に自動的に送信できるメールのリマインダーについて説明します。
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# メールのリマインダー

{{ee-feature}}

メールでリマインダーを送信する目的は、ストアを訪問したユーザーに対して、プロモーションを利用して購入を促すことです。 特定の条件セットを満たした場合に、メールでリマインダーを顧客に自動的に送信できます。 例えば、買い物かごやウィッシュリストに何かを追加したが、まだ購入していない顧客にリマインダーを送信できます。 リマインダーをメールで使用すると、顧客にストアに戻るように促したり、 [クーポンコード](price-rules-cart-coupon.md) インセンティブとして。 クーポンコードは、メールのリマインダーのバッチごとに自動的に生成でき、各バッチに関連付けられているオファーを制御できます。

メールのリマインダーは、買い物かごが放棄されてから特定の日数が経過した後や、定義したい他の条件に対してトリガーできます。 一般的な条件には、買い物かごの合計値、数量、買い物かごの中の商品などがあります。

>[!NOTE]
>
>顧客に、一致する放棄された買い物かご、ウィッシュリストまたはその両方の組み合わせが複数ある場合、メールのリマインダーはその顧客に対して 1 回だけトリガーされます。 同じメールのリマインダーを再度トリガーするには、 _[!UICONTROL Repeat Schedule]_メールの間隔の日数を設定するフィールド。

![メールのリマインダー](./assets/email-reminders.png){width="700" zoomable="yes"}

## メールのリマインダーの設定

メールのリマインダールールは、分、時間、または日ごとに定期的に送信できます。 この設定によって、1 つのバッチで送信されるメールの数と、メッセージの送信者として表示されるストア ID が決定されます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Promotions]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Automated Email Reminder Rules]** を選択し、次の操作を実行します。

   ![顧客設定 – 自動メールリマインダールール](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - を設定 **[!UICONTROL Enable Reminder Emails]** 対象： `Yes`.

   - 自動メールのリマインダーを受け取る新規顧客に対してチェックを実行する頻度を設定するには、次のように設定します **[!UICONTROL Frequency]** を次のいずれかに変更します。

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - 適切な **[!UICONTROL Interval]**、に基づく _[!UICONTROL Frequency]_の設定値。

   - を設定 **[!UICONTROL Start Time]** 24 時間の時間に基づいて、メールが送信される時刻（時、分、秒）。

   - 1 つのバッチで送信できるメールの数を制限するには、次のフィールドに数を入力します **[!UICONTROL Maximum Emails per One Run]** フィールド。

   - 失敗したメールの送信を繰り返し試みないようにするには、最大試行回数をに入力します **[!UICONTROL Email Send Failure Threshold]** フィールド。

   - を設定 **[!UICONTROL Reminder Email Sender]** に [店舗の連絡先](../getting-started/store-details.md#store-email-addresses) これは、リマインダーメールの送信者として表示されます。

   これらのオプションの詳細なリストについては、を参照してください [自動メールリマインダールール](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) が含まれる _設定リファレンス_.

1. 完了したら、 **[!UICONTROL Save Config]**.

## メールリマインダーテンプレート

デフォルトのメールリマインダーテンプレートはカスタマイズでき、様々なプロモーション用に追加のテンプレートを作成できます。 メールのリマインダーには、メッセージに組み込むことができる特定の変数の選択があります。 これらの変数の情報は、設定したメールリマインダールールと、クーポンに関連付けられた買い物かご価格ルールによって決定されます。 「変数の挿入」ボタンを使用すると、変数を含むマークアップタグをテンプレートに挿入できます。 詳しくは、 [電子メール](../systems/email-templates.md).

![メールリマインダーのプレビュー](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### メールリマインダーテンプレートのカスタマイズ

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. クリック **[!UICONTROL Add New Template]**.

1. が含まれる **[!UICONTROL Template]** リストの下 `Magento_Reminder`、を選択します **[!UICONTROL Promotion Notification/Reminder]** テンプレート。

1. クリック **[!UICONTROL Load Template]**.

標準に従う [指示](../systems/email-template-custom.md) テンプレートをカスタマイズします。

### メールリマインダー変数

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

#### E メール フッターテンプレート

```
{{template config_path="design/email/footer_template"}}
```

#### メールヘッダーテンプレート

```
{{template config_path="design/email/header_template"}}
```

#### 電子メールロゴ画像の代替

```
{{var logo_alt}}
```

#### 電子メールロゴ画像 URL

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
