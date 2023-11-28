---
title: Google site tools
description: コンテンツの最適化、トラフィックの分析、カタログの買い物集約者やマーケットプレイスへの接続に使用できるGoogleツールの統合について説明します。
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Google site tools

ストア設定は、次のGoogleツールと統合され、コンテンツの最適化、トラフィックの分析、カタログの買い物集約やマーケットプレイスへの接続に役立ちます。

- [Google Analytics](google-analytics.md)  — 用途 _Google Universal Analytics_ を使用して、オフラインおよびモバイルアプリのインタラクションをサポートし、継続的な更新にアクセスできるように、追跡用の追加のカスタムディメンションおよび指標を定義します。

- [Google Content Experiment](google-content-experiments.md)  — 製品、カテゴリ、コンテンツページに対して、Google AnalyticsContent Experiment を使用して A/B テストを設定します。

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ )Google Tag Manager を使用して、マーケティングキャンペーンイベントに関連する多数のタグを管理します。

- [Google AdWords](google-adwords.md) - Google AdWords キャンペーンを作成し、ストアのコンバージョンを追跡します。

{{gtag-api-note}}

## Googleのプライバシー設定

ビジネスが、 [GDPR](../getting-started/compliance-gdpr.md) または [CCPA](../getting-started/compliance-ccpa.md)のデフォルト設定を変更し、プライバシー要件を満たすようにGoogleツールのデフォルト設定を変更します。 顧客データの使用にコンプライアンスを維持するには、次の手順に従います。

### 手順 1:Google設定の更新

1. [ログイン][1]{: target=&quot;_blank&quot;} を貴社のGoogle Analyticsアカウントに追加します。

1. 左側のサイドバーの下部で、「 **[!UICONTROL Admin]**&#x200B;をクリックし、編集するアカウント（該当する場合）に移動します。

1. Adobe Analytics の **[!UICONTROL Account]** 列、クリック **[!UICONTROL Account Settings]**.

1. プライバシー規制の要件を満たすために、データ共有を無効にします。

   デフォルトのGoogle Analytics設定は、会社データをGoogleやその他の関係者と共有します。データの共有を無効にするには、次の設定の選択チェックボックスをオフにします。

   - Google Products &amp; Services
   - ベンチマーク
   - テクニカルサポート
   - アカウントスペシャリスト

1. を受け入れる _データ処理の修正_.

   Google Ads のデータ処理用語では、Googleがデータを処理する方法と、GDPR の対象となるビジネスのデータセキュリティを確保するために必要な措置について説明します。 法人および連絡先情報の記録も、修正に伴って管理されます。 宛先 [詳細情報][2]{: target=&quot;_blank&quot;} の場合は、ページ上部のメッセージに表示されるリンクをクリックします。

   - ページを下にスクロールして **[!UICONTROL Data Processing Amendment]**.
   - クリック **[!UICONTROL Review Amendment]** 読む _Google Ads のデータ処理用語_.
   - クリック **[!UICONTROL Accept]**.
   - クリック **[!UICONTROL Save]**.

1. 次を完了： _DPA 管理_ 詳細。

   - クリック **[!UICONTROL Manage DPA Details]** をクリックして DPA 管理ページを開き、連絡先と組織の法人を編集できます。

   - Adobe Analytics の **[!UICONTROL Legal Entities]** セクションで、 _編集_ ( ![Google編集アイコン](./assets/google-icon-edit.png) ) アイコンをクリックし、組織に 1 つ以上の登録済み名前を追加します。 完了したら、「 **[!UICONTROL Save]**.

   - Adobe Analytics の **連絡先** セクションで、 _追加_ ( ![Google追加アイコン](./assets/google-icon-add.png) ) アイコンをクリックし、最初の連絡先の情報を入力します。 次に、該当する各ロールのチェックボックスを選択し、 **[!UICONTROL Add]**.

      - プライマリ連絡先 — （通知 E メールアドレス）通知の送信先となる連絡先。
      - データ保護担当者 — （該当する場合）プライバシー規制への準拠を促進するように指定された人。
      - 欧州経済圏 (EEA) 担当者 — （該当する場合）EU 外のお客様を GDPR 義務に関して代表する人。

     該当する場合は、別の連絡先を追加する場合に繰り返します。

### 手順 2:Google JS ライブラリを変更する

Googleでは、Google製品に応じて、Web サイトの使用状況を測定するための 3 つの JavaScript ライブラリがサポートされています。 `gtag.js`, `analytics.js`、および `ga.js`. プライバシー要件を満たすために、標準コードは次のように変更できます。

#### IP アドレスを匿名化する

使用する IP アドレスを匿名化するには **_Google Universal Analytics_**、次のスニペットを `analytics.js` Web サーバー上のライブラリ：

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

詳しくは、 [Analytics.js フィールドのリファレンス][3]{: target=&quot;_blank&quot;}(Googleヘルプ )。

従来の `ga.js` ライブラリで、次のスニペットを追加します。

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

使用する IP アドレスを匿名化するには **_Google Tag Manager_**&#x200B;を設定し、 `anonymize_ip` パラメーター `true` （内） `gtag.js` ライブラリを Web サーバー上に配置する必要があります。

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

詳しくは、 [Analytics での IP 匿名化][4] (Googleヘルプ )

#### SSL を強制

すべてのGoogleデータをセキュアソケットレイヤー (SSL) 経由で強制的に送信するには、次のスニペットをに追加します。 `analytics.js` ライブラリを Web サーバー上に配置する必要があります。

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### 手順 3：プライバシーポリシーを更新する

を更新します。 [プライバシーポリシー](../getting-started/privacy-policy.md) 会社を次のように述べます。

- Google Analyticsを使用
- IP アドレスをマスクして個人情報を非表示にする
- Googleデータ共有がオフになりました
- Google AnalyticsCookie で他のGoogleサービスを使用しない

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
