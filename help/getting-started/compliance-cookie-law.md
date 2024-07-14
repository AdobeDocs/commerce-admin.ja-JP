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

Cookie は、サイトへの各訪問者のコンピューターに保存される小さなファイルで、情報の一時的な保持場所として使用されます。 Cookie に保存される情報は、ショッピングエクスペリエンスのパーソナライズ、訪問者の買い物かごへのリンク、トラフィックパターンの測定、プロモーションの有効性の向上に使用されます。 Cookie の使用に関する多くの国の法律に対応するために、Adobe CommerceとMagento Open Sourceでは、マーチャントに対して、お客様の同意を得るための選択肢を提供しています。 Adobe CommerceおよびMagento Open Sourceのデフォルト cookie のリストについては、[Cookie リファレンス ](#default-cookies) を参照してください。

>[!NOTE]
>
>[EU 一般データ保護規則 ](compliance-gdpr.md) に準拠するためにデフォルトの ](../merchandising-promotions/google-tools.md#google-privacy-settings)0}Google プライバシー設定 } を変更する場合、Google Analytics Cookie の使用に関するユーザーの同意を得る必要はありません。[

## 方法 1：暗黙の同意

黙示的な同意とは、ストアの訪問者が、Cookie が操作に必要な部分であることを明確に理解し、サイトを使用することで、それらを使用する権限を間接的に付与していることを意味します。 暗黙の同意を得るための鍵は、訪問者が十分な情報に基づいた意思決定をおこなうための十分な情報を提供することです。 多くのストアでは、すべての標準ページの上部にメッセージが表示され、ストアのプライバシーポリシーへのリンクとともに、cookie の使用方法の概要が表示されます。 プライバシーポリシーには、ストアが収集する情報の種類と使用方法を記述する必要があります。

## 方法 2：同意の表明

ストアを _cookie 制限モード_ で操作するには、訪問者は、cookie をコンピューターに保存する前に同意を表明する必要があります。 同意が得られない限り、ストアの多くの機能は使用できません。 例えば、ストアでGoogle Analyticsが使用可能な場合、訪問者が Cookie の使用権限を付与した後にのみ呼び出すことができます。

## cookie 制限モード

cookie 制限モードが有効になっている場合、ストアを訪問した訪問者には、フル機能の操作に cookie が必要であることを通知されます。 テーマに応じて、メッセージはヘッダーの上、フッターの下、またはページ上の別の場所に表示される場合があります。 このメッセージは、詳細情報を提供するプライバシーポリシーにリンクしており、訪問者が「許可」ボタンをクリックして同意を付与するよう促しています。 同意が得られると、メッセージは消えます。

[ プライバシーポリシー ](privacy-policy.md)）には、ストアの名前と連絡先情報を含め、ストアで使用される各 Cookie の目的を説明する必要があります。 詳しくは、[Cookie リファレンス ](#default-cookies) を参照してください。

>[!NOTE]
>
>プライバシーポリシーの URL キーを変更する場合は、新しい URL キーにトラフィックをリダイレクトするようにカスタム URL 書き換えを作成する必要もあります。 それ以外の場合は、Cookie 制限モード メッセージ内のリンクは `404 Page Not Found` を返します。

![ ストアフロントの例 – cookie 制限通知 ](./assets/storefront-cookie-restriction-message.png){width="600"}

### 手順 1:cookie 制限モードを有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のナビゲーションパネルの **[!UICONTROL General]** の下で、「**[!UICONTROL Web]**」を選択します。

1. 「**[!UICONTROL Default Cookie Settings]**」セクションを展開し、次の操作を実行します。

   ![Web 設定 – デフォルトの cookie 設定 ](./assets/web-default-cookie-settings.png){width="600"}

   - **[!UICONTROL Cookie Lifetime]** を秒単位で入力します。

   - 他のフォルダーで Cookie を使用できるようにする場合は、**[!UICONTROL Cookie Path]** を入力します。 サイトの任意の場所で cookie を使用できるようにするには、スラッシュ（`/`）を入力します。 この値には、cookie パスのみを含めることができ、その他の cookie パラメーターを含めることはで **_ません_**。

   - サブドメインで cookie を使用できるようにするには、「**[!UICONTROL Cookie Domain]**」フィールド（`subdomain.yourdomain.com`）にサブドメイン名を入力します。 すべてのサブドメインで cookie を使用できるようにするには、ドメイン名の前にピリオド（`.yourdomain.com`）を入力します。 この値には、cookie ドメインのみを含めることができ、その他の cookie パラメーターを含めること **_できません_**。

   - JavaScriptなどのスクリプト言語が Cookie にアクセスしないようにするには、**HTTP のみを使用** が `Yes` に設定されていることを確認します。

   - **[!UICONTROL Cookie Restriction Mode]** を `Yes` に設定します。

     必要に応じて、チェックボックスをオフにし、「**[!UICONTROL OK]**」をクリックして範囲の切り替えを確定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

1. キャッシュを更新するように求められたら、システムメッセージの **[!UICONTROL Cache Management]** リンクをクリックします。 次に、無効な各キャッシュを更新します。

### 手順 2：プライバシーポリシーを更新する

会社が収集する情報とその使用方法が反映されるように [ プライバシーポリシー ](privacy-policy.md) を更新します。

## デフォルトの Cookie

Adobe CommerceとMagento Open Sourceのデフォルトの Cookie は、マーチャントが [GDPR](compliance-gdpr.md) などのプライバシー規制の要件を満たすのに役立つように、免除/非免除に分類されています。 マーチャントは、この情報を参考にして、法的アドバイザーに相談して、包括的なプライバシー規制コンプライアンス戦略の一環としてプライバシーと Cookie ポリシーを更新する必要があります。

次の Cookie は [!DNL Commerce] オンプレミスおよびクラウドのインストール用に「標準」で使用されます。 これらの Cookie は、お客様から明示的にリクエストされた機能で必要になる場合があります。 セッション Cookie の有効期間については、[ セッションの有効期間 ](../customers/customer-online-options.md) を参照してください。

これらの Cookie の一部では、必要に応じて、有効/無効を含む設定オプションが提供される場合があります。

### リクエストされた機能の Cookie （除外）


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）Google Tag Manager で使用されます。 買い物かごから削除された製品 SKU、名前、価格、数量をキャプチャし、サードパーティスクリプトによって今後の統合で情報を利用できるようにします。

#### `guest-view`

ゲストの買い物客が注文ステータスを取得するために使用する注文 ID を格納します。 ゲスト注文表示。 _[!DNL Orders and Returns]_ウィジェットで使用されます。

- 安全ですか？ 不可
- HTTP のみ：はい
- 有効期限ポリシー：セッション
- モジュール：`Magento_Sales`

#### `login_redirect`

顧客がログインを指示される前に読み込まれていた宛先ページを保持します。 ログイン リダイレクトは、[ ミニ カートを表示 [] 構成オプションが `Yes` に設定されている場合に、ログインしている顧客のミニ カート ](../stores-purchase/cart-configuration.md#mini-cart) 使用されます。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール：`Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）パフォーマンスを向上させるために、バナーコンテンツをローカルに保存します。

#### `mage-messages`

Cookie 同意メッセージ、様々なエラーメッセージなど、ユーザーに表示されるエラーメッセージやその他の通知をトラッキングします。 メッセージは、買い物客に表示された後、Cookie から削除されます。

この cookie を無効にするオプションはありません。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：期間 1 年。 メッセージがユーザーに表示される際に、フロントエンドでクリアされます。
- モジュール：`Magento_Theme`

#### `mage-translation-storage` （ローカルストレージ）

買い物客からリクエストされた際に、翻訳済みコンテンツを格納します。 [ 翻訳戦略 ](../configuration-reference/advanced/developer.md) が「辞書（ストアフロント側での翻訳）」として設定されている場合に使用します。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール：`Magento_Translation`

#### `mage-translation-file-version` （ローカルストレージ）

ローカルストレージ内の翻訳のバージョンをトラッキングします。 [ 翻訳戦略 ](../configuration-reference/advanced/developer.md) が `Dictionary (Translation on Storefront side)` として設定されている場合に使用されます。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール：`Magento_Translation`

#### `product_data_storage` （ローカルストレージ）

最近閲覧/比較された製品に関連する製品データの設定を保存します。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール：`Magento_Catalog`

#### `recently_compared_product` （ローカルストレージ）

最近比較した製品の製品 ID を格納します。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール：`Magento_Catalog`

#### `recently_compared_product_previous` （ローカルストレージ）

前に比較した製品の製品 ID を保存してナビゲーションを容易にします。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール：`Magento_Catalog`

#### `recently_viewed_product` （ローカルストレージ）

最近閲覧した製品の製品 ID を保存して、ナビゲーションを簡単にします。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール：`Magento_Catalog`

#### `recently_viewed_product_previous` （ローカルストレージ）

最近閲覧した製品の製品 ID を保存して、ナビゲーションを簡単にします。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール：`Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） [Google Tag Manager が使用 ](../merchandising-promotions/google-tag-manager.md)。 買い物かごに追加された製品 SKU、名前、価格、数量をキャプチャし、サードパーティスクリプトによって今後の統合で情報を利用できるようにします。

#### `stf`

SendFriend （[Email a Friend](../stores-purchase/email-a-friend.md)） モジュールによってメッセージが送信された時間を記録します。

- 安全ですか？ はい
- HTTP のみ：はい
- 有効期限ポリシー：セッション
- モジュール：`Magento_SendFriend`

#### `X-Magento-Vary`

Varnish 静的コンテンツ キャッシュを使用する際のパフォーマンスを向上させる構成設定。

- 安全ですか？ はい
- HTTP のみ：はい
- 有効期限ポリシー：PHP の session.cookie_lifetime 設定に基づく
- モジュール：`Magento_PageCache`

#### `form_key`

すべてのフォーム送信にランダムな文字列を追加して、クロスサイトリクエストフォージェリ（CSRF）からデータを保護するセキュリティ対策。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：
   - PHP: session.cookie_lifetime の設定に基づく
   - JS:Session
- モジュール：ページキャッシュ

#### `mage-cache-sessid`

この cookie の値は、ローカルキャッシュストレージのクリーンアップをトリガーします。 Cookie がバックエンドアプリケーションによって削除されると、管理者はローカルストレージをクリーンアップし、cookie の値を `true` に設定します。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール：`Magento_Customer`

#### `mage-cache-storage`

e コマース機能を有効にする訪問者固有のコンテンツのローカルストレージ。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール：`Magento_Customer`、`Magento_Persistent`

#### `mage-cache-storage` （ローカルストレージ）

e コマース機能を有効にする訪問者固有のコンテンツのローカルストレージ。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：セッション
- モジュール：`Magento_Customer`、`Magento_Persistent`、`Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` （ローカルストレージ）

無効化する必要がある特定のコンテンツセクションのローカルストレージを強制します。

- 安全ですか？ 不可
- HTTP のみ：いいえ
- 有効期限ポリシー：ローカルストレージあたり
- モジュール：`Magento_Customer`

#### `persistent_shopping_cart`

永続的な買い物かごのキー（ID）を格納して、匿名の買い物客に買い物かごを復元できるようにします。

- 安全ですか？ はい
- HTTP のみ：はい
- 有効期限ポリシー：[ 永続的な買い物かご ](../stores-purchase/cart-persistent.md) – 永続有効期間（秒）の設定に基づいています
- モジュール：`Magento_Persistent`

#### `private_content_version`

顧客コンテンツを含んだページにランダムな一意の番号と時間を追加して、ページがサーバー上にキャッシュされないようにします。

PHP では、JavaScript as a cookie で、JavaScriptでは、ローカルストレージに対して、複数の場所で設定されます。

HTTP のみ=`Yes` （リクエストに基づく）の場合、Cookie は HTTPS リクエストの最中に設定されると保護され、HTTP リクエストの最中に設定されると保護されません。

- 安全ですか？ `Yes` （リクエストに基づく）、`No`
- HTTP のみ：`No`
- 有効期限ポリシー：[ 永続的な買い物かご ](../stores-purchase/cart-persistent.md) – 永続有効期間（秒）の設定に基づいています
   - PHP: `1` 年/`315360000s` （10 年）
   - JS:`1` 日
   - JS ローカルストレージ：ローカルストレージルールごと（永続的）
- モジュール：`Magento_PageCache`、`Magento_Customer`

#### `section_data_ids`

買い物客が開始したアクションに関連する、顧客固有の情報を格納します（ウィッシュリストの表示やチェックアウト情報など）。

- 安全ですか？`No`
- HTTP のみ：`No`
- 有効期限ポリシー：`Session`
- モジュール：`Magento_Customer`

#### `store`

買い物客が選択した特定のストア表示/ロケールをトラッキングします。

- 安全ですか？`No`
- HTTP のみ：`Yes`
- 有効期限ポリシー：`1` 年
- モジュール：`Magento_Store`

#### `mage-banners-cache-storage` - ローカルストレージ

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）バナー機能用のローカルストレージ。

- 安全ですか？`No`
- HTTP のみ：`No`
- 有効期限ポリシー：ローカルストレージルールごと
- モジュール：`Magento_Banner`

## Google Analyticsの cookie

次の Cookie は、[Google Analytics](../merchandising-promotions/google-analytics.md) またはGoogle Universal Analytics がインストールで完全に有効な場合に使用されます。 プライバシー規制に準拠するためにこれらの Cookie を無効にするには、[Google プライバシー設定 ](../merchandising-promotions/google-tools.md#google-privacy-settings) を参照してください。 詳しくは、[Web サイトでのGoogle Analytics cookie の使用 ][1] を参照してください。

### Google Universal Analytics の Cookie – 適用除外なし

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）JavaScript ライブラリ：`gtag.js` および `analytics.js`

- `_ga`：サイトへの訪問者を区別します。
- `_gid`：サイトへの訪問者を区別します。
- `gat`：リクエスト率のスロットルに使用されます。
- `dc_gtm_<property-id>`: [Google Tag Manager](../merchandising-promotions/google-tag-manager.md) でGoogle Analyticsがデプロイされる際のリクエスト率を調整します。
- `AMP_TOKEN`:AMP Client ID サービスからクライアント ID を取得するために使用できるトークンが含まれています。 その他の使用可能な値には、オプトアウト、実行中のリクエスト、AMP Client ID サービスからのクライアント ID の取得エラーなどがあります。
- `_gac_<property-id>`：ユーザーのキャンペーン関連の情報が含まれます。 Google AdWords コンバージョンタグは、Google Analyticsが [AdWords][2] アカウントにリンクされている場合にこの cookie を読み取ります。

### Google Analyticsの Cookie – 適用除外なし

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）JavaScript ライブラリ：`ga.js`

- `__utma`：買い物客とセッションを区別します。 この cookie は、JavaScript ライブラリの実行時に作成され、`__utma` の Cookie が存在しません。 cookie は、データがGoogle Analyticsに送信されるたびに更新されます。
- `__utmt`：リクエスト率のスロットルに使用されます。
- `__utmb`：新規セッション/訪問回数を決定します。 この cookie は、JavaScript ライブラリの実行時に作成され、`__utmb` の Cookie が存在しません。 cookie は、データがGoogle Analyticsに送信されるたびに更新されます。
- `_utmz`：買い物客がサイトに到達した方法を説明するトラフィックソースまたはキャンペーンを保存します。 この cookie はJavaScript ライブラリの実行時に作成され、Google Analyticsにデータが送信されるたびに更新されます。
- `__utmv`：訪問者レベルのカスタム変数データを格納します。 この cookie は、開発者が訪問者レベルのカスタム変数で `_setCustomVar` メソッドを使用すると作成されます。 この cookie はGoogle Analyticsにデータが送信されるたびに更新されます。

## 製品のRecommendationsの cookie

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）次の Cookie が Product RecommendationsでAdobe Commerceのお客様向けに使用されます。 これらの Cookie は [DataServices モジュール ](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html) と共にインストールされます。

- `mg_dnt`：サイトで cookie の同意を管理するカスタムコードがある場合は、](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html)Adobe Commerce データ収集を制限 [ できます。
- `user_allowed_save_cookie`: [cookie 制限モード ](#cookie-restriction-mode) に使用されます。
- `authentication_flag`：買い物客がサインインまたはログアウトしたかどうかを示します。 この cookie は、`dataservices_customer_id` cookie と同時に更新されます。
- `dataservices_customer_id`：買い物客がサインインまたはログアウトしたかどうかを示します。 この cookie には、システム内の顧客の一意の ID が含まれます。
- `dataservices_customer_group`：顧客のグループを示します。 この cookie は、顧客のグループ ID の [sha1](https://en.wikipedia.org/wiki/SHA-1) チェックサムとして保存されます。
- `dataservices_cart_id`：買い物客の買い物かごアクションを識別します。 この cookie には、システム内のお客様の一意の買い物かご ID が含まれています。
- `dataservices_product_context`：買い物客の製品インタラクションを識別します。 この Cookie には、システム内の顧客の一意の見積もり ID が含まれています。

## その他の cookie

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） Adobe Commerceのお客様向けに設定されている Cookie は次のとおりです。 これらの Cookie は [DataServices モジュール ](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html) と共にインストールされます。

- `mg`: Snowplow JavaScript トラッカーによって設定されます。 詳しくは、[Snowplow ドキュメント ](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options) を参照してください。
- `com.adobe.alloy.getTld`：現在の web ページのホスト名では、https://publicsuffix.orgで説明されているように、「パブリックサフィックス」ではない最上位のドメインになります。 基本的に、これは Cookie を受け入れられる最上位のドメインです。 この cookie は [Alloy Web SDK](https://github.com/adobe/alloy) の一部です。

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
