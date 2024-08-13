---
title: '[!DNL Adobe Commerce B2B] リリースノート'
description: リリースの変更点について詳しくは、リリースノート  [!DNL Adobe Commerce B2B]  参照してください。
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: d717a16f3ca20e51b002c6de19c696e090553052
workflow-type: tm+mt
source-wordcount: '7033'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] リリースノート

B2BAdobeのこれらのリリースノートでは、拡張機能がリリースサイクル中に追加した追加と修正をキャプチャしています。以下に例を示します。

![ 新機能 ](../assets/new.svg) 新機能
![ 修正された問題 ](../assets/fix.svg) 修正および改善
![ 既知の問題 ](../assets/bug.svg)

>[!NOTE]
>
>使用可能なAdobe Commerce リリースでサポートされている B2B Commerce拡張機能のバージョンについて詳しくは、[ 製品の可用性 ](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) を参照してください。

## B2B 1.5.0 – ベータ版

{{$include /help/_includes/b2b-beta-note.md}}

*2023 年 11 月 13 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

B2B v1.5.0 ベータ版リリースには、新機能、品質の向上、バグ修正が含まれています。

![ 新規 ](../assets/new.svg) 見積機能の改善により、バイヤーとセラーが見積を管理し、見積ネゴシエーションをより効果的に行えるようになりました。

- **見積もりをドラフトとして保存**<!--B2B-2566--> - ショッピング・カートから [ 見積もりリクエスト ](quote-request.md) を作成する際に、バイヤーは [!UICONTROL Request a Quote] のフォームで **[!UICONTROL Save as Draft]** を選択して、見積もりをドラフトとして保存できるようになりました。

  下書きの見積もりに有効期限がありません。 購入者は、アカウントダッシュボードの「[!UICONTROL My Quotes]」セクションで、下書きの見積もりを確認および更新できます。

- **Quote の名前を変更**<!--B2B-2596--> - 「**[!UICONTROL Rename]**」オプションを選択して、[Quote detail](account-dashboard-my-quotes.md#quote-actions) ページから Quote 名を変更できるようになりました。 このオプションは、権限を持つ購入者が見積もりを編集する際に使用できます。 名前の変更イベントは Quote History Log に記録されます。

- **見積書の複製**<!--B2B-2701--> - バイヤーとセラーは、既存の見積書をコピーして新しい見積書を作成できるようになりました。 Quote の詳細ビューからコピーを作成するには、管理 **[!UICONTROL Create Copy]** たは [ ストアフロント ](account-dashboard-my-quotes.md#quote-actions) の ](quote-price-negotiation.md#button-bar)Quote の詳細ビュー [ を選択します。

- **品目値引ロック**<!--B2B-2597--> – 見積ネゴシエーション中に、セラーは品目値引ロックを使用して、値引を適用する際の柔軟性を高めることができます。 例えば、販売者は、品目に特別品目割引を適用し、品目をロックして、それ以上の割引を防ぐことができます。 品目がロックされている場合、見積レベルの値引が適用される際に品目価格を更新することはできません。 [ 購買担当の見積の開始 ](sales-rep-initiates-quote.md) を参照してください。

![ 新会社 ](../assets/new.svg)**管理**<!--B2B-2901-->：指定された親会社に会社を割り当てることで、マーチャントはAdobe Commerceの会社を階層的な組織として表示および管理できるようになりました。 会社を親に割り当てると、親の会社管理者が会社アカウントを管理できるようになります。 許可された管理者ユーザーのみが、会社の割り当てを追加および管理できます。 詳しくは、[ 会社階層の管理 ](assign-companies.md) を参照してください。

- 「会社」ページに、新しい「**[!UICONTROL Company Type]**」フィールドで親および子会社を識別します。 マーチャントは、会社タイプ別に会社ビューをフィルタリングしたり、行項目または一括アクションを使用して会社を管理したりできます。

- マーチャントは、[!UICONTROL Company Account] のページの新しい「**[!UICONTROL Company Hierarchy]**」セクションから会社の割り当てを追加および管理できます。

- API デベロッパーは、新しい会社関係 REST API エンドポイント `/V1/company/{parentId}/relations` を使用して、会社の割り当てを作成、表示、削除できます。 [Web API 開発者ガイド ](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) の *会社オブジェクトの管理* を参照してください。

![ 問題の修正 ](../assets/fix.svg)<!--ACP2E-1984--> 管理者の見積書の詳細表示で「**[!UICONTROL Print]**」ボタンをクリックすると、見積書をPDFとして保存するように促すプロンプトが表示されるようになりました。 以前は、マーチャントは見積りの詳細を含むページにリダイレクトされていました。

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1742--> 以前は、パーセンテージが 0 で数量が変更された顧客見積を送信すると、管理者は例外をスローしましたが、数量は保存されていました。 この修正が適用されると、`0 percentage` の適切な例外に対してメッセージがスローされます。

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1742--> 見積ネゴシエーション中に、セラーは「見積依頼見積値引」フィールドで `0%` 定値引を指定し、見積をバイヤーに送り返すことができるようになりました。 以前は、売り手が 0% の割引を入力し、見積もりを購入者に送り返した場合、管理者は `Exception occurred during quote sending` のエラーメッセージを返しました。

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-2097-->ReCaptcha V3 がストアフロントのチェックアウト用に設定されている場合、B2B 見積のチェックアウトプロセス中に ReCaptcha 検証が正しく機能するようになりました。 以前は、検証が失敗し、`recaptcha validation failed, please try again` のエラーメッセージが表示されていました。

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1825--> 会社がブロックされると、会社に関連付けられているユーザーは発注書を送信できなくなります。 以前は、会社がブロックされている場合、会社に関連付けられているユーザーが発注書を送信することができました。

![ 問題の修正 ](../assets/fix.svg)<!--ACP2E-1933--> 会社管理者は、ストアフロントから会社ユーザーを追加できるようになりました。 以前は、管理者ユーザーが新しいユーザーを追加しようとすると、Commerceでエラーがログに記録されていました。ユーザー名：`CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`。

## B2B v1.4.2-p2

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg) Adobe Commerce 2.4.7-p2 以降および 2.4.6-p7 以降のセキュリティパッチリリースとの互換性が追加されました。 B2B 1.4.2-p2 リリースには含まれていません
[GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server) をサポートします。

>[!IMPORTANT]
>
>Adobe Commerce B2B バージョン 1.4.2 以降は、PHP 8.2 と互換性があります。Commerce インスタンスをバージョン 2.4.7 以降にアップグレードする場合は、インスタンスが PHP バージョン 8.2 を使用してAdobe Commerce B2B リリースとの互換性を保っていることを確認します。


https://wiki.corp.adobe.com/display/3DI/How+to+Create+and+Update+a+New+HelpX+Page#HowtoCreateandUpdateaNewHelpXPage-LinkstoupdateHelpXdocumentation:

## B2B v1.4.2-p1

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg) Adobe Commerce 2.4.7-p1 以降および 2.4.6-p6 以降のセキュリティパッチリリースとの互換性が追加されました。

>[!IMPORTANT]
>
>Adobe Commerce B2B バージョン 1.4.2 以降は、PHP 8.2 と互換性があります。Commerce インスタンスをバージョン 2.4.7 以降にアップグレードする場合は、インスタンスが PHP バージョン 8.2 を使用してAdobe Commerce B2B リリースとの互換性を保っていることを確認します。 さらに、B2B 1.4.2 以降では、現在、[GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server) をサポートしていません。


## B2B v1.4.2

*2023 年 10 月 10 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

