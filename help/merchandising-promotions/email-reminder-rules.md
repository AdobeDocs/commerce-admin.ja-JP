---
title: メールのリマインダー
description: 特定の条件のセットを満たした場合に、顧客に自動的に送信できるメールのリマインダーについて説明します。
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# メールのリマインダー

{{ee-feature}}

メールでリマインダーを送信する目的は、ストアを訪問したユーザーに対して、プロモーションを利用して購入を促すことです。 特定の条件セットを満たした場合に、メールでリマインダーを顧客に自動的に送信できます。 例えば、買い物かごやウィッシュリストに何かを追加したが、まだ購入していない顧客にリマインダーを送信できます。 メールのリマインダーを使用して、顧客がストアに戻るように促し、インセンティブとして [ クーポンコード ](price-rules-cart-coupon.md) を含めることができます。 クーポンコードは、メールのリマインダーのバッチごとに自動的に生成でき、各バッチに関連付けられているオファーを制御できます。

メールのリマインダーは、買い物かごが放棄されてから特定の日数が経過した後や、定義したい他の条件に対してトリガーできます。 一般的な条件には、買い物かごの合計値、数量、買い物かごの中の商品などがあります。

>[!NOTE]
>
>顧客に、一致する放棄された買い物かご、ウィッシュリストまたはその両方の組み合わせが複数ある場合、メールのリマインダーはその顧客に対して 1 回だけトリガーされます。 同じメールのリマインダーを再度トリガーするには、「_[!UICONTROL Repeat Schedule]_」フィールドを使用して、メール間の日数を設定します。

![ メールのリマインダー ](./assets/email-reminders.png){width="700" zoomable="yes"}

## メールのリマインダーの設定

メールのリマインダールールは、分、時間、または日ごとに定期的に送信できます。 この設定によって、1 つのバッチで送信されるメールの数と、メッセージの送信者として表示されるストア ID が決定されます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Promotions]**」を選択します。

1. **[!UICONTROL Automated Email Reminder Rules]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![ 顧客設定 – 自動メールリマインダールール ](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enable Reminder Emails]** を `Yes` に設定します。

   - 自動メールのリマインダーを受け取る新規顧客に対してチェックを実行する頻度を設定するには、**[!UICONTROL Frequency]** を次のいずれかに設定します。

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - _[!UICONTROL Frequency]_&#x200B;の設定に基づいて、適切な&#x200B;**[!UICONTROL Interval]**&#x200B;を設定します。

   - **[!UICONTROL Start Time]** を、24 時間の時間に基づいてメールを送信する時、分、秒に設定します。

   - 1 つのバッチで送信できるメールの数を制限するには、「**[!UICONTROL Maximum Emails per One Run]**」フィールドに数値を入力します。

   - 失敗したメールの送信を繰り返し試みないようにするには、最大試行回数を **[!UICONTROL Email Send Failure Threshold]** フィールドに入力します。

   - リマインダーメールの送信者として表示される [ 店舗連絡先 ](../getting-started/store-details.md#store-email-addresses) に **[!UICONTROL Reminder Email Sender]** を設定します。

   これらのオプションの詳細なリストについては、[ 設定リファレンス ](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) の _自動メールリマインダールール_ を参照してください。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## メールリマインダーテンプレート

デフォルトのメールリマインダーテンプレートはカスタマイズでき、様々なプロモーション用に追加のテンプレートを作成できます。 メールのリマインダーには、メッセージに組み込むことができる特定の変数の選択があります。 これらの変数の情報は、設定したメールリマインダールールと、クーポンに関連付けられた買い物かご価格ルールによって決定されます。 「変数の挿入」ボタンを使用すると、変数を含むマークアップタグをテンプレートに挿入できます。 詳しくは、[ メール ](../systems/email-templates.md) を参照してください。

![ メールリマインダーのプレビュー ](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### メールリマインダーテンプレートのカスタマイズ

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Communications]_/**[!UICONTROL Email Templates]**&#x200B;に移動します。

1. 「**[!UICONTROL Add New Template]**」をクリックします。

1. `Magento_Reminder` の下の **[!UICONTROL Template]** リストで、**[!UICONTROL Promotion Notification/Reminder]** テンプレートを選択します。

1. 「**[!UICONTROL Load Template]**」をクリックします。

標準 [ 手順 ](../systems/email-template-custom.md) に従って、テンプレートをカスタマイズします。

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
