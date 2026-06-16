---
title: Google サイトツール
description: コンテンツの最適化、トラフィックの分析、カタログのショッピングアグリゲーターやマーケットプレイスへの接続に使用できる、Google toolsの統合機能について説明します。
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
TQID: https://experienceleague.adobe.com/P-IniOyLDfDk8oe1v9ysmRV6yC7IWpxUBaFF--2YMCg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c32adafa-ed01-4b31-997e-2413013911b0id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 662
ht-degree: 0%

---

# Google サイトツール

ストア設定は、次のGoogleツールと統合されています。これにより、コンテンツの最適化、トラフィックの分析、カタログとショッピングアグリゲーターやマーケットプレイスの連携が可能になります。

- [Google Analytics](google-analytics.md) - _Google Universal Analytics_&#x200B;を使用して、オフラインおよびモバイルアプリのインタラクションのサポート、継続的な更新へのアクセスを含む、トラッキング用の追加のカスタムディメンションと指標を定義します。

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） Google Tag Managerを使用して、マーケティングキャンペーンイベントに関連する多くのタグを管理します。

- [Google AdWords](google-adwords.md) - Google AdWords キャンペーンを作成し、ストアのコンバージョンを追跡します。

{{gtag-api-note}}

## Googleのプライバシー設定

[GDPR](../getting-started/compliance-gdpr.md)や[CCPA](../getting-started/compliance-ccpa.md)などのプライバシー規制に準拠する必要がある場合は、Google ツールのデフォルト設定を変更して、プライバシー要件に対応させてください。 顧客データの使用をコンプライアンスに準拠するように、次の手順に従ってください。

### 手順1:Google設定の更新

1. [会社のGoogle Analytics アカウントに](https://www.google.com/analytics/){: target="_blank"} ログインします。

1. 左側のサイドバーの下部にある「**[!UICONTROL Admin]**」を選択し、編集するアカウントに移動します（該当する場合）。

1. **[!UICONTROL Account]**&#x200B;列で、**[!UICONTROL Account Settings]**&#x200B;をクリックします。

1. プライバシー規制の要件を満たすために、データ共有をオフにします。

   Google Analyticsのデフォルト設定では、企業データがGoogleやその他の関係者と共有されます。データ共有をオフにするには、次の設定の「選択」チェックボックスをオフにします。

   - Googleの製品とサービス
   - ベンチマーク
   - テクニカルサポート
   - アカウントスペシャリスト

1. _データ処理修正_&#x200B;に同意します。

   Google Adsのデータ処理条件では、Googleがデータを処理する方法と、GDPRの対象となる企業のデータセキュリティを確保するために必要な対策について説明します。 お客様の法人および連絡先情報の記録も、修正条項に従って保持されます。 [詳細情報](https://support.google.com/analytics/answer/3379636){: target="_blank"}を表示するには、ページ上部にあるメッセージ内のリンクをクリックします。

   - ページを&#x200B;**[!UICONTROL Data Processing Amendment]**&#x200B;までスクロールします。
   - **[!UICONTROL Review Amendment]**&#x200B;をクリックして、_Google Ads Data Processing Terms_&#x200B;を読んでください。
   - **[!UICONTROL Accept]**&#x200B;をクリックします。
   - **[!UICONTROL Save]**&#x200B;をクリックします。

1. _DPA管理_&#x200B;の詳細を完了します。

   - 「**[!UICONTROL Manage DPA Details]**」をクリックして、連絡先と組織の法人を編集できるDPA管理ページを開きます。

   - **[!UICONTROL Legal Entities]** セクションで、_編集_ （![Google編集アイコン ](./assets/google-icon-edit.png)）アイコンをクリックし、登録されている名前を1つ以上追加します。 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

   - **連絡先** セクションで、_Add_ （![Google add icon](./assets/google-icon-add.png)）アイコンをクリックし、最初の連絡先の情報を入力します。 次に、該当する各役割のチェックボックスを選択し、**[!UICONTROL Add]**&#x200B;をクリックします。

      - プライマリ連絡先 – （通知の電子メールアドレス）通知が送信される連絡先。
      - データ保護責任者 – （該当する場合） プライバシー規制への準拠を容易にするように指定された人物。
      - 欧州経済地域（EEA）担当者 – （該当する場合） GDPR義務に関してEU外のお客様を代表する人物。

     これを繰り返して、必要に応じて別の連絡先を追加します。

### 手順2:Google JS ライブラリの変更

Googleでは、Google製品に応じて、3つのJavaScript ライブラリをサポートし、web サイトの使用状況を測定します。`gtag.js`、`analytics.js`、`ga.js`。 プライバシー要件を満たすために、標準コードを次のように変更できます。

#### IP アドレスの匿名化

**_Google Universal Analytics_**&#x200B;で使用されるIP アドレスを匿名化するには、次のスニペットをweb サーバーの`analytics.js` ライブラリに追加します。

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

詳しくは、Google ヘルプの[Analytics.js フィールドリファレンス ](https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference){: target="_blank"}を参照してください。

従来の`ga.js` ライブラリを使用する場合は、次のスニペットを追加します。

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

**_Google Tag Manager_**&#x200B;が使用するIP アドレスを匿名化するには、Web サーバー上の`gtag.js` ライブラリの`anonymize_ip` パラメーターを`true`に設定します。

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

詳しくは、Google ヘルプの「[AnalyticsでのIP匿名化](https://support.google.com/analytics/answer/2763052)」を参照してください。

#### SSLを強制

すべてのGoogle データをSSL （Secure Socket Layer）経由で強制的に送信するには、次のスニペットをweb サーバーの`analytics.js` ライブラリに追加します。

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### 手順3：プライバシーポリシーの更新

[ プライバシーポリシー](../getting-started/privacy-policy.md)を更新して、会社を次のように記述します。

- Google Analyticsの使用
- IP アドレスをマスクして個人情報を非表示にする
- Google データ共有をオフにしました
- Google Analytics Cookieで他のGoogle サービスを使用しない
