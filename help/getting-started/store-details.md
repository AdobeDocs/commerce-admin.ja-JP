---
title: ストアの詳細
description: ストアの基本情報を更新する方法を説明します。
exl-id: f4910ff7-4fcc-482f-be1d-cad8564cdd86
feature: Configuration
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1786'
ht-degree: 0%

---

# ストアの詳細

ストアの基本情報には、ストアの名前と住所、電話番号、メールアドレスが含まれます。メールアドレスは、メールメッセージ、請求書、その他の顧客に送信されるお知らせに表示されます。

![一般設定 – ストアの詳細](./assets/config-general-store-details.png){width="900" zoomable="yes"}

## [!UICONTROL Store Information]

この _[!UICONTROL Store Information]_セクションでは、販売ドキュメントおよびその他のコミュニケーションに表示される基本情報を提供します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 次の下 **[!UICONTROL General]** 左側のナビゲーションパネルで、を選択します。 **[!UICONTROL General]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Store Information]** セクション。

   ![一般設定 – ストア情報](./assets/general-store-information.png){width="700"}

1. ストアの詳細に従ってオプションを設定します。

   - を入力 **[!UICONTROL Store Name]** すべての通信で使用する。

   - を入力 **[!UICONTROL Store Phone Number]**&#x200B;表示する形式。

   - の場合 **[!UICONTROL Store Hours of Operation]**、店舗の営業時間を入力します。 例： `Mon - Fri, 9-5, Sat 9-noon PST`.

   - 「」を選択します **[!UICONTROL Country]** ビジネスの所在地。

   - 「」を選択します **[!UICONTROL Region/State]** 国と。

   - を入力 **[!UICONTROL Store Address]**. アドレスが長い場合は、アドレスを **店舗の住所 2**.

   - 該当する場合、 **[!UICONTROL VAT Number]** あなたの店の。

     番号を確認するには、 **[!UICONTROL Validate VAT Number]** ボタン。 詳しくは、 [VAT ID の検証](../stores-purchase/vat.md#vat-id-validation).

1. 完了したら、 **[!UICONTROL Save Config]**.

ストア情報の設定オプションの詳細については、を参照してください。 [_設定リファレンスガイド_](../configuration-reference/general/general.md#store-information).

## [!UICONTROL Locale Options]

ロケールは、ストア全体で使用される多くの設定を決定します。 その一部を次に示します。

- 言語
- 国
- 税率
- 通貨
- 価格
- 数値フォーマット

ロケール設定は、各ストアに使用されるタイムゾーンと言語を決定し、そのエリアの営業週の曜日を識別します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のナビゲーションパネル **[!UICONTROL General]**、を選択 **[!UICONTROL General]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Locale Options]** セクション。

   ![一般設定 – ロケールオプション](./assets/general-locale-options.png){width="700"}

1. を選択 **[!UICONTROL Timezone]** リストから。

1. を設定 **[!UICONTROL Locale]** をストアの言語に変更します。

1. を設定 **[!UICONTROL Weight Unit]** を、通常、ロケールからの出荷に使用される測定単位に変更します。

1. を設定 **[!UICONTROL First Day of the Week]** を、お住まいの地域で週の最初の曜日と見なされる日に変更します。

1. が含まれる **[!UICONTROL Weekend Days]** リストで、お住まいの地域の週末に当たる日を選択します。

   複数日を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各項目をクリックします。

1. 完了したら、 **[!UICONTROL Save Config]**.

ロケール設定オプションについて詳しくは、 [設定リファレンスガイド](../configuration-reference/general/general.md#locale-options).

## [!UICONTROL State Options]

多くの国では、都道府県または地域が郵送先住所の必須の部分です。 この情報は、配送および請求情報、税率の計算などに使用されます。 都道府県を指定する必要がない国の場合は、このフィールドをアドレスから完全に省略するか、オプションのフィールドとして含めることができます。

標準の住所形式は国によって異なるので、請求書、梱包明細、出荷ラベルの住所の書式設定に使用するテンプレートを編集することもできます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 次の下 **[!UICONTROL General]** 左側のナビゲーションパネルで、を選択します。 **[!UICONTROL General]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL State Options]** セクション。

   ![一般設定 – 状態オプション](./assets/general-state-options.png){width="700"}

1. の使用 **[!UICONTROL State is required for]** 地域/都道府県が必須入力である国を一覧から選択します。

1. を設定 **[!UICONTROL Allow to Choose State if it is Optional for Country]** を次のいずれかに変更します。

   `Yes`  – 都道府県フィールドが必須でない国では、はオプションのエントリとして都道府県フィールドを含みます。

   `No`  – 都道府県フィールドが必須でない国では、都道府県フィールドを省略します。

1. 完了したら、 **[!UICONTROL Save Config]**.

状態設定オプションの詳細については、を参照してください [設定リファレンスガイド](../configuration-reference/general/general.md#state-options).

## [!UICONTROL Country Options]

国オプションは、ビジネスが所在する国と、支払いを受け入れる国を識別します。

### ストアの国オプションの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のナビゲーションパネル **[!UICONTROL General]**、を選択 **[!UICONTROL General]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Country Options]** セクション。

   >[!NOTE]
   >
   >必要に応じて、 **[!UICONTROL Use system value]** 変更する各設定のチェックボックス。

   ![一般設定 – 国設定](./assets/general-country-options.png){width="700"}

1. を選択します。 **[!UICONTROL Default Country]** ビジネスの所在地。

1. が含まれる **[!UICONTROL Allow Countries]** リストで、注文を受け入れる国を選択します。

   デフォルトでは、リスト内のすべての国が選択されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各項目をクリックします。

1. の使用 **[!UICONTROL Zip/Postal Code is Optional for]** 住所の一部に郵便番号を含める必要がないビジネスを行う国を選択するリストです。

1. が含まれる **[!UICONTROL European Union Countries]** リストで、ビジネスを行う EU 内の国を選択します。

   デフォルトでは、すべての EU 諸国が選択されています。 必要な国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各項目をクリックします。

1. が含まれる **[!UICONTROL Top Destinations]** リストで、販売のターゲットとする主な国を選択します。

1. 完了したら、 **[!UICONTROL Save Config]**.

### 特定の配信方法の国オプションの設定

利用可能な国ごとに特定の国への配送を設定することもできます [配信方法](../stores-purchase/delivery.md) （UPS、FedEx など）。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルでを展開します。 **[!UICONTROL Sales]** を選択します **[!UICONTROL Delivery Methods]**.

1. 特定の国を適用する配送業者を選択します。

1. の場合 **[!UICONTROL Ship to Applicable Countries]**、選択を解除 **[!UICONTROL Use system value]** チェックボックスをオンにして、 **[!UICONTROL Specific Countries]** オプション。

1. が含まれる **[!UICONTROL Top Destinations]** リストで、配送先となる主要国を選択します。

   ![DHL 配信方法の国オプションの設定例](./assets/country-options-for-specific-delivery-method.png){width="700"}

1. 完了したら、 **[!UICONTROL Save Config]**.

### リソースのトラブルシューティング

国の設定に関する問題のトラブルシューティングについては、次を参照してください [!DNL Commerce] サポートナレッジベース記事：

- [国の追加方法](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-add-a-new-country-to-magento-2.html)
- [入力された countryId は存在しません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-15/mdva-33393-magento-patch-provided-countryid-does-not-exist.html)

## [!UICONTROL Merchant Location]

マーチャントの場所の設定は、の設定に使用します [支払い方法](../stores-purchase/payments.md). この設定に値がない場合、 [デフォルトの国](#uicontrol-country-options) 設定が使用されます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルでを展開します。 **[!UICONTROL Sales]** を選択します **[!UICONTROL Payment Methods]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **マーチャントの場所** セクションを選択して、 **[!UICONTROL Merchant Country]**.

   ![マーチャントの場所の設定](./assets/payment-methods-merchant-location.png){width="600"}

1. 完了したら、 **[!UICONTROL Save Config]**.

支払方法の構成オプションの詳細については、 [設定リファレンスガイド](../configuration-reference/sales/payment-methods.md).

## 通貨

通貨設定 – ベースを定義します [通貨](../stores-purchase/currency-configuration.md) および支払いとして受け入れられる追加の通貨。 また、通貨レートを自動的に更新するために使用されるインポート接続とスケジュールを確立します。

通貨記号 – を定義します。 [通貨記号](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) 製品価格および販売ドキュメント （注文や請求書など）に表示されます。 [!DNL Commerce] は、世界 200 か国以上の通貨をサポートしています。

通貨レートの更新 – 通貨レートは次のいずれかになります [更新日](../stores-purchase/currency-update.md) 必要に応じて、または事前に定義されたスケジュールに従って、手動でストアに読み込みます。

通貨選択 – 複数の通貨が使用可能な場合、 [通貨選択](../stores-purchase/currency.md) はストアのヘッダーで使用できます。

## [!UICONTROL Store Email Addresses]

各ストアまたは表示の個別の機能または部門を表す最大 5 つの異なるメールアドレスを設定できます。 次の事前定義済みのメール ID に加えて、必要に応じて設定できるカスタム ID がいくつかあります。

- 一般連絡先
- 営業担当者
- カスタマーサポート

各 ID とそれに関連するメールアドレスは、特定の自動メールメッセージに関連付けることができ、ストアから送信されるメールメッセージの送信者として表示されます。

### 手順 1：ドメインのメールアドレスの設定

ストアのメールアドレスを設定する前に、各をドメインの有効なメールアドレスとして設定する必要があります。 必要な各メールアドレスを作成するには、サーバー管理者またはメールホスティングプロバイダーの手順に従います。

### 手順 2：ストアのメールアドレスの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 次の下 **[!UICONTROL General]** 左側のナビゲーションパネルで、を選択します。 **[!UICONTROL Store Email Addresses]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL General Contact]** を選択し、次の操作を実行します。

   ![一般設定 – メールアドレスの保存](./assets/store-email-addresses-general-contact.png){width="600"}

   - の場合 **[!UICONTROL Sender Name]**：一般的な連絡先 ID に関連付けられている人の名前を入力し、メールメッセージの送信者として表示します。

   - の場合 **[!UICONTROL Sender Email]**：関連付けられているメールアドレスを入力します。

1. 使用する予定の各ストアメールアドレスに対して、このプロセスを繰り返します。

1. 完了したら、 **[!UICONTROL Save Config]**.

### 手順 3：営業メール設定の更新

カスタムメールアドレスを使用する場合は、関連するメールメッセージの設定を更新して、正しい ID が送信者として表示されるようにします。

1. 左側のナビゲーションパネルでを展開します。 **[!UICONTROL Sales]** を選択します **[!UICONTROL Sales Emails]**.

   このページには、次の各項目に対する個別のセクションがあります。

   - 注文および注文のコメント
   - 請求書および請求書注釈
   - 出荷および出荷注釈
   - クレジット・メモとクレジット・メモの注釈
   - RMA、RMA 認証、RMA 管理者コメント、RMA 顧客コメント ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

1. の概要 **[!UICONTROL Order]**&#x200B;各メッセージの「」セクションを展開し、正しい送信者が選択されていることを確認します。

   ![販売設定 – 販売メール](./assets/sales-emails-order.png){width="600"}

1. 完了したら、 **[!UICONTROL Save Config]**.

販売メールの設定オプションについて詳しくは、 [_設定リファレンスガイド_](../configuration-reference/sales/sales-emails.md).

## お問い合わせフォーム

この _お問い合わせ_ 店舗のフッターにあるリンクは、顧客が連絡を取り合うための簡単な方法です。 顧客はフォームに入力して、メッセージをストアに送信できます。 A 規格 [!DNL Commerce] インストール時にデフォルトが表示される _お問い合わせ_ フォーム。 フォームを送信すると、ありがとうメッセージが表示されます

デフォルトのお問い合わせフォームは、CMS ページではなくコードから直接レンダリングされることを理解しておくことが重要です。

![既定の連絡先ページ](./assets/page-contact-us-default.png){width="700"}

ストアフッターには、ストア全体で利用できるお問い合わせページへのリンクが含まれています。

![フッターの Contact Us リンク](./assets/storefront-footer-contact-us.png){width="700"}

Luma のサンプルデータには、ストアに合わせてページをカスタマイズする方法を示す、お問い合わせページに関する追加情報が含まれています。

![Contact Us page](./assets/storefront-contact-us.png){width="700"}

### お問い合わせフォームの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のナビゲーションパネル **[!UICONTROL General]**、を選択 **[!UICONTROL Contacts]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Contact Us]** セクションとセット **[!UICONTROL Enable Contact Us]** 対象： `Yes`.

   ![一般設定 – お問い合わせ](./assets/contacts-contact-us.png){width="600"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Email Options]** 「」セクションを選択して、メール連絡先オプションを設定します。

   ![一般設定 – メールオプション](./assets/contacts-email-options.png){width="600"}

   - の場合 **[!UICONTROL Send Emails to]**：お問い合わせフォームからのメッセージが送信されるメールアドレスを入力します。

   - を設定 **[!UICONTROL Email Sender]** お問い合わせフォームからメッセージの送信者として表示されるストア ID に追加されます。 例：カスタムメール 2.

   - を設定 **[!UICONTROL Email Template]** お問い合わせフォームから送信されるメッセージに使用されるテンプレート。

1. 競合する場合は、 **[!UICONTROL Save Config]**.

### コンテンツのカスタマイズ

のコンテンツはカスタマイズできます _お問い合わせ_ 店舗やカスタマーサービスポリシーのニーズに合わせたフォーム。

### 方法 1：サンプルデータの使用

Luma サンプルデータには以下が含まれます _Contact Us Info_ ストアに合わせてカスタマイズできるブロック。 この `contact-us-info` [ブロック](../content-design/blocks.md) お問い合わせページに独自のコンテンツを追加するように簡単に変更できます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. の検索 **[!UICONTROL Contact Us Info]** リストでブロックして次で開く： **[!UICONTROL Edit]** モード。

   ![お問い合わせ情報ブロック](./assets/content-block-contact-us-info.png){width="700"}

1. ブロックページの下部で、 **[!UICONTROL Edit with Page Builder]**.

   ![コンテンツブロック – お問い合わせ例](./assets/content-block-contact-us-content.png){width="700"}

   >[!NOTE]
   >
   >以下がある場合： [[!DNL Page Builder] disabled](../page-builder/setup.md#disable-dnl-page-builder)は、エディターを使用できます [ツールバー](../content-design/editor.md) テキストの書式を設定するには、次を追加します [画像](../content-design/editor-insert-image.md) および [links](../content-design/editor-insert-link.md).

1. HTMLコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](../page-builder/assets/pb-icon-settings.png) ） アイコンをクリックします。

1. 店舗の連絡先を入力したに従って、HTMLコードを編集し、クリックします。 **[!UICONTROL Save]**.

   ![コンテンツブロック -HTMLコードを編集](./assets/content-block-contact-us-html.png){width="700"}

1. を終了 [!DNL Page Builder] ステージとクリック **[!UICONTROL Save Block]**.

### 方法 2：サンプルデータなし

>[!IMPORTANT]
>
>2.4.0 リリース以降、CMS ブロックまたは CMS ページ内で連絡先フォームを呼び出すことができなくなりました。 お問い合わせフォームをカスタマイズする際は、レイアウト xml またはカスタムテーマテンプレートを使用してください。

デフォルトでは、買い物客は次を使用して連絡先フォームにアクセスします _連絡先リンク_ ストアフロントページのフッターで。 連絡先ページのカスタマイズの詳細については、 [フロントエンド開発者ガイド][theme-guide].

[theme-guide]: https://developer.adobe.com/commerce/frontend-core/guide/themes/
