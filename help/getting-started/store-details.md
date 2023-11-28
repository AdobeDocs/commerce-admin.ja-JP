---
title: ストアの詳細
description: ストアの基本情報を更新する方法を説明します。
exl-id: f4910ff7-4fcc-482f-be1d-cad8564cdd86
feature: Configuration
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1797'
ht-degree: 0%

---

# ストアの詳細

ストアの基本情報には、顧客に送信される電子メールメッセージ、請求書、その他の通信に表示されるストア名とアドレス、電話番号、電子メールアドレスが含まれます。

![一般的な設定 — ストアの詳細](./assets/config-general-store-details.png){width="900" zoomable="yes"}

## [!UICONTROL Store Information]

The _[!UICONTROL Store Information]_「 」セクションでは、セールスドキュメントや他のコミュニケーションに表示される基本情報を提供します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下 **[!UICONTROL General]** 左側のナビゲーションパネルで、「 」を選択します。 **[!UICONTROL General]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Store Information]** 」セクションに入力します。

   ![一般設定 — ストア情報](./assets/general-store-information.png){width="700"}

1. ストアの詳細に従ってオプションを設定します。

   - 次を入力します。 **[!UICONTROL Store Name]** すべての通信で使用する

   - 次を入力します。 **[!UICONTROL Store Phone Number]**&#x200B;表示する形式で書式設定されます。

   - の場合 **[!UICONTROL Store Hours of Operation]**」をクリックして、営業時間として店舗を開く時間を入力します。 例： `Mon - Fri, 9-5, Sat 9-noon PST`.

   - を選択します。 **[!UICONTROL Country]** ビジネスの所在地

   - を選択します。 **[!UICONTROL Region/State]** 国と共に

   - 次を入力します。 **[!UICONTROL Store Address]**. アドレスが長い場合は、 **店舗の住所行 2**.

   - 該当する場合は、 **[!UICONTROL VAT Number]** お客様のストアの

     番号を確認するには、 **[!UICONTROL Validate VAT Number]** 」ボタンをクリックします。 詳しくは、 [VAT ID の検証](../stores-purchase/vat.md#vat-id-validation).

1. 完了したら、「 **[!UICONTROL Save Config]**.

ストア情報の設定オプションについて詳しくは、 [_設定リファレンスガイド_](../configuration-reference/general/general.md#store-information).

## [!UICONTROL Locale Options]

ロケールによって、ストア全体で使用される設定の多くが決まります。 その一部を次に示します。

- 言語
- 国
- 税率
- 通貨
- 価格
- 数値の形式

ロケール設定は、各店舗で使用するタイムゾーンと言語を決定し、その地域の稼働週間の日数を示します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで、 **[!UICONTROL General]**&#x200B;を選択します。 **[!UICONTROL General]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Locale Options]** 」セクションに入力します。

   ![一般設定 — ロケールオプション](./assets/general-locale-options.png){width="700"}

1. を選択します。 **[!UICONTROL Timezone]** を選択します。

1. 設定 **[!UICONTROL Locale]** をストアの言語に設定します。

1. 設定 **[!UICONTROL Weight Unit]** を指定します。

1. 設定 **[!UICONTROL First Day of the Week]** を、地域の週の最初の曜日と見なされる日に設定します。

1. Adobe Analytics の **[!UICONTROL Weekend Days]** リストで、地域の週末に該当する日を選択します。

   複数の日を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各項目をクリックします。

1. 完了したら、「 **[!UICONTROL Save Config]**.

ロケールの設定オプションについて詳しくは、 [設定リファレンスガイド](../configuration-reference/general/general.md#locale-options).

## [!UICONTROL State Options]

多くの国では、郵送先住所の一部として、州、都道府県、地域が必要です。 この情報は、送料や請求に関する情報や、税率の計算などに使用されます。 都道府県を指定する必要がない国の場合は、フィールドを住所から完全に省略するか、任意のフィールドとして含めることができます。

標準の住所の形式は国によって異なるので、請求書、梱包伝票、発送ラベルの住所の形式設定に使用するテンプレートを編集することもできます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下 **[!UICONTROL General]** 左側のナビゲーションパネルで、「 」を選択します。 **[!UICONTROL General]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL State Options]** 」セクションに入力します。

   ![一般設定 — 状態オプション](./assets/general-state-options.png){width="700"}

1. 以下を使用します。 **[!UICONTROL State is required for]** リストを選択して、地域/都道府県が必須のエントリである各国を選択します。

1. 設定 **[!UICONTROL Allow to Choose State if it is Optional for Country]** を次のいずれかに変更します。

   `Yes`  — 州フィールドが必須でない国では、「州」フィールドをオプションのエントリとして含めます。

   `No`  — 州フィールドが必須でない国では、州フィールドを省略します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

状態の設定オプションについて詳しくは、 [設定リファレンスガイド](../configuration-reference/general/general.md#state-options).

## [!UICONTROL Country Options]

国オプションは、ビジネスの所在国と支払いを受け入れる国を特定します。

### ストアの国のオプションを設定します

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで、 **[!UICONTROL General]**&#x200B;を選択します。 **[!UICONTROL General]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Country Options]** 」セクションに入力します。

   >[!NOTE]
   >
   >必要に応じて、 **[!UICONTROL Use system value]** チェックボックスをオンにします。

   ![一般設定 — 国設定](./assets/general-country-options.png){width="700"}

1. を選択します。 **[!UICONTROL Default Country]** ビジネスの所在地

1. Adobe Analytics の **[!UICONTROL Allow Countries]** 「 」リストで、注文を受け入れる国を選択します。

   デフォルトでは、リスト内のすべての国が選択されます。 複数の国を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各項目をクリックします。

1. 以下を使用します。 **[!UICONTROL Zip/Postal Code is Optional for]** 住所の一部に郵便番号を含める必要のない業務を行う各国を選択するリスト。

1. Adobe Analytics の **[!UICONTROL European Union Countries]** リストで、EU 内でビジネスを行う国を選択します。

   デフォルトでは、すべての EU 加盟国が選択されています。 必要な国を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各項目をクリックします。

1. Adobe Analytics の **[!UICONTROL Top Destinations]** 「 」リストで、販売のターゲットとする主要国を選択します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

### 特定の配信方法の国のオプションを設定します

また、利用可能な国ごとに、特定の国への配送を設定することもできます [配信方法](../stores-purchase/delivery.md) （UPS、FedEx など）。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Delivery Methods]**.

1. 特定の国を適用する輸送先を選択します。

1. の場合 **[!UICONTROL Ship to Applicable Countries]**、選択を解除 **[!UICONTROL Use system value]** チェックボックスをオンにして、 **[!UICONTROL Specific Countries]** オプション。

1. Adobe Analytics の **[!UICONTROL Top Destinations]** 「 」リストで、配送先の主要国を選択します。

   ![DHL 配信メソッドの国のオプションの設定例](./assets/country-options-for-specific-delivery-method.png){width="700"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

### リソースのトラブルシューティング

国の設定に関する問題のトラブルシューティングについては、次を参照してください。 [!DNL Commerce] サポートに関するナレッジベース記事：

- [国の追加方法](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-add-a-new-country-to-magento-2.html)
- [指定された countryId が存在しません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-15/mdva-33393-magento-patch-provided-countryid-does-not-exist.html)

## [!UICONTROL Merchant Location]

マーチャントの場所の設定を使用して、 [支払い方法](../stores-purchase/payments.md). この設定に値がない場合、 [デフォルトの国](#uicontrol-country-options) の設定が使用されます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Payment Methods]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **商社の場所** 」セクションで、 **[!UICONTROL Merchant Country]**.

   ![マーチャントの場所の設定](./assets/payment-methods-merchant-location.png){width="600"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

「支払い方法」構成オプションの詳細は、 [設定リファレンスガイド](../configuration-reference/sales/payment-methods.md).

## 通貨

通貨設定 — ベースを定義します。 [通貨](../stores-purchase/currency-configuration.md) および支払として受け入れられるその他の通貨 また、通貨レートを自動的に更新するために使用するインポート接続とスケジュールも設定します。

通貨記号 — [通貨記号](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) 製品価格や、注文書や請求書などの販売ドキュメントに表示されます。 [!DNL Commerce] は、世界 200 カ国以上からの通貨をサポートしています。

通貨レートの更新 — 通貨レートは次のとおりです。 [更新済み](../stores-purchase/currency-update.md) 必要に応じて、手動で、またはストアにインポートするか、事前に定義されたスケジュールに従って、

通貨の選択 — 複数の通貨が使用可能な場合は、 [通貨選択](../stores-purchase/currency.md) は、ストアのヘッダーで使用できます。

## [!UICONTROL Store Email Addresses]

最大 5 つの異なる電子メールアドレスを使用して、各店舗またはビューの個別の機能や部門を表すことができます。 次の定義済みの電子メール ID に加えて、必要に応じて設定できるカスタム ID がいくつかあります。

- 一般連絡先
- セールス担当者
- カスタマーサポート

各 ID と関連する電子メールアドレスは、特定の自動電子メールメッセージに関連付けることができ、ストアから送信された電子メールメッセージの送信者として表示されます。

### 手順 1：ドメインの電子メールアドレスを設定する

ストアの電子メールアドレスを設定する前に、それぞれをドメインの有効な電子メールアドレスとして設定する必要があります。 必要な各電子メールアドレスを作成するには、サーバー管理者または電子メールホストプロバイダーの指示に従います。

### 手順 2：ストアの電子メールアドレスを設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下 **[!UICONTROL General]** 左側のナビゲーションパネルで、「 」を選択します。 **[!UICONTROL Store Email Addresses]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL General Contact]** 」セクションで次の操作を実行します。

   ![一般的な設定 — 電子メールアドレスを保存](./assets/store-email-addresses-general-contact.png){width="600"}

   - の場合 **[!UICONTROL Sender Name]**「 」には、電子メールメッセージの送信者として表示する「一般的な連絡先 ID 」に関連付けられている人物の名前を入力します。

   - の場合 **[!UICONTROL Sender Email]**」に、関連する電子メールアドレスを入力します。

1. 使用する予定のストアの電子メールアドレスごとに、このプロセスを繰り返します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

### 手順 3：セールスメールの設定を更新する

カスタム電子メールアドレスを使用する場合は、関連する電子メールメッセージの設定を必ず更新し、正しい ID が送信者として表示されるようにします。

1. 左側のナビゲーションパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Sales Emails]**.

   ページには、次の各項目に対して個別のセクションがあります。

   - 注文および注文に関するコメント
   - 請求書および請求書コメント
   - 出荷および出荷コメント
   - クレジット・メモおよびクレジット・メモのコメント
   - RMA、RMA 認証、RMA 管理者コメント、および RMA 顧客コメント ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ )

1. の使用を開始 **[!UICONTROL Order]**&#x200B;で、各メッセージの「 」セクションを展開し、正しい送信者が選択されていることを確認します。

   ![セールス構成 — セールスメール](./assets/sales-emails-order.png){width="600"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

セールスメールの設定オプションについて詳しくは、 [_設定リファレンスガイド_](../configuration-reference/sales/sales-emails.md).

## お問い合わせフォーム

The _お問い合わせ_ ストアのフッターにリンクを使用すると、顧客が簡単に連絡を取ることができます。 顧客はフォームに入力して、ストアにメッセージを送信できます。 標準 [!DNL Commerce] インストール時にデフォルトが表示されます _お問い合わせ_ フォーム。 フォームを送信すると、「ありがとうございます」というメッセージが表示されます

デフォルトの「Contact Us」フォームは、CMS ページからではなくコードから直接レンダリングされることを理解しておくことが重要です。

![デフォルトのお問い合わせページ](./assets/page-contact-us-default.png){width="700"}

ストアのフッターには、ストア全体で利用できる「お問い合わせ」ページへのリンクが含まれます。

![フッターのお問い合わせリンク](./assets/storefront-footer-contact-us.png){width="700"}

Luma サンプルデータには、ストアに合わせてページをカスタマイズする方法を示す、お問い合わせページに関する追加情報が含まれています。

![お問い合わせページ](./assets/storefront-contact-us.png){width="700"}

### 連絡先フォームの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで、 **[!UICONTROL General]**&#x200B;を選択します。 **[!UICONTROL Contacts]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Contact Us]** セクションとセット **[!UICONTROL Enable Contact Us]** から `Yes`.

   ![一般設定 — お問い合わせ](./assets/contacts-contact-us.png){width="600"}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Email Options]** 「 」セクションを開き、e メール連絡先オプションを設定します。

   ![一般設定 — E メールオプション](./assets/contacts-email-options.png){width="600"}

   - の場合 **[!UICONTROL Send Emails to]**「 Contact Us 」フォームからのメッセージを送信する電子メールアドレスを入力します。

   - 設定 **[!UICONTROL Email Sender]** 「連絡先」フォームからのメッセージの送信者として表示されるストア id。 例：カスタム電子メール 2。

   - 設定 **[!UICONTROL Email Template]** を、「連絡先」フォームから送信されるメッセージに使用するテンプレートに追加します。

1. 競合が発生したら、「 **[!UICONTROL Save Config]**.

### コンテンツのカスタマイズ

コンテンツをカスタマイズするには、 _お問い合わせ_ ストアおよび顧客サービスポリシーのニーズに合ったフォームを作成します。

### 方法 1：サンプルデータの使用

Luma サンプルデータには、 _お問い合わせ情報_ ストア用にカスタマイズできるブロック。 The `contact-us-info` [ブロック](../content-design/blocks.md) は、簡単に変更して、お客様独自のコンテンツをお客様の連絡先ページに追加できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 次を検索： **[!UICONTROL Contact Us Info]** リスト内でブロックし、次で開く **[!UICONTROL Edit]** モード。

   ![お問い合わせ情報ブロック](./assets/content-block-contact-us-info.png){width="700"}

1. ブロックページの下部で、 **[!UICONTROL Edit with Page Builder]**.

   ![コンテンツブロック — お問い合わせの例](./assets/content-block-contact-us-content.png){width="700"}

   >[!NOTE]
   >
   >次の条件を満たしている場合： [[!DNL Page Builder] 無効](../page-builder/setup.md#disable-dnl-page-builder)を使用する場合は、エディターを使用できます。 [ツールバー](../content-design/editor.md) テキストを書式設定し、 [画像](../content-design/editor-insert-image.md) および [リンク](../content-design/editor-insert-link.md).

1. HTMLコンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](../page-builder/assets/pb-icon-settings.png) ) アイコンをクリックします。

1. ストアの連絡先情報を指定し、HTMLコードを編集して、 **[!UICONTROL Save]**.

   ![コンテンツブロック —HTMLコードを編集](./assets/content-block-contact-us-html.png){width="700"}

1. を終了します。 [!DNL Page Builder] ステージングしてクリック **[!UICONTROL Save Block]**.

### 方法 2：サンプルデータがない場合

>[!IMPORTANT]
>
>2.4.0 リリース以降、CMS ブロックまたは CMS ページ内で連絡先フォームを呼び出すことができなくなりました。 連絡先フォームのすべてのカスタマイズは、レイアウト xml またはカスタムテーマテンプレートを使用して行う必要があります。

デフォルトでは、買い物客は _連絡先リンク_ をクリックします。 連絡先ページのカスタマイズについて詳しくは、 [フロントエンド開発者ガイド][theme-guide].

[theme-guide]: https://developer.adobe.com/commerce/frontend-core/guide/themes/
