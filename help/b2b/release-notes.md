---
title: '[!DNL Adobe Commerce B2B] リリースノート'
description: リリースの変更点について詳しくは、リリースノート  [!DNL Adobe Commerce B2B]  参照してください。
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: de145205e5fcdcb49ca7626b2666e82af102344f
workflow-type: tm+mt
source-wordcount: '8702'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] リリースノート

B2B 拡張機能のこれらのリリースノートでは、リリースサイクルでAdobeによって追加された追加と修正が取り込まれています。これには、以下が含まれます。

![新規](../assets/new.svg) 新規機能
![固定問題](../assets/fix.svg) 修正点および改善点
![既知の問題](../assets/bug.svg) 既知の問題

>[!NOTE]
>
>利用可能な Adobe Systems Commerce リリースでサポートされている B2B Commerce 拡張機能のバージョンについては、 [製品の可用性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html?lang=ja) を参照してください。

## B2B 1.5.2

*2025年4月8日*

[!BADGE サポート対象]{type=Informative tooltip="サポート"} Adobe Systems Commerce バージョン 2.4.8、2.4.7-p5 および 2.4.6-p10 のセキュリティパッチリリース。Adobe Systems Commerce バージョン 2.4.7 から 2.4.7-p4、2.4.6 から 2.4.6-p9 との互換性

B2B v1.5.2 リリースには、品質の改善とバグ修正が含まれています。

### 会社管理

![ 新規 ](../assets/new.svg)<!-- B2B-4123 --> 管理者は、ストアフロントの会社スイッチャーを使用して、1 つのアカウントから複数の会社を管理できるようになりました。 主なメリットは次のとおりです。

- **シンプルな複数企業管理**：管理者は、1 つのユーザー・アカウントで複数の企業を監視できるため、企業ごとに個別のログインを作成して管理する必要がなくなります。
- **効率的な企業切り替え** – 直感的なインターフェイスにより、管理者は企業間を迅速に切り替えて更新を行うことができ、複数のエンティティを管理する際の生産性が向上します。
- **オペレーションの合理化**：地域のマネージャとビジネス・リーダーは、すべての企業を一元的に管理できるため、意思決定の迅速化とビジネス・オペレーションの円滑化が可能になります。

この機能強化は、B2B 1.5.0 の複数会社メンバーシップ機能に基づいています。この機能により、ユーザーは複数の会社に属することができますが、会社間の管理者アクセスはサポートされませんでした。 会社切り替えボタンを使用すると、適切なアクセス制御と会社固有の表示を維持しながら、管理者アカウントを個別に設定する必要がなくなります。

### 会社

![ 修正された問題 ](../assets/fix.svg)<!-- B2B-4480 --> 買い物かごに商品を入れたまま会社ユーザーとしてログインすると、ゲスト顧客に `No such entity with cartId = ?` しいエラーメッセージが表示される問題を修正しました。

### 譲渡可能見積

![ 修正された問題 ](../assets/fix.svg) B2B v1.5.2 リリースには、交渉可能な引用符に関する次の修正が含まれています。

- &#x200B;<!-- B2B-3252 -->[!UICONTROL Line Item Discount Amount] フィールドで入力が検証され、負の割引値の入力が防止されるようになりました。
- &#x200B;<!-- B2B-3224 -->長い行項目のメモが切り詰められ、B2B のお客様には読みにくいユーザーエクスペリエンスの問題を修正しました。
- &#x200B;<!-- B2B-2865 -->B2B のお客様は、見積りを作成する際に、小数値（1.5 や 2.75 など）を使用して製品数量を指定できるようになりました。

### 見積もりテンプレート

![ 新規 ](../assets/new.svg)<!-- B2B-4104 --> B2B 購入者と販売者が、見積もりテンプレートに外部ドキュメントリンクを添付する新しい機能。 この機能を使用すると、DocuSign や Adobe Sign などのサービスでホストされているドキュメントに引用符で直接リンクでき、既存のファイル添付機能を補完できます。 主なメリットは次のとおりです。

- 重大な契約および契約への直接アクセスによる合理化された共同作業
- 最新のドキュメントに瞬時にアクセスでき、透明性が向上
- ファイルのダウンロードとアップロードの必要性を排除することにより、見積もり交渉を迅速化
- 外部ドキュメントホスティングサービスを使用した柔軟なドキュメント管理

## B2B 1.5.1

*2025 年 2 月 11 日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"} Adobe Commerce バージョン 2.4.7-p4 以降および 2.4.6-p9 以降のセキュリティパッチリリース。
Adobe Commerce バージョン 2.4.8-beta1 から 2.4.8-beta2、2.4.7 から 2.4.7-p3、2.4.6 から 2.4.9-p8 との互換性

B2B v1.5.1 リリースには、品質の改善とバグ修正が含まれています。

### 会社

![ 修正された問題 ](../assets/fix.svg)<!-- B2B-4422 --> 顧客が見積もりの詳細ページで会社を切り替えようとした場合、ある会社のために作成された見積もりを別の会社の価格で注文するために使用できないように、システムは顧客を *アクセス拒否* ページにリダイレクトするようになりました。 以前は、ユーザーは、ある会社の価格で見積もりを作成してから、別の会社に切り替えて、異なる価格で注文することができました。

### 品目割引

![ 修正された問題 ](../assets/fix.svg)<!-- B2B-2938 --> 見積もりの再計算シナリオで発生するパフォーマンスの低下に対処することで、システム効率を向上しました。 以前は、買い物かごの行項目ごとに 2 つの新しいエンティティが追加され、データベースリクエストが顕著に増加し、パフォーマンスが低下する原因となっていました。

### 譲渡可能見積

![ 問題を修正しました ](../assets/fix.svg)<!-- B2B-3820 -->Luma ストアフロントの引用テンプレートページの *[!UICONTROL min/max qty]* フィールドにJavaScriptの検証が適用された場合、UI 要素の位置が維持されるようになりました。 以前は、これらのフィールドにJavaScriptの検証を適用すると、ページ上の他の UI 要素がシフトしていました。

### ショッピングカート

![ 問題を修正 ](../assets/fix.svg)<!-- B2B-4222 --> 複数の会社アカウントを管理するユーザーのショッピングエクスペリエンスを効率化するように設計された、新しい買い物かご管理システムを導入しました。 この新しいシステムは、買い物かごを顧客アカウントではなく個々の会社に関連付けて、次の機能をサポートすることで、買い物体験を合理化し、ワークフローを改善します。

- **企業固有の買い物かご：** – 企業固有の価格と製品オプションをサポートするために、買い物かごが個々の企業にリンクされるようになりました。
- **シームレスな切り替え**：ユーザーは、各企業の買い物かごの内容に影響を与えることなく、異なる企業アカウントを容易に切り替えることができます。
- **コンテキストの整合性** – 買い物かごの詳細はすべて、それぞれの会社のコンテキスト内に残り、一貫性と信頼性の高いショッピングエクスペリエンスを提供します。

## B2B 1.5.0

*2024 年 10 月 30 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート"} Adobe Systems Commerce バージョン 2.4.7-p3+ および 2.4.6-p8+ セキュリティパッチリリース。Adobe Systems Commerce バージョン 2.4.8-beta1、2.4.7 から 2.4.7-p2、2.4.6 から 2.4.6-p7 と互換性があります。