B2B v1.4.2 リリースには、品質の改善とバグ修正が含まれています。

![ 修正された問題 ](../assets/fix.svg)<!--B2B-2897--> 販売者が購入者の会社に関連付けられた共有カタログで使用できない製品 SKU を含む購入者見積を作成すると、エラーメッセージ `The SKU you entered is not available in the shared catalog. Please check the SKU and try again` が表示されます。  販売者は、利用できない製品を削除するまで見積もりを保存できません。 以前は、使用できない SKU を含んだ見積もりが保存され、ストアフロントに見積もりが読み込まれませんでした。

>[!IMPORTANT]
>
>Adobe Commerce B2B バージョン 1.4.2 以降は、PHP 8.2 と互換性があります。Commerce インスタンスをバージョン 2.4.7 以降にアップグレードする場合は、インスタンスが PHP バージョン 8.2 を使用してAdobe Commerce B2B リリースとの互換性を保っていることを確認します。 さらに、B2B 1.4.2 以降では、現在、[GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server) をサポートしていません。

## B2B v1.4.1

*2023 年 8 月 7 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html)。 Adobe Commerce 2.4.7-beta1 と互換性あり。

B2B v1.4.1 リリースには、品質の改善とバグ修正が含まれています。

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1825--> 会社がブロックされると、会社に関連付けられているユーザーは発注書を送信できなくなります。 以前は、会社がブロックされている場合、会社に関連付けられているユーザーが発注書を送信することができました。

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1943--> 製品のバックオーダーのステータスがストアフロントに正しく表示されるようになりました。 以前は、出荷可能な製品が誤ってバックオーダーと識別されていました。

![ 問題を修正 ](../assets/fix.svg)<!--ACP2E-1862--> 会社登録フォームに顧客ファイルタイプ属性が含まれている場合、登録プロセス中にアップロードされたファイルは、会社を作成した後、会社管理者のアカウント情報に含まれるようになりました。 以前は、添付ファイルが見つかりませんでした。

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1793--> 設定可能な製品のスウォッチセレクターが、購買依頼リスト品目の設定ページに期待どおりに表示されるようになりました。 以前は、スウォッチセレクターは購買依頼リスト項目設定ページのドロップダウンフィールドとして表示されていました。

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1968-->[ 会社GraphQLクエリ ](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) を使用して会社の詳細を返す場合、結果がエラーなく正常に返されるようになりました。

## B2B v1.4.0

*2023 年 6 月 13 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html)。 Adobe Commerce 2.4.7-beta1 との互換性

このリリースには、B2B の交渉可能な引用符と複数のバグ修正に関する新機能と機能強化が含まれています。

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.7-beta1 との互換性が追加されました。

![ 新規 ](../assets/new.svg)**売り手が見積もりを開始** – 売り手は、管理の見積もりグリッドおよび顧客グリッドから直接買い手の見積もりを開始できるようになりました。 この機能により、見積もりプロセスが合理化され、お客様の複雑さが軽減されます。 顧客が注文を開始していない場合、販売者は顧客に代わってすばやく見積もりを作成し、交渉プロセスを開始できます。 以前は、見積もりは、購入者、または顧客としてログインした販売者のみがストアフロントから作成できました。

![ 新規 ](../assets/new.svg)**明細品目値引およびネゴシエーション**—<!--B2B-2440--> 見積内で、B2B バイヤーおよびセラーは、明細品目レベルで値引および手形の交換を交渉して、基本契約に達するまで交渉できるようになりました。 メモの作成と更新は、明細品目と見積履歴に含まれ、通信を追跡します。 以前は、購入者と販売者は、メモを交換したり、見積もりレベルで割引を適用したりすることしかできませんでした。

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、「発注書」オプションが有効になっており、PayPal 支払いオプションを使用して作成されたバーチャル見積もりが選択されている場合、支払い中に正しい詳細が表示されるようになりました。 以前は、これらの条件の下で合計はゼロとして表示されていました。

![ 修正された問題 ](../assets/fix.svg) <!--ACP2E-1504--> クレジット制限が 999 を超える会社を保存しようとすると、検証エラーが発生しなくなりました。 以前は、会社のクレジット制限が 999 を超える場合、Adobeコマースにコンマ区切り記号が挿入され、検証エラーが発生して更新を保存できませんでした。

![ 修正された問題 ](../assets/fix.svg) <!--ACP2E-1474--> 交渉可能な見積もりで注文を行っても、選択した配送先住所は変更されません。 以前は、注文すると、選択した配送先住所がデフォルトの配送先住所に変更されていました。

![ 修正された問題 ](../assets/fix.svg) <!--ACP2E-1429--> B2B 機能のストア設定で、「**[!UICONTROL Enable Shared Catalog direct products price assigning]**」フィールドが自動的に無効になりました。 ストアフロントでは、**[!UICONTROL Enable Company]** 設定または **[!UICONTROL Enable Shared Catalog]** 設定が **[!UICONTROL No]** に設定されている場合、非表示になります。

![ 修正された問題 ](../assets/fix.svg) <!--ACP2E-1683--> ストアフロントから会社アカウントを作成する際に、Commerceは、会社登録を処理する前にメールアドレスを検証するようになりました。 メールアドレスが無効な場合、操作は失敗し、アカウントの更新は処理されません。 以前は、メールアドレスが無効なために会社アカウントの作成要求が失敗した場合でも、顧客アカウントが作成されていました。

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1664--> 共有カタログと価格構造に二重引用符を含む製品 SKU で、管理者でエラーが発生しなくなりました。

![ 修正された問題 ](../assets/fix.svg) <!--ACP2E-1498--> Commerce アプリケーションの Varnish 設定を更新して、ゲストユーザーが他のお客様グループからのデータを表示できないようにしました。

### 既知の問題

[Adobe Commerce バージョン 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html) で B2B 1.4.0 をインストールまたはアップグレードすると、次のエラーが発生します。

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

この問題を修正するには、[stability tag](https://getcomposer.org/doc/04-schema.md#package-links) を使用して、B2B セキュリティパッケージの手動依存関係を追加することにより、B2B セキュリティパッケージの手動依存関係を追加します。 手順については、[Adobe Commerce ナレッジベース ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html) を参照してください。

## B2B v1.3.5

*2023 年 3 月 14 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg) Adobe Commerce 2.4.6-p2 との互換性をサポートするために、B2B バージョン 1.3.5-p2 をリリースしました。

![ 新規 ](../assets/new.svg) Adobe Commerce 2.4.6-p1 との互換性をサポートするために、B2B バージョン 1.3.5-p1 をリリースしました。

>[!NOTE]
>
>Commerceを 2.4.6 から [ 最新リリース ](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6) にアップグレードした後、必ずサポートされている B2B 1.3.5 パッチリリースに更新してください。 または、B2B 拡張機能をバージョン 1.3.5 からバージョン 1.4.0 以降にアップグレードして、最新機能を取得します。

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.6 がサポートされるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerceでは、「発注書」オプションが有効になっており、PayPal 支払いオプションを使用して作成されたバーチャル見積もりが選択されている場合、支払い中に正しい詳細が表示されるようになりました。 以前は、これらの条件の下で合計はゼロとして表示されていました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-609--> **閲覧を許可カテゴリ** 設定の顧客グループのリストに、共有カタログに関連する顧客グループが含まれなくなりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-1244--> 税金/VAT 番号の顧客属性が、管理者とストアフロントの両方の会社管理者アカウントで期待どおりに機能するようになりました。 会社アカウントを作成する際に、カスタムの税金/VAT 属性は不要になりました。 以前は、マーチャントがカスタムの税金/VAT 属性を持つ会社アカウントを作成すると、Adobe Commerceがストアフロントと管理者の両方で検証エラーをスローしていました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-1236--> 特定の範囲で共有カタログ機能を無効にすると正しく機能するようになりました。 以前は、マーチャントが共有カタログ設定を保存すると、Adobe Commerceが無効なスコープを設定していました。

