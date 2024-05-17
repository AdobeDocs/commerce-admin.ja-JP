---
title: Cookie 法への準拠
description: Cookie の使用に関する多くの国の法律に対応するために、Adobe CommerceとMagento Open Sourceでは、マーチャントに対して、お客様の同意を得るための選択肢を提供しています。
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2105'
ht-degree: 0%

---

# Cookie 法への準拠

Cookie は、サイトへの各訪問者のコンピューターに保存される小さなファイルで、情報の一時的な保持場所として使用されます。 Cookie に保存される情報は、ショッピングエクスペリエンスのパーソナライズ、訪問者の買い物かごへのリンク、トラフィックパターンの測定、プロモーションの有効性の向上に使用されます。 Cookie の使用に関する多くの国の法律に対応するために、Adobe CommerceとMagento Open Sourceでは、マーチャントに対して、お客様の同意を得るための選択肢を提供しています。 Adobe CommerceとMagento Open Sourceのデフォルト cookie のリストについては、 [cookie の参照](#default-cookies).

>[!NOTE]
>
>デフォルトの [Google プライバシー設定](../merchandising-promotions/google-tools.md#google-privacy-settings) 規定に従う [EU 一般データ保護規則](compliance-gdpr.md)ただし、Google Analytics cookie の使用に関してユーザーの同意を得る必要はありません。

## 方法 1：暗黙の同意

黙示的な同意とは、ストアの訪問者が、Cookie が操作に必要な部分であることを明確に理解し、サイトを使用することで、それらを使用する権限を間接的に付与していることを意味します。 暗黙の同意を得るための鍵は、訪問者が十分な情報に基づいた意思決定をおこなうための十分な情報を提供することです。 多くのストアでは、すべての標準ページの上部にメッセージが表示され、ストアのプライバシーポリシーへのリンクとともに、cookie の使用方法の概要が表示されます。 プライバシーポリシーには、ストアが収集する情報の種類と使用方法を記述する必要があります。

## 方法 2：同意の表明

ストアの操作 _cookie 制限モード_ cookie をコンピューターに保存する前に、訪問者が同意を表明する必要があります。 同意が得られない限り、ストアの多くの機能は使用できません。 例えば、ストアでGoogle Analyticsが使用可能な場合、訪問者が Cookie の使用権限を付与した後にのみ呼び出すことができます。

## cookie 制限モード

cookie 制限モードが有効になっている場合、ストアを訪問した訪問者には、フル機能の操作に cookie が必要であることを通知されます。 テーマに応じて、メッセージはヘッダーの上、フッターの下、またはページ上の別の場所に表示される場合があります。 このメッセージは、詳細情報を提供するプライバシーポリシーにリンクしており、訪問者が「許可」ボタンをクリックして同意を付与するよう促しています。 同意が得られると、メッセージは消えます。

あなたの [プライバシーポリシー](privacy-policy.md)）には、ストア名と連絡先情報を含め、ストアで使用される各 cookie の目的を説明する必要があります。 詳しくは、 [cookie の参照](#default-cookies).

>[!NOTE]
>
>プライバシーポリシーの URL キーを変更する場合は、新しい URL キーにトラフィックをリダイレクトするようにカスタム URL 書き換えを作成する必要もあります。 それ以外の場合、Cookie 制限モード メッセージ内のリンクは、を返します `404 Page Not Found`.

![ストアフロントの例 – cookie 制限通知](./assets/storefront-cookie-restriction-message.png){width="600"}

### 手順 1:cookie 制限モードを有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のナビゲーションパネル **[!UICONTROL General]**、を選択 **[!UICONTROL Web]**.

1. を展開します。 **[!UICONTROL Default Cookie Settings]** を選択し、次の操作を実行します。

   ![Web 設定 – デフォルトの cookie 設定](./assets/web-default-cookie-settings.png){width="600"}

   - を入力 **[!UICONTROL Cookie Lifetime]** （秒）。

   - Cookie を他のフォルダーで使用できるようにする場合は、 **[!UICONTROL Cookie Path]**. サイト内の任意の場所で cookie を使用できるようにするには、スラッシュ（`/`）に設定します。 この値には、cookie のパスのみを含めることができます。 **_できません_** その他の cookie パラメーターが含まれます。

   - サブドメインで cookie を使用できるようにするには、サブドメイン名を **[!UICONTROL Cookie Domain]** フィールド （`subdomain.yourdomain.com`）に設定します。 すべてのサブドメインで cookie を使用できるようにするには、ドメイン名の前にピリオド（`.yourdomain.com`）に設定します。 この値には、cookie ドメインのみを含めることができます。 **_できません_** その他の cookie パラメーターが含まれます。

   - JavaScript などのスクリプト言語が Cookie にアクセスしないようにするには、次の点を確認してください **HTTP のみを使用** はに設定されています。 `Yes`.

   - を設定 **[!UICONTROL Cookie Restriction Mode]** 対象： `Yes`.

     必要に応じて、このチェックボックスをオフにし、 **[!UICONTROL OK]** スコープの切り替えを確認します。

1. 完了したら、 **[!UICONTROL Save Config]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** システムメッセージ内のリンク。 次に、無効な各キャッシュを更新します。

### 手順 2：プライバシーポリシーを更新する

を更新 [プライバシーポリシー](privacy-policy.md) 会社が収集する情報とその使用方法が反映されるように設定します。

## デフォルトの Cookie

Adobe CommerceとMagento Open Sourceのデフォルトの Cookie は、マーチャントが次のようなプライバシー規制の要件を満たすのに役立つように、免除/非免除に分類されます [GDPR](compliance-gdpr.md). マーチャントは、この情報を参考にして、法的アドバイザーに相談して、包括的なプライバシー規制コンプライアンス戦略の一環としてプライバシーと Cookie ポリシーを更新する必要があります。

次の Cookie はによって使用されます [!DNL Commerce] オンプレミスおよびクラウドのインストール用の「標準」。 これらの Cookie は、お客様から明示的にリクエストされた機能で必要になる場合があります。 セッション cookie の有効期間については、を参照してください。 [セッションの有効期間](../customers/customer-online-options.md).

これらの Cookie の一部では、必要に応じて、有効/無効を含む設定オプションが提供される場合があります。

### リクエストされた機能の Cookie （除外）


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）Google Tag Manager で使用されます。 買い物かごから削除された製品 SKU、名前、価格、数量をキャプチャし、サードパーティスクリプトによって今後の統合で情報を利用できるようにします。

#### `guest-view`

ゲストの買い物客が注文ステータスを取得するために使用する注文 ID を格納します。 ゲスト注文表示。 使用されている場所 _[!DNL Orders and Returns]_ウィジェット。

- 安全ですか？ 不可
- HTTP のみ：はい
- 有効期限ポリシー：セッション
- モジュール： `Magento_Sales`

#### `login_redirect`

顧客がログインを指示される前に読み込まれていた宛先ページを保持します。 ログイン リダイレクトは、ログインしている顧客のミニ カートで次の場合に使用されます [ミニ カートの表示](../stores-purchase/cart-configuration.md#mini-cart) 設定オプションがに設定されています `Yes`.

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール： `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）パフォーマンスを向上させるために、バナーコンテンツをローカルに保存します。

#### `mage-messages`

Cookie 同意メッセージ、様々なエラーメッセージなど、ユーザーに表示されるエラーメッセージやその他の通知をトラッキングします。 メッセージは、買い物客に表示された後、Cookie から削除されます。

この cookie を無効にするオプションはありません。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：期間 1 年。 メッセージがユーザーに表示される際に、フロントエンドでクリアされます。
- モジュール： `Magento_Theme`

#### `mage-translation-storage` （ローカルストレージ）

買い物客からリクエストされた際に、翻訳済みコンテンツを格納します。 次の場合に使用されます [翻訳戦略](../configuration-reference/advanced/developer.md) は「辞書（ストアフロント側での翻訳）」として設定されます。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Translation`

#### `mage-translation-file-version` （ローカルストレージ）

ローカルストレージ内の翻訳のバージョンをトラッキングします。 次の場合に使用されます [翻訳戦略](../configuration-reference/advanced/developer.md) はとして設定されます `Dictionary (Translation on Storefront side)`.

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Translation`

#### `product_data_storage` （ローカルストレージ）

最近閲覧/比較された製品に関連する製品データの設定を保存します。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Catalog`

#### `recently_compared_product` （ローカルストレージ）

最近比較した製品の製品 ID を格納します。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Catalog`

#### `recently_compared_product_previous` （ローカルストレージ）

前に比較した製品の製品 ID を保存してナビゲーションを容易にします。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Catalog`

#### `recently_viewed_product` （ローカルストレージ）

最近閲覧した製品の製品 ID を保存して、ナビゲーションを簡単にします。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Catalog`

#### `recently_viewed_product_previous` （ローカルストレージ）

最近閲覧した製品の製品 ID を保存して、ナビゲーションを簡単にします。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）以下が使用： [Google Tag Manager](../merchandising-promotions/google-tag-manager.md). 買い物かごに追加された製品 SKU、名前、価格、数量をキャプチャし、サードパーティスクリプトによって今後の統合で情報を利用できるようにします。

#### `stf`

SendFriend がメッセージを送信した時間を記録します（[友達にメールを送信](../stores-purchase/email-a-friend.md)） モジュール。

- 安全ですか？ はい
- HTTP のみ：はい
- 有効期限ポリシー：セッション
- モジュール： `Magento_SendFriend`

#### `X-Magento-Vary`

Varnish 静的コンテンツ キャッシュを使用する際のパフォーマンスを向上させる構成設定。

- 安全ですか？ はい
- HTTP のみ：はい
- 有効期限ポリシー：PHP の session.cookie_lifetime 設定に基づく
- モジュール： `Magento_PageCache`

#### `form_key`

すべてのフォーム送信にランダムな文字列を追加して、クロスサイトリクエストフォージェリ（CSRF）からデータを保護するセキュリティ対策。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：
   - PHP: session.cookie_lifetime の設定に基づく
   - JS:Session
- モジュール：ページキャッシュ

#### `mage-cache-sessid`

この cookie の値は、ローカルキャッシュストレージのクリーンアップをトリガーします。 Cookie がバックエンドアプリケーションによって削除されると、管理者はローカルストレージをクリーンアップし、cookie の値をに設定します `true`.

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール： `Magento_Customer`

#### `mage-cache-storage`

e コマース機能を有効にする訪問者固有のコンテンツのローカルストレージ。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール： `Magento_Customer`, `Magento_Persistent`

#### `mage-cache-storage` （ローカルストレージ）

e コマース機能を有効にする訪問者固有のコンテンツのローカルストレージ。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール： `Magento_Customer`, `Magento_Persistent`, `Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` （ローカルストレージ）

無効化する必要がある特定のコンテンツセクションのローカルストレージを強制します。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージあたり
- モジュール： `Magento_Customer`

#### `persistent_shopping_cart`

永続的な買い物かごのキー（ID）を格納して、匿名の買い物客に買い物かごを復元できるようにします。

- 安全ですか？ はい
- HTTP のみ：はい
- 有効期限ポリシー：基準 [永続ショッピングカート](../stores-purchase/cart-persistent.md)  – 永続性の有効期間（秒）の設定
- モジュール： `Magento_Persistent`

#### `private_content_version`

顧客コンテンツを含んだページにランダムな一意の番号と時間を追加して、ページがサーバー上にキャッシュされないようにします。

PHP、Cookie としての JavaScript、ローカルストレージへの JavaScript など、複数の場所で設定されます。

HTTP のみ=`Yes` （リクエストに基づく）を指定した場合、Cookie は HTTPS リクエストの最中に設定されると保護され、HTTP リクエストの最中に設定されると保護されません。

- 安全ですか？ `Yes` （ご要望による）、 `No`
- HTTP のみ： `No`
- 有効期限ポリシー：基準 [永続ショッピングカート](../stores-purchase/cart-persistent.md)  – 永続性の有効期間（秒）の設定
   - PHP: `1` 年/ `315360000s` （10 年）
   - JS: `1` 日
   - JS ローカルストレージ：ローカルストレージルールごと（永続的）
- モジュール： `Magento_PageCache`, `Magento_Customer`

#### `section_data_ids`

買い物客が開始したアクションに関連する、顧客固有の情報を格納します（ウィッシュリストの表示やチェックアウト情報など）。

- 安全ですか？ `No`
- HTTP のみ： `No`
- 有効期限ポリシー： `Session`
- モジュール： `Magento_Customer`

#### `store`

買い物客が選択した特定のストア表示/ロケールをトラッキングします。

- 安全ですか？ `No`
- HTTP のみ： `Yes`
- 有効期限ポリシー： `1` 年
- モジュール： `Magento_Store`

#### `mage-banners-cache-storage` - ローカルストレージ

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）バナー機能用のローカルストレージ。

- 安全ですか？ `No`
- HTTP のみ： `No`
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Banner`

## Google Analyticsの cookie

次の場合に次の Cookie が使用されます [Google Analytics](../merchandising-promotions/google-analytics.md) または、Google Universal Analytics がインストールで完全に有効になっています。 プライバシー規制に準拠するためにこれらの cookie を無効にするには、を参照してください。 [Google プライバシー設定](../merchandising-promotions/google-tools.md#google-privacy-settings). 詳しくは、 [Google Analytics Web サイトでの Cookie の使用][1].

### Google Universal Analytics の Cookie – 適用除外なし

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） JavaScript ライブラリ： `gtag.js` および `analytics.js`

- `_ga`：サイトへの訪問者を区別します。
- `_gid`：サイトへの訪問者を区別します。
- `gat`：リクエスト率のスロットルに使用されます。
- `dc_gtm_<property-id>`:Google Analyticsがでデプロイされる際のスロットルリクエストの割合 [Google Tag Manager](../merchandising-promotions/google-tag-manager.md).
- `AMP_TOKEN`:AMP Client ID サービスからクライアント ID を取得するために使用できるトークンが含まれています。 その他の使用可能な値には、オプトアウト、実行中のリクエスト、AMP Client ID サービスからのクライアント ID の取得エラーなどがあります。
- `_gac_<property-id>`：ユーザーのキャンペーン関連の情報が含まれます。 Google Analyticsがお客様にリンクされている場合、Google AdWords コンバージョンタグはこの Cookie を読み取ります [AdWords][2] アカウント。

### Google Analyticsの Cookie – 適用除外なし

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） JavaScript ライブラリ： `ga.js`

- `__utma`：買い物客とセッションを区別します。 この Cookie は、JavaScript ライブラリの実行時に作成されるもので、既存のライブラリがない場合に作成されます `__utma` cookie。 cookie は、データがGoogle Analyticsに送信されるたびに更新されます。
- `__utmt`：リクエスト率のスロットルに使用されます。
- `__utmb`：新規セッション/訪問回数を決定します。 この Cookie は、JavaScript ライブラリの実行時に作成されるもので、既存のライブラリがない場合に作成されます `__utmb` cookie。 cookie は、データがGoogle Analyticsに送信されるたびに更新されます。
- `_utmz`：買い物客がサイトにどのように到達したかを説明するトラフィックソースまたはキャンペーンを保存します。 この cookie は JavaScript ライブラリの実行時に作成され、Google Analyticsにデータが送信されるたびに更新されます。
- `__utmv`：訪問者レベルのカスタム変数データを格納します。 この Cookie は、開発者がパラメーターを使用する際に作成されます `_setCustomVar` 訪問者レベルのカスタム変数を使用したメソッド。 この cookie はGoogle Analyticsにデータが送信されるたびに更新されます。

## 製品のRecommendationsの cookie

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） Product Recommendationsでは、Adobe Commerceのお客様向けに次の Cookie が使用されます。 これらの Cookie は、 [DataServices モジュール](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg_dnt`：次の操作が可能 [Adobe Commerceのデータ収集の制限](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html) サイトで cookie の同意を管理するカスタムコードがある場合。
- `user_allowed_save_cookie`：に使用 [cookie 制限モード](#cookie-restriction-mode).
- `authentication_flag`：買い物客がサインインまたはログアウトしたかどうかを示します。 この Cookie は、と同時に更新されます `dataservices_customer_id` cookie。
- `dataservices_customer_id`：買い物客がサインインまたはログアウトしたかどうかを示します。 この cookie には、システム内の顧客の一意の ID が含まれます。
- `dataservices_customer_group`：顧客のグループを示します。 この Cookie は次の形式で保存されます。 [sha1](https://en.wikipedia.org/wiki/SHA-1) 顧客のグループ ID のチェックサム。
- `dataservices_cart_id`：買い物客の買い物かごアクションを識別します。 この cookie には、システム内のお客様の一意の買い物かご ID が含まれています。
- `dataservices_product_context`：買い物客の製品インタラクションを識別します。 この Cookie には、システム内の顧客の一意の見積もり ID が含まれています。

## その他の cookie

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）Adobe Commerceのお客様向けに次の Cookie が設定されています。 これらの Cookie は、 [DataServices モジュール](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg`:Snowplow JavaScript トラッカーによって設定されます。 詳しくは、 [Snowplow ドキュメント](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld`：現在の web ページのホスト名に対して、これはhttps://publicsuffix.orgで説明されている「パブリックサフィックス」ではない最上位のドメインです。 基本的に、これは Cookie を受け入れられる最上位のドメインです。 この cookie は [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
