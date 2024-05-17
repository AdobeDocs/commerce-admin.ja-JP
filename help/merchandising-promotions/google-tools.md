---
title: Google サイトツール
description: コンテンツを最適化し、トラフィックを分析し、カタログをショッピングアグリゲータおよびマーケットプレイスに接続するために使用できる、Google ツール統合について説明します。
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Google サイトツール

ストア設定は、コンテンツを最適化し、トラフィックを分析し、カタログをショッピングアグリゲータおよびマーケットプレイスに接続するのに役立つ、次のGoogle ツールと統合されています。

- [Google Analytics](google-analytics.md)  – 使用 _Google Universal Analytics_ オフラインおよびモバイルアプリのインタラクションをサポートし、継続的な更新にアクセスできるので、トラッキング用の追加のカスタムディメンションと指標を定義できます。

- [Google コンテンツ実験](google-content-experiments.md) -Google Analyticsコンテンツ実験を使用して、製品、カテゴリまたはコンテンツページに対する A/B テストを設定します。

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）Google タグマネージャーを使用して、マーケティングキャンペーンイベントに関連する多くのタグを管理します。

- [Google AdWords](google-adwords.md) - Google AdWords キャンペーンを作成し、ストアのコンバージョンを追跡します。

{{gtag-api-note}}

## Google プライバシー設定

次のようなプライバシー規制に準拠する必要がある場合： [GDPR](../getting-started/compliance-gdpr.md) または [CCPA](../getting-started/compliance-ccpa.md)プライバシー要件を満たすようにGoogle ツールのデフォルト設定を変更します。 次の手順に従って、顧客データの使用が引き続きコンプライアンスに準拠していることを確認します。

### 手順 1:Google設定の更新

1. [ログイン][1]{: target=&quot;_blank&quot;} を会社のGoogle Analytics アカウントに追加します。

1. 左サイドバーの下部にある **[!UICONTROL Admin]**&#x200B;に移動した後、編集するアカウントに移動します（該当する場合）。

1. が含まれる **[!UICONTROL Account]** 列、クリック **[!UICONTROL Account Settings]**.

1. プライバシー規制の要件を満たすには、データ共有をオフにします。

   デフォルトのGoogle Analytics設定では、会社のデータがGoogleや他の関係者と共有されます。データ共有を無効にするには、次の設定のチェックボックスをオフにします。

   - Googleの製品とサービス
   - ベンチマーク
   - テクニカルサポート
   - アカウントスペシャリスト

1. を承認 _データ処理の修正_.

   Google Ads データ処理条件では、Googleによるデータの処理方法と、GDPR の対象となるビジネスのデータセキュリティを確保するために必要な対策について説明します。 法人の記録と連絡先情報も修正で維持されます。 終了 [詳細を表示する][2]{: target=&quot;_blank&quot;}、ページ上部のメッセージ内のリンクをクリックします。

   - ページを下にスクロールして、 **[!UICONTROL Data Processing Amendment]**.
   - クリック **[!UICONTROL Review Amendment]** を読む _Google広告のデータ処理条件_.
   - クリック **[!UICONTROL Accept]**.
   - クリック **[!UICONTROL Save]**.

1. を完了する _DPA 管理_ の詳細。

   - クリック **[!UICONTROL Manage DPA Details]** 連絡先と組織の法人を編集できる DPA 管理ページを開きます。

   - が含まれる **[!UICONTROL Legal Entities]** セクションで、 _編集_ （ ![Google編集アイコン](./assets/google-icon-edit.png) ） アイコンをクリックし、組織の登録済みの名前を 1 つ以上追加します。 完了したら、 **[!UICONTROL Save]**.

   - が含まれる **連絡先** セクションで、 _追加_ （ ![Google追加アイコン](./assets/google-icon-add.png) ）アイコンをクリックし、最初の連絡先の情報を入力します。 次に、該当する各役割のチェックボックスをオンにし、 **[!UICONTROL Add]**.

      - プライマリ連絡先 – （通知メールアドレス）通知の送信先の連絡先。
      - データ保護責任者 – （該当する場合）プライバシー規制のコンプライアンスを促進するために指定された人物。
      - 欧州経済領域（EEA）担当者 – （該当する場合） GDPR 義務に関して EU 外の顧客を代表する人物。

     必要に応じて、繰り返して別の連絡先を追加します。

### 手順 2:Google JS ライブラリを変更する

Googleでは、Google製品に応じて web サイトの使用状況を測定する 3 つの JavaScript ライブラリがサポートされています。 `gtag.js`, `analytics.js`、および `ga.js`. プライバシー要件を満たすために、標準コードを次のように変更できます。

#### IP アドレスの匿名化

で使用される IP アドレスを匿名化するには **_Google Universal Analytics_**&#x200B;次のスニペットをに追加します `analytics.js` web サーバー上のライブラリ：

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

詳しくは、 [Analytics.js フィールドリファレンス][3]Google ヘルプの {: target=&quot;_blank&quot;}。

レガシーを使用する場合 `ga.js` ライブラリに、次のスニペットを追加します。

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

で使用される IP アドレスを匿名化するには **_Google Tag Manager_**、を設定 `anonymize_ip` パラメーター先 `true` が含まれる `gtag.js` web サーバー上のライブラリ。

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

詳しくは、 [Analytics での IP の匿名化][4] （Google ヘルプ）。

#### SSL を強制

すべてのGoogle データを Secure Socket Layer （SSL）経由で強制的に送信するには、次のスニペットをに追加します。 `analytics.js` web サーバー上のライブラリ。

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### 手順 3：プライバシーポリシーを更新する

を更新 [プライバシーポリシー](../getting-started/privacy-policy.md) 会社について次のように述べます。

- Google Analyticsの使用
- IP アドレスをマスクして個人情報を非表示にする
- さんは、Google Data Sharing を無効にしました
- Google Analytics cookie で他のGoogle サービスを使用しない

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