Adobe Systems Commerce B2B バージョン 1.5.0 は PHP 8.3 とも互換性があり、 [GraphQL アプリケーション サーバー](https://experienceleague.adobe.com/ja/docs/commerce-operations/performance-best-practices/concepts/application-server) をサポートしています。

B2B v1.5.0 リリースには、新機能、品質の向上、バグ修正が含まれています。

>[!NOTE]
>
> B2B 1.5.0 リリースで導入された下位互換性のない変更 (BIC) については、「 [後方互換性のない変更](backward-incompatible-changes.md) トピックのハイライトとリファレンス情報を確認してください。

### 会社情報管理

![ 新規 ](../assets/new.svg)**会社管理**<!--B2B-2901--> – マーチャントは、指定された親会社に会社を割り当てることで、Adobe Commerceの会社を階層的な組織として表示および管理できるようになりました。 会社を親に割り当てると、親の会社管理者が会社アカウントを管理できるようになります。 許可された管理者ユーザーのみが、会社の割り当てを追加および管理できます。 詳しくは、[ 会社階層の管理 ](manage-company-hierarchy.md) を参照してください。

- 管理者の *[!UICONTROL Company Account]* ページの新しい「*[!UICONTROL Company Hierarchy]*」セクションで、会社の割り当てを追加および管理します。

- 新しい *[!UICONTROL Company Type]* 設定で会社を並べ替え、フィルタリングします。 会社グリッドの「*[!UICONTROL Company Type]*」列は、会社が個々の会社であるか、組織階層の一部（親または子）であるかを示します。

![ 新規 ](../assets/new.svg)**大規模な会社設定の管理**<!--B2B-2849--> - *[!UICONTROL Companies]* または *[!UICONTROL Company Hierarchy]* グリッドから会社を管理する際に使用できる *[!UICONTROL Change company setting]* の一括アクションを使用して、選択した会社の会社設定をすばやく変更します。 例えば、会社のグループに対して新しい共有カタログを作成した場合、各会社を個別に編集する代わりに、1 回の操作で共有カタログの設定を変更できます。

![ 新規 ](../assets/new.svg) API デベロッパーは、新しい会社関係 REST API エンドポイント `/V1/company/{parentId}/relations` を使用して、会社の割り当てを作成、表示、削除できます。 [Web API 開発者ガイド ](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) の *会社オブジェクトの管理* を参照してください。

### 会社情報アカウント

![新機能](../assets/new.svg)<!--B2B-2828--> **複数会社割り当て** - ユーザーを複数の会社に割り当てることで会社会社ユーザのアカウントアクセスを簡素化します。 たとえば、複数の会社サイトから注文するバイヤーがいる場合は、1 つのアカウントを作成し、バイヤーが協力するすべての会社をそのアカウントに割り当てます。 その後、購入者は一度ログインし、店頭から会社を選択して会社アカウントを切り替えることができます。

>[!NOTE]
>
>会社ユーザーは複数の会社に割り当てることができますが、1 つの会社の会社管理者になることはできません。

![ 新規 ](../assets/new.svg) <!--B2B-2747--> **会社範囲セレクター** – 複数の会社に割り当てられている会社ユーザーがストアフロントで会社を変更できる機能を提供します。 範囲が切り替わると、データが更新され、新しい会社のコンテキストに基づいて情報が表示されます。 例えば、新しい会社が別の共有カタログを使用している場合、会社のユーザーには、新しい共有カタログに基づいて製品、価格、その他の情報が表示されます。 注文、見積もり、見積もりテンプレートに関連するコンテンツも、選択した会社のコンテキストに基づいて更新されます。

>[!NOTE]
>買い物かごの内容には、現在の顧客が選択した項目が反映されます。 アクティブな買い物かごがあり、別の会社を選択している顧客は、新しい会社のコンテキストに基づいて製品の品揃え、価格、プロモーションの割引を反映するように買い物かごを更新するよう促されます。 新しい会社に関連付けられているカタログで利用できない製品は、買い物かごから削除されます。 製品の価格や在庫が異なる場合、買い物かごは更新され、選択した会社のコンテキストで利用可能なデータが反映されます。<!--B2B-4222-->

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1933--> 会社管理者は、ストアフロントから会社ユーザーを追加できるようになりました。 以前は、管理者ユーザーが新しいユーザーを追加しようとすると、Commerceでエラーがログに記録されていました。ユーザー名：`CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`。

### 見積もりテンプレートと見積もりテンプレート

見積機能の改善により、バイヤーとセラーは見積もりと見積ネゴシエーションをより効果的に管理できます。

![ 新規 ](../assets/new.svg) 見積もりテンプレート **&#x200B;**—<!--B2B-3367--> 購入者と販売者は、再利用可能でカスタマイズ可能な見積もりテンプレートを作成することで、見積もりプロセスを合理化できるようになりました。 見積テンプレートを使用すると、見積ネゴシエーション・プロセスを 1 回完了できます。バイヤーは、各受注に対して見積ネゴシエーション・プロセスを実行するのではなく、定型受注に対して事前承認済のリンクされた見積を生成できます。 Quote テンプレートは、次の高度な機能を追加することにより、既存の Quote 機能を拡張します。

- **注文しきい値** 売り手は最小注文と最大注文のコミットメントを設定し、買い手が合意された購入量に従うことを確認できます。
- **最小品目オーダー数量と最大品目オーダー数量の設定** を使用すると、バイヤーは、新規テンプレートや他のネゴシエーションを必要とせずに、リンクされた見積のオーダー数量を柔軟に調整できます。
- **生成され、正常に完了した注文のリンクされた見積もりの数を追跡** して、交渉済の契約の履行に関するインサイトを得ます。
- **リンクされた見積** は、見積テンプレートで交渉された条件に基づいて定型受注を発行するためにバイヤーが有効な見積テンプレートから生成する事前承認済の見積です。

![ 既存 ](../assets/new.svg) 見積もり機能に関する新 **な機能強化**

- **更新されたCommerce アクセス制御リスト（ACL）ルールにより** B2B マネージャーおよびスーパーバイザーは、下位ユーザーの見積もりと見積もりテンプレートを管理できます。 表示、編集および削除アクセスの詳細な設定は、別々のルールでサポートされています。

- **見積もりをドラフトとして保存**<!--B2B-2566--> - 買い物かごから [見積もりリクエスト](quote-request.md) を作成するときに、購入者は見積もりをドラフトとして保存して、販売者との見積もり交渉プロセスを開始する前に見積もりを確認および更新できるようになりました。 ドラフト見積もりには有効期限日付がありません。 購入者は、アカウントダッシュボードの「[!UICONTROL My Quotes]」セクションで、下書きの見積もりを確認および更新できます。

- **Quote の名前を変更**<!--B2B-2596--> - 「**[!UICONTROL Rename]**」オプションを選択して、[Quote detail](account-dashboard-my-quotes.md#quote-actions) ページから Quote 名を変更できるようになりました。 このオプションは、権限を持つ購入者が見積もりを編集する際に使用できます。 名前の変更イベントは Quote History Log に記録されます。

- **見積書の複製**<!--B2B-2701--> - バイヤーとセラーは、既存の見積書をコピーして新しい見積書を作成できるようになりました。 Quote の詳細ビューからコピーを作成するには、管理 **[!UICONTROL Create Copy]** たは [ ストアフロント ](account-dashboard-my-quotes.md#quote-actions) の [&#128279;](quote-price-negotiation.md#button-bar)Quote の詳細ビュー  を選択します。

- **見積品目を購買依頼リストに移動**<!--B2B-2755-->：購買担当は、見積ネゴシエーション・プロセスに製品を含めないことにした場合、見積から製品を削除して購買依頼リストに保存できるようになりました。

- **見積りから複数の製品を削除**<!--B2B-2881--> – 多数の製品がある見積もりについて、バイヤーは複数の製品を選択し、見積りの詳細ページの *[!UICONTROL Actions]* コントロールにある「*[!UICONTROL Remove]*」オプションを使用して、見積りから複数の製品を削除できるようになりました。 以前のリリースでは、買い手は製品を 1 つずつ削除する必要がありました。

- **明細品目値引ロック**<!--B2B-2597--> – 見積ネゴシエーション中に、セラーは明細品目値引ロックを使用して、見積ネゴシエーション・プロセス中に値引を適用する際の柔軟性を高めることができます。 例えば、販売者は、品目に特別品目割引を適用し、品目をロックして、それ以上の割引を防ぐことができます。 品目がロックされている場合、見積レベルの値引が適用される際に品目価格を更新することはできません。 [ 購買担当の見積の開始 ](sales-rep-initiates-quote.md) を参照してください。

![ 修正された問題 ](../assets/fix.svg)**既存の引用機能の修正**

- 管理者が Quote の詳細表示で「*[!UICONTROL Print]*」ボタンをクリックすると、Quote をPDFとして保存するよう促すメッセージが表示されるようになりました。 以前は、マーチャントは見積りの詳細を含むページにリダイレクトされていました。<!--ACP2E-1984-->

- 以前は、割合と数量の変更を含む顧客の見積 `0` を送信すると、管理者は例外をスローしていましたが、数量は保存されていました。 この修正プログラムの適用後、 `0 percentage` メッセージと共に適切な例外がスローされます。 <!--ACP2E-1742-->

- 見積もり交渉中に、販売者は 交渉済み見積もり見積もり割引 フィールドで `0%` 割引を指定し、見積もりを購入者に返送できるようになりました。 以前は、販売者が 0% の割引を入力して見積もりを購入者に返送した場合、管理者は `Exception occurred during quote sending` エラーメッセージを返していました。 <!--ACP2E-1742-->

- ReCaptcha V3 がストアフロントのチェックアウト用に設定されている場合、B2B 見積のチェックアウトプロセス中に ReCaptcha 検証が正しく機能するようになりました。 以前は、 `recaptcha validation failed, please try again` エラーメッセージを表示して検証が失敗していました。  <!--ACP2E-2097-->

### 発注書

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1825--> 会社がブロックされると、会社に関連付けられているユーザーは発注書を送信できなくなります。 以前は、会社がブロックされている場合、会社に関連付けられているユーザーが発注書を送信することができました。

## B2B v1.4.2-p5

*2025 年 4 月 8 日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"}Adobe Commerce 2.4.7-p5 以降および 2.4.6-p10 以降のセキュリティパッチリリース。

![ 新規 ](../assets/new.svg) Adobe Commerce 2.4.7-p5 以降および 2.4.6-p10 以降のセキュリティパッチリリースとの互換性が追加されました。

![固定 問題](../assets/fix.svg) [セキュリティ情報 APSB25-26](https://helpx.adobe.com/jp/security/products/magento/apsb25-26.html) に記載されているセキュリティ修正が含まれています。

{{b2b-compatibility}}

## B2B v1.4.2-p4

*2025年2月11日*

[!BADGE サポート対象]{type=Informative tooltip="サポート"} Adobe Systems Commerce 2.4.7-p4+ および 2.4.6-p9+ セキュリティパッチリリース。

![新規](../assets/new.svg) Adobe Systems Commerce 2.4.7-p4+ および 2.4.6-p9+ セキュリティパッチリリースとの互換性を追加しました。

![ 修正された問題 ](../assets/fix.svg) [ セキュリティ速報 APSB25-08](https://helpx.adobe.com/jp/security/products/magento/apsb25-08.html) に記載されているセキュリティ修正が含まれます。

{{b2b-compatibility}}

## B2B v1.4.2-p3

*2024 年 10 月 8 日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"}Adobe Commerce 2.4.7-p3 以降および 2.4.6-p8 以降のセキュリティパッチリリース。

![ 新規 ](../assets/new.svg) Adobe Commerce 2.4.7-p3 以降および 2.4.6-p8 以降のセキュリティパッチリリースとの互換性が追加されました。

![ 修正された問題 ](../assets/fix.svg) [ セキュリティ速報 APSB24-73](https://helpx.adobe.com/jp/security/products/magento/apsb24-73.html) に記載されているセキュリティ修正が含まれます。

{{b2b-compatibility}}

## B2B v1.4.2-p2

[!BADGE サポート対象]{type=Informative tooltip="サポート"} Adobe Systems Commerce 2.4.7-p2+ および 2.4.6-p7+ セキュリティパッチリリース。

![新規](../assets/new.svg) Adobe Systems Commerce 2.4.7-p2+ および 2.4.6-p7+ セキュリティパッチリリースとの互換性を追加しました。

![問題固定](../assets/fix.svg) セキュリティ情報 xxxx に記載されているセキュリティ修正が含まれています。

{{b2b-compatibility}}

## B2B v1.4.2-p1

*2024年8月9日*

[!BADGE サポート対象]{type=Informative tooltip="サポート"} Adobe Systems Commerce 2.4.7-p1+ および 2.4.6-p6+ セキュリティパッチリリース。

![新規](../assets/new.svg) Adobe Systems Commerce 2.4.7-p1+ および 2.4.6-p6+ セキュリティパッチリリースとの互換性を追加しました。

{{b2b-compatibility}}

## B2B v1.4.2

*2023 年 10 月 10 日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"} Adobe Commerce バージョン 2.4.7 および 2.4.6 から 2.4.6-p5 へのバージョン。

B2B v1.4.2 リリースには、品質の改善とバグ修正が含まれています。

![ 修正された問題 ](../assets/fix.svg)<!--B2B-2897--> 販売者が購入者の会社に関連付けられた共有カタログで使用できない製品 SKU を含む購入者見積を作成すると、エラーメッセージ `The SKU you entered is not available in the shared catalog. Please check the SKU and try again` が表示されます。  販売者は、利用できない製品を削除するまで見積もりを保存できません。 以前は、使用できない SKU を含んだ見積もりが保存され、ストアフロントに見積もりが読み込まれませんでした。

>[!IMPORTANT]
>
>Adobe Commerce B2B バージョン 1.4.2 以降は、PHP 8.2 と互換性があります。Commerce インスタンスをバージョン 2.4.7 以降にアップグレードする場合は、インスタンスが PHP バージョン 8.2 を使用してAdobe Commerce B2B リリースとの互換性を保っていることを確認します。 さらに、B2B 1.4.2 以降では、現在、[GraphQL Application Server](https://experienceleague.adobe.com/ja/docs/commerce-operations/performance-best-practices/concepts/application-server) をサポートしていません。

## B2B v1.4.1

*2023 年 8 月 7 日*

[!BADGE &#x200B; サポート &#x200B;]{type=Informative tooltip="サポート"} [Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=ja)。 Adobe Commerce 2.4.7-beta1 と互換性あり。

B2B v1.4.1 リリースには、品質の改善とバグ修正が含まれています。

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1825--> 会社がブロックされると、会社に関連付けられているユーザーは発注書を送信できなくなります。 以前は、会社がブロックされている場合、会社に関連付けられているユーザーが発注書を送信することができました。

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1943--> 製品のバックオーダーのステータスがストアフロントに正しく表示されるようになりました。 以前は、出荷可能な製品が誤ってバックオーダーと識別されていました。

![ 問題を修正 ](../assets/fix.svg)<!--ACP2E-1862--> 会社登録フォームに顧客ファイルタイプ属性が含まれている場合、登録プロセス中にアップロードされたファイルは、会社を作成した後、会社管理者のアカウント情報に含まれるようになりました。 以前は、添付ファイルが見つかりませんでした。

![固定問題](../assets/fix.svg) <!--ACP2E-1793-->コンフィギュレーション可能製品のスウォッチセレクターが、要求リスト品目コンフィギュレーション ページに期待どおりに表示されるようになりました。 以前は、スウォッチセレクターは購買依頼リスト項目設定ページのドロップダウンフィールドとして表示されていました。

![固定問題](../assets/fix.svg) <!--ACP2E-1968-->[会社情報 GraphQL クエリ](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure)を使用して会社の詳細を返すと、結果がエラーなしで正常に返されるようになりました。

## B2B v1.4.0

*2023 年 6 月 13 日*

[!BADGE &#x200B; サポート &#x200B;]{type=Informative tooltip="サポート"} [Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=ja)。 Adobe Commerce 2.4.7-beta1 との互換性

このリリースには、B2B の交渉可能な引用符と複数のバグ修正に関する新機能と機能強化が含まれています。

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.7-beta1 との互換性が追加されました。

![ 新規 ](../assets/new.svg)**売り手が見積もりを開始** – 売り手は、管理の見積もりグリッドおよび顧客グリッドから直接買い手の見積もりを開始できるようになりました。 この機能により、見積もりプロセスが合理化され、お客様の複雑さが軽減されます。 顧客が注文を開始していない場合、売り手は顧客に代わって見積もりをすばやく作成し、交渉プロセス開始できます。 以前は、見積もりは、購入者、または顧客としてログインした販売者のみがストアフロントから作成できました。

![ 新規 ](../assets/new.svg)**明細品目値引およびネゴシエーション**—<!--B2B-2440--> 見積内で、B2B バイヤーおよびセラーは、明細品目レベルで値引および手形の交換を交渉して、基本契約に達するまで交渉できるようになりました。 メモの作成と更新は、明細品目と見積履歴に含まれ、通信を追跡します。 以前は、購入者と販売者は、メモを交換したり、見積もりレベルで割引を適用したりすることしかできませんでした。

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、「発注書」オプションが有効になっており、PayPal 支払いオプションを使用して作成されたバーチャル見積もりが選択されている場合、支払い中に正しい詳細が表示されるようになりました。 以前は、これらの条件の下で合計はゼロとして表示されていました。

![固定問題](../assets/fix.svg) <!--ACP2E-1504--> 与信限度額が 999 を超える会社を保存しようとしたときに検証エラーが発生しなくなりました。 以前は、999 を超える会社与信限度額の場合、Adobe Systems コマースではコンマ区切り記号が挿入されていたため、検証エラーが発生して更新が保存されませんでした。

![固定問題](../assets/fix.svg) <!--ACP2E-1474-->  交渉可能な見積もりで注文しても、選択した配送先住所は変更されません。 以前は、注文時に選択した配送先住所がデフォルトの配送先住所に変更されていました。

![ 修正された問題 ](../assets/fix.svg) <!--ACP2E-1429--> B2B 機能のストア設定で、「**[!UICONTROL Enable Shared Catalog direct products price assigning]**」フィールドが自動的に無効になりました。 ストアフロントでは、 **[!UICONTROL Enable Company]** 設定または **[!UICONTROL Enable Shared Catalog]** 設定が **[!UICONTROL No]** に設定されている場合に非表示されます。

![ 修正された問題 ](../assets/fix.svg) <!--ACP2E-1683--> ストアフロントから会社アカウントを作成する際に、Commerceは、会社登録を処理する前にメールアドレスを検証するようになりました。 If the email address is invalid, the operation fails and no account updates are processed. Previously, a customer account was created even if the request to create a company account failed because of an invalid email address.

![ 修正された問題 ](../assets/fix.svg)<!--ACP2E-1664--> 共有カタログと価格構造に二重引用符を含む製品 SKU で、管理者でエラーが発生しなくなりました。

![ 修正された問題 ](../assets/fix.svg) <!--ACP2E-1498--> Commerce アプリケーションの Varnish 設定を更新して、ゲストユーザーが他のお客様グループからのデータを表示できないようにしました。

### 既知の問題

[Adobe Systems Commerce バージョン 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=ja) に B2B 1.4.0 をインストールまたはアップグレードすると、次のエラーが発生します。

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

この問題は、 [安定性 タグ](https://getcomposer.org/doc/04-schema.md#package-links) を使用して B2B セキュリティ パッケージの手動依存関係を追加することで、B2B セキュリティ パッケージの手動依存関係を追加することで修正できます。 手順については、 [Adobe Systems コマース ナレッジ ベース](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html?lang=ja) を参照してください。

## B2B v1.3.5-p10

*2025年4月8日*

[!BADGE サポート対象]{type=Informative tooltip="サポート"} Adobe Systems Commerce 2.4.6-p10+ セキュリティパッチリリース。

![新規](../assets/new.svg) Adobe Systems Commerce 2.4.6-p10 セキュリティパッチリリースとの互換性を追加しました。

![ 修正された問題 ](../assets/fix.svg) [ セキュリティ速報 APSB25-26](https://helpx.adobe.com/jp/security/products/magento/apsb25-26.html) に記載されているセキュリティ修正が含まれます。

## B2B v1.3.5-p9

*2025 年 2 月 11 日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"} Adobe Commerce 2.4.6-p9+ セキュリティパッチリリース。

![新規](../assets/new.svg) Adobe Systems Commerce 2.4.6-p9 セキュリティパッチリリースとの互換性を追加しました。

![ 修正された問題 ](../assets/fix.svg) [ セキュリティ速報 APSB25-08](https://helpx.adobe.com/jp/security/products/magento/apsb25-08.html) に記載されているセキュリティ修正が含まれます。

## B2B v1.3.5-p8

*2024年10月8日*

[!BADGE サポート対象]{type=Informative tooltip="サポート"} Adobe Systems Commerce 2.4.6-p8+ セキュリティパッチリリース。

![新規](../assets/new.svg) Adobe Systems Commerce 2.4.6-p8 セキュリティパッチリリースとの互換性を追加しました。

![固定の問題](../assets/fix.svg) [セキュリティ情報 APSB24-73](https://helpx.adobe.com/jp/security/products/magento/apsb24-73.html) に記載されているセキュリティ修正が含まれています。

## B2B v1.3.5-p7

*2024年8月9日*

[!BADGE サポート対象]{type=Informative tooltip="サポート"} Adobe Systems Commerce 2.4.6-p7+ セキュリティパッチリリース。

![ 新規 ](../assets/new.svg) Adobe Commerce 2.4.6-p7 セキュリティパッチリリースとの互換性が追加されました。

## B2B v1.3.5

*2023 年 3 月 14 日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"} Adobe Commerce 2.4.0 ～ 2.4.6 以降

![ 新規 ](../assets/new.svg) Adobe Commerce 2.4.6-p2 との互換性をサポートするために、B2B バージョン 1.3.5-p2 をリリースしました。

![ 新規 ](../assets/new.svg) Adobe Commerce 2.4.6-p1 との互換性をサポートするために、B2B バージョン 1.3.5-p1 をリリースしました。

>[!NOTE]
>
>Commerceを 2.4.6 から [ 最新リリース ](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=ja#2.4.6) にアップグレードした後、必ずサポートされている B2B 1.3.5 パッチリリースに更新してください。 または、B2B 拡張機能をバージョン 1.3.5 からバージョン 1.4.0 以降にアップグレードして、最新機能を取得します。

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

## B2B v1.3.4-p12

*2025 年 4 月 8 日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"}Adobe Commerce 2.4.0 以降のバージョン

![New](../assets/new.svg) Added support for Adobe Commerce 2.4.5-p12.

![固定 問題](../assets/fix.svg) [セキュリティ情報 APSB25-26](https://helpx.adobe.com/jp/security/products/magento/apsb25-26.html) に記載されているセキュリティ修正が含まれています。

## B2B v1.3.4-p11

*2025 年 2 月 11 日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"}Adobe Commerce 2.4.0 以降のバージョン

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.5-p11 がサポートされるようになりました。

![固定問題](../assets/fix.svg) [セキュリティ情報 APSB25-08](https://helpx.adobe.com/jp/security/products/magento/apsb25-08.html) に記載されているセキュリティ修正が含まれています。

## B2B v1.3.4-p10

*2024年10月9日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"}Adobe Commerce 2.4.0 以降のバージョン

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.5-p10 がサポートされるようになりました。

![ 修正された問題 ](../assets/fix.svg) [ セキュリティ速報 APSB24-73](https://helpx.adobe.com/jp/security/products/magento/apsb24-73.html) に記載されているセキュリティ修正が含まれます。

## B2B v1.3.4

*2022 年 8 月 9 日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"}Adobe Commerce 2.4.0 以降のバージョン

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.5 がサポートされるようになりました。

![問題固定](../assets/fix.svg) <!--- ACP2E-453-->Adobe Systems Commerce は、既存の会社情報が API 呼び出しによって更新されるたびに電子メール通知を送信しなくなりました。 電子メールは、会社が作成されたときにのみ送信されるようになりました。

![問題](../assets/fix.svg) <!--- ACP2E-406-->Adobe Systemsコマース固定、 **[!UICONTROL Enable Cross Border Trade]** 税計算設定が有効になっている場合、交渉可能な見積もりの総計が正しく計算されるようになりました。

![固定問題](../assets/fix.svg) <!--- ACP2E-322-->**[!UICONTROL Move out of stock to the bottom]**&#x200B;設定が有効になっている場合、在庫が更新された後、コンフィギュレーション可能な製品が製品リストの最後の位置に移動されるようになりました。新しいカスタム データベース クエリが実装され、Elasticsearch インデックスの並べ替え順序で管理者が有効な並べ替え順序に従うようになりました。 以前は、この設定が有効になっている場合、コンフィギュレーション可能製品とその子製品はリストの下部に移動されませんでした。

![問題固定](../assets/fix.svg) <!--- ACP2E-308-->購入 注文メールがマルチサイト デプロイメントの各 Web サイトのメール送信設定を順守するようになりました。 **[!UICONTROL Disable Email Communications]**&#x200B;設定のチェックが、電子メールキューのカスタムロジックに追加されます。以前は、Adobe Commerceは、セカンダリ web サイトのメール送信設定を受け入れませんでした。

![ 修正された問題 ](../assets/fix.svg)<!--- ACP2E-302--> クイックオーダーページの SKU フィールドのタイトルが、わかりやすくするために変更されました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-543--> 買い物客が「SKU または商品名を入力 **フィールドに無効な SKU を入力すると、Adobe Commerceにエラーメッセージが表示され** ようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-1753--> 会社管理者の **[!UICONTROL Account Created in]** フィールドに、会社を保存した後も期待どおりの値が保持されるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-722 -->`uid` でフィルタリングされた購買依頼リストを取得する際に、`customer` クエリが空の結果を返さなくなりました。

![ 問題を修正 ](../assets/fix.svg)<!--- ACP2E-210 --> ストアクレジットが 1 回だけ適用されるように、`collectQuoteTotals` 呼び出しの前にプラグインを追加しました。

![ 修正された問題 ](../assets/fix.svg)<!--- ACP2E-665 --> 管理者が管理者からアカウントを削除すると、ユーザーはログインページにリダイレクトされるようになりました。 以前は、Adobe Commerceがエラーをスローしていました。 プラグイン（`SessionPlugin`）のコードブロックは、`try…catch` ブロック内に配置されています。 以前は、このコードは汎用例外処理ブロック内にラップされていませんでした。

![固定問題](../assets/fix.svg) <!--- ACP2E-661 --> モバイルモードのクイックオーダーページで、有効な製品名またはSKUを入力した後に **Enter** を押すと、買い物客が期待どおりに次のフィールドに移動するようになりました。

![issue](../assets/fix.svg) <!--- ACP2E-607 -->会社情報固定チェックアウト ワークフローの [請求] セクションと [配送先住所] セクションに期待どおりに名前が表示されるようになりました。

![問題固定](../assets/fix.svg) <!--- ACP2E-375 -->**[!UICONTROL Zero Subtotal Checkout]**&#x200B;支払い方法が無効になっている場合、ストアクレジットが利用できなくなる。以前は、[ストアクレジット] チェックボックスは、管理者からの注文配置中に機能しませんでした。 アプリケーションはストアクレジットで注文を行わず、次のエラーを表示しました: `The requested Payment Method is not available`。

## B2B v1.3.3

*2022年8月9日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"}Adobe Commerce 2.4.0 以降のバージョン

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.4 がサポートされるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41985--> 会社の役割が 10 万件を超えるデプロイメントでAdobe Commerce 2.3.x からAdobe Commerce 2.4.x にアップグレードするのに必要な時間が大幅に短縮されました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-42153--> POST `V1/order/:orderId/invoice` リクエストで、**[!UICONTROL Payment on Account]** 支払い方法が有効な場合に部分請求書の作成がサポートされるようになりました。 以前は、Adobe Commerceは次のエラーをスローしていました：`An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`。 [GitHub-32428](https://github.com/magento/magento2/issues/32428)

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

![固定問題](../assets/fix.svg) <!--- MC-42399--> `rest/V1/company/{id}` リクエスト が期待どおりに `is_purchase_order_enabled` 属性値を返すようになりました。

![固定問題](../assets/fix.svg) <!--- ACP2E-128--> 特例文字顧客属性が _会社情報 Admin_ タブに期待どおりに表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-130--> マイアカウント ページのマイウィッシュリスト ブロックが、会社管理者および会社ユーザーに対して期待どおりに表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-133--> クイックオーダーエラーが買い物かごに表示されなくなりました。 以前は、カタログに SKU が見つからなかった場合、Adobe Commerceによって買い物かごにこのエラーが表示されていました：`The SKU was not found in the catalog`。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-194--> 共有カタログの保存操作が、より高速に実行されるように最適化されました。 以前は、多くの顧客グループを含む共有カタログの保存に数分かかることがありました。

![問題固定](../assets/fix.svg) <!--- MC-42240--> Adobe Systems Commerce は、親カテゴリが削除されたときに、 `sharedcatalog_category_permissions` テーブルからすべてのサブカテゴリ権限を削除するようになりました。 以前は、親カテゴリデータのみが削除されていました。

## B2B v1.3.2

*2022年8月29日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"}Adobe Commerce 2.4.0 以降のバージョン

![New](../assets/new.svg) Added support for Adobe Commerce 2.4.3.

![Fixed issue](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce now successfully sends update emails about expired negotiable quotes. Previously, when a negotiable quote expired, Adobe Commerce did not send update emails.

![Fixed issue](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce now successfully sends update emails about soon to expire and expired negotiable quotes when a `cron` job is missing.

### 会社

![固定問題](../assets/fix.svg) <!--- MC-41542--> [新規作成 会社情報アカウントページ国のドロップダウン] フィールドに空のオプション値が一覧表示されなくなりました。 以前は、最初の 2 つのオプション値と国コード `AN` は空でした。

![固定問題](../assets/fix.svg) <!--- MC-41260--> 会社 ユーザーによって作成された注文の **[!UICONTROL Return]** ボタンをクリックすると、管理ユーザーが期待どおりに 作成 Return ページにリダイレクトされるようになりました。 以前は、管理者は注文ヒストリーページにリダイレクトされていました。

![固定問題](../assets/fix.svg) <!--- MC-40798-->`bin/magento setup:upgrade`中に `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` メソッドを実行する際に、Adobe Systems Commerce がメモリ不足エラーで失敗しなくなりました。以前は、Adobe Systems Commerce はアクセス許可を初期化するときに コレクション にバッチ サイズを使用せず、代わりにすべての会社ロールのコレクションをロードしていました。

![固定問題](../assets/fix.svg) <!--- MC-40551--> 会社情報ユーザーが顧客カスタム属性値を編集および更新できるようになりました。 以前は、これらの属性はフォームの作成と編集ユーザー正常にバインドされていませんでした。 会社ユーザーは異なる属性値を入力できましたが、Adobe Systems Commerce はこれらの値を正しく保存しませんでした。

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

![ 修正された問題 ](../assets/fix.svg)<!--- MC-40426--> マーチャントは、POST `rest/all/V1/requisition_lists` エンドポイントを使用して、顧客用の購買依頼リストを作成できるようになりました。 以前は、Adobe Commerceが購買依頼リストを作成しようとした際に、次の 400 エラーがスローされていました。`Could not save Requisition List`

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41123--> 買い物かごに在庫切れの商品も含まれている場合、買い物かごの在庫商品に「**[!UICONTROL Add to Requisition List]**」ボタンが表示されるようになりました。 以前は、1 つの買い物かごに 2 つの製品が含まれ、そのうち 1 つが在庫切れの場合、どちらの製品にも「_[!UICONTROL Add to Requisition List]_」ボタンが表示されませんでした。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-40877--> REST API を使用して、製品を購買依頼リストに追加できるようになりました。

![ 修正された問題 ](../assets/fix.svg) 購買依頼リスト <!--- MC-40155--> 値 **[!UICONTROL Latest Activity Date]** ロケール形式に準拠するようになりました。

![ 修正された問題 ](../assets/fix.svg)<!--- MC-39580-->Adobe Commerceで、購買依頼リストからバンドル商品を編集する際に致命的なエラーがスローされなくなりました。

![ 修正された問題 ](../assets/fix.svg)Adobe Commerce<!--- MC-40454-->、カスタマイズ可能なオプションを `(File)` つ商品を購買依頼リストからウィッシュリストに追加すると、正しい商品価格が表示されるようになりました。 アップロードしたファイルへのリンクも、期待どおりに表示されます。 以前は、Adobe Commerceで誤った製品価格が表示され、ファイルへのリンクが表示されていませんでした。

![ 問題を修正 ](../assets/fix.svg) <!--- MC-36383--> カスタマイズ可能なオプションを備え `(File)` 製品を、購買依頼リストから買い物かごに追加できるようになりました。

### 共有カタログ

![固定問題](../assets/fix.svg) <!--- MC-40497--> 特定の Web サイトに限定された役割を持つ管理者は、共有カタログを作成、表示、および編集できるようになりました。 以前は、Adobe Systems Commerce は、制限付き役割を持つ管理者が共有カタログを作成しようとすると致命的なエラーをスローしていました。

![ 修正された問題 ](../assets/fix.svg) <!--- MC-41337--> レイヤードナビゲーションの結果に、フィルタリングされた属性を持つ製品の正確な数が含まれるようになり、買い物客は複数のフィルターを適用できるようになりました。 以前は、1 つのフィルターのみを適用できましたが、Adobe Commerceのレイヤーナビゲーションで、不正確な製品数が表示されていました。

![ 修正された問題 ](../assets/fix.svg) Adobe Commerce<!--- MC-40779-->、検索結果のレイヤー化されたナビゲーションフィルターに製品数を正しく表示するようになりました。 以前は、検索結果ページのプラグインはElasticsearchを使用せずに、データベースに新しいクエリを発行していました。

![問題固定](../assets/fix.svg) <!--- MC-39978--> マーチャントがデフォルトの共有カタログからすべての商品を削除しても、Adobe Systems Commerce は階層価格を削除しなくなりました。

![固定問題](../assets/fix.svg) <!--- MC-39802--> 共有カタログが有効になっている場合、フィルターは現在のカテゴリでフィルタリングされ、すべてのページに正しく表示されるようになりました。 以前は、フィルターは現在のページに対してのみ誤って計算され、現在のカテゴリでフィルタリングされませんでした。

![固定問題](../assets/fix.svg) <!--- MC-39522--> 共有カタログが有効になっている場合、GraphQL `products` クエリ共有カタログに割り当てられていない製品の製品の価格帯とカテゴリを返さなくなりました。 以前は、クエリは製品の集計を返していましたが、製品自体は `items` 配列に返されませんでした均等。

## B2B v1.3.1

*2021 年 2 月 9 日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"}Adobe Commerce 2.4.0 以降のバージョン

![New](../assets/new.svg) Added support for Adobe Commerce 2.4.2.

![New](../assets/new.svg) Online payment methods are now supported for purchase orders.

![ 修正された問題 ](../assets/fix.svg) この製品を以前の注文で使用した際に、購買依頼リストから直接買い物かごに設定可能な製品を追加しても、システムエラーが返されなくなりました。

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、分割データベース設定がデプロイされた際に、発注書に対して「自分の承認が必要」タブが正しく表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、発注書を表示する際に、バンドル商品とギフトカードに関する詳細が表示されるようになりました。

![ 修正された問題 ](../assets/fix.svg) 買い物客は、**[!UICONTROL Website Restriction]** が有効で、**[!UICONTROL Restriction Mode]** が `Private Sales: Login Only` に設定されているストアで閲覧している間、自分のアカウントにログインした後、期待どおりにリダイレクトされるようになりました。 Previously, shoppers were redirected to the store home page. <!--- MC-38934-->

![Fixed issue](../assets/fix.svg) Order history now loads as expected in a company administrator&#39;s account dashboard page in deployments with a B2B company hierarchy that contains many customers (greater than 13000). Previously, order history loaded slowly or not at all, and Adobe Commerce displayed a 503 error. <!--- MC-38830-->

![ 修正された問題 ](../assets/fix.svg) カテゴリ ページから購買依頼リストにカスタマイズ可能なオプションを含む未設定製品を追加すると、Adobe Commerceで複数の同一の警告メッセージが表示されなくなりました。<!--- MC-38342-->

![ 修正された問題 ](../assets/fix.svg) B2B の共有カタログが有効な場合、新しい製品や重複した製品がカテゴリページで期待どおりに表示されるようになりました。<!--- MC-38307-->

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、会社の顧客グループが更新された際に、会社管理者に関連付けられた正しい `store_id` を保持するようになりました。 以前は、グループが更新されると、`store_id` がデフォルトのストアに変更されていました。<!--- MC-38196-->

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceは、グループ化された商品を買い物かごに追加する場合と同じ方法で、グループ化された商品をシンプルな商品のリストとして購買依頼リストに保存するようになりました。 以前は、Adobe Commerceによるグループ化された商品の保存方法により、購買依頼リストからのグループ化された商品のリンクは、グループ化された商品ではなく、常にシンプルな商品にリダイレクトされていました。<!--- MC-38049-->

![ 修正された問題 ](../assets/fix.svg) 注文情報を CSV 形式で書き出す際に、**[!UICONTROL Company Name]** フィールドで注文をフィルタリングできるようになりました。 以前は、Adobe Commerceは `var/export/{file-id}` にエラーを記録していました。<!--- MC-37785-->

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、ストアフロントで「新規購買依頼リストの作成」タブを選択すると、「購買依頼リストの作成」ポップアップが期待どおりに表示されるようになりました。<!--- MC-37915-->

![ 修正された問題 ](../assets/fix.svg) 購買依頼リストに、リストに追加されたすべてのグループ化製品と数量が含まれるようになりました。 以前は、販売員が商品詳細ページから商品を追加した後に購買依頼リストに移動すると、Adobe Commerceに「`1 product(s) require your attention - Options were updated. Please review available configurations`」というエラーが表示されていました。<!--- MC-37621-->

![ 修正された問題 ](../assets/fix.svg) マルチサイトデプロイメントで会社を作成する際に、正しいストア表示が関連する web サイトに関連付けられるようになりました。 Previously, you could not create a company, and Adobe Commerce displayed this error: `The store view is not in the associated website`. <!--- MC-37488-->

![ 修正された問題 ](../assets/fix.svg) クイックオーダーを使用して SKU 別に製品を並べ替えても、CSV ファイルで製品数量が重複しなくなりました。<!--- MC-37427-->

![ 修正された問題 ](../assets/fix.svg) クイックオーダーページの _[!UICONTROL Enter Multiple SKUs]_&#x200B;セクションに空の値が含まれている場合、「**[!UICONTROL Add to Cart]**」ボタンがブロックされなくなりました。 代わりに、Adobe Commerceに有効な SKU を入力するように求めるメッセージが表示されるようになりました。<!--- MC-37387-->

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

- 特定の支払い方法に対する割引は、購入者が最終チェックアウト中に支払い方法を変更した場合でも、発注書のチェックアウト中に保持されます。 その結果、お客様は権利のない割引を受けることができます。 この問題は、支払方法が変更されても、元の支払方法の買い物かごルールが引き続き適用されるために発生します。 **_回避策_**：なし。 詳しくは、[Adobe Commerce 2.4.2 B2B の既知の問題：お支払い方法が変更された後、オンライン発注書に対する割引が残ります ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html?lang=ja)_ナレッジベース_ に関する記事を参照してください。<!-- B2B-1012 -->

- `deleteRequisitionListOutput` の問合せでは、残りの購買依頼リストではなく、削除された購買依頼リストに関する詳細が戻されます。<!--- MC-39894-->

## B2B v1.3.0

*2020 年 10 月 15 日*

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"}Adobe Commerce 2.4.0 以降のバージョン

このリリースには、注文承認、発送方法、買い物かご、管理者アクションのログ記録などの改善が含まれています。

![New](../assets/new.svg) Added support for Adobe Commerce 2.4.1.

![新規](../assets/new.svg) B2B注文の承認が強化され、使いやすさが向上し、発注書に対する一括アクションが可能になりました。

![新規](../assets/new.svg) B2Bマーチャントは、各会社情報に提供される配送方法を制御できるようになりました。<!--- BUNDLE-160 161 162 -->

![ 新規 ](../assets/new.svg) マーチャントは、ユーザーが 1 回のアクションで買い物かごの内容をクリアでき、この機能を web サイトの <!--- BUNDLE-108 --> ージごとに独立して設定できるようになりました

![ 新規 ](../assets/new.svg) B2B 購入者は、個々の商品または買い物かごの内容全体を購買依頼リストに直接追加できるようになりました。<!--- BUNDLE-145 144-->

![新規](../assets/new.svg) B2B販売者は、支払い方法としてアカウントの支払いを使用して、顧客に代わって管理者から注文を作成できます。 <!--- BUNDLE-166 178-->

![新規](../assets/new.svg) マーチャントは、顧客の詳細ページからユーザーに関連付けられているすべての見積もりを直接表示できるようになりました。 <!--- BUNDLE-139 -->

![新規](../assets/new.svg) マーチャントは [今すぐオンラインの顧客] グリッドを会社情報でフィルター処理できるようになりました。 <!--- BUNDLE-137 -->

![新規](../assets/new.svg) 管理者は、営業担当者によって管理内の顧客をフィルタできるようになりました。 <!--- BUNDLE-110 -->

![新規](../assets/new.svg) 不正なアカウントやスパムアカウントの作成を減らすために、マーチャントはストアフロントの新規会社情報リクエストフォームでGoogleのreCAPTCHAを有効にできるようになりました。 <!--- BUNDLE-154 -->

![新規](../assets/new.svg) 会社情報モジュールで実行された管理者アクションが管理アクションログに記録されるようになりました。 アクションは、関連するすべての 会社 モジュール( `Company`、 `NegotiableQuote`、 `CompanyCredit`、 `SharedCatalog`)からログに記録されます。  <!--- BUNDLE-180 181 182 183 -->

![問題固定](../assets/fix.svg)ログインした管理者が B2B がインストールされている展開で顧客を削除する権限を持っていない場合、Adobe Systems Commerce は **顧客** ページに&#x200B;**[!UICONTROL Delete customer]**&#x200B;ボタンを表示しなくなりました。<!--- MC-35655-->

![問題固定](../assets/fix.svg) 顧客グリッドで顧客を編集するときに、会社情報に割り当てられている顧客の顧客グループが自動的に変更されなくなりました。 <!--- MC-35254-->

![固定問題](../assets/fix.svg)マーチャントが共有カタログを作成すると、カタログ権限設定で顧客グループにこのアクセス権が割り当てられると、カテゴリ内の&#x200B;**[!UICONTROL Display Product Prices]**&#x200B;および&#x200B;**[!UICONTROL Add to Cart]**&#x200B;機能に対して権限が自動的に`Allow`設定されるようになりました。以前は、これらの設定は、カタログ権限が `Allow` に設定されている場合、`Deny`均等に自動的に設定されていました。<!--- MC-34792-->

![ 修正された問題 ](../assets/fix.svg) 製品を製品編集ページから編集した際に、共有カタログカテゴリの権限が上書きされなくなりました。<!--- MC-34777-->

![ 修正された問題 ](../assets/fix.svg) マーチャントが **[!UICONTROL Allow To Exceed Credit Limit]** 設定を有効にすると、お客様が指定されたクレジット制限を超える権限を持っていることを確認するメール通知をAdobe Commerceが送信するようになりました。 以前は、Adobe Commerceから送信される通知メールで、お客様が制限を超える権限を持っていないことを示していました。<!--- MC-34584-->

![Fixed issue](../assets/fix.svg) The HTML container that surrounds product price on requisition lists is now rendered correctly for the children of bundled products. <!--- MC-36331-->

![Fixed issue](../assets/fix.svg) Merchants can now designate the language in which company user email is sent when creating a company in multi-language deployments. Previously, the drop-down menu the enables merchants to select the appropriate store view and language was not displayed.  <!--- MC-35777-->

![ 修正された問題 ](../assets/fix.svg) カスタムの顧客アドレス属性フィールドが、ストアフロントのチェックアウトワークフローで期待どおりに表示されるようになりました。<!--- MC-35607-->

![ 修正された問題 ](../assets/fix.svg) 「B2B 機能の設定」タブが正しく開くようになりました。 <!--- MC-35458--> ゲストは QuickOrder を使用して商品を買い物かごに追加し、商品を正常に削除できるようになりました。 以前は、買い物客が QuickOrder を使用して買い物かごに複数の製品を追加してから、製品を削除しても、製品が削除されませんでした。<!--- MC-35327-->

![ 修正された問題 ](../assets/fix.svg) 状態が **不要** に設定されている場合、`region_id` を指定せずに、REST API PUT `/V1/company/:companyId` リクエストを使用して会社を更新できるようになりました。 以前は、`region_id` が必須でなくても、指定されていない場合、Adobe Commerceがエラーをスローしていました。<!--- MC-35304-->

![ 修正された問題 ](../assets/fix.svg)REST API （`http://magento.local/rest/V1/company/2`、`2` は会社 ID を表す）を使用して B2B 会社を作成または更新した場合、期待どおりに応答に `applicable_payment_method` または `available_payment_methods` の設定が含まれるようになりました。<!--- MC-35248-->

![ 修正された問題 ](../assets/fix.svg) ストアフロントで購買依頼リストを作成する際に、マーチャントが **Enter**&#x200B;**[!UICONTROL Save]** ボタンを使用すると、Adobe Commerceに 404 ページが表示されなくなりました。<!--- MC-35094-->

![ 修正された問題 ](../assets/fix.svg) 新しい製品が公開共有カタログに割り当てられると、カテゴリ権限が変更されなくなりました。 以前は、カテゴリ権限は複製されていました。<!--- MC-34386-->

![ 修正された問題 ](../assets/fix.svg) 会社のメールを更新するために使用される REST API エンドポイント PUT `rest/default/V1/company/{id}` で、大文字と小文字が区別されなくなりました。<!--- MC-34308-->

![ 修正された問題 ](../assets/fix.svg) 報酬モジュールを無効にすると、顧客アカウントの B2B 機能に影響しなくなりました。 以前は、報酬モジュールが無効の場合、会社プロファイル、会社ユーザー、役割と権限という B2B 関連のタブは表示されませんでした。<!--- MC-34191-->

![ 修正された問題 ](../assets/fix.svg) 会社アカウントに変更が加えられた場合、Adobe Commerceでメール通知に正しい送信者名が使用されるようになりました。 以前Adobe Commerceでは、すべてのメールに対して、デフォルトスコープで定義された一般的な連絡先の送信者名を使用していました。<!--- MC-33917-->

![ 修正された問題 ](../assets/fix.svg) 物理製品と仮想製品の両方を含む注文に対して、複数出荷を正常に実装できるようになりました。<!--- MC-33818-->

![ 修正された問題 ](../assets/fix.svg)**[!UICONTROL Access Restriction]** が有効で、**[!UICONTROL Restriction Mode]** が `Sales: Login Only` に設定されている場合、マーチャントは、マイアカウントおよび会社構造ページの _[!UICONTROL Company Users]_&#x200B;セクションから会社ユーザーを作成できるようになりました。 以前は、マーチャントがユーザー `Can not register new customer due to restrictions are enabled` を作成しようとすると、Adobe Commerceがこのエラーをスローしていました。<!--- MC-33608-->

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

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポート"}Adobe Commerce 2.4.0 以降のバージョン

![ 新規 ](../assets/new.svg)Adobe Commerce 2.4.0 がサポートされるようになりました。

![ 新規 ](../assets/new.svg) ストアフロントの注文検索。[Divante](https://www.divante.com/) の Marek Mularczyk 氏とコミュニティメンバーの協力により感謝が追加されました。

![ 新規 ](../assets/new.svg) 発注が強化され、書き換えられます。 これらは、Adobe Commerceにデフォルトで含まれるようになりました。

![ 新規 ](../assets/new.svg) 発注承認ルールが実装されました。 これらのルールを使用すると、ユーザーは注文の購入ルールを作成して、発注書ワークフローを制御できます。

![ 新規 ](../assets/new.svg) お客様としてログインがAdobe Commerceにデフォルトで含まれるようになりました。 この機能を使用すると、サイト従業員は、顧客としてログインして表示内容を確認することで、顧客を支援できます。

![ 修正された問題 ](../assets/fix.svg)Elasticsearchを使用したレイヤーナビゲーションで、属性集計が正しく機能するようになりました

![固定問題](../assets/fix.svg) 特殊文字による注文の検索が正しく機能するようになりました。

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

![固定の問題](../assets/fix.svg) 以前は、Git が「許可して顧客に通知」に設定されている場合に、API を使用して見積項目を保存すると失敗していました。 この API 呼び出しは期待どおりに動作するようになりました。

![問題固定](../assets/fix.svg) 見積もりの詳細 ページに固定商品の税が表示されるようになりました。

![固定問題](../assets/fix.svg) 以前は、[見積もり] ページの [コメント] タブで添付ファイルをクリックすると、ファイルダウンロードする失敗していました。 この動作は期待どおりに動作するようになりました。

### 既知の問題

- Adobe Systems Commerce が、複数の Web サイトデプロイメントで B2B 1.2.0 にアップグレードするときに例外をスローします。 `setup:upgrade`を実行すると、このエラーは `PurchaseOrder` モジュール:`Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder` で発生します。**回避策**: `magento.com` の **マイアカウント** > **ダウンロード** セクションから入手できるようになった `InitPurchaseOrderSalesSequence` データ パッチ修正プログラムに `B2B-716 Add NonTransactionableInterface` インターフェイスをインストールします。
- 購入注文 (PO) が承認される前に割引コードの有効期限が切れた場合、発注書は割引金額を表示し続けますが、発注書が承認されると、注文は割引されていない合計で発注されます。 **回避策**: この問題の `B2B-709 Purchase Order Discount patch` 修正プログラムをインストールします。この修正プログラムは、`magento.com` の **マイアカウント** > **ダウンロード** セクションから入手できます。
- 購買発注の品目が在庫切れの場合、または発注書が実際の注文に変換されるときの量が不十分な場合、エラーが発生します。 バックオーダーが有効になっている場合、オーダーは通常どおり処理されます。
