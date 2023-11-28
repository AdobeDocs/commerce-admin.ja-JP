---
title: 付加価値税 (VAT)
description: '&lt；ここに説明を追加 (&gt);'
exl-id: 20dbcb86-e558-47f2-968d-b5c9ec5f665b
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1992'
ht-degree: 0%

---

# 付加価値税 (VAT)

一部の国では、商品やサービスに付加価値税 (VAT) が課せられます。 顧客に販売する製造または流通プロセス、材料、またはサービスの段階に応じて、異なる VAT 率が存在する場合があります。 複数の VAT レートを適用して、期限の税を正しく計算できます。

コマースは、同じ国にいる場合、マーチャントまたは顧客の住所に基づいて付加価値税を課すように設定できます。 VAT 計算は、通常、出荷先に基づいておこなわれ、出荷元ではありません。 ほとんどのシナリオでは、顧客の配送先住所に基づいて VAT を計算する構成設定で十分です。

## シナリオの例

- ある EU 国の VAT 登録事業で、他の EU 国の個人に商品を供給する場合、VAT は商人の所在地に基づいて「距離販売」として計算されます。

- 英国の住所に出荷される英国の店舗から買い物をするオランダのビジネスは、英国の VAT 率を支払う必要があります。

- ～の販売のために [ダウンロード可能な製品](../catalog/product-create-downloadable.md)または _デジタル商品_&#x200B;の場合、VAT 率は商業者の所在地ではなく、配送先に基づきます。 詳しくは、 [デジタル商品の供給場所](taxes.md#place-of-supply-for-digital-goods-eu).