![ 修正された問題 ](../assets/fix.svg) 管理者ユーザー <!--- ACP2E-1203-->、会社ユーザーの顧客カスタム属性値を保存できるようになりました。 以前は、会社ユーザーの顧客カスタム属性を保存できませんでした。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-1221--> パフォーマンスの問題は、多くの会社の権限が既に割り当てられている場合に、GraphQLを通じて提供される会社の権限の検証で解決されます。

![ 修正された問題 ](../assets/fix.svg)<!--- ACP2E-1242--> クイックオーダーを使用して利用可能な在庫を超える量の商品を追加すると、Adobe Commerceが買い物かごページでエラーをスローしなくなりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-1090--> 会社の権限操作 `SELECT` パフォーマンスが向上しました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-2456--> カテゴリクエリで、クエリ対象のカテゴリに対してカテゴリ権限が明示的に設定されていない場合、ストア設定に従って製品価格を返すようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-6829--> 承認済みの見積もりリクエストを使用して購入を完了する際に、「**[!UICONTROL Place Order]**」ボタンが期待どおりに機能するようになりました。 交渉可能な見積もり `negotiableQuoteCheckoutSessionPlugin` プラグインに関する問題が解決されました。

## B2B v1.3.4

*2022 年 8 月 9 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.5 がサポートされるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-453--> 既存の会社が API 呼び出しによって更新されるたびに、Adobe Commerceがメール通知を送信しなくなりました。 会社を作成した場合にのみメールが送信されるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerceでは、**[!UICONTROL Enable Cross Border Trade]** 税の計算設定が有効な場合、交渉可能な見積もりの総計を正しく計算するようになりました。

![ 修正された問題 ](../assets/fix.svg)<!--- ACP2E-322--> 設定 **[!UICONTROL Move out of stock to the bottom]** 定が有効な場合、在庫が更新された後、設定可能な製品が製品リストの最後の位置に移動されるようになりました。 新しいカスタムデータベースクエリが実装され、Elasticsearchインデックスの並べ替え順が管理者向けの並べ替え順に従うようになりました。 以前は、この設定が有効な場合、設定可能な製品とその子製品は、リストの下部に移動されませんでした。

![ 問題の修正 ](../assets/fix.svg)<!--- ACP2E-308--> 発注書のメールが、マルチサイトデプロイメントの各 web サイトのメール送信設定に従うようになりました。 メールキューのカスタムロジックに **[!UICONTROL Disable Email Communications]** 設定のチェックが追加されます。 以前は、Adobe Commerceは、セカンダリ web サイトのメール送信設定を受け入れませんでした。

![ 修正された問題 ](../assets/fix.svg)<!--- ACP2E-302--> クイックオーダーページの SKU フィールドのタイトルが、わかりやすくするために変更されました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-543--> 買い物客が「SKU または商品名を入力 **フィールドに無効な SKU を入力すると、Adobe Commerceにエラーメッセージが表示され** ようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-1753--> 会社管理者の **[!UICONTROL Account Created in]** フィールドに、会社を保存した後も期待どおりの値が保持されるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-722 -->`uid` でフィルタリングされた購買依頼リストを取得する際に、`customer` クエリが空の結果を返さなくなりました。

![ 問題を修正 ](../assets/fix.svg)<!--- ACP2E-210 --> ストアクレジットが 1 回だけ適用されるように、`collectQuoteTotals` 呼び出しの前にプラグインを追加しました。

![ 修正された問題 ](../assets/fix.svg)<!--- ACP2E-665 --> 管理者が管理者からアカウントを削除すると、ユーザーはログインページにリダイレクトされるようになりました。 以前は、Adobe Commerceがエラーをスローしていました。 プラグイン（`SessionPlugin`）のコードブロックは、`try…catch` ブロック内に配置されています。 以前は、このコードは、汎用の例外処理ブロック内にラップされていませんでした。

![ 問題を修正 ](../assets/fix.svg) <!--- ACP2E-661 --> モバイルモードのクイックオーダーのページで、有効な製品名または SKU を入力した後に **Enter** を押すと、買い物客が期待どおりに次のフィールドに移動するようになりました。

![ 問題の修正 ](../assets/fix.svg)<!--- ACP2E-607 --> チェックアウトワークフローの請求と配送先住所のセクションに、会社名が期待どおりに表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg)<!--- ACP2E-375 --> ストアの支払い方法が無効になっている場合、スト **[!UICONTROL Zero Subtotal Checkout]** クレジットを使用できなくなりました。 以前は、管理者からの発注時に「クレジットを保存」チェックボックスが機能していませんでした。 店舗クレジットで注文が行われず、次のエラーが表示されました：`The requested Payment Method is not available`。

## B2B v1.3.3

