---
title: Google サイトツール
description: コンテンツを最適化し、トラフィックを分析し、カタログをショッピングアグリゲータおよびマーケットプレイスに接続するために使用できる、Google ツール統合について説明します。
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Google サイトツール

ストア設定は、コンテンツを最適化し、トラフィックを分析し、カタログをショッピングアグリゲータおよびマーケットプレイスに接続するのに役立つ、次のGoogle ツールと統合されています。

- [Google Analytics](google-analytics.md) - _Google Universal Analytics_ を使用すると、オフラインおよびモバイルアプリのインタラクションをサポートし、継続的な更新にアクセスできるので、トラッキング用にさらにカスタムディメンションと指標を定義できます。

- [Google タグマネージャー ](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） Google タグマネージャーを使用して、マーケティングキャンペーンイベントに関連する多くのタグを管理します。

- [Google AdWords](google-adwords.md) - Google AdWords キャンペーンを作成し、ストアのコンバージョンを追跡します。

{{gtag-api-note}}

## Google プライバシー設定

[GDPR](../getting-started/compliance-gdpr.md) または [CCPA](../getting-started/compliance-ccpa.md) などのプライバシー規制に準拠する必要がある場合は、プライバシー要件を満たすようにGoogle ツールのデフォルト設定を変更します。 次の手順に従って、顧客データの使用が引き続きコンプライアンスに準拠していることを確認します。

### 手順 1:Google設定の更新

1. 会社のGoogle Analytics アカウントに [ ログイン ](https://www.google.com/analytics/){: target="_blank"} します。

1. 左側のサイドバーの下部で「**[!UICONTROL Admin]**」を選択し、編集するアカウントに移動します（該当する場合）。

1. 「**[!UICONTROL Account]**」列で「**[!UICONTROL Account Settings]**」をクリックします。

1. プライバシー規制の要件を満たすには、データ共有をオフにします。

   デフォルトのGoogle Analytics設定では、会社のデータがGoogleや他の関係者と共有されます。データ共有を無効にするには、次の設定のチェックボックスをオフにします。

   - Googleの製品とサービス
   - ベンチマーク
   - テクニカルサポート
   - アカウントスペシャリスト

1. _データ処理の修正_ を受け入れます。

   Google Ads データ処理条件では、Googleによるデータの処理方法と、GDPR の対象となるビジネスのデータセキュリティを確保するために必要な対策について説明します。 法人の記録と連絡先情報も修正で維持されます。 [ 詳細情報 ](https://support.google.com/analytics/answer/3379636){: target="_blank"} するには、ページ上部のメッセージ内のリンクをクリックします。

   - **[!UICONTROL Data Processing Amendment]** までページを下にスクロールします。
   - **[!UICONTROL Review Amendment]** をクリックして、_Google Ads データ処理条件_ をお読みください。
   - 「**[!UICONTROL Accept]**」をクリックします。
   - 「**[!UICONTROL Save]**」をクリックします。

1. _DPA 管理_ の詳細を入力します。

   - 「**[!UICONTROL Manage DPA Details]**」をクリックすると、DPA 管理ページが開き、担当者および組織の法的エンティティを編集できます。

   - 「**[!UICONTROL Legal Entities]**」セクションで、「_編集_ （![Google編集アイコン ](./assets/google-icon-edit.png)）」アイコンをクリックし、組織の 1 つ以上の登録名を追加します。 完了したら、「**[!UICONTROL Save]**」をクリックします。

   - 「**連絡先**」セクションで、「_追加_ （![Google追加アイコン ](./assets/google-icon-add.png)）」アイコンをクリックして、最初の連絡先の情報を入力します。 次に、該当する各役割のチェックボックスをオンにして、「**[!UICONTROL Add]**」をクリックします。

      - プライマリ連絡先 – （通知メールアドレス）通知の送信先の連絡先。
      - データ保護責任者 – （該当する場合）プライバシー規制のコンプライアンスを促進するために指定された人物。
      - 欧州経済領域（EEA）担当者 – （該当する場合） GDPR 義務に関して EU 外の顧客を代表する人物。

     必要に応じて、繰り返して別の連絡先を追加します。

### 手順 2:Google JS ライブラリを変更する

Googleでは、Google製品に応じて web サイトの使用状況を測定する 3 つのJavaScript ライブラリ（`gtag.js`、`analytics.js`、`ga.js`）がサポートされています。 プライバシー要件を満たすために、標準コードを次のように変更できます。

#### IP アドレスの匿名化

**_Google Universal Analytics_** で使用される IP アドレスの匿名化を行うには、次のスニペットを Web サーバー上の `analytics.js` ライブラリに追加します。

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

詳しくは、Google ヘルプの [Analytics.js フィールドリファレンス ](https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference){: target="_blank"} を参照してください。

従来の `ga.js` ライブラリを使用する場合は、次のスニペットを追加します。

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

**_Google Tag Manager_** で使用される IP アドレスを匿名化するには、Web サーバー上の `anonymize_ip` ライブラリで `true` パラメーターを `gtag.js` に設定します。

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

詳しくは、Google ヘルプの [Analytics での IP 匿名化 ](https://support.google.com/analytics/answer/2763052) を参照してください。

#### SSL を強制

すべてのGoogle データを Secure Socket Layer （SSL）経由で強制的に送信するには、次のスニペットを web サーバーの `analytics.js` ライブラリに追加します。

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### 手順 3：プライバシーポリシーを更新する

[ プライバシーポリシー ](../getting-started/privacy-policy.md) を更新し、会社について説明します。

- Google Analyticsの使用
- IP アドレスをマスクして個人情報を非表示にする
- さんは、Google Data Sharing を無効にしました
- Google Analytics cookie で他のGoogle サービスを使用しない
