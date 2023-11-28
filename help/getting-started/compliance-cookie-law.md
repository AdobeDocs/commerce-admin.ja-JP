---
title: Cookie の法令遵守
description: 多くの国でクッキーの使用に関する法律に対応するため、Adobe CommerceとMagento Open Sourceはマーチャントに対して、顧客の同意を得る方法を選択できます。
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2145'
ht-degree: 0%

---

# Cookie の法令遵守

cookie とは、サイトの各訪問者のコンピューターに保存され、情報を一時的に保持する場所として使用される小さなファイルです。 Cookie に保存される情報は、買い物かごのパーソナライズ、訪問者の買い物かごへのリンク、トラフィックパターンの測定、プロモーションの効果の向上に使用されます。 多くの国でクッキーの使用に関する法律に対応するため、Adobe CommerceとMagento Open Sourceはマーチャントに対して、顧客の同意を得る方法を選択できます。 Adobe CommerceおよびMagento Open Sourceのデフォルトの Cookie の一覧については、 [Cookie リファレンス](#default-cookies).

>[!NOTE]
>
>デフォルトの [Googleのプライバシー設定](../merchandising-promotions/google-tools.md#google-privacy-settings) 応ずる [EU 一般データ保護規則](compliance-gdpr.md)の場合、Google AnalyticsCookie を使用するためのユーザーの同意を取得する必要はありません。

## 方法 1：暗黙の同意

暗黙の同意とは、ストアへの訪問者が cookie が操作に必要な部分であることを明確に理解し、お客様のサイトを使用することで、cookie を使用する権限を間接的に付与したことを意味します。 黙示的な同意を得るための鍵は、訪問者が十分な情報を提供し、十分な情報に基づいて判断を下すことです。 多くのストアでは、すべての標準ページの上部にメッセージが表示され、cookie の使用方法の概要と、ストアのプライバシーポリシーへのリンクが示されます。 プライバシーポリシーは、ストアが収集する情報の種類と使用方法を記述する必要があります。

## 方法 2：表明された同意

でのストアの操作 _cookie 制限モード_ では、cookie をコンピューターに保存する前に、訪問者が同意を表明する必要があります。 同意が得られない限り、ストアの多くの機能は使用できません。 例えば、ストアでGoogle Analyticsが使用可能な場合、訪問者が Cookie を使用する権限を付与した後でのみ呼び出すことができます。

## Cookie 制限モード

cookie 制限モードが有効になっている場合、ストアへの訪問者に対して、フル機能の操作には cookie が必要である旨の通知が送信されます。 テーマに応じて、メッセージはヘッダーの上、フッターの下、またはページ上の別の場所に表示されます。 このメッセージは、お客様のプライバシーポリシーに詳細情報がリンクされており、「許可」ボタンをクリックして同意するよう訪問者に促します。 同意が得られると、メッセージは表示されなくなります。

お使いの [プライバシーポリシー](privacy-policy.md)) には、ストアの名前と連絡先情報が含まれ、ストアで使用される各 cookie の目的を説明する必要があります。 詳しくは、 [Cookie リファレンス](#default-cookies).

>[!NOTE]
>
>プライバシーポリシーの URL キーを変更した場合、トラフィックを新しい URL キーにリダイレクトするために、カスタム URL の書き換えも作成する必要があります。 それ以外の場合、Cookie 制限モードメッセージ内のリンクは、 `404 Page Not Found`.

![ストアフロントの例 — cookie 制限の通知](./assets/storefront-cookie-restriction-message.png){width="600"}

### 手順 1:Cookie 制限モードを有効にする

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで、 **[!UICONTROL General]**&#x200B;を選択します。 **[!UICONTROL Web]**.

1. を展開します。 **[!UICONTROL Default Cookie Settings]** 」セクションで次の操作を実行します。

   ![Web 設定 — デフォルトの Cookie 設定](./assets/web-default-cookie-settings.png){width="600"}

   - 次を入力します。 **[!UICONTROL Cookie Lifetime]** 秒単位で指定します。

   - 他のフォルダーで Cookie を利用できるようにする場合は、 **[!UICONTROL Cookie Path]**. サイト内の任意の場所で Cookie を使用できるようにするには、スラッシュ (`/`) をクリックします。 この値には、Cookie のパスのみを含めることができ、 **_できません_** には、その他の cookie パラメーターが含まれます。

   - サブドメインで Cookie を使用できるようにするには、 **[!UICONTROL Cookie Domain]** フィールド (`subdomain.yourdomain.com`) をクリックします。 すべてのサブドメインで Cookie を使用できるようにするには、ドメイン名の前にピリオド (`.yourdomain.com`) をクリックします。 この値には、Cookie ドメインのみを含めることができ、 **_できません_** には、その他の cookie パラメーターが含まれます。

   - JavaScript などのスクリプト言語が cookie にアクセスできないようにするには、必ず **HTTP のみを使用** が `Yes`.

   - 設定 **[!UICONTROL Cookie Restriction Mode]** から `Yes`.

     必要に応じて、チェックボックスをオフにして、 **[!UICONTROL OK]** スコープの切り替えを確認します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** リンクをクリックします。 次に、無効な各キャッシュを更新します。

### 手順 2：プライバシーポリシーを更新する

を更新します。 [プライバシーポリシー](privacy-policy.md) 会社が収集した情報とその使用方法を反映したものになります。

## デフォルトの cookie

Adobe CommerceとMagento Open Sourceのデフォルトの cookie は、商人がプライバシー規制 ( [GDPR](compliance-gdpr.md). マーチャントはこの情報をガイドとして使用し、プライバシーポリシーと cookie ポリシーを包括的なプライバシー規制コンプライアンス戦略の一環として更新するために法務顧問に相談する必要があります。

次の Cookie は、 [!DNL Commerce] オンプレミスおよびクラウドインストールの場合は「out of box」です。 これらの cookie は、お客様から明示的に要求された機能で必要になる場合があります。 セッション cookie の有効期間について詳しくは、 [セッションの有効期間](../customers/customer-online-options.md).

これらの cookie の一部には、必要に応じて有効/無効を含む設定オプションが用意されています。

### 要求された機能 Cookie （適用対象外）


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ )Google Tag Manager で使用されます。 買い物かごから削除された製品の SKU、名前、価格および数量をキャプチャし、サードパーティのスクリプトで情報を将来の統合に使用できるようにします。

#### `guest-view`

ゲスト買い物客が注文ステータスを取得するために使用する注文 ID を保存します。 ゲストによる注文ビュー。 使用場所 _[!DNL Orders and Returns]_ウィジェット。

- 安全ですか？ いいえ
- HTTP のみ：はい
- 有効期限ポリシー：セッション
- モジュール： `Magento_Sales`

#### `login_redirect`

顧客がログインを指示される前に読み込まれていた宛先ページを保持します。 ログインした顧客に対して、ログインリダイレクトはミニカートと共に使用されます ( [ミニカートを表示](../stores-purchase/cart-configuration.md#mini-cart) 設定オプションは次のように設定されます。 `Yes`.

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール： `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) バナーコンテンツをローカルに保存して、パフォーマンスを向上させます。

#### `mage-messages`

Cookie の同意メッセージや様々なエラーメッセージなど、ユーザーに表示されるエラーメッセージやその他の通知を追跡します。 メッセージは、買い物客に表示された後に、Cookie から削除されます。

この cookie を無効にするオプションはありません。

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：期間 1 年。 メッセージがユーザーに表示される際に、フロントエンドでクリアされました。
- モジュール： `Magento_Theme`

#### `mage-translation-storage` （ローカルストレージ）

買い物客からリクエストされた場合に翻訳されたコンテンツを保存します。 次の場合に使用 [翻訳戦略](../configuration-reference/advanced/developer.md) は、「辞書（ストアフロント側の翻訳）」として設定されます。

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Translation`

#### `mage-translation-file-version` （ローカルストレージ）

ローカルストレージ内の翻訳のバージョンを追跡します。 次の場合に使用 [翻訳戦略](../configuration-reference/advanced/developer.md) 次のように設定されています： `Dictionary (Translation on Storefront side)`.

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Translation`

#### `product_data_storage` （ローカルストレージ）

最近表示された製品/比較対象の製品に関連する製品データの設定を格納します。

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Catalog`

#### `recently_compared_product` （ローカルストレージ）

最近比較した製品の製品 ID を格納します。

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Catalog`

#### `recently_compared_product_previous` （ローカルストレージ）

ナビゲーションを容易にするために、以前と比較した製品の製品 ID を保存します。

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Catalog`

#### `recently_viewed_product` （ローカルストレージ）

最近表示した製品の製品 ID を保存し、ナビゲーションを容易にします。

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Catalog`

#### `recently_viewed_product_previous` （ローカルストレージ）

最近表示された製品の製品 ID を保存し、ナビゲーションを容易にします。

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 使用者 [Google Tag Manager](../merchandising-promotions/google-tag-manager.md). 買い物かごに追加された製品の SKU、名前、価格、数量をキャプチャし、サードパーティのスクリプトでその情報を将来の統合に使用できるようにします。

#### `stf`

SendFriend ([友達にメールを送信](../stores-purchase/email-a-friend.md)) モジュールです。

- 安全ですか？ はい
- HTTP のみ：はい
- 有効期限ポリシー：セッション
- モジュール： `Magento_SendFriend`

#### `X-Magento-Vary`

Vanish 静的コンテンツキャッシュを使用する際のパフォーマンスを向上させる構成設定。

- 安全ですか？ はい
- HTTP のみ：はい
- 有効期限ポリシー： PHP の設定に基づく session.cookie_lifetime
- モジュール： `Magento_PageCache`

#### `form_key`

クロスサイトリクエストフォージェリ (CSRF) からデータを保護するために、すべてのフォーム送信にランダムな文字列を追加するセキュリティ対策です。

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：
   - PHP: PHP の設定に基づく session.cookie_lifetime
   - JS：セッション
- モジュール：ページキャッシュ

#### `mage-cache-sessid`

この Cookie の値は、ローカルキャッシュストレージのトリガーをクリーンアップします。 バックエンドアプリケーションによって cookie が削除されると、管理者はローカルストレージをクリーンアップし、cookie の値をに設定します。 `true`.

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール： `Magento_Customer`

#### `mage-cache-storage`

e コマース機能を有効にする訪問者固有のコンテンツのローカルストレージ。

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール： `Magento_Customer`, `Magento_Persistent`

#### `mage-cache-storage` （ローカルストレージ）

e コマース機能を有効にする訪問者固有のコンテンツのローカルストレージ。

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール： `Magento_Customer`, `Magento_Persistent`, `Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` （ローカルストレージ）

無効化する必要のある特定のコンテンツセクションを強制的にローカルに保存します。

- 安全ですか？ いいえ
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージごと
- モジュール： `Magento_Customer`

#### `persistent_shopping_cart`

匿名の買い物客が買い物かごを復元できるように、永続的な買い物かごのキー (ID) を保存します。

- 安全ですか？ はい
- HTTP のみ：はい
- 有効期限ポリシー：基準 [永続的な買い物かご](../stores-purchase/cart-persistent.md)  — 永続性の有効期間（秒）設定
- モジュール： `Magento_Persistent`

#### `private_content_version`

顧客コンテンツを含むページに、ランダムで一意の数と時間を追加して、サーバー上でキャッシュされないようにします。

これは複数の場所に設定されます。PHP、JavaScript では cookie として、JavaScript ではローカルストレージとしてです。

HTTP のみ=の場合`Yes` （リクエストに基づく）とは、HTTPS リクエスト時に設定される場合は cookie がセキュアで、HTTP リクエスト時に設定される場合は unsecure であることを意味します。

- 安全ですか？ `Yes` （リクエストに基づいて） `No`
- HTTP のみ： `No`
- 有効期限ポリシー：基準 [永続的な買い物かご](../stores-purchase/cart-persistent.md)  — 永続性の有効期間（秒）設定
   - PHP: `1` 年/ `315360000s` （10 年）
   - JS: `1` 日
   - JS ローカルストレージ：ローカルストレージルールごと（無期限）
- モジュール： `Magento_PageCache`, `Magento_Customer`

#### `section_data_ids`

買い物客が開始したアクションに関する顧客固有の情報（ウィッシュリストの表示やチェックアウト情報など）を格納します。

- 安全ですか？ `No`
- HTTP のみ： `No`
- 有効期限ポリシー： `Session`
- モジュール： `Magento_Customer`

#### `store`

買い物客が選択した特定のストア表示/ロケールを追跡します。

- 安全ですか？ `No`
- HTTP のみ： `Yes`
- 有効期限ポリシー： `1` 年
- モジュール： `Magento_Store`

#### `mage-banners-cache-storage`  — ローカルストレージ

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) バナー機能用のローカルストレージ。

- 安全ですか？ `No`
- HTTP のみ： `No`
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール： `Magento_Banner`

## Google Analyticsの cookie

次の Cookie は、 [Google Analytics](../merchandising-promotions/google-analytics.md) またはGoogle Universal Analytics がインストールで完全に有効になっている。 プライバシー規制への準拠のためにこれらの cookie を無効にするには、 [Google Privacy Settings](../merchandising-promotions/google-tools.md#google-privacy-settings). 詳しくは、 [Web サイトでのGoogle AnalyticsCookie の使用][1].

### Google Universal Analytics の cookie — 非免除

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ )JavaScript ライブラリ： `gtag.js` および `analytics.js`

- `_ga`：サイトへの訪問者を区別します。
- `_gid`：サイトへの訪問者を区別します。
- `gat`：リクエスト率をスロットルするために使用します。
- `dc_gtm_<property-id>`：でGoogle Analyticsがデプロイされたときのリクエスト率を制限します。 [Google Tag Manager](../merchandising-promotions/google-tag-manager.md).
- `AMP_TOKEN`:AMP Client ID サービスからクライアント ID を取得するために使用できるトークンを含みます。 その他の指定可能な値には、オプトアウト、inflight リクエスト、AMP クライアント ID サービスからクライアント ID を取得する際のエラーなどがあります。
- `_gac_<property-id>`：ユーザーのキャンペーン関連情報が含まれます。 Google AdWords コンバージョンGoogle Analyticsは、 [AdWords][2] アカウント。

### Google AnalyticsCookie — 非適用

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ )JavaScript ライブラリの場合： `ga.js`

- `__utma`：買い物客とセッションを区別します。 この cookie は、JavaScript ライブラリが実行され、既存の JavaScript ライブラリが存在しない場合に作成されます `__utma` cookie. cookie は、データがGoogle Analyticsに送信されるたびに更新されます。
- `__utmt`：リクエスト率をスロットルするために使用します。
- `__utmb`：新しいセッション/訪問を決定します。 この cookie は、JavaScript ライブラリが実行され、既存の JavaScript ライブラリが存在しない場合に作成されます `__utmb` cookie. cookie は、データがGoogle Analyticsに送信されるたびに更新されます。
- `_utmz`：買い物客がサイトに到達した方法を説明するトラフィックソースまたはキャンペーンを保存します。 Cookie は、JavaScript ライブラリが実行されると作成され、データがGoogle Analyticsに送信されるたびに更新されます。
- `__utmv`：訪問者レベルのカスタム変数データを格納します。 この cookie は、開発者が `_setCustomVar` メソッドを訪問者レベルのカスタム変数で使用する必要があります。 この cookie は、データがGoogle Analyticsに送信されるたびに更新されます。

## 製品のRecommendationsの cookie

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ )Product Recommendationsでは、Adobe Commerceのお客様に対して次の Cookie が使用されます。 これらの cookie は、 [DataServices モジュール](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg_dnt`：次の操作を実行できます。 [Adobe Commerceのデータ収集を制限](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html) サイト上で cookie の同意を管理するカスタムコードがある場合。
- `user_allowed_save_cookie`：に使用 [cookie 制限モード](#cookie-restriction-mode).
- `authentication_flag`：買い物客がサインインしたか、サインアウトしたかを示します。 この cookie は、 `dataservices_customer_id` cookie.
- `dataservices_customer_id`：買い物客がサインインしたか、サインアウトしたかを示します。 この Cookie には、システム内での顧客の一意の ID が含まれます。
- `dataservices_customer_group`：顧客のグループを示します。 この cookie は、 [sha1](https://en.wikipedia.org/wiki/SHA-1) 顧客のグループ ID のチェックサム。
- `dataservices_cart_id`：買い物客の買い物かごのアクションを識別します。 この Cookie には、システム内での顧客の一意の買い物かご ID が含まれます。
- `dataservices_product_context`：買い物客の製品のインタラクションを識別します。 この cookie には、システム内での顧客の一意の見積もり ID が含まれます。

## その他の cookie

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ )Adobe Commerceのお客様向けに、次の Cookie が設定されています。 これらの cookie は、 [DataServices モジュール](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg`:Snowplow JavaScript トラッカーによって設定されます。 詳しくは、 [Snowplow ドキュメント](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld`：現在の Web ページのホスト名が、https://publicsuffix.orgで説明されているように、「パブリックサフィックス」でない最上位のドメインです。 基本的に、これは cookie を受け入れることができる最上位のドメインです。 この cookie は、 [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