*2022 年 8 月 9 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.4 がサポートされるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41985--> 会社の役割が 10 万件を超えるデプロイメントでAdobe Commerce 2.3.x からAdobe Commerce 2.4.x にアップグレードするのに必要な時間が大幅に短縮されました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42153-->POSTの `V1/order/:orderId/invoice` リクエストで、**[!UICONTROL Payment on Account]** 支払い方法が有効な場合に、部分請求書の作成がサポートされるようになりました。 以前は、Adobe Commerceは次のエラーをスローしていました：`An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`。 [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41975--> 顧客の買い物かごに他の製品が含まれている場合、PayPal Payflow Pro は B2B 譲渡可能な見積もりで期待どおりに機能するようになりました。 Adobe Commerceが注文を正常に処理し、期待どおりにメールを顧客に送信するようになりました。 以前は、Adobe Commerceが致命的なエラーをスローし、値が 0 の確認メールをお客様に送信していました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41819--> 共有カタログ内の一部の製品を除外した後、カタログ検索結果ページにページネーションが正しく表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42886--> 管理者で会社ユーザーを作成または保存する際に、顧客のカスタム属性が期待どおりに保存されるようになりました。

![ 問題を修正しました ](../assets/fix.svg) <!--- MC-42927--> 「新しい会社を作成」フォームを一度クリックすると、フォームが複数の送信されないように、「**[!UICONTROL Submit]**」ボタンが無効になりました。 以前は、このボタンを繰り返しクリックすると、このフォームを複数回送信してエラーが発生する可能性がありました。

![ 修正された問題 ](../assets/fix.svg) 買い物客 <!--- MC-42787--> 並べ替えが無効になっているストアにログインした際に、Adobe Commerceでストアフロントに並べ替えリンクが表示されなくなりました。

![ 修正された問題 ](../assets/fix.svg) 共有カタログ <!--- MC-43115--> 有効な場合、SKU によるクイックオーダー検索で大文字と小文字が区別されなくなりました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42203--> 会社を作成する際に、顧客属性のファイルを更新できるようになりました。 以前は、添付ファイルのタイプが `File` の会社を作成しようとすると、Adobe Commerceは会社を作成せず、例外ログ `Something went wrong while saving file` に次のエラーを記録していました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42242--> （`File`）または（`Image`）タイプのカスタム属性を持つ顧客アカウントを持つ会社を作成できるようになりました。 以前は、アカウントにこれらのカスタマイズ可能なオプションのいずれかが含まれている場合、会社編集ページローダーが解決されず、会社の詳細を編集できませんでした。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42268--> 共有カタログが有効な場合、`products` クエリが正確な `total_count` フィールドを返すようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42203--> 会社を作成する際に、顧客属性のファイルを更新できるようになりました。 以前は、添付ファイルのタイプが `File` の会社を作成しようとすると、Adobe Commerceは会社を作成せず、例外ログ `Something went wrong while saving file` に次のエラーを記録していました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-43178--> オンライン配送方法を無効にした後、_会社設定_ ページと _会社を作成_ ページが期待どおりに動作するようになりました。 検証が追加され、無効になった出荷モジュールの処理が試行できなくなりました。 以前は、Adobe Commerceには「`Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`」というエラーが表示されていました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42214--> _カテゴリ_ ページに、部分的なインデックス作成中に権限が生成されている間、一貫した製品データが表示されるようになりました。 ディレクトリ権限の新しい部分インデクサーがこのプロセスに追加されました。 以前は、インデクサーの実行中に表示されるデータが正しくありませんでした。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42567--> カタログの権限が使用され、製品が共有カタログに割り当てられている場合、`categoryList` クエリが正しい製品数を返すようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42528--> `categoryList` クエリは、カテゴリ権限に従い、許可されたカテゴリのみを返すようになりました。 以前は、割り当て済みカテゴリと未割り当てのカテゴリをすべて返していました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42399--> `rest/V1/company/{id}` リクエストが、期待どおりに `is_purchase_order_enabled` 属性値を返すようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-128--> カスタム顧客属性が「_会社管理者_」タブに期待どおりに表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-130--> マイアカウント ページのマイウィッシュリスト ブロックが、会社管理者および会社ユーザーに対して期待どおりに表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-133--> クイックオーダーエラーが買い物かごに表示されなくなりました。 以前は、カタログに SKU が見つからなかった場合、Adobe Commerceによって買い物かごにこのエラーが表示されていました：`The SKU was not found in the catalog`。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-194--> 共有カタログの保存操作が、より高速に実行されるように最適化されました。 これまで、共有カタログを多数の顧客グループと共に保存するには、数分かかる場合がありました。

![ 修正された問題 ](../assets/fix.svg)Adobe Commerce<!--- MC-42240-->、親カテゴリが削除されると、`sharedcatalog_category_permissions` テーブルからすべてのサブカテゴリ権限を削除するようになりました。 以前は、親カテゴリデータのみが削除されていました。

## B2B v1.3.2

*2022 年 8 月 29 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.3 がサポートされるようになりました。

![ 修正された問題 ](../assets/fix.svg)Adobe Commerce<!--- MC-39862-->、期限切れの譲渡性見積に関する更新メールを正常に送信するようになりました。 以前は、交渉可能な見積もりの有効期限が切れた場合、Adobe Commerceは更新メールを送信しませんでした。

![ 修正された問題 ](../assets/fix.svg)Adobe Commerce<!--- MC-40682-->、`cron` ジョブがない場合、まもなく期限切れになる更新メールと、期限切れの交渉可能な引用符を正常に送信するようになりました。

### 会社

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41542--> 「新しい会社アカウントを作成」ページの国ドロップダウンフィールドに空のオプション値が表示されなくなりました。 以前は、最初の 2 つのオプション値と国コード `AN` は空でした。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41260--> 会社のユーザーが作成した注文の「**[!UICONTROL Return]**」ボタンをクリックすると、管理者ユーザーが期待どおりに返品の作成ページにリダイレクトされるようになりました。 以前は、管理者は注文履歴ページにリダイレクトされていました。

![ 修正された問題 ](../assets/fix.svg)`bin/magento setup:upgrade` 行中に `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` メソッド <!--- MC-40798--> 実行した際に、Adobe Commerceがメモリ不足エラーで失敗しなくなりました。 以前は、Adobe Commerceは、権限の初期化時にバッチサイズをコレクションに使用せず、代わりにすべての会社の役割のコレクションを読み込んでいました。

![ 修正された問題 ](../assets/fix.svg) 会社ユーザー <!--- MC-40551-->、顧客のカスタム属性値を編集および更新できるようになりました。 以前は、これらの属性は、ユーザーの作成および編集フォームに正しくバインドされていませんでした。 会社ユーザーは異なる属性値を入力できましたが、Adobe Commerceはこれらの値を正しく保存しませんでした。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-32653--> 会社の役割の権限のリソースツリーを、期待どおりに翻訳できるようになりました。 以前は、有効な翻訳ファイルが存在しても、権限ツリーは翻訳されませんでした。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-40358--> Adobe Commerceで、B2B ユーザーのカスタムカスタマー属性値が期待どおりに保存されるようになりました。 以前は、カスタムの顧客属性を含む会社アカウントを作成するとテンプレートエラーがトリガーされ、Adobe Commerceがフォームを正常に読み込めませんでした。 `company_create_account` のレイアウトに引数を追加することで、この問題が解決しました。

![ 修正された問題 ](../assets/fix.svg) すべてのユーザー <!--- MC-41721--> 表示、アクティブユーザーを表示、非アクティブユーザーを表示などの会社ユーザーフィルターが期待どおりに動作するようになりました。 以前は、会社ユーザーページのフィルタリングアクションがJavaScript エラーの原因となっていました。

### 会社クレジット

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41551--> web サイトレベルの権限のみを含む制限付きアカウントを持つ管理者が、web サイトとは異なる通貨を使用する会社を作成できるようになりました。

![ 修正された問題 ](../assets/fix.svg) Adobe Commerce<!--- MC-41523-->、正しい `from` メールアドレスと範囲から会社のメールを送信するようになりました。 以前は、Adobe Commerceは、会社のクレジット割り当てや更新メールを送信する際に、web サイトの範囲を考慮していませんでした。

### クイック注文

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42104--> CSV ファイルからのクイックオーダーを使用して注文を作成すると、存在しない SKU で期待どおりに動作するようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-40268--> クイックオーダーを使用して複数の SKU で検索を実行すると、期待どおりに動作するようになりました。 以前は、結果に重複エントリが含まれていました。

![ 問題を修正 ](../assets/fix.svg) <!--- MC-40261--> クイックオーダー中に SKU を使用して複数の製品を選択した場合に、追加製品リストの表示で SKU が小文字と大文字で同じように処理されるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-40225--> クイックオーダーを使用すると、買い物客が指定した数量で製品が追加されるようになりました。 以前は、Adobe Commerceは、買い物客が指定した数量が 1 を超える場合でも、1 つの商品のみを追加していました。

![ 問題を修正 ](../assets/fix.svg) <!--- MC-41283--> クイック注文のオートコンプリート機能が、一部の SKU で機能するようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41299--> Adobe Commerceでは、**個別に表示されない** として設定されている商品が、クイックオーダーページの自動候補リストと検索結果に表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42402--> 買い物客がクイックオーダーフォームを使用して、大文字を含む SKU で複数の製品を追加できるようになりました。 以前は、最初の製品のみが追加されていました。

### 譲渡可能見積

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41232--> 買い物客は、「URL」フィールドにネゴシエート可能な見積もりにリンクを貼り付けて正常にログインした後、ネゴシエート可能な見積もりページにリダイレクトされるようになりました。 以前は、買い物客はマイアカウントページにリダイレクトされていました。

![ 問題を修正 ](../assets/fix.svg) <!--- MC-39317--> チェックアウト時に作成された顧客アカウント用に、日付がカスタマイズ可能なオプションを含む製品を含む注文で、並べ替えが期待どおりに機能するようになりました。 以前は、Adobe Commerceは並べ替えを処理せず、次のエラーを表示していました：`The product has required options. Enter the options and try again`。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-39063--> 発注書モジュールが無効になっている場合、交渉可能な見積もりの配送先住所はチェックアウト中に編集できなくなります。 この動作は、以前の修正でネゴシエーション可能な見積もりチェックアウトレンダラーから `isQuoteAddressLocked` が削除されたことによって発生しています。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-38967--> マーチャントは、管理者から交渉可能な見積もりに製品を追加できるようになりました。

### 発注書

![ 修正された問題 ](../assets/fix.svg) <!--- MC-39983--> Adobe Commerceでは、**[!UICONTROL Name Prefix]** 属性が `required` に設定されている場合、PayPal Express チェックアウトを使用して注文を行うと、期待どおりに情報エラーメッセージが表示されるようになりました。 以前は、Adobe Commerceによる注文やエラーメッセージの表示はありませんでした。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-39620--> Google タグマネージャーが有効な場合、発注書モジュールの請求先住所の UI コンポーネントで見積先住所が正しく使用されるようになりました。 以前は、支払いページでJavaScript エラーが発生していました。

### 購買依頼リスト

![ 修正された問題 ](../assets/fix.svg) <!--- MC-40426--> マーチャントは、POST `rest/all/V1/requisition_lists` エンドポイントを使用して、顧客の購買依頼リストを作成できるようになりました。 以前は、Adobe Commerceが購買依頼リストを作成しようとした際に、次の 400 エラーがスローされていました。`Could not save Requisition List`

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41123--> 買い物かごに在庫切れの商品も含まれている場合、買い物かごの在庫商品に「**[!UICONTROL Add to Requisition List]**」ボタンが表示されるようになりました。 以前は、1 つの買い物かごに 2 つの製品が含まれ、そのうち 1 つが在庫切れの場合、どちらの製品にも「_[!UICONTROL Add to Requisition List]_」ボタンが表示されませんでした。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-40877--> REST API を使用して、製品を購買依頼リストに追加できるようになりました。

![ 修正された問題 ](../assets/fix.svg) 購買依頼リスト <!--- MC-40155--> 値 **[!UICONTROL Latest Activity Date]** ロケール形式に準拠するようになりました。

![ 修正された問題 ](../assets/fix.svg)<!--- MC-39580-->Adobe Commerceで、購買依頼リストからバンドル商品を編集する際に致命的なエラーがスローされなくなりました。

![ 修正された問題 ](../assets/fix.svg)Adobe Commerce<!--- MC-40454-->、カスタマイズ可能なオプションを `(File)` つ商品を購買依頼リストからウィッシュリストに追加すると、正しい商品価格が表示されるようになりました。 アップロードしたファイルへのリンクも、期待どおりに表示されます。 以前は、Adobe Commerceで誤った製品価格が表示され、ファイルへのリンクが表示されていませんでした。

![ 問題を修正 ](../assets/fix.svg) <!--- MC-36383--> カスタマイズ可能なオプションを備え `(File)` 製品を、購買依頼リストから買い物かごに追加できるようになりました。

### 共有カタログ

![ 修正された問題 ](../assets/fix.svg) <!--- MC-40497--> 特定の web サイトに限定された役割を持つ管理者が、共有カタログの作成、表示、編集ができるようになりました。 以前は、限られたロールを持つ管理者が共有カタログを作成しようとすると、Adobe Commerceが致命的なエラーをスローしていました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41337--> レイヤードナビゲーションの結果に、フィルタリングされた属性を持つ製品の正確な数が含まれるようになり、買い物客は複数のフィルターを適用できるようになりました。 以前は、1 つのフィルターのみを適用できましたが、Adobe Commerceのレイヤーナビゲーションで、不正確な製品数が表示されていました。

![ 修正された問題 ](../assets/fix.svg) Adobe Commerce<!--- MC-40779-->、検索結果のレイヤー化されたナビゲーションフィルターに製品数を正しく表示するようになりました。 以前は、検索結果ページのプラグインはElasticsearchを使用していませんでしたが、データベースに新しいクエリを発行しました。

![ 修正された問題 ](../assets/fix.svg)<!--- MC-39978--> マーチャントがデフォルトの共有カタログからすべての商品を削除した場合に、Adobe Commerceで階層価格が削除されなくなりました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-39802--> 共有カタログが有効な場合、フィルターが現在のカテゴリでフィルタリングされ、すべてのページに正しく表示されるようになりました。 以前は、フィルターは現在のページに対してのみ誤って計算され、現在のカテゴリではフィルタリングされていませんでした。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-39522--> 共有カタログが有効な場合に、共有カタログに割り当てられていない商品の場合、GraphQL `products` クエリが商品の価格範囲とカテゴリを返さなくなりました。 以前は、製品自体が `items` 配列で返されなかった場合でも、クエリは製品の集計を返していました。

## B2B v1.3.1

*2021 年 2 月 9 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.2 がサポートされるようになりました。

![ 新規 ](../assets/new.svg) 発注書でオンライン支払い方法がサポートされるようになりました。

![ 修正された問題 ](../assets/fix.svg) この製品を以前の注文で使用した際に、購買依頼リストから直接買い物かごに設定可能な製品を追加しても、システムエラーが返されなくなりました。

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、分割データベース設定がデプロイされた際に、発注書に対して「自分の承認が必要」タブが正しく表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、発注書を表示する際に、バンドル商品とギフトカードに関する詳細が表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg) 買い物客は、**[!UICONTROL Website Restriction]** が有効で、**[!UICONTROL Restriction Mode]** が `Private Sales: Login Only` に設定されているストアで閲覧している間、自分のアカウントにログインした後、期待どおりにリダイレクトされるようになりました。 以前は、買い物客はストアのホームページにリダイレクトされていました。<!--- MC-38934-->

