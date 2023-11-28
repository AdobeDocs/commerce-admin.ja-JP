---
title: '''[!DNL B2B for Adobe Commerce] リリースノート'
description: リリースノートで [!DNL B2B for Adobe Commerce] 拡張機能のリリース。
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 1123cf4b257a83a61914c378104c43e952512e7d
workflow-type: tm+mt
source-wordcount: '6937'
ht-degree: 0%

---

# [!DNL B2B for Adobe Commerce] リリースノート

B2B 拡張機能に関するこれらのリリースノートでは、リリースサイクル中にAdobeが追加した追加や修正点を示します。以下に例を示します。

![新規](../assets/new.svg) 新機能
![修正された問題](../assets/fix.svg) 修正点および改善点
![既知の問題](../assets/bug.svg) 既知の問題

>[!NOTE]
>
>詳しくは、 [製品の可用性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) 使用可能なAdobe Commerceリリースでサポートされている B2B Commerce 拡張機能のバージョンについて詳しくは、を参照してください。

## B2B 1.5.0-beta

{{$include /help/_includes/b2b-beta-note.md}}

*2023 年 11 月 14 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

B2B v1.5.0-beta リリースには、新機能、品質の改善、バグ修正が含まれています。

![新規](../assets/new.svg) 見積もり機能の改善により、購入者と販売者は見積もりと見積もり交渉をより効果的に管理できます。

- **見積もりを下書きとして保存**<!--B2B-2566-->— [見積もりリクエスト](quote-request.md) 買い物かごから、購入者は、「 **[!UICONTROL Save as Draft]** の [!UICONTROL Request a Quote] フォーム。

  下書き見積もりに有効期限がありません。 購入者は、 [!UICONTROL My Quotes] 」セクションに表示されます。

- **見積もりの名前を変更**<!--B2B-2596--> — 購入者は、 [見積もりの詳細](account-dashboard-my-quotes.md#quote-actions) ページを選択して **[!UICONTROL Rename]** オプション。 このオプションは、承認された購入者が見積もりの編集時に使用できます。 名前変更イベントは、Quote History Log に記録されます。

- **見積もりの複製**<!--B2B-2701--> — 購入者と販売者は、既存の見積もりをコピーして、新しい見積もりを作成できるようになりました。 Quote の詳細ビューで、「  **[!UICONTROL Create Copy]** の [見積もりの詳細ビュー](quote-price-negotiation.md#button-bar) ( 管理者または [ストアフロント](account-dashboard-my-quotes.md#quote-actions).

- **品目の割引ロック**<!--B2B-2597--> — 見積のネゴシエーション中、販売者は、割引を適用する際に、より柔軟に行項目の割引ロックを使用できます。 例えば、販売者は特別な行項目の割引を品目に適用し、品目をロックして、それ以上の割引を防ぐことができます。 品目がロックされている場合、見積レベルの割引が適用されると品目価格は更新できません。 詳しくは、 [購入者の見積もりを開始](sales-rep-initiates-quote.md).

![新規&#x200B;](../assets/new.svg)**会社管理**<!--B2B-2901--> — マーチャントは、指定された親会社に会社を割り当てることで、Adobe Commerceの会社を階層組織として表示および管理できるようになりました。 会社を親に割り当てた後は、親会社管理者が会社アカウントを管理できます。 会社の割り当てを追加および管理できるのは、権限を持つ管理者ユーザーだけです。 詳しくは、 [会社階層の管理](assign-companies.md).

- 会社ページで、新しい **[!UICONTROL Company Type]** フィールドは、親会社と子会社を識別します。 マーチャントは、会社タイプ別に会社ビューをフィルタリングし、行項目または一括アクションを使用して会社を管理できます。

- マーチャントは、新しい **[!UICONTROL Company Hierarchy]** のセクション [!UICONTROL Company Account] ページに貼り付けます。

- API 開発者は、新しい会社関係 REST API エンドポイントを使用できます。 `/V1/company/{parentId}/relations` 会社の割り当てを作成、表示、および削除するには、次の手順に従います。 詳しくは、 [会社オブジェクトの管理](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) （内） *Web API 開発者ガイド*.

![修正された問題](../assets/fix.svg)<!--ACP2E-1984-->クリックした **[!UICONTROL Print]** 管理者の [Quote の詳細 ] ビューのボタンが表示され、見積もりをPDFとして保存するよう求められます。 以前は、マーチャントは引用の詳細を含むページにリダイレクトされていました。

![修正された問題](../assets/fix.svg) <!--ACP2E-1742-->以前は、0 パーセントの顧客見積を送信し、数量を変更すると、管理者は例外をスローしましたが、数量は保存していました。 この修正が適用された後、 `0 percentage` メッセージに対する適切な例外がスローされます。

![修正された問題](../assets/fix.svg) <!--ACP2E-1742-->見積ネゴシエーション中に、販売者は次の項目を指定できます。 `0%` 「交渉済み見積もり」の「割引」フィールドに値引きを入力し、見積もりを購入者に送り返します。 以前は、販売者が 0%の割引を受けて見積もりを購入者に送り返した場合、管理者は `Exception occurred during quote sending` エラーメッセージ。

![修正された問題](../assets/fix.svg) <!--ACP2E-2097-->ReCaptcha V3 がストアフロントのチェックアウト用に設定されている場合、B2B 見積もりのチェックアウトプロセス中に ReCaptcha 検証が正しく機能するようになりました。 以前は、検証は `recaptcha validation failed, please try again` エラーメッセージ。

![修正された問題](../assets/fix.svg) <!--ACP2E-1825-->会社がブロックされた後、会社に関連付けられたユーザーが発注を行うことができなくなりました。 以前は、会社に関連付けられたユーザーは、会社がブロックされたときに発注を行うことがありました。

![修正された問題](../assets/fix.svg)<!--ACP2E-1933-->会社の管理者がストアフロントから会社のユーザーを追加できるようになりました。 以前は、管理者ユーザーが新しいユーザーを追加しようとすると、Commerce はエラーをログに記録していました。 `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

## B2B v1.4.2

*2023 年 10 月 11 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

B2B v1.4.2 リリースには、品質の改善とバグ修正が含まれています

![修正された問題](../assets/fix.svg) <!--B2B-2897-->販売者が、購入者の会社に関連付けられた共有カタログにない製品 SKU を含む購入者の見積もりを作成すると、エラーメッセージが表示されます `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  販売者は、利用できない製品を削除するまで見積もりを保存できません。 以前は、見積もりは使用できない SKU を含めて保存され、見積もりのストアフロントへの読み込みに失敗していました。

## B2B v1.4.1

*2023 年 8 月 8 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Adobe Commerce 2.4.7-beta1 との互換性。

B2B v1.4.1 リリースには、品質の改善とバグ修正が含まれています。

![修正された問題](../assets/fix.svg) <!--ACP2E-1825-->会社がブロックされた後、会社に関連付けられたユーザーが発注を行うことができなくなりました。 以前は、会社に関連付けられたユーザーは、会社がブロックされたときに発注を行うことがありました。

![修正された問題](../assets/fix.svg) <!--ACP2E-1943-->ストアフロントに製品のバックオーダーステータスが正しく表示されるようになりました。 以前は、出荷に使用できた製品が誤って逆注文と見なされていました。

![修正された問題](../assets/fix.svg) <!--ACP2E-1862-->会社登録フォームに顧客ファイルタイプ属性が含まれる場合、登録プロセス中にアップロードされたファイルが、会社の作成後に会社管理者のアカウント情報に含まれるようになりました。 以前は、添付ファイルが見つかりませんでした。

![修正された問題](../assets/fix.svg) <!--ACP2E-1793-->設定可能な製品のスウォッチセレクターが、購買依頼リスト項目設定ページに期待どおりに表示されるようになりました。 以前は、スウォッチセレクターは、購買依頼リスト項目設定ページのドロップダウンフィールドとして表示されていました。

![修正された問題](../assets/fix.svg) <!--ACP2E-1968-->を使用する場合、 [会社のGraphQLクエリ](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) 会社の詳細を返すために、結果がエラーなしで正常に返されるようになりました。

## B2B v1.4.0

*2023 年 6 月 14 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Adobe Commerce 2.4.7-beta1 との互換性

このリリースには、B2B のネゴシエーション可能な見積もりと複数のバグ修正に関する新機能および機能強化が含まれています。

![新規](../assets/new.svg) Adobe Commerce 2.4.7-beta1 との互換性を追加しました。

![新規](../assets/new.svg) **販売者が見積もりを開始しました** — 販売者は、管理者の「Quote」グリッドと「Customer」グリッドから、購入者の見積もりを直接開始できるようになりました。 この機能により、見積もりプロセスが合理化され、お客様の複雑さが軽減されます。 顧客が受注を開始していない場合、販売者は顧客に代わって見積もりを迅速に作成し、ネゴシエーション・プロセスを開始できます。 以前は、見積もりは、購入者がストアフロントから作成したり、顧客としてログインした販売者のみが作成できました。

![新規](../assets/new.svg) **品目の割引とネゴシエーション**—<!--B2B-2440--> 見積もりの中で、B2B の購入者と販売者は、契約に達するまで割引を適用し、メモを交換しながら、品目レベルで交渉できるようになりました。 メモの作成と更新は、通信を追跡するために行項目と見積もり履歴に含まれます。 以前は、購入者と販売者は、見積もりレベルでのみメモの交換と割引の適用が可能でした。

![修正された問題](../assets/fix.svg) 「発注」オプションが有効になっていて、PayPal 支払オプションを使用して作成された仮想見積もりが選択されている場合、Adobe Commerceは支払い中に正しい詳細を表示するようになりました。 以前は、これらの条件では、合計は 0 と表示されていました。

![修正された問題](../assets/fix.svg) <!--ACP2E-1504--> クレジット制限が 999 を超える会社を保存しようとすると、検証エラーが発生しなくなりました。 以前は、会社のクレジット制限が 999 を超える場合、Adobeコマースでコンマ区切り文字が挿入されていたので、検証エラーが発生して更新が保存されませんでした。

![修正された問題](../assets/fix.svg) <!--ACP2E-1474-->  選択した配送先住所は、交渉可能な見積もりで注文を行った場合、変更されなくなりました。 以前は、注文を行った際に、選択した配送先住所がデフォルトの配送先住所に変更されていました。

![修正された問題](../assets/fix.svg) <!--ACP2E-1429--> B2B 機能のストア設定で、 **[!UICONTROL Enable Shared Catalog direct products price assigning]** フィールドは自動的に無効になりました。 ストアフロントでは、 **[!UICONTROL Enable Company]** 設定または **[!UICONTROL Enable Shared Catalog]** 設定は次のように設定されています： **[!UICONTROL No]**.

![修正された問題](../assets/fix.svg) <!--ACP2E-1683--> ストアフロントから会社アカウントを作成する際に、会社登録を処理する前に Commerce が電子メールアドレスを検証するようになりました。 E メールアドレスが無効な場合、操作は失敗し、アカウントの更新は処理されません。 以前は、会社アカウントの作成リクエストが電子メールアドレスが無効なために失敗した場合でも、顧客アカウントが作成されていました。

![修正された問題](../assets/fix.svg) <!--ACP2E-1664--> 共有カタログに二重引用符を含む製品 SKU と価格構造は、管理でエラーを引き起こさなくなりました。

![修正された問題](../assets/fix.svg) <!--ACP2E-1498--> ゲストユーザーが他の顧客グループのデータを表示できないように、コマースアプリケーションの Vanish 設定を更新しました。

### 既知の問題

B2B 1.4.0 を [Adobe Commerceバージョン 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html)に設定されていない場合、次のエラーが発生します。

```terminal
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

B2B セキュリティパッケージの手動依存関係を [安定性タグ](https://getcomposer.org/doc/04-schema.md#package-links). 手順については、 [Adobe Commerce Knowledge Base](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5

*2023 年 3 月 15 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![新規](../assets/new.svg) Adobe Commerce 2.4.6-p2 との互換性をサポートするため、B2B バージョン 1.3.5-p2 がリリースされました。

![新規](../assets/new.svg) Adobe Commerce 2.4.6-p1 との互換性をサポートするため、B2B バージョン 1.3.5-p1 をリリースしました。

>[!NOTE]
>
>Commerce を 2.4.6 から [最新リリース](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6)を使用する場合は、サポートされている B2B 1.3.5 パッチリリースに必ず更新してください。 または、B2B 拡張機能をバージョン 1.3.5 からバージョン 1.4.0 以降にアップグレードして、最新の機能を取得します。

![新規](../assets/new.svg) Adobe Commerce 2.4.6 のサポートを追加しました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-689--> 「発注」オプションが有効になっていて、PayPal 支払オプションを使用して作成された仮想見積もりが選択されている場合、Adobe Commerceは支払い中に正しい詳細を表示するようになりました。 以前は、これらの条件では、合計は 0 と表示されていました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-609--> の顧客グループのリスト **ブラウジングカテゴリを許可** の設定に、共有カタログに関連する顧客グループが含まれなくなりました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-1244--> 税/VAT 番号顧客属性が、管理者とストアフロントの両方の会社の管理者アカウントで期待どおりに機能するようになりました。 会社口座の作成にカスタム税/VAT 属性は不要になりました。 以前は、商人がカスタムの Tax/VAT 属性を持つ会社アカウントを作成すると、Adobe Commerceはストアフロントと管理者の両方で検証エラーをスローしていました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-1236--> 特定のスコープでの共有カタログ機能の無効化が正しく機能するようになりました。 以前は、Adobe Commerceが共有カタログ設定を保存した場合、マーチャントは無効な範囲を設定していました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-1203--> 管理者ユーザーは、会社ユーザーの顧客カスタム属性値を保存できるようになりました。 以前は、会社ユーザーの顧客カスタム属性を保存できませんでした。

![修正された問題](../assets/fix.svg) <!--- ACP2E-1221--> 多数の会社権限が既に割り当てられている場合、GraphQLを通じて提供される会社権限の検証によって、パフォーマンスの問題が解決されました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-1242--> クイックオーダーを使用して使用可能な在庫を超える数量の製品を追加した場合、Adobe Commerceが買い物かごページでエラーをスローしなくなりました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-1090--> のパフォーマンス `SELECT` 会社権限の操作が改善されました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-2456--> カテゴリクエリで、問い合わせ対象のカテゴリに対して明示的に設定されたカテゴリ権限がない場合、ストア設定に従って製品価格が返されるようになりました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-6829--> The **[!UICONTROL Place Order]** 承認された見積もりリクエストを使用して購入を完了する際、ボタンが期待どおりに機能するようになりました。 交渉可能な見積もりの問題 `negotiableQuoteCheckoutSessionPlugin` プラグインが解決されました。

## B2B v1.3.4

*2022 年 8 月 10 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![新規](../assets/new.svg) Adobe Commerce 2.4.5 のサポートを追加しました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerceは、API 呼び出しによって既存の会社が更新されるたびに、電子メール通知を送信しなくなりました。 会社が作成された場合にのみ、E メールが送信されるようになりました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerceは、 **[!UICONTROL Enable Cross Border Trade]** 税の計算設定が有効です。

![修正された問題](../assets/fix.svg) <!--- ACP2E-322-->在庫が更新された後、設定可能な製品が製品リストの最後の位置に移動され、 **[!UICONTROL Move out of stock to the bottom]** の設定が有効になっています。 新しいカスタムデータベースクエリが実装され、Elasticsearchインデックスの並べ替え順が管理者が有効な並べ替え順に従うようになりました。 以前は、この設定が有効になっている場合、設定可能な製品とその子製品がリストの下部に移動されませんでした。

![修正された問題](../assets/fix.svg) <!--- ACP2E-308-->発注電子メールで、マルチサイトデプロイメントで各 Web サイトの電子メール送信設定が使用できるようになりました。 のチェック **[!UICONTROL Disable Email Communications]** 設定が電子メールキューのカスタムロジックに追加されました。 以前は、Adobe Commerceはセカンダリ Web サイトの電子メール送信設定を保持していませんでした。

![修正された問題](../assets/fix.svg) <!--- ACP2E-302-->クイックオーダーページの「 SKU 」フィールドのタイトルが変更され、わかりやすくなりました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerceで、買い物客が **SKU または製品名を入力** フィールドに入力します。

![修正された問題](../assets/fix.svg) <!--- ACP2E-1753-->The **[!UICONTROL Account Created in]** 会社管理者のフィールドは、会社を保存した後も期待どおりの値を保持するようになりました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-722 -->The `customer` クエリがでフィルタリングされた購買依頼リストを取得する際に、空の結果が戻されなくなりました。 `uid`.

![修正された問題](../assets/fix.svg) <!--- ACP2E-210 -->の前にプラグインを追加しました。 `collectQuoteTotals` を呼び出して、ストアのクレジットが 1 回だけ適用されるようにします。

![修正された問題](../assets/fix.svg) <!--- ACP2E-665 -->管理者がアカウントを管理者から削除すると、ユーザーがログインページにリダイレクトされるようになりました。 以前は、Adobe Commerceはエラーをスローしていました。 プラグイン (`SessionPlugin`) コードブロックが `try…catch` ブロック。 以前は、このコードは汎用の例外処理ブロック内にラップされていませんでした。

![修正された問題](../assets/fix.svg) <!--- ACP2E-661 --> モバイルモードのクイックオーダーページで、 **入力** 有効な製品名または SKU を入力した後、買い物客は期待どおりに次のフィールドに移動します。

![修正された問題](../assets/fix.svg) <!--- ACP2E-607 -->会社名がチェックアウトワークフローの「請求」および「配送先住所」セクションに期待どおりに表示されるようになりました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-375 -->現在は、 **[!UICONTROL Zero Subtotal Checkout]** 支払い方法が無効です。 以前は、管理者からの注文配置時に、「クレジットを保存」チェックボックスが機能していませんでした。 アプリケーションは、ストアクレジットを含む注文を行わず、次のエラーを表示しました： `The requested Payment Method is not available`.

## B2B v1.3.3

*2022 年 8 月 10 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![新規](../assets/new.svg) Adobe Commerce 2.4.4 のサポートを追加しました。

![修正された問題](../assets/fix.svg) <!--- MC-41985--> 会社の役割が 10 万件を超えるデプロイメントで、Adobe Commerce 2.3.x からAdobe Commerce 2.4.x にアップグレードするのに要する時間が大幅に短縮されました。

![修正された問題](../assets/fix.svg) <!--- MC-42153--> POST `V1/order/:orderId/invoice` リクエストで、 **[!UICONTROL Payment on Account]** 支払い方法が有効です。 以前は、Adobe Commerceが次のエラーをスローしていました。 `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![修正された問題](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro は、お客様の買い物かごに他の製品が含まれている場合に B2B のネゴシエーション可能な見積もりで期待どおりに動作するようになりました。 Adobe Commerceは正常に注文を処理し、顧客に期待どおりに電子メールを送信するようになりました。 以前は、Adobe Commerceで致命的なエラーが発生し、値が 0 の場合に確認 E メールをお客様に送信していました。

![修正された問題](../assets/fix.svg) <!--- MC-41819--> 共有カタログ内の一部の製品を除外した後、カタログ検索結果ページにページネーションが正しく表示されるようになりました。

![修正された問題](../assets/fix.svg) <!--- MC-42886--> 管理者で会社ユーザーを作成または保存する際、顧客カスタム属性が期待どおりに保存されるようになりました。

![修正された問題](../assets/fix.svg) <!--- MC-42927--> The **[!UICONTROL Submit]** 「会社を新規作成」ボタンが 1 回のクリック後に無効になり、複数のフォームが送信されないようになりました。 以前は、このボタンを繰り返しクリックしてこのフォームを複数回送信すると、エラーが発生していました。

![修正された問題](../assets/fix.svg) <!--- MC-42787--> 買い物客が、注文の変更が無効になっているストアにログインした場合、Adobe Commerceでストアフロントに並べ替えリンクが表示されなくなりました。

![修正された問題](../assets/fix.svg) <!--- MC-43115--> 共有カタログが有効な場合、SKU によるクイックオーダー検索では、大文字と小文字が区別されなくなりました。

![修正された問題](../assets/fix.svg) <!--- MC-42203--> 会社の作成時に顧客属性のファイルを更新できるようになりました。 以前は、タイプの添付ファイルを持つ会社を作成しようとしたとき `File`:Adobe Commerceは会社を作成せず、次のエラーを例外ログに記録しました： `Something went wrong while saving file`.

![修正された問題](../assets/fix.svg) <!--- MC-42242--> を使用したカスタム属性 (`File`) または (`Image`) 型です。 以前は、アカウントにこれらのカスタマイズ可能なオプションが含まれている場合、会社の編集用ページローダーが解決されず、会社の詳細を編集できませんでした。

![修正された問題](../assets/fix.svg) <!--- MC-42268--> The `products` クエリが正確なを返すようになりました。 `total_count` フィールド（共有カタログが有効な場合）

![修正された問題](../assets/fix.svg) <!--- MC-42203-->  会社の作成時に顧客属性のファイルを更新できるようになりました。 以前は、タイプの添付ファイルを持つ会社を作成しようとしたとき `File`:Adobe Commerceは会社を作成せず、次のエラーを例外ログに記録しました： `Something went wrong while saving file`.

![修正された問題](../assets/fix.svg) <!--- MC-43178--> The _会社の設定_ および _会社を作成_ オンライン発送方法を無効にした後、ページが期待どおりに動作するようになりました。 無効な出荷モジュールの処理が試行されるのを防ぐための検証が追加されました。 以前は、Adobe Commerceに次のエラーが表示されていました。 `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![修正された問題](../assets/fix.svg) <!--- MC-42214--> The _カテゴリ_ 部分的なインデックス作成中に権限が生成されている間、ページに一貫した製品データが表示されるようになりました。 このプロセスに、ディレクトリ権限用の新しい部分インデクサーが追加されました。 以前は、インデクサーの実行中に表示されるデータが正しくありませんでした。

![修正された問題](../assets/fix.svg) <!--- MC-42567--> The `categoryList` カタログ権限が使用され、製品が共有カタログに割り当てられている場合、クエリが正しい数の製品を返すようになりました。

![修正された問題](../assets/fix.svg) <!--- MC-42528--> The `categoryList` クエリは、カテゴリ権限に従い、許可されたカテゴリのみを返すようになりました。 以前は、割り当て済みおよび未割り当てのカテゴリがすべて返されていました。

![修正された問題](../assets/fix.svg) <!--- MC-42399--> The `rest/V1/company/{id}` リクエストを返す `is_purchase_order_enabled` 属性値が期待どおりに表示されます。

![修正された問題](../assets/fix.svg) <!--- ACP2E-128--> カスタム顧客属性が、 _会社管理者_ タブをクリックします。

![修正された問題](../assets/fix.svg) <!--- ACP2E-130--> 会社管理者および会社ユーザーに対して、マイアカウントページのマイウィッシュリストブロックが期待どおりに表示されるようになりました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-133--> クイック注文エラーが買い物かごに表示されなくなりました。 以前は、Adobe Commerceで、カタログに SKU が見つからない場合に、次のエラーが買い物かごに表示されていました。  `The SKU was not found in the catalog`.

![修正された問題](../assets/fix.svg) <!--- ACP2E-194--> 共有カタログの保存操作が最適化され、高速に実行できるようになりました。 以前は、多くの顧客グループと共有カタログを保存する場合、数分かかることがありました。

![修正された問題](../assets/fix.svg) <!--- MC-42240--> Adobe Commerceは、すべてのサブカテゴリの権限を `sharedcatalog_category_permissions` 表に示されます。 以前は、親カテゴリデータのみが削除されていました。

## B2B v1.3.2

*2022 年 8 月 30 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![新規](../assets/new.svg) Adobe Commerce 2.4.3 のサポートを追加しました。

![修正された問題](../assets/fix.svg) <!--- MC-39862--> Adobe Commerceは有効期限切れのネゴシエーション可能見積もりに関する更新メールを正常に送信するようになりました。 以前は、ネゴシエーション可能な見積もりの期限が切れると、Adobe Commerceは更新メールを送信しませんでした。

![修正された問題](../assets/fix.svg) <!--- MC-40682--> Adobe Commerceは期限切れに近い更新メールを正常に送信し、期限切れのネゴシエーション可能見積もりを、 `cron` ジョブが見つかりません。

### 会社情報

![修正された問題](../assets/fix.svg) <!--- MC-41542--> 「新しい会社アカウントページの国を作成」ドロップダウンフィールドに空のオプション値が表示されなくなりました。 以前は、最初の 2 つのオプション値と国コード `AN` は空でした。

![修正された問題](../assets/fix.svg) <!--- MC-41260--> クリック **[!UICONTROL Return]** ボタンを使用して、会社のユーザーが作成した注文を返すページに管理者ユーザーが期待どおりにリダイレクトするようになりました。 以前は、管理者は注文履歴ページにリダイレクトされていました。

![修正された問題](../assets/fix.svg) <!--- MC-40798--> Adobe Commerceで `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` 次のメソッド： `bin/magento setup:upgrade`. 以前は、Adobe Commerceでは、権限を初期化する際にコレクションのバッチサイズを使用せず、会社のすべての役割のコレクションを読み込んでいました。

![修正された問題](../assets/fix.svg) <!--- MC-40551--> 会社のユーザーは、顧客カスタム属性値を編集および更新できるようになりました。 以前は、これらの属性は、ユーザー作成フォームと編集フォームで正しくバインドされていませんでした。 会社のユーザーは異なる属性値を入力できましたが、Adobe Commerceはこれらの値を正しく保存できませんでした。

![修正された問題](../assets/fix.svg) <!--- MC-32653--> 会社の役割権限のリソースツリーを、期待どおりに翻訳できるようになりました。 以前は、有効な翻訳ファイルが存在していても、権限ツリーは翻訳されませんでした。

![修正された問題](../assets/fix.svg) <!--- MC-40358--> Adobe Commerceは、B2B ユーザーのカスタム顧客属性値を期待どおりに保存するようになりました。 以前は、カスタム顧客属性を含む会社アカウントを作成すると、テンプレートエラーが発生し、Adobe Commerceでフォームが正常に読み込まれませんでした。 レイアウトへの引数の追加 `company_create_account` この問題を解決しました。

![修正された問題](../assets/fix.svg) <!--- MC-41721--> 「すべてのユーザーを表示」、「アクティブなユーザーを表示」、「非アクティブなユーザーを表示」などの会社のユーザーフィルターが、期待どおりに機能するようになりました。 以前は、会社のユーザーページでフィルタ処理を実行すると JavaScript エラーが発生していました。

### 会社のクレジット

![修正された問題](../assets/fix.svg) <!--- MC-41551--> Web サイトレベルの権限のみを含む制限付きアカウントを持つ管理者は、Web サイトとは異なる通貨を使用する会社を作成できるようになりました。

![修正された問題](../assets/fix.svg) <!--- MC-41523--> Adobe Commerceが正しいから会社の E メールを送信するようになりました。 `from` メールアドレスと範囲。 以前は、Adobe Commerceが会社のクレジット割り当てを送信したり電子メールを更新したりする際に、Web サイトの範囲を考慮していませんでした。

### クイックオーダー

![修正された問題](../assets/fix.svg) <!--- MC-42104--> 存在しない SKU で、CSV ファイルからクイックオーダーを使用して注文を作成すると、期待どおりに動作するようになりました。

![修正された問題](../assets/fix.svg) <!--- MC-40268--> クイックオーダーを使用した複数の SKU の検索が期待どおりに動作するようになりました。 以前は、の結果に重複エントリが含まれていました。

![修正された問題](../assets/fix.svg) <!--- MC-40261--> 「追加された製品」リストの表示では、クイックオーダー時に SKU を使用して複数の製品を選択する場合に、SKU を小文字および大文字で入力して同じように扱うようになりました。

![修正された問題](../assets/fix.svg) <!--- MC-40225--> クイックオーダーを使用すると、買い物客が指定した数量で商品が追加されるようになりました。 以前は、Adobe Commerceは買い物客が指定した数量が 1 を超えた場合でも、1 つの製品を追加しました。

![修正された問題](../assets/fix.svg) <!--- MC-41283--> クイックオーダーのオートコンプリート機能が部分的な SKU で機能するようになりました。

![修正された問題](../assets/fix.svg) <!--- MC-41299--> Adobe Commerceに、 **個別には表示されません** をクイックオーダーページの自動提案リストと検索結果に追加します。

![修正された問題](../assets/fix.svg) <!--- MC-42402--> 買い物客がクイックオーダーフォームを使用して、大文字を含む SKU 別に複数の製品を追加できるようになりました。 以前は、最初の製品のみが追加されていました。

### 交渉可能な見積もり

![修正された問題](../assets/fix.svg) <!--- MC-41232--> 買い物客は、「URL」フィールドにネゴシエーション可能な見積もりへのリンクを貼り付け、正常にログインした後、ネゴシエーション可能な見積もりページにリダイレクトされるようになりました。 以前は、買い物客はマイアカウントページにリダイレクトされていました。

![修正された問題](../assets/fix.svg) <!--- MC-39317--> チェックアウト時に作成された顧客アカウント用の日付カスタマイズ可能なオプションを含む製品を含む注文に対して、並べ替えが期待どおりに機能するようになりました。 以前は、Adobe Commerceは並べ替えを処理せず、次のエラーを表示していました。 `The product has required options. Enter the options and try again`.

![修正された問題](../assets/fix.svg) <!--- MC-39063--> 発注モジュールが無効になっている場合、譲渡可能見積書の配送先住所は、チェックアウト時に編集できなくなりました。 この動作は、以前の修正によるもので、 `isQuoteAddressLocked` は、ネゴシエーション可能な見積もりチェックアウトレンダラーから削除されました。

![修正された問題](../assets/fix.svg) <!--- MC-38967--> マーチャントは、管理者からの交渉可能な見積もりに製品を追加できるようになりました。

### 発注書

![修正された問題](../assets/fix.svg) <!--- MC-39983--> Adobe Commerceで、PayPal Express Checkout を使用して発注した際に、 **[!UICONTROL Name Prefix]** 属性が `required`. 以前は、Adobe Commerceは注文をせず、エラーメッセージを表示しませんでした。

![修正された問題](../assets/fix.svg) <!--- MC-39620--> Google Tag Manager が有効になっている場合、発注書モジュールの請求先住所の UI コンポーネントで、見積もり住所が正しく使用されるようになりました。 以前は、支払いページで JavaScript エラーが発生していました。

### 購買依頼リスト

![修正された問題](../assets/fix.svg) <!--- MC-40426--> 商人がPOST `rest/all/V1/requisition_lists` エンドポイント：顧客の購買依頼リストを作成します。 以前は、Adobe Commerceで購買依頼リストを作成しようとすると、次の 400 エラーが発生していました。 `Could not save Requisition List`.

![修正された問題](../assets/fix.svg) <!--- MC-41123--> The **[!UICONTROL Add to Requisition List]** 買い物かごに在庫切れの製品も含まれている場合に、買い物かごの在庫中の製品のボタンが表示されるようになりました。 以前は、買い物かごに 2 つの製品が含まれていて、そのうちの 1 つが在庫切れの場合、 _[!UICONTROL Add to Requisition List]_どちらの製品にもボタンが表示されなかった問題を修正しました。

![修正された問題](../assets/fix.svg) <!--- MC-40877--> これで、REST API を使用して、製品を購買依頼リストに追加できます。

![修正された問題](../assets/fix.svg) <!--- MC-40155--> 要求リスト **[!UICONTROL Latest Activity Date]** の値は、ロケールの形式に従うようになりました。

![修正された問題](../assets/fix.svg) <!--- MC-39580--> 購買依頼リストからバンドル製品を編集した際に、Adobe Commerceで致命的なエラーがスローされなくなりました。

![修正された問題](../assets/fix.svg) <!--- MC-40454--> カスタマイズ可能なオプションを含む製品を追加すると、Adobe Commerceに正しい製品価格が表示されるようになりました `(File)` を購買依頼リストからウィッシュ・リストに追加します。 アップロードされたファイルへのリンクも期待どおりに表示されます。 以前は、Adobe Commerceで誤った製品価格が表示され、ファイルへのリンクは表示されませんでした。

![修正された問題](../assets/fix.svg) <!--- MC-36383--> カスタマイズ可能なオプションを持つ製品 `(File)` これで、購買依頼リストから買い物かごに追加できるようになりました。

### 共有カタログ

![修正された問題](../assets/fix.svg) <!--- MC-40497--> 特定の Web サイトに限定された役割を持つ管理者は、共有カタログを作成、表示、編集できるようになりました。 以前は、役割が限られた管理者が共有カタログを作成しようとすると、Adobe Commerceで致命的なエラーが発生していました。

![修正された問題](../assets/fix.svg) <!--- MC-41337--> レイヤーナビゲーションの結果に、フィルターされた属性を持つ製品の正確な数が含まれるようになりました。買い物客は、複数のフィルターを適用できるようになりました。 以前は、1 つのフィルターのみを適用でき、Adobe Commerceのレイヤーナビゲーションに不正確な製品数が表示されていました。

![修正された問題](../assets/fix.svg) <!--- MC-40779--> Adobe Commerceで、検索結果のレイヤーナビゲーションフィルターに製品数が正しく表示されるようになりました。 以前は、検索結果ページのプラグインでElasticsearchが使用されていませんでしたが、データベースに新しいクエリが発行されていました。

![修正された問題](../assets/fix.svg) <!--- MC-39978--> Adobe Commerceは、マーチャントがデフォルトの共有カタログからすべての製品を削除する際に、階層価格を削除しなくなりました。

![修正された問題](../assets/fix.svg) <!--- MC-39802--> 現在のカテゴリでフィルターが適用され、共有カタログが有効な場合はすべてのページで正しく表示されるようになりました。 以前は、現在のページのみに対してフィルターが誤って計算され、現在のカテゴリではフィルターされませんでした。

![修正された問題](../assets/fix.svg) <!--- MC-39522--> ザGraphQL `products` 共有カタログが有効な場合、共有カタログに割り当てられていない製品の製品の価格範囲とカテゴリがクエリによって返されなくなりました。 以前は、クエリは、製品自体が `items` 配列。

## B2B v1.3.1

*2021 年 2 月 10 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![新規](../assets/new.svg) Adobe Commerce 2.4.2 のサポートを追加しました。

![新規](../assets/new.svg) 注文でオンラインの支払い方法がサポートされるようになりました。

![修正された問題](../assets/fix.svg) この製品が以前の注文で使用された場合に、構成可能な製品を購買依頼リストから買い物かごに直接追加しても、システム・エラーは戻されなくなりました。

![修正された問題](../assets/fix.svg) 分割データベース設定がデプロイされる際に、Adobe Commerceに発注書に対して「自分の承認が必要」タブが正しく表示されるようになりました。

![修正された問題](../assets/fix.svg) Adobe Commerceで、注文を表示する際に、バンドル製品とギフトカードに関する詳細が表示されるようになりました。

![修正された問題](../assets/fix.svg) ストアで閲覧中にアカウントにログインした後、買い物客が期待どおりにリダイレクトされるようになりました。 **[!UICONTROL Website Restriction]** が有効かつ **[!UICONTROL Restriction Mode]** が `Private Sales: Login Only`. 以前は、買い物客はストアのホームページにリダイレクトされていました。 <!--- MC-38934-->

![修正された問題](../assets/fix.svg) 多くの顧客 (13000以上 ) を含む B2B 会社階層を持つデプロイメントの、会社管理者のアカウントダッシュボードページで、注文履歴が期待どおりに読み込まれるようになりました。 以前は、注文履歴の読み込みが遅いか、まったく遅くなっており、Adobe Commerceで 503 エラーが表示されていました。 <!--- MC-38830-->

![修正された問題](../assets/fix.svg) カスタマイズ可能なオプションを含む未構成の製品を「カテゴリ」ページから「購買依頼リスト」に追加すると、Adobe Commerceで複数の同一の警告メッセージが表示されなくなりました。 <!--- MC-38342-->

![修正された問題](../assets/fix.svg) B2B 共有カタログが有効になっている場合、新しい製品と重複した製品がカテゴリページに期待どおりに表示されるようになりました。 <!--- MC-38307-->

![修正された問題](../assets/fix.svg) Adobe Commerceが正しい状態を維持 `store_id` 会社の顧客グループが更新されたときに会社管理者に関連付けられる。 以前は、 `store_id` グループが更新された際に、デフォルトのストアに変更されました。 <!--- MC-38196-->

![修正された問題](../assets/fix.svg) Adobe Commerceでは、グループ化された製品を買い物かごに追加するのと同じ方法で、単純な製品のリストとして購買依頼リストに保存するようになりました。 以前は、Adobe Commerceがグループ化された製品を保存したので、購買依頼リストからのグループ化された製品のリンクは、常に単純な製品にリダイレクトされ、グループ化された製品にはリダイレクトされませんでした。 <!--- MC-38049-->

![修正された問題](../assets/fix.svg) これで、 **[!UICONTROL Company Name]** フィールドを使用して、注文情報を CSV 形式で書き出すとき。 以前は、Adobe Commerceは次の場所にエラーを記録していました： `var/export/{file-id}`. <!--- MC-37785-->

![修正された問題](../assets/fix.svg) ストアフロントの「新規購買依頼リストの作成」タブを選択すると、Adobe Commerceに「購買依頼リストの作成」ポップアップが期待どおりに表示されるようになりました。 <!--- MC-37915-->

![修正された問題](../assets/fix.svg) 購買依頼リストに、グループ化されたすべての製品と数量が含まれるようになりました。 以前は、商人が製品詳細ページから製品を追加した後で購買依頼リストに移動すると、Adobe Commerceに次のエラーが表示されていました。 `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![修正された問題](../assets/fix.svg) 複数サイトの導入で会社を作成する際、適切なストア表示が関連する Web サイトに関連付けられるようになりました。 以前は、会社を作成できず、Adobe Commerceに次のエラーが表示されていました。 `The store view is not in the associated website`. <!--- MC-37488-->

![修正された問題](../assets/fix.svg) クイックオーダーを使用して SKU で製品を並べ替えても、CSV ファイルで製品数が重複しなくなりました。 <!--- MC-37427-->

![修正された問題](../assets/fix.svg) The **[!UICONTROL Add to Cart]** ボタンが _[!UICONTROL Enter Multiple SKUs]_「クイックオーダー」ページの「 」セクションに空の値が含まれています。 代わりに、Adobe Commerceに有効な SKU の入力を求めるメッセージが表示されるようになりました。 <!--- MC-37387-->

![修正された問題](../assets/fix.svg) 購買依頼リストから製品レビューを発行すると、Adobe Commerceが製品ページに次のメッセージを表示するようになりました。 `You submitted your review for moderation`. レビューは、保留中のレビューページ（管理者）にも表示されます **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**) をクリックします。 以前は、Adobe Commerceがレビューを保留中のレビューのリストに追加していましたが、製品ページに 404 エラーが表示されていました。 <!--- MC-37119-->

![修正された問題](../assets/fix.svg) のパフォーマンス `sharedCatalogUpdateCategoryPermissions` 消費者が改善されました。 共有カタログを作成した後、カタログ権限インデクサーは、すべての顧客グループではなく、共有カタログの顧客グループ ID のみを使用するようになりました。 <!--- MC-36770-->

![修正された問題](../assets/fix.svg) 買い物客のデフォルト以外のアドレスに関連付けられたカスタム顧客アドレス属性フィールドが、ストアフロントチェックアウトワークフローで期待どおりに保存されるようになりました。 <!--- MC-36630-->

![修正された問題](../assets/fix.svg) ストアのデフォルトの共有カタログに属する製品の注文は、Admin REST API(`rest/V1/carts/{<CART_ID>/items`) が期待どおりに表示されます。 Adobe Commerceは、 `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. 以前は、Adobe Commerceは商品を買い物客の買い物かごに追加せず、次のエラーをスローしていました。 `No such shared catalog entity`. <!--- MC-36535-->

![修正された問題](../assets/fix.svg) Adobe Commerceは、Adobe Commerceストアのアドレスから新しい会社ユーザー登録電子メールを送信するようになりました。 以前は、この電子メールは会社の管理者のアドレスから送信されていました。 <!--- MC-36480-->

![修正された問題](../assets/fix.svg) Adobe Commerceでは、マーチャントに対して新しい属性の保存を許可する前に、予約済みの会社属性名の重複をカスタム属性で確認するようになりました。 <!--- MC-36282-->

![修正された問題](../assets/fix.svg) The `credit_history` クエリは、最初に割り当てられた金額と購入した金額の両方について、指定した会社のクレジット履歴を返すようになりました。 以前は、このクエリはエラーを返していました。

![修正された問題](../assets/fix.svg) The **[!UICONTROL Company]** および  **[!UICONTROL Job Title]** アカウント情報の編集ページのフィールドは編集できなくなりました。

### 既知の問題

- B2B 購入者は、通常の発注フローを回避するために、オンライン支払い方法を使用できます。 このシナリオは、購入者が（例えば、プロモコードやギフトカードで）チェックアウトの合計を 0 に減らして、コードやギフトカードを削除できる場合に発生する可能性があります。 その場合でも、Adobe Commerceは割り当てられたカタログの品目の価格に基づいて、正しい金額の注文を行います。 **_回避策_**：オンラインでの支払い方法で発注書の承認を有効にする場合、ギフトカードおよびクーポンコードを無効にします。 <!--- B2B-1603-->

- PayPal Express Checkout を使用して注文を行おうとすると、購入者は買い物かごにリダイレクトされ、 **[!UICONTROL In-Context Mode]** は無効です。 <!--- B2B-1604-->

- Adobe Commerceでは、購入者が発注を作成してからチェックアウトページに移動すると、404 エラーが表示されることがあります。 このエラーは、購入者が以前の購入を完了せずにチェックアウトページに移動する前に、オンライン支払い方法で別の発注書を作成した場合に発生します。 購入者は引き続き発注書を配置できます。 **_周りを回避する_**：なし。 <!--- B2B-1605-->

- 特定の支払い方法の割引は、購入者が最終的なチェックアウト時に支払い方法を変更した場合でも、発注のチェックアウト時に保持されます。 その結果、顧客は権利のない割引を受けることができます。 この問題は、支払い方法が変更されたにもかかわらず、元の支払い方法の買い物かごルールが適用されているために発生します。 **_周りを回避する_**：なし。 詳しくは、 [Adobe Commerce 2.4.2 B2B の既知の問題：支払い方法が変更された後、オンラインの発注書に対する割引が残る](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _ナレッジベース_ 記事。 <!-- B2B-1012 -->

- The `deleteRequisitionListOutput` 「問合せ」では、残りの購買依頼リストの代わりに、削除した購買依頼リストに関する詳細が戻されます。 <!--- MC-39894-->

## B2B v1.3.0

*2020 年 10 月 16 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

このリリースには、注文の承認、発送方法、買い物かご、管理者アクションのログ記録の改善が含まれています。

![新規](../assets/new.svg) Adobe Commerce 2.4.1 のサポートを追加しました。

![新規](../assets/new.svg) B2B 注文の承認が強化され、使いやすさが向上し、発注書に対する一括アクションが可能になりました。

![新規](../assets/new.svg) B2B の商人は、各会社に提供される発送方法を制御できるようになりました。<!--- BUNDLE-160 161 162 -->

![新規](../assets/new.svg) マーチャントは、ユーザーが 1 回の操作で買い物かごの内容を消去できるようになり、この機能を各 Web サイトで個別に設定できるようになりました。 <!--- BUNDLE-108 -->

![新規](../assets/new.svg) B2B 購入者は、個々の品目または買い物かごの内容全体を直接購入依頼リストに追加できるようになりました。 <!--- BUNDLE-145 144-->

![新規](../assets/new.svg) B2B 商人は、顧客に代わって、支払い方法として「アカウントでの支払い」を使用して、管理者から注文を作成できます。 <!--- BUNDLE-166 178-->

![新規](../assets/new.svg) マーチャントは、顧客の詳細ページから、ユーザーに関連するすべての引用符を直接表示できるようになりました。 <!--- BUNDLE-139 -->

![新規](../assets/new.svg) マーチャントは、企業別に「顧客を今すぐオンライン」グリッドをフィルタリングできるようになりました。 <!--- BUNDLE-137 -->

![新規](../assets/new.svg) 管理者は、管理者の顧客をセールス担当別にフィルタリングできるようになりました。 <!--- BUNDLE-110 -->

![新規](../assets/new.svg) 不正またはスパムのアカウントの作成を減らすために、マーチャントはストアフロントの「新しい会社のリクエスト」フォームでGoogle reCAPTCHA を有効にできるようになりました。 <!--- BUNDLE-154 -->

![新規](../assets/new.svg) 会社モジュールで実行された管理アクションが管理アクションログに記録されるようになりました。 アクションは、関連するすべての会社モジュールから記録されます。 `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`.  <!--- BUNDLE-180 181 182 183 -->

![修正された問題](../assets/fix.svg) Adobe Commerceに **[!UICONTROL Delete customer]** ボタン **顧客** ページを表示します。 <!--- MC-35655-->

![修正された問題](../assets/fix.svg) 顧客グリッドで顧客を編集したときに、会社に割り当てられた顧客に対して、顧客グループが自動的に変更されることはなくなりました。 <!--- MC-35254-->

![修正された問題](../assets/fix.svg) マーチャントが共有カタログを作成すると、権限が自動的に `Allow` （の） **[!UICONTROL Display Product Prices]** および **[!UICONTROL Add to Cart]** カタログ権限設定で顧客グループにこのアクセスが割り当てられた場合のカテゴリ内の機能。 以前は、これらの設定は自動的に `Deny` （カタログ権限がに設定されている場合も） `Allow`.<!--- MC-34792-->

![修正された問題](../assets/fix.svg) 製品を製品編集ページから編集する際に、共有カタログカテゴリの権限が上書きされなくなりました。<!--- MC-34777-->

![修正された問題](../assets/fix.svg) Adobe Commerceが、マーチャントが **[!UICONTROL Allow To Exceed Credit Limit]** 設定。 以前は、Adobe Commerceから送信される通知 E メールは、お客様が上限を超える権限を持っていないことを示していました。 <!--- MC-34584-->

![修正された問題](../assets/fix.svg) 購買依頼リスト上の製品価格を囲むHTMLコンテナが、バンドルされた製品の子に対して正しくレンダリングされるようになりました。 <!--- MC-36331-->

![修正された問題](../assets/fix.svg) マーチャントは、多言語のデプロイメントで会社を作成する際に、会社のユーザーの E メールを送信する言語を指定できるようになりました。 以前は、のドロップダウンメニューを使用すると、商人が適切な店舗表示を選択し、言語が表示されていませんでした。  <!--- MC-35777-->

![修正された問題](../assets/fix.svg) ストアフロントのチェックアウトワークフローで、カスタム顧客住所属性フィールドが期待どおりに表示されるようになりました。 <!--- MC-35607-->

![修正された問題](../assets/fix.svg) 「B2B 機能設定」タブが正しく開くようになりました。 <!--- MC-35458-->ゲストは QuickOrder を使用して、買い物かごに製品を追加し、アイテムを正常に削除できるようになりました。 以前は、買い物客が QuickOrder を使用して複数の製品を買い物かごに追加し、製品を削除しても、製品は削除されませんでした。 <!--- MC-35327-->

![修正された問題](../assets/fix.svg) REST APIPUTを使用して会社を更新できるようになりました `/V1/company/:companyId` 指定しないリクエスト `region_id` 状態が次のように設定されている場合 **不要**. 以前は、 `region_id` が不要な場合、Adobe Commerceは、指定されていない場合にエラーをスローしました。 <!--- MC-35304-->

![修正された問題](../assets/fix.svg) REST API(`http://magento.local/rest/V1/company/2`です。 `2` は会社 ID を表します )、応答には次の設定が含まれるようになりました `applicable_payment_method` または `available_payment_methods` 期待どおり。 <!--- MC-35248-->

![修正された問題](../assets/fix.svg) Adobe Commerceで **入力** ボタンをクリックする代わりに **[!UICONTROL Save]** 」ボタンをクリックします。<!--- MC-35094-->

![修正された問題](../assets/fix.svg) 新しい製品が公開共有カタログに割り当てられる際、カテゴリの権限は変更されなくなりました。 以前は、カテゴリ権限が重複していました。 <!--- MC-34386-->

![修正された問題](../assets/fix.svg) REST API エンドポイントPUT `rest/default/V1/company/{id}`（会社の電子メールの更新に使用）は、大文字と小文字が区別されなくなりました。 <!--- MC-34308-->

![修正された問題](../assets/fix.svg) 報酬モジュールを無効にしても、顧客アカウントの B2B 機能に影響が及ぶことはなくなりました。 以前は、報酬モジュールが無効になっている場合、会社プロファイル、会社ユーザー、役割および権限の B2B 関連のタブは表示されませんでした。<!--- MC-34191-->

![修正された問題](../assets/fix.svg) 会社アカウントを変更した場合、Adobe Commerceは電子メール通知で正しい送信者名を使用するようになりました。 以前は、Adobe Commerceは、すべての E メールに対して、デフォルトの範囲で定義されている一般的な連絡先送信者名を使用していました。 <!--- MC-33917-->

![修正された問題](../assets/fix.svg) 物理製品と仮想製品の両方を含む注文に対して、マルチ配送を正常に実装できるようになりました。 <!--- MC-33818-->

![修正された問題](../assets/fix.svg) マーチャントは、 _[!UICONTROL Company Users]_」セクションをクリックします。**[!UICONTROL Access Restriction]**が有効かつ&#x200B;**[!UICONTROL Restriction Mode]**が `Sales: Login Only`. 以前は、Adobe Commerceは、商人がユーザーを作成しようとすると次のエラーをスローしていました。 `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![修正された問題](../assets/fix.svg) Adobe Commerceは、顧客がアカウント情報を保存した際に、顧客の顧客グループをデフォルトにリセットしなくなりました。 <!--- MC-33554-->

![修正された問題](../assets/fix.svg) Adobe Commerceで、アクティブな買い物かごを持つ顧客を顧客グループに割り当てた場合に、致命的なエラーがスローされなくなりました。 <!--- MC-33313-->

![修正された問題](../assets/fix.svg) Adobe Commerceが `addToCart` クイックオーダーおよび購買依頼の DataLayer イベントにページが表示されます。  <!--- MC-33295-->

![修正された問題](../assets/fix.svg) 会社に割り当てられたセールス担当者に送信される通知 E メールに、割り当てられた会社のロゴが含まれるようになりました。 以前は、通知 E メールには、アップロードされた会社のロゴではなく、デフォルトの LUMA ロゴが含まれていました。 <!--- MC-33232-->

![修正された問題](../assets/fix.svg) 購買依頼リストには、グループ化されたすべての製品と数量がリストに追加されました。 以前は、商人が製品詳細ページから製品を追加した後で購買依頼リストに移動すると、Adobe Commerceに次のエラーが表示されていました。 `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![修正された問題](../assets/fix.svg) The `products` クエリが正確なを返すようになりました。 `total_count` フィールド（共有カタログが有効な場合） <!--- MC-42268-->

![修正された問題](../assets/fix.svg) オンライン配送方法を無効にした後、会社の設定ページと会社の作成ページが期待どおりに動作するようになりました。 無効な出荷モジュールの処理が試行されるのを防ぐための検証が追加されました。 以前は、Adobe Commerceに次のエラーが表示されていました。 `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![修正された問題](../assets/fix.svg) 統合テストのメモリ消費が削減され、テストパフォーマンスが向上し、テスト完了に要する時間が短縮されました。 <!--- AC-266-->

## B2B v1.2.0

*2020 年 7 月 29 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![新規](../assets/new.svg) Adobe Commerce 2.4.0 のサポートを追加しました。

![新規](../assets/new.svg) ストアフロント注文検索、Marek Mularczyk による投稿に対する感謝の追加 [ディバンテ](https://www.divante.com/) コミュニティメンバーと

![新規](../assets/new.svg) 発注書は拡張され、書き換えられます。 これらは、Adobe Commerceにデフォルトで含まれるようになりました。

![新規](../assets/new.svg) 発注承認ルールが実装されました。 これらのルールを使用すると、注文の購入ルールを作成して、発注ワークフローを制御できます。

![新規](../assets/new.svg) 「顧客としてログイン」は、Adobe Commerceにデフォルトで含まれるようになりました。 この機能を使用すると、サイト従業員は顧客としてログインし、見たものを見ることで顧客を支援できます。

![修正された問題](../assets/fix.svg) Elasticsearchを使用したレイヤーナビゲーションで、属性の集約が正しく機能するようになりました。

![修正された問題](../assets/fix.svg) 特殊文字による注文の検索が正しく機能するようになりました。

![修正された問題](../assets/fix.svg) クリック **[!UICONTROL Clear All]** 「 」ボタンをクリックすると、すべてのフィルターが折りたたまれるのではなく、展開されるようになりました。

![修正された問題](../assets/fix.svg) 製品の SKU/名前が注文履歴の検索フィルターの概要に含まれるようになりました。

![修正された問題](../assets/fix.svg) 並べ替えインジケータが「マイ発注」グリッドに正しく表示されるようになりました。

![修正された問題](../assets/fix.svg) 現在は、「承認」、「キャンセル」、「却下」および「発注」の各ボタンを 1 回だけクリックできます。 以前は、「 」ボタンを複数回クリックしていました。

![修正された問題](../assets/fix.svg) 発注書の「承認」、「却下」、「キャンセル」および「検証」の各ボタンがモバイルデバイスで正しく表示されるようになりました。

![修正された問題](../assets/fix.svg) 以前は、期限切れの割引を使用して発注を承認し、注文の合計は更新されませんでした。 これで、正しい合計が表示されるように発注の合計が更新されました。

![修正された問題](../assets/fix.svg) 2.3.4 で、カスタム拡張属性が顧客住所から見積もり住所にコピーされない問題が発生しました。 この問題が修正されました。

![修正された問題](../assets/fix.svg) B2B がインストールされている場合、カテゴリを共有カタログに割り当てると SQL エラーが表示されます。 この問題が修正されました。

![修正された問題](../assets/fix.svg) 変数の種類の値が正しくないので、管理者は構成可能な製品を注文に追加できませんでした。 オプションのドロップダウンが表示されませんでした。 この機能は正しく動作するようになりました。

![修正された問題](../assets/fix.svg) 以前は、[ ログインしていない ] グループのカテゴリ権限を編集すると、変更を保存する際にエラーが発生していました。 この問題が修正されました。

![修正された問題](../assets/fix.svg) ストア管理者が共有カタログにない注文に商品を追加できるようにする修正が追加されました。 以前は、カタログにない項目を追加すると、エラーメッセージが表示されていました。

![修正された問題](../assets/fix.svg) 以前は、コマンドの実行後に `php bin/magento indexer:set-dimensions-mode catalog_product_price website` 共有カタログを作成しようとすると、エラーが発生します。 この問題が修正されました。

![修正された問題](../assets/fix.svg) 会社を追加し、会社の管理者をデフォルト以外の Web サイトに割り当てると、誤ったサイト ID が送信され、エラーが発生していました。 この問題が修正されました。

![修正された問題](../assets/fix.svg) 以前は、顧客が別の顧客グループに移動された後、 _クイックオーダー_ が失敗し、エラーが発生しました。 この問題が修正されました。

![修正された問題](../assets/fix.svg) 以前は、B2B の引用符を含む WebAPI を使用してチェックアウトしようとすると、誤った値が API に送信され、エラーが発生していました。 この問題が修正されました。

![修正された問題](../assets/fix.svg) 以前は、API を使用して会社を「Active」に設定すると、エラーが発生していました。 この問題が修正されました。

![修正された問題](../assets/fix.svg) 不要なため `form` タグを使用すると、提示された送料を変更した後に Enter キーを押したときに、注文ページが自動的に更新されます。 この問題が修正されました。

![修正された問題](../assets/fix.svg) 以前は、カタログページで商品の表示制限を設定し、その制限が商品の総数を下回る場合にエラーが発生していました。 この機能は現在は期待どおりに動作します。

![修正された問題](../assets/fix.svg) 以前は、会社の管理者を変更すると、元の管理者アドレスが新しい管理者にコピーされ、2 つのアドレスが割り当てられていました。 現在は、正しいアドレスのみが追加されます。

![修正された問題](../assets/fix.svg) 以前は、Git が「許可済みで顧客に通知」に設定されている場合に、API を使用して見積もり項目を保存すると、失敗していました。 この API 呼び出しは、現在は期待どおりに動作します。

![修正された問題](../assets/fix.svg) 「見積」詳細ページに固定製品税が表示されます。

![修正された問題](../assets/fix.svg) 以前は、My Quotes ページの「コメント」タブで添付ファイルをクリックすると、ファイルのダウンロードに失敗していました。 この動作は、期待どおりに動作するようになりました。

### 既知の問題

- 複数 Web サイトのデプロイメントで B2B 1.2.0 にアップグレードすると、Adobe Commerceで例外がスローされる。 条件 `setup:upgrade` 実行時に、このエラーが `PurchaseOrder` モジュール： `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **回避策**: `B2B-716 Add NonTransactionableInterface` インターフェイスから `InitPurchaseOrderSalesSequence` データパッチホットフィックス ( 現在は **マイアカウント** > **ダウンロード** のセクション `magento.com`.
- 割引コードの有効期限が切れた後も発注書 (PO) には引き続き割引額が表示されますが、発注書が承認されると、その注文は割引されない合計になります。 **回避策**: `B2B-709 Purchase Order Discount patch` この問題のホットフィックス（現在は次から利用可能） **マイアカウント** > **ダウンロード** のセクション `magento.com`.
- 発注書の品目が在庫切れの場合、または発注書が実際の注文に変換された際に数量が不十分な場合は、エラーが発生します。 バックオーダーが有効な場合、オーダーは通常どおり処理されます。