>[!TIP]
>
>一部の国境を越えた出荷と B2B 出荷は、より複雑な税務要件を持っています。 コマースインストールのネイティブ機能を拡張するには、 [Marketplace](https://marketplace.magento.com/extensions/accounting-finance/taxes.html).

## VAT の構成

次の手順は、小売顧客向けの販売用に英国で 20% VAT を設定するサンプル手順を示しています。 その他の税率や国については、一般的な手順に従いますが、国、VAT 率、顧客タイプなどに対応する具体的な情報を入力します。

>[!NOTE]
>
>先に進む前に、お客様の地域で VAT に適用されるルールや規制を確認してください。

特定の BT 取引では、VAT は評価されません。 コマースでは、顧客の VAT ID を検証して、VAT が適切に評価（または評価対象外）されたかを確認できます。 詳しくは、 [VAT ID の検証](#vat-id-validation).

### 手順 1：顧客税区分の設定

税率を追加すると、税務処理基準の作成プロセスが開始されます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   ![顧客税区分の設定](./assets/vat-zones.png){width="600" zoomable="yes"}

1. VAT と共に使用するのに適した顧客税区分があることを確認します。

   この例では、という名前の顧客税区分があることを確認します。 _小売顧客_. この税区分が存在しない場合は、 **[!UICONTROL Add New Tax Rate]**.

1. 次を入力します。 **[!UICONTROL Tax Identifier]** 新しい税区分に対して。

   すべての税率が _税率_ フィールド _税務処理基準情報_ 税務処理基準を作成する場合。

1. 郵便番号範囲 ( ～ ) を設定するには、 **[!UICONTROL Zip/Post is Range]** チェックボックス。

1. を選択します。 **[!UICONTROL Country]** 税率が適用される場合。

1. 次を入力します。 **[!UICONTROL Rate Percent]** 購入時の税率の計算に使用されます。

1. 完了したら、「 **[!UICONTROL Save Rate]**.

提出された税率に基づいて、後続の税ルールを作成できます。 税率がないと、税務処理基準の作成は不可能になる。

### 手順 2：製品税区分の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** >  _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. クリック **[!UICONTROL Add New Tax Rule]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Additional Settings]** 」セクションに入力します。

   ![製品税区分を設定します](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. の下 _製品税区分_&#x200B;をクリックし、 **[!UICONTROL Add New Tax Class]**.

1. 使用可能な製品税区分のリストに新しい区分を追加し、3 つの新しい区分を作成するには、 **[!UICONTROL Name]** 新しい税区分のチェックマークをクリックします。

   - `VAT Standard`
   - `VAT Reduced`
   - `VAT Zero`

1. クリック **[!UICONTROL Save Class]** 追加する新しいクラスごとに

1. クリック **[!UICONTROL Save Rule]**.

### 手順 3：税ゾーンおよび率の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** >  _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   この例では、米国の税率を削除するか、そのままにしておくことができます。

1. クリック **[!UICONTROL Add New Tax Rate]**.

   ![税ゾーンと税率の設定](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

1. 新しいレートを次のように定義します。

   **VAT 標準**

   - 税金識別子： `VAT Standard`
   - 国と州： `United Kingdom`
   - 割合： `20.00`

   **VAT 削減**

   - 税金識別子： `VAT Reduced`
   - 国と州： `United Kingdom`
   - 割合： `5.00`

1. クリック **[!UICONTROL Save Rate]** 各料金に対して

### 手順 4：税務処理基準の設定

税務処理基準は、顧客税区分、製品税区分および税率の組み合わせです。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. 次の手順に従って、新しい税金ルールを追加します。

   **VAT 標準**

   - 名前： `VAT Standard`
   - 顧客税区分： `Retail Customer`
   - 製品税区分： `VAT Standard`
   - 税率： `VAT Standard Rate`

   **減価税**

   - 名前： `VAT Reduced`
   - 顧客税区分： `Retail Customer`
   - 製品税区分： `VAT Reduced`
   - 税率： `VAT Reduced Rate`

1. クリック **[!UICONTROL Save Rule]** 各料金に対して

### 手順 5：税区分を製品に適用

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Manage Products]**.

1. カタログの製品を編集モードで開きます。

1. 次の日： _一般_ ページで、 **[!UICONTROL Tax Class]** オプションを選択し、 **[!UICONTROL VAT Class]** 製品に適用される

1. 完了したら、「 **[!UICONTROL Save]**.

   ![製品に税区分を適用](./assets/vat-apply-classes.png){width="600" zoomable="yes"}

## フィールドの説明

### ストア情報

コマースでは次を使用します [ストア情報の設定](../configuration-reference/general/general.md#store-information) 商人情報に基づいて VAT を計算します。

**[!UICONTROL VAT Number]**  — 商人に割り当てられる付加価値税番号。

**[!UICONTROL Validate VAT Number]** - [VAT 検証](#vat-id-validation) VAT 番号が [欧州委員会](https://ec.europa.eu/taxation_customs/vies/) データベース。

### 顧客情報

コマースは、次のフィールドを使用して、VAT を次に基づいて計算します [顧客情報](../customers/account-dashboard-account-information.md)) をクリックします。

#### アカウント情報

**[!UICONTROL Tax/VAT Number]**  — 該当する場合、顧客に割り当てられる税番号または付加価値税番号。

#### アドレス

**[!UICONTROL VAT Number]**  — 該当する場合、顧客の特定の請求または配送先住所に関連付けられた付加価値税番号。 ～の販売のために [デジタル商品](taxes.md#place-of-supply-for-digital-goods-eu))EU 内では、VAT の金額は配送先に基づきます。

### 顧客アカウント

コマースでは次を使用します [顧客設定](../customers/account-options-new.md) VAT を計算します。

**[!UICONTROL Show VAT Number on Storefront]**  — 顧客アカウントで使用可能なアドレス帳に顧客の VAT 番号フィールドが含まれるかどうかを決定します。

**[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]** - VAT ID は、VAT 検証で使用される場合の顧客の VAT 番号の内部識別子です。 VAT 検証中に、Commerce は数値が [欧州委員会](https://ec.europa.eu/taxation_customs/vies/) データベース。 お客様は、検証結果に基づいて、4 つのデフォルト顧客グループのいずれかに自動的に割り当てられます。

## VAT ID の検証

_VAT ID の検証_ マーチャントと顧客のロケールに基づいて、欧州連合 (EU) 内で発生する B2B トランザクションに必要な税金を自動的に計算します。 コマースは、 [欧州委員会][1] サーバー。

>[!NOTE]
>
>VAT 関連の税務処理基準は、他の税務処理基準に影響を与えず、他の税務処理基準の適用を妨げません。 一度に適用できる税務処理基準は 1 つだけです。

- VAT は、商人と顧客が同じ EU 国にいる場合に請求されます。
- 商人と顧客が異なる EU 諸国に属し、両者が EU 登録事業者である場合、VAT は請求されません。

ストア管理者は、アカウントの作成、住所の作成または更新、チェックアウト時に、顧客に自動的に割り当てることができる、複数のデフォルトの顧客グループを作成します。 その結果、国内（国内）と EU 域内の売上に異なる税制ルールが使用されることになります。

>[!IMPORTANT]
>
>出荷が不要な仮想またはダウンロード可能な製品を販売する場合は、顧客の所在国の VAT 率を組合内と国内の両方の販売に使用する必要があります。 仮想製品に対応する製品税区分に対して、追加の個別税ルールを作成します。

### 顧客登録ワークフロー

VAT ID 検証が有効な場合は、登録後に各顧客が VAT ID 番号を入力するよう提案されます。 ただし、このフィールドに入力できるのは、VAT の顧客を登録した買い物客のみです。

お客様が VAT 番号および他の住所フィールドを指定し、保存すると、その住所が保存され、VAT ID 検証要求が欧州委員会サーバーに送信されます。 検証の結果に従って、デフォルトグループの 1 つが顧客に割り当てられます。 このグループは、顧客または管理者がデフォルトの住所の VAT ID を変更したり、デフォルトの住所全体を変更した場合に変更できます。 1 ページのチェックアウト中に、グループが一時的に変更される（グループの変更がエミュレートされる）ことがあります。

有効にした場合、個々の顧客の VAT ID 検証を上書きするには、 _[!UICONTROL Customer Information]_ページに貼り付けます。

### チェックアウトワークフロー

顧客の VAT 検証がチェックアウト中に実行されると、VAT 要求識別子と VAT 要求日が注文の [ コメント履歴 ] セクションに保存されます。

VAT ID 検証およびチェックアウト時の顧客グループの変更に関するシステムの動作は、各トランザクションでの検証と自動グループ変更の無効化の設定の設定によって異なります。 この項では、フロントエンドのチェックアウトに対する VAT ID 検証機能の実装について説明します。

お客様がGoogle Express Checkout、PayPal Express Checkout、または他の外部チェックアウト方法を使用している場合、チェックアウトは外部の支払いゲートウェイ側で完全に実行されます。 このシナリオでは、 _各トランザクションでの検証_ 設定を適用できず、顧客グループはチェックアウト中に変更できません。

![VAT 検証チェックアウトワークフロー](./assets/vat-id-validation2.png){width="550" zoomable="yes"}

### VAT ID 検証の構成

VAT ID 検証を構成するには、まず必要な顧客グループを設定し、関連する税区分、税率およびルールを作成する必要があります。 次に、ストアの VAT ID 検証を有効にし、設定を完了します。

次の例は、VAT ID 検証に税区分と税率が使用される方法を示しています。 例を確認し、使用する店舗に必要な税区分とルールを設定する手順に従います。

#### 例： VAT ID 検証に必要な最小税金ルール

| 税務処理基準#1 |  |
|--- |--- |
| 顧客税区分 | 顧客税区分には、次を含める必要があります。 <br />国内のお客様向けのクラス。 <br />VAT ID の形式が正しくない顧客用のクラス。<br />VAT ID の検証に失敗した顧客のクラス。 |
| 製品税区分 | 製品税区分には、バンドルと仮想を除くすべてのタイプの製品の区分を含める必要があります。 |
| 税率 | 税率には、商人の国の VAT 率を含める必要があります。 |

{style="table-layout:auto"}

| 税務処理基準#2 |   |
|--- |--- |
| 顧客税区分 | EU 内の顧客用のクラス。 |
| 製品税区分 | 仮想を除くすべてのタイプの製品のクラス。 |
| 税率 | VAT レートは、商家の国を除くすべての EU 諸国に対して設定されます。 現在、この率は 0%です。 |

{style="table-layout:auto"}

| 税務処理基準#3 | （仮想製品およびダウンロード可能な製品に必要） |
|--- |--- |
| 顧客税区分 | 顧客税区分には、次を含める必要があります。 <br/>国内顧客向けクラス <br/>無効な VAT ID を持つ顧客の区分 VAT ID の検証に失敗した顧客の区分 |
| 製品税区分 | 仮想製品のクラス。 |
| 税率 | 商人の国の VAT 率。 |

{style="table-layout:auto"}

| 税務処理基準#4 | （仮想製品およびダウンロード可能な製品に必要） |
|--- |--- |
| 顧客税区分 | EU 内の顧客用のクラス。 |
| 製品税区分 | 仮想製品のクラス。 |
| 税率 | VAT レートは、商家の国を除くすべての EU 諸国に対して設定されます。 現在、この率は 0%です。 |

{style="table-layout:auto"}

#### 手順 1:VAT 関連の顧客グループの作成

VAT ID 検証では、VAT ID 検証結果に従って、次の 4 つのデフォルト顧客グループの 1 つが顧客に自動的に割り当てられます。

- 国内
- EU 域内
- 無効な VAT ID
- 検証エラー

ビジネス・ロジックに準拠している場合は、VAT ID 検証用の顧客グループを作成したり、既存のグループを使用したりできます。 VAT ID 検証を構成する場合は、作成した各顧客グループを、適切な VAT ID 検証結果を持つ顧客のデフォルトとして割り当てる必要があります。

#### ステップ 2:VAT 関連の区分、レートおよびルールの作成

各税金ルールは、次の 3 つのエンティティで定義されます。

- 顧客税区分
- 製品税区分
- 税率

を作成します。 [税務処理基準](tax-rules.md) VAT ID 検証を効果的に使用するために。

- 税ルールには税率と [税制](tax-class.md).
- 税区分が次に割り当てられています： [顧客グループ](../customers/customer-groups.md).

#### 手順 3:VAT ID 検証の有効化と構成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 必要に応じて、 **[!UICONTROL Store View]** を設定します。

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Customer Configuration]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Create New Account Options]** 」セクションに入力します。

   次の例では、VAT 検証に関連しない一般的な顧客設定が暗くなっています。

   ![新しいアカウントオプションの作成](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable Automatic Assignment to Customer Group]** から `Yes` 必要に応じて、次のフィールドに入力します。

   - **[!UICONTROL Default Group]**
   - **[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]**
   - **[!UICONTROL Show VAT Number on Storefront]**

1. 完了したら、「 **[!UICONTROL Save Config]**.

#### 手順 4:VAT ID と場所の国を設定します

1. 左側のパネルで、を展開します。 **[!UICONTROL General]** を選択します。 **[!UICONTROL General]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Store Information]** 」セクションに入力します。

   ![ストア情報](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. を選択します。 **[!UICONTROL Country]**.

1. を入力します。 **[!UICONTROL VAT Number]** をクリックします。 **[!UICONTROL Validate VAT Number]**.

   結果がすぐに表示されます。

1. 完了したら、「 **[!UICONTROL Save Config]**.

#### ステップ 5:EU 加盟国のリストの確認

1. 次で続行： _一般_ 設定ページ、展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Countries Options]** 」セクションに入力します。

   ![国オプション](../configuration-reference/general/assets/general-country-options.png){width="600" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL European Union Countries]** リストで、EU の各メンバー国が選択されていることを確認します。

   デフォルト設定を変更するには、 **システム値を使用** チェックボックス。 Ctrl キー (PC) または Command キー (Mac) を押しながら、追加または削除する国をクリックします。

1. 完了したら、「 **[!UICONTROL Save Config]**.


[1]: https://ec.europa.eu/taxation_customs/vies/