![ 修正された問題 ](../assets/fix.svg) 多数の顧客（13000 を超える）を含む B2B の会社階層を使用したデプロイメントで、会社管理者のアカウントダッシュボードページで、注文履歴が期待どおりに読み込まれるようになりました。 以前は、注文履歴の読み込みに時間がかかったり、まったく時間がかからなかったりして、Adobe Commerceに 503 エラーが表示されていました。<!--- MC-38830-->

![ 修正された問題 ](../assets/fix.svg) カテゴリ ページから購買依頼リストにカスタマイズ可能なオプションを含む未設定製品を追加すると、Adobe Commerceで複数の同一の警告メッセージが表示されなくなりました。<!--- MC-38342-->

![ 修正された問題 ](../assets/fix.svg) B2B の共有カタログが有効な場合、新しい製品や重複した製品がカテゴリページで期待どおりに表示されるようになりました。<!--- MC-38307-->

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、会社の顧客グループが更新された際に、会社管理者に関連付けられた正しい `store_id` を保持するようになりました。 以前は、グループが更新されると、`store_id` がデフォルトのストアに変更されていました。<!--- MC-38196-->

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceは、グループ化された商品を買い物かごに追加する場合と同じ方法で、グループ化された商品をシンプルな商品のリストとして購買依頼リストに保存するようになりました。 以前は、Adobe Commerceによるグループ化された商品の保存方法により、購買依頼リストからのグループ化された商品のリンクは、グループ化された商品ではなく、常にシンプルな商品にリダイレクトされていました。<!--- MC-38049-->

![ 修正された問題 ](../assets/fix.svg) 注文情報を CSV 形式で書き出す際に、**[!UICONTROL Company Name]** フィールドで注文をフィルタリングできるようになりました。 以前は、Adobe Commerceは `var/export/{file-id}` にエラーを記録していました。<!--- MC-37785-->

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、ストアフロントで「新規購買依頼リストの作成」タブを選択すると、「購買依頼リストの作成」ポップアップが期待どおりに表示されるようになりました。<!--- MC-37915-->

![ 修正された問題 ](../assets/fix.svg) 購買依頼リストに、リストに追加されたすべてのグループ化製品と数量が含まれるようになりました。 以前は、販売員が商品詳細ページから商品を追加した後に購買依頼リストに移動すると、Adobe Commerceに「`1 product(s) require your attention - Options were updated. Please review available configurations`」というエラーが表示されていました。<!--- MC-37621-->

![ 修正された問題 ](../assets/fix.svg) マルチサイトデプロイメントで会社を作成する際に、正しいストア表示が関連する web サイトに関連付けられるようになりました。 以前は会社を作成できませんでしたが、Adobe Commerceに「`The store view is not in the associated website`」というエラーが表示されていました。<!--- MC-37488-->

![ 修正された問題 ](../assets/fix.svg) クイックオーダーを使用して SKU 別に製品を並べ替えても、CSV ファイルで製品数量が重複しなくなりました。<!--- MC-37427-->

![ 修正された問題 ](../assets/fix.svg) クイックオーダーページの _[!UICONTROL Enter Multiple SKUs]_セクションに空の値が含まれている場合、「**[!UICONTROL Add to Cart]**」ボタンがブロックされなくなりました。 代わりに、Adobe Commerceに有効な SKU を入力するように求めるメッセージが表示されるようになりました。<!--- MC-37387-->

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceは、購買依頼リストから商品レビューを発行すると、商品ページに次のメッセージを表示するようになりました。`You submitted your review for moderation` レビューは、保留中のレビューのページ（Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**）にも表示されます。 以前は、Adobe Commerceは保留中のレビューのリストにレビューを追加しましたが、商品ページで 404 エラーが発生しました。<!--- MC-37119-->

![ 修正された問題 ](../assets/fix.svg) `sharedCatalogUpdateCategoryPermissions` コンシューマーのパフォーマンスが向上しました。 共有カタログを作成した後、カタログ権限インデクサーは、すべての顧客グループではなく、共有カタログの顧客グループ ID のみを使用するようになりました。<!--- MC-36770-->

![ 修正された問題 ](../assets/fix.svg) 買い物客のデフォルト以外の住所に関連付けられたカスタム顧客住所属性フィールドが、ストアフロントのチェックアウトワークフローで期待どおりに保存されるようになりました。<!--- MC-36630-->

![ 問題を修正しました ](../assets/fix.svg) ストアのデフォルトの共有カタログに属する製品の注文を、期待どおりに管理 REST API （`rest/V1/carts/{<CART_ID>/items`）を使用して、買い物客に対して配置できるようになりました。 Adobe Commerceは、`\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave` でカタログ権限の検証を共有する前に、商品が公開カタログに割り当てられたかどうかを確認するようになりました。 以前は、Adobe Commerceは商品を買い物客の買い物かごに追加せず、次のエラーをスローしていました。`No such shared catalog entity`。<!--- MC-36535-->

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceが、Adobe Commerce ストアのアドレスから新しい会社ユーザー登録メールを送信するようになりました。 以前は、このメールは会社の管理者のアドレスから送信されていました。<!--- MC-36480-->

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceは、マーチャントに新しい属性の保存を許可する前に、予約済みの会社属性名の重複についてカスタム属性を確認するようになりました。<!--- MC-36282-->

![ 修正された問題 ](../assets/fix.svg)`credit_history` クエリでは、最初に割り当てられた金額と購入された金額の両方について、指定された会社のクレジット履歴を返すようになりました。 以前は、このクエリはエラーを返していました。

![ 修正された問題 ](../assets/fix.svg) アカウント情報を編集ページの「**[!UICONTROL Company]**」フィールドと「**[!UICONTROL Job Title]**」フィールドが編集できなくなりました。

### 既知の問題

- B2B 購入者は、オンライン支払い方法を使用して、通常の発注書フローをバイパスできます。 このシナリオは、購入者がチェックアウト全体の合計を 0 に減らし（プロモーションコードやギフトカードなど）、そのコードまたはギフトカードを削除した場合に発生する可能性があります。 そうした状況でも、Adobe Commerceは、割り当てられたカタログの商品の価格に基づいて正しい金額を注文します。 **_回避策_**：発注承認でオンライン支払方法が有効な場合は、ギフト カードおよびクーポン コードを無効にします。<!--- B2B-1603-->

- 購入者は、PayPal Express Checkout を使用して発注から注文を行おうとすると、**[!UICONTROL In-Context Mode]** が無効な場合、買い物かごにリダイレクトされます。<!--- B2B-1604-->

- 購入者が発注書を作成した後、チェックアウトページに移動すると、Adobe Commerceで 404 エラーが表示される場合があります。 このエラーは、購入者が、以前の購入を完了せずにチェックアウトページに移動する前に、オンラインの支払い方法を使用して別の発注書を以前に作成した場合に発生します。 買い手はまだ発注書を配置することができます。 **_回避策_**：なし。<!--- B2B-1605-->

- 特定の支払い方法に対する割引は、購入者が最終チェックアウト中に支払い方法を変更した場合でも、発注書のチェックアウト中に保持されます。 その結果、お客様は権利のない割引を受けることができます。 この問題は、支払方法が変更されても、元の支払方法の買い物かごルールが引き続き適用されるために発生します。 **_回避策_**：なし。 詳しくは、[Adobe Commerce 2.4.2 B2B の既知の問題：お支払い方法が変更された後、オンライン発注書に対する割引が残ります ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html)_ナレッジベース_ に関する記事を参照してください。<!-- B2B-1012 -->

- `deleteRequisitionListOutput` の問合せでは、残りの購買依頼リストではなく、削除された購買依頼リストに関する詳細が戻されます。<!--- MC-39894-->

## B2B v1.3.0

*2020 年 10 月 15 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

このリリースには、注文承認、発送方法、買い物かご、管理者アクションのログ記録などの改善が含まれています。

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.1 がサポートされるようになりました。

![ 新規 ](../assets/new.svg)B2B 注文の承認が強化され、使いやすさが向上し、発注書に対する一括アクションが可能になりました。

![ 新規 ](../assets/new.svg) B2B のマーチャントは、各会社に提供される発送方法を制御できるようになりました。<!--- BUNDLE-160 161 162 -->

![ 新規 ](../assets/new.svg) マーチャントは、ユーザーが 1 回のアクションで買い物かごの内容をクリアでき、この機能を web サイトの <!--- BUNDLE-108 --> ージごとに独立して設定できるようになりました

![ 新規 ](../assets/new.svg) B2B 購入者は、個々の商品または買い物かごの内容全体を購買依頼リストに直接追加できるようになりました。<!--- BUNDLE-145 144-->

![ 新規 ](../assets/new.svg) B2B マーチャントは、支払い方法として「アカウント内支払い」を使用することにより、顧客に代わって管理者から注文を作成できます。<!--- BUNDLE-166 178-->

![ 新規 ](../assets/new.svg) マーチャントは、ユーザーに関連付けられたすべての見積もりを顧客の詳細ページから直接表示できるようになりました。<!--- BUNDLE-139 -->

![ 新規 ](../assets/new.svg) マーチャントは、オンラインで顧客を会社別にフィルタリングできるようになりました。<!--- BUNDLE-137 -->

![ 新規 ](../assets/new.svg) 管理者は、管理者の顧客を営業担当者でフィルタリングできるようになりました。<!--- BUNDLE-110 -->

![ 新規 ](../assets/new.svg) 不正なアカウントやスパムアカウントの作成を減らすために、マーチャントは、ストアフロントの新規会社リクエストフォームでGoogle reCAPTCHA を有効にできるようになりました。<!--- BUNDLE-154 -->

![ 新規 ](../assets/new.svg) 会社モジュールで実行された管理者アクションは、管理アクションログに記録されるようになりました。 アクションは、すべての関連する会社モジュール（`Company`、`NegotiableQuote`、`CompanyCredit`、`SharedCatalog`）から記録されます。<!--- BUNDLE-180 181 182 183 -->

![ 修正された問題 ](../assets/fix.svg)B2B がインストールされているデプロイメントで、ログイン管理者がお客様を削除する権限を持っていない場合、Adobe Commerceで **お客様** ページに「**[!UICONTROL Delete customer]**」ボタンが表示されなくなりました。<!--- MC-35655-->

![ 修正された問題 ](../assets/fix.svg) 顧客グリッドで顧客を編集するときに、会社に割り当てられている顧客の顧客グループが自動的に変更されなくなりました。<!--- MC-35254-->

![ 修正された問題 ](../assets/fix.svg) マーチャントが共有カタログを作成すると、カタログ権限設定で顧客グループにこのアクセス権が割り当てられたときに、カテゴリの **[!UICONTROL Display Product Prices]** 機能と **[!UICONTROL Add to Cart]** 機能に対する権限が自動的に `Allow` に設定されるようになりました。 以前は、カタログ権限が `Allow`.<!--- MC-34792--> に設定されている場合でも、これらの設定は自動的に `Deny` に設定されていました

![ 修正された問題 ](../assets/fix.svg) 製品を製品編集ページから編集した際に、共有カタログカテゴリの権限が上書きされなくなりました。<!--- MC-34777-->

![ 修正された問題 ](../assets/fix.svg) マーチャントが **[!UICONTROL Allow To Exceed Credit Limit]** 設定を有効にすると、お客様が指定されたクレジット制限を超える権限を持っていることを確認するメール通知をAdobe Commerceが送信するようになりました。 以前は、Adobe Commerceから送信される通知メールで、お客様が制限を超える権限を持っていないことを示していました。<!--- MC-34584-->

![ 修正された問題 ](../assets/fix.svg) 購買依頼リストの商品価格を囲むHTMLコンテナが、バンドルされた商品の子に対して正しく表示されるようになりました。<!--- MC-36331-->

![ 修正された問題 ](../assets/fix.svg) 多言語デプロイメントで会社を作成する際に、マーチャントが会社のユーザーのメールの送信言語を指定できるようになりました。 以前は、のドロップダウンメニューを使用すると、マーチャントは適切なストア表示を選択できましたが、言語は表示されませんでした。 <!--- MC-35777-->

![ 修正された問題 ](../assets/fix.svg) カスタムの顧客アドレス属性フィールドが、ストアフロントのチェックアウトワークフローで期待どおりに表示されるようになりました。<!--- MC-35607-->

![ 修正された問題 ](../assets/fix.svg) 「B2B 機能の設定」タブが正しく開くようになりました。 <!--- MC-35458--> ゲストは QuickOrder を使用して商品を買い物かごに追加し、商品を正常に削除できるようになりました。 以前は、買い物客が QuickOrder を使用して買い物かごに複数の製品を追加してから、製品を削除しても、製品が削除されませんでした。<!--- MC-35327-->

![ 修正された問題 ](../assets/fix.svg) 状態が **不要** に設定されている場合、`region_id` を指定せずに、REST API PUTを使用して `/V1/company/:companyId` リクエストを更新できるようになりました。 以前は、`region_id` が必須でなくても、指定されていない場合、Adobe Commerceがエラーをスローしていました。<!--- MC-35304-->

![ 修正された問題 ](../assets/fix.svg)REST API （`http://magento.local/rest/V1/company/2`、`2` は会社 ID を表す）を使用して B2B 会社を作成または更新した場合、期待どおりに応答に `applicable_payment_method` または `available_payment_methods` の設定が含まれるようになりました。<!--- MC-35248-->

![ 修正された問題 ](../assets/fix.svg) ストアフロントで購買依頼リストを作成する際に、マーチャントが **Enter****[!UICONTROL Save]** ボタンを使用すると、Adobe Commerceに 404 ページが表示されなくなりました。<!--- MC-35094-->

![ 修正された問題 ](../assets/fix.svg) 新しい製品が公開共有カタログに割り当てられると、カテゴリ権限が変更されなくなりました。 以前は、カテゴリ権限は複製されていました。<!--- MC-34386-->

![ 修正された問題 ](../assets/fix.svg) 会社のメールを更新するために使用される REST API エンドポイントPUT`rest/default/V1/company/{id}` で、大文字と小文字が区別されなくなりました。<!--- MC-34308-->

![ 修正された問題 ](../assets/fix.svg) 報酬モジュールを無効にすると、顧客アカウントの B2B 機能に影響しなくなりました。 以前は、報酬モジュールが無効の場合、会社プロファイル、会社ユーザー、役割と権限という B2B 関連のタブは表示されませんでした。<!--- MC-34191-->

![ 修正された問題 ](../assets/fix.svg) 会社アカウントに変更が加えられた場合、Adobe Commerceでメール通知に正しい送信者名が使用されるようになりました。 以前Adobe Commerceでは、すべてのメールに対して、デフォルトスコープで定義された一般的な連絡先の送信者名を使用していました。<!--- MC-33917-->

![ 修正された問題 ](../assets/fix.svg) 物理製品と仮想製品の両方を含む注文に対して、複数出荷を正常に実装できるようになりました。<!--- MC-33818-->

![ 修正された問題 ](../assets/fix.svg)**[!UICONTROL Access Restriction]** が有効で、**[!UICONTROL Restriction Mode]** が `Sales: Login Only` に設定されている場合、マーチャントは、マイアカウントおよび会社構造ページの _[!UICONTROL Company Users]_セクションから会社ユーザーを作成できるようになりました。 以前は、マーチャントがユーザー `Can not register new customer due to restrictions are enabled` を作成しようとすると、Adobe Commerceがこのエラーをスローしていました。<!--- MC-33608-->

![ 修正された問題 ](../assets/fix.svg) お客様がアカウント情報を保存した際に、Adobe Commerceがお客様のカスタマーグループをデフォルトにリセットしなくなりました。<!--- MC-33554-->

![ 修正された問題 ](../assets/fix.svg) 管理者がアクティブな買い物かごを持つお客様を顧客グループに割り当てた際に、Adobe Commerceが致命的なエラーをスローしなくなりました。<!--- MC-33313-->

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、クイックオーダーおよび購買依頼リストページ用に `addToCart` DataLayer イベントが提供されるようになりました。 <!--- MC-33295-->

![ 修正された問題 ](../assets/fix.svg) 会社に割り当てられた営業担当者に送信される通知メールに、割り当てられた会社ロゴが含まれるようになりました。 以前は、通知メールには、アップロードされた企業ロゴではなく、デフォルトの LUMA ロゴが含まれていました。<!--- MC-33232-->

![ 修正された問題 ](../assets/fix.svg) 購買依頼リストに、リストに追加されたすべてのグループ化製品と数量が含まれるようになりました。 以前は、販売員が商品詳細ページから商品を追加した後に購買依頼リストに移動すると、Adobe Commerceに「`1 product(s) require your attention - Options were updated. Please review available configurations`」というエラーが表示されていました。<!--- MC-32877-->

![ 修正された問題 ](../assets/fix.svg) 共有カタログが有効な場合、`products` クエリが正確な `total_count` フィールドを返すようになりました。<!--- MC-42268-->

![ 修正された問題 ](../assets/fix.svg) オンライン配送方法を無効にした後、会社の設定ページと会社の作成ページが期待どおりに動作するようになりました。 検証が追加され、無効になった出荷モジュールの処理が試行できなくなりました。 以前は、Adobe Commerceには「`Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`」というエラーが表示されていました。<!--- MC-43178-->

![ 修正された問題 ](../assets/fix.svg) 統合テストのメモリ消費が削減されました。これにより、テストのパフォーマンスが向上し、テスト完了に要する時間が短縮されます。<!--- AC-266-->

## B2B v1.2.0

*2020 年 7 月 28 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.0 がサポートされるようになりました。

![ 新規 ](../assets/new.svg) ストアフロントの注文検索。[Divante](https://www.divante.com/) の Marek Mularczyk 氏とコミュニティメンバーの協力により感謝が追加されました。

![ 新規 ](../assets/new.svg) 発注が強化され、書き換えられます。 これらは、Adobe Commerceにデフォルトで含まれるようになりました。

![ 新規 ](../assets/new.svg) 発注承認ルールが実装されました。 これらのルールを使用すると、ユーザーは注文の購入ルールを作成して、発注書ワークフローを制御できます。

![ 新規 ](../assets/new.svg) お客様としてログインがAdobe Commerceにデフォルトで含まれるようになりました。 この機能を使用すると、サイト従業員は、顧客としてログインして表示内容を確認することで、顧客を支援できます。

![ 修正された問題 ](../assets/fix.svg)Elasticsearchを使用した階層型ナビゲーションで、属性の集計が正しく機能するようになりました

![ 問題を修正 ](../assets/fix.svg) 特殊文字による注文の検索が正常に機能するようになりました。

![ 修正された問題 ](../assets/fix.svg) 「**[!UICONTROL Clear All]**」ボタンをクリックすると、フィルターを折りたたむのではなく、すべてのフィルターが展開されるようになりました。

![ 修正された問題 ](../assets/fix.svg) 製品 SKU/名前が注文履歴の検索フィルターの概要に含まれるようになりました。

![ 修正された問題 ](../assets/fix.svg) 並べ替えインジケーターがマイ発注書グリッドに正しく表示されるようになりました。

![ 問題が修正されました ](../assets/fix.svg) 承認、キャンセル、拒否および発注書の各ボタンは 1 回だけクリックできるようになりました。 以前は、このボタンを複数回クリックすることができました。

![ 修正された問題 ](../assets/fix.svg) モバイルデバイスで、発注書の「承認」、「却下」、「キャンセル」および「検証」ボタンが正しくレンダリングされるようになりました。

![ 修正された問題 ](../assets/fix.svg) 以前は、有効期限切れの割引が適用された発注を承認すると、注文が全額に配置され、発注合計が更新されませんでした。 発注書合計が更新され、正しい合計が表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg)2.3.4 で導入された問題では、カスタム拡張属性が顧客アドレスから見積もりアドレスにコピーされません。 この問題は修正されました。

![ 修正された問題 ](../assets/fix.svg)B2B がインストールされている場合、共有カタログにカテゴリを割り当てると、SQL エラーが表示されます。 この問題は修正されました。

![ 修正された問題 ](../assets/fix.svg) 変数タイプの値が正しくないため、管理者は注文に設定可能な製品を追加できませんでした。 オプションのドロップダウンは表示されません。 この機能は正常に動作するようになりました。

![ 修正された問題 ](../assets/fix.svg) 以前、ログインしていないグループのカテゴリ権限を編集する際に、変更を保存するとエラーが発生していました。 この問題は修正されました。

![ 修正された問題 ](../assets/fix.svg) 修正が追加され、ストア管理者が共有カタログにない注文に製品を追加できるようになりました。 以前は、カタログにない項目を追加すると、エラーメッセージが表示されていました。

![ 修正された問題 ](../assets/fix.svg) 以前は、コマンド `php bin/magento indexer:set-dimensions-mode catalog_product_price website` を実行してから共有カタログを作成しようとすると、エラーが発生していました。 この問題は修正されました。

![ 問題を修正 ](../assets/fix.svg) 会社を追加し、デフォルト以外の web サイトに会社管理者を割り当てると、誤ったサイト ID が送信されてエラーが発生していました。 この問題は修正されました。

![ 修正された問題 ](../assets/fix.svg) 以前は、顧客が別の顧客グループに移動された後、_クイックオーダー_ を使用して注文に製品を追加すると、エラーで失敗していました。 この問題は修正されました。

![ 修正された問題 ](../assets/fix.svg) 以前は、B2B の引用で WebAPI を使用してチェックアウトしようとすると、誤った値が API に送信され、エラーが発生していました。 この問題は修正されました。

![ 問題を修正 ](../assets/fix.svg) 以前、API で会社を「アクティブ」に設定すると、エラーが発生していました。 この問題は修正されました。

![ 問題を修正 ](../assets/fix.svg) 不要な `form` タグにより、提案された発送料金を変更した後に Enter キーを押すと、注文ページが自動的に更新されます。 この問題は修正されました。

![ 問題を修正 ](../assets/fix.svg) 以前、カタログページに製品の表示制限を設定し、その制限が製品の合計数より少なかった場合に、エラーが発生していました。 その機能は期待どおりに動作するようになりました。

![ 問題の修正 ](../assets/fix.svg) 以前は、会社の管理者を変更すると、元の管理者アドレスが新しい管理者にコピーされ、2 つのアドレスが付与されていました。 現在は、正しいアドレスのみが追加されています。

![ 問題を修正 ](../assets/fix.svg) 以前は、Git が「許可され、顧客に通知」に設定されている場合に、API を使用して引用項目を保存すると失敗していました。 この API 呼び出しが期待どおりに動作するようになりました。

![ 修正された問題 ](../assets/fix.svg) 固定製品税が見積りの詳細ページに表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg) 以前は、自分の見積もりページの「コメント」タブで添付ファイルをクリックしても、ファイルをダウンロードできませんでした。 この動作は期待どおりに動作するようになりました。

### 既知の問題

- 複数の web サイトをデプロイした環境で B2B 1.2.0 にアップグレードすると、Adobe Commerceで例外がスローされる。 `setup:upgrade` を実行すると、`PurchaseOrder` モジュール `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder` でこのエラーが発生します。 **回避策**:`B2B-716 Add NonTransactionableInterface` インターフェイスを `InitPurchaseOrderSalesSequence` データパッチのホットフィックスにインストールします。このホットフィックスは、`magento.com` の「**マイアカウント**/**ダウンロード**」セクションから利用できるようになりました。
- 発注（PO）が承認される前に割引コードの有効期限が切れた場合、発注には引き続き割引額が表示されますが、発注が承認されると、注文は割引前の合計に配置されます。 **回避策**：この問題の `B2B-709 Purchase Order Discount patch` ホットフィックスをインストールします。このホットフィックスは、`magento.com` の **マイアカウント**/**ダウンロード** セクションから利用できます。
- 発注書を実際の注文に変換する際に、発注書の品目が在庫切れであるか、数量が不十分な場合は、エラーが発生します。 バックオーダーが有効な場合、オーダーは通常どおり処理されます。
