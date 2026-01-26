---
title: 付加価値税（VAT）
description: '&lt；ここに説明を追加&gt;'
exl-id: 20dbcb86-e558-47f2-968d-b5c9ec5f665b
feature: Taxes
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 0%

---

# 付加価値税（VAT）

製品やサービスに付加価値税を課す国もあります。 お客様に販売する製造または流通プロセス、材料、またはサービスの段階に応じて、異なる VAT レートが存在する場合があります。 複数の VAT レートを適用して、期限の税金を正しく計算できます。

Commerceでは、同じ国に居住している場合に、マーチャントまたはカスタマーの住所のいずれかに基づいて付加価値税を請求するように設定できます。 VAT 計算は通常、出荷元ではなく、出荷先に基づいています。 ほとんどの場合、顧客の配送先住所に基づいて VAT を計算する設定で十分です。

## サンプルシナリオ

- ある EU 諸国の VAT 登録ビジネスで、別の EU 諸国の個人に商品を供給する場合、VAT はマーチャントの場所に基づいて「遠隔販売」として計算されます。

- オランダで、英国の店舗から英国の住所に配送される商品を購入する企業は、英国の VAT 税率を支払う必要があります。

- [ ダウンロード可能な商品 ](../catalog/product-create-downloadable.md) または _デジタル商品_ の販売の場合、VAT 税率は販売者の場所ではなく出荷先に基づきます。 [ デジタル商品の供給場所 ](taxes.md#place-of-supply-for-digital-goods-eu) を参照。

>[!TIP]
>
>一部のクロスボーダーおよび B2B 配送では、より複雑な税金要件があります。 Commerce インストールのネイティブ機能を拡張するには、[Marketplace](https://marketplace.magento.com/extensions/accounting-finance/taxes.html) から税務管理ソリューションを追加することを検討してください。

## VAT の構成

以下の手順には、小売顧客への販売のために英国で 20% の VAT を設定するサンプル手順が含まれています。 その他の税率や国については、一般的な手順に従いますが、お住まいの国、VAT 率、お客様のタイプなどに対応する具体的な情報を入力してください。

>[!NOTE]
>
>続行する前に、お住まいの地域の VAT に適用される規則と規制を確認してください。

B2B 取引の中には、VAT が評価されないものもあります。 Commerceでは、お客様の VAT ID を検証することにより、VAT が適切に評価されている（または評価されていない）ことを確認できます。 [VAT ID 検証 ](#vat-id-validation) を参照してください。

### 手順 1：顧客税区分の設定

税務処理基準を作成するプロセスは、税率を追加することから始まります。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Taxes]_/**[!UICONTROL Tax Zones and Rates]**に移動します。

   ![ 顧客税区分の設定 ](./assets/vat-zones.png){width="600" zoomable="yes"}

1. VAT で使用するのに適切な顧客税クラスがあることを確認してください。

   この例では、「Retail Customer _という名前の顧客税クラスがあることを確認し_ す。 この税金区分が存在しない場合は、「**[!UICONTROL Add New Tax Rate]**」をクリックします。

1. 新しい税区分の **[!UICONTROL Tax Identifier]** を入力します。

   税務処理基準を作成すると、すべての税率が _税務処理基準情報_ の _税率_ フィールドに表示されます。

1. 郵便番号の範囲（範囲/範囲）を設定するには、「**[!UICONTROL Zip/Post is Range]**」チェックボックスを選択します。

1. 税率を適用する **[!UICONTROL Country]** を選択します。

1. 購入時の税率計算に使用される **[!UICONTROL Rate Percent]** を入力します。

1. 完了したら、「**[!UICONTROL Save Rate]**」をクリックします。

提出された税率に基づいて、後続の税務処理基準を作成できます。 税率がない場合、税務規則の作成は不可能になります。

### 手順 2：製品税区分の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Taxes]_/**[!UICONTROL Tax Rules]**に移動します。

1. 「**[!UICONTROL Add New Tax Rule]**」をクリックします。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Additional Settings]**」セクションを展開します。

   ![ 製品税区分の設定 ](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. _製品税区分_ で、「**[!UICONTROL Add New Tax Class]**」をクリックします。

1. 使用可能な製品税金区分のリストに新規区分を追加し、3 つの新規区分を作成するには、新規税金区分の **[!UICONTROL Name]** を入力してチェックマークをクリックします。

   - `VAT Standard`
   - `VAT Reduced`
   - `VAT Zero`

1. 追加する新しいクラスごとに **[!UICONTROL Save Class]** をクリックします。

1. 「**[!UICONTROL Save Rule]**」をクリックします。

### 手順 3：税金ゾーンおよび税率の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Taxes]_/**[!UICONTROL Tax Zones and Rates]**に移動します。

   この例では、米国の税率を削除するか、そのままにしておくことができます。

1. 「**[!UICONTROL Add New Tax Rate]**」をクリックします。

   ![ 税ゾーンと税率の設定 ](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

1. 次のように新規レートを定義します。

   **VAT 基準**

   - 税金識別子：`VAT Standard`
   - 国と都道府県：`United Kingdom`
   - 料率：`20.00`

   **VAT 引き下げ**

   - 税金識別子：`VAT Reduced`
   - 国と都道府県：`United Kingdom`
   - 料率：`5.00`

1. 各料金の **[!UICONTROL Save Rate]** をクリックします。

### 手順 4：税務処理基準の設定

税務処理基準は、顧客税金区分、製品税金区分および税率の組合せです。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Taxes]_/**[!UICONTROL Tax Rules]**に移動します。

1. 次のように新規税務処理基準を追加します。

   **VAT 基準**

   - 名前：`VAT Standard`
   - 顧客税区分：`Retail Customer`
   - 製品税クラス：`VAT Standard`
   - 税率：`VAT Standard Rate`

   **Vat 減額**

   - 名前：`VAT Reduced`
   - 顧客税区分：`Retail Customer`
   - 製品税クラス：`VAT Reduced`
   - 税率：`VAT Reduced Rate`

1. 各料金の **[!UICONTROL Save Rule]** をクリックします。

### 手順 5：製品への税金区分の適用

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Manage Products]** に移動します。

1. カタログの製品を編集モードで開きます。

1. _一般_ ページで、「**[!UICONTROL Tax Class]**」オプションを見つけて、製品に適用する **[!UICONTROL VAT Class]** を選択します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   ![ 製品への税区分の適用 ](./assets/vat-apply-classes.png){width="600" zoomable="yes"}

## フィールドの説明

### ストア情報

Commerceでは、次の [Store Information 設定 ](../configuration-reference/general/general.md#store-information) を使用して、マーチャント情報に基づいて VAT を計算します。

**[!UICONTROL VAT Number]**：業者に割り当てられる付加価値税番号。

**[!UICONTROL Validate VAT Number]** - [VAT 検証 ](#vat-id-validation) は、VAT 番号が [ 欧州委員会 ](https://ec.europa.eu/taxation_customs/vies/) データベース内の対応するレコードと一致することを確認します。

### 顧客情報

Commerceでは、次のフィールドを使用して、（お客様情報 [ に基づいて VAT](../customers/account-dashboard-account-information.md) 計算します。

#### アカウント情報

**[!UICONTROL Tax/VAT Number]** – 該当する場合、顧客に割り当てられた税金番号または付加価値税番号。

#### アドレス

**[!UICONTROL VAT Number]** – 該当する場合、顧客の特定の請求先または配送先住所に関連付けられている付加価値税番号。 EU 域内での [ デジタル商品 ](taxes.md#place-of-supply-for-digital-goods-eu)）の販売に関しては、VAT の金額は出荷先に基づきます。

### 顧客アカウント

Commerceでは、次の [ 顧客設定 ](../customers/account-options-new.md) を使用して VAT が計算されます。

**[!UICONTROL Show VAT Number on Storefront]** – 顧客アカウントで使用可能なアドレス帳に顧客の VAT 番号フィールドが含まれるかどうかを決定します。

**[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]** - VAT ID は、VAT 検証で使用される顧客の VAT 番号の内部識別子です。 VAT 認証時に、Commerceは番号が [ 欧州委員会 ](https://ec.europa.eu/taxation_customs/vies/) のデータベースと一致することを確認します。 検証結果に基づいて、顧客を 4 つのデフォルト顧客グループのいずれかに自動的に割り当てることができます。

## VAT ID の検証

_VAT ID 検証_ は、マーチャントと顧客のロケールに基づいて、EU 内で発生する B2B 取引に必要な税金を自動的に計算します。 Commerceは、[ 欧州委員会 ](https://ec.europa.eu/taxation_customs/vies/) サーバーの web サービスを使用して VAT ID の検証を実行します。

>[!NOTE]
>
>VAT に関連する税務規則は、他の税務規則に影響を与えず、他の税務規則の適用を妨げません。 一度に 1 つの税務処理基準のみを適用できます。

- 加盟店とお客様が同じ EU 加盟国にいる場合は、VAT が請求されます。
- 加盟店とお客様が異なる EU 諸国に居住し、両者が EU に登録された事業体である場合、VAT は請求されません。

店舗管理者は、アカウントの作成、住所の作成または更新、チェックアウトの際に自動的に顧客に割り当てることができる複数のデフォルトの顧客グループを作成します。 その結果、国内（国内）と EU 内の販売に異なる税務規則が使用されます。

>[!IMPORTANT]
>
>配送を必要としないバーチャルまたはダウンロード可能な商品を販売する場合は、お客様の所在国の VAT レートを EU 内販売と国内販売の両方に使用する必要があります。 仮想製品に対応する製品税区分に対して、追加の個別税務処理基準を作成します。

### 顧客登録ワークフロー

VAT ID 検証が有効化されている場合、登録後に各顧客に VAT ID 番号の入力が提案されます。 ただし、このフィールドに入力する必要があるのは、VAT 登録を受けた買い物客のみです。

顧客が VAT 番号およびその他の所在地フィールドを指定して保存を選択すると、システムは所在地を保存し、VAT ID 検証要求を欧州委員会サーバーに送信します。 検証の結果に応じて、デフォルトのグループの 1 つが顧客に割り当てられます。 このグループは、顧客または管理者が既定の住所の VAT ID を変更した場合、または既定の住所全体を変更した場合に変更できます。 1 ページのチェックアウト中に、グループを一時的に変更できる（グループの変更がエミュレートされる）場合があります。

有効化すると、_[!UICONTROL Customer Information]_のページのチェックボックスをオンにして、個々の顧客の VAT ID 検証を上書きできます。

### チェックアウトワークフロー

チェックアウト中に顧客の VAT 検証が実行されると、VAT 要求識別子と VAT 要求日が注文の「コメント履歴」セクションに保存されます。

チェックアウト中の VAT ID 検証および顧客グループの変更に関するシステム動作は、「各取引で検証」および「自動グループ変更の無効化」の設定方法によって異なります。 ここでは、フロントエンドでのチェックアウトに対する VAT ID 検証機能の実装について説明します。

お客様がGoogle Express Checkout、PayPal Express Checkout、またはその他の外部チェックアウト方法を使用している場合、チェックアウトは外部の支払い方法の横で完全に実行されます。 このシナリオでは、「_各トランザクションで検証_ 設定は適用できず、チェックアウト中に顧客グループを変更することはできません。

![VAT 検証チェックアウト ワークフロー ](./assets/vat-id-validation2.png){width="550" zoomable="yes"}

### VAT ID 検証の構成

VAT ID 検証を構成するには、まず必要な顧客グループを設定し、関連する税クラス、税率およびルールを作成する必要があります。 次に、ストアの VAT ID 検証を有効にし、設定を完了します。

次の例は、VAT ID の検証に税金区分と税率を使用する方法を示しています。 例を確認し、店舗に必要な税区分とルールを設定する手順に従います。

#### 例：VAT ID 検証に必要な最小税務処理基準

| 税務処理基準#1 |  |
|--- |--- |
| 顧客税金クラス | 顧客税区分には、次を含める必要があります。<br /> 国内顧客の区分。 <br />VAT ID の形式が正しくない顧客用のクラス。<br />VAT ID の検証に失敗した顧客のクラス。 |
| 製品税クラス | 製品税クラスには、バンドルとバーチャルを除くすべてのタイプの製品のクラスを含める必要があります。 |
| 税率 | 税率には、商人の国の VAT 率を含める必要があります。 |

{style="table-layout:auto"}

| 税務処理基準#2 |   |
|--- |--- |
| 顧客税金クラス | 組合内顧客のクラス。 |
| 製品税クラス | 仮想を除くすべてのタイプの製品のクラス。 |
| 税率 | 加盟国以外のすべての EU 諸国の VAT 税率。 現在このレートは 0% です。 |

{style="table-layout:auto"}

| 税務処理基準#3 | （バーチャルおよびダウンロード可能な製品に必要） |
|--- |--- |
| 顧客税金クラス | 顧客税区分には次が含まれる必要があります。<br/> 国内顧客の区分 <br/> 無効な VAT ID を持つ顧客の区分 VAT ID 検証に失敗した顧客の区分 |
| 製品税クラス | 仮想製品のクラス。 |
| 税率 | 販売者の国の VAT 率です。 |

{style="table-layout:auto"}

| 税務処理基準#4 | （バーチャルおよびダウンロード可能な製品に必要） |
|--- |--- |
| 顧客税金クラス | 組合内顧客のクラス。 |
| 製品税クラス | 仮想製品のクラス。 |
| 税率 | 加盟国以外のすべての EU 諸国の VAT 税率。 現在このレートは 0% です。 |

{style="table-layout:auto"}

#### 手順 1:VAT 関連顧客グループの作成

VAT ID 検証では、VAT ID 検証結果に従って、4 つのデフォルト顧客グループのいずれかが顧客に自動的に割り当てられます。

- 国内
- EU 内
- VAT ID が無効です
- 検証エラー

ビジネス・ロジックに準拠している場合は、VAT ID 検証用の顧客グループを作成するか、既存のグループを使用できます。 VAT ID 検証を設定する場合、適切な VAT ID 検証結果を持つ顧客に対して、作成された各顧客グループをデフォルトとして割り当てる必要があります。

#### 手順 2：付加価値税関連の区分、税率およびルールの作成

各税務処理基準は、次の 3 つのエンティティで定義されます。

- 顧客税金クラス
- 製品税クラス
- 税率

VAT ID 検証を効果的に使用するための [ 税ルール ](tax-rules.md) を作成します。

- 税務処理基準には、税率と [ 税区分 ](tax-class.md) が含まれます。
- 税金クラスは [ 顧客グループ ](../customers/customer-groups.md) に割り当てられます。

#### 手順 3:VAT ID 検証の有効化と設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 必要に応じて、設定の **[!UICONTROL Store View]** を設定します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Customer Configuration]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Create New Account Options]**」セクションを展開します。

   次の例では、VAT 検証に関連しない一般的な顧客設定はグレー表示になっています。

   ![ 新規アカウントオプションの作成 ](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable Automatic Assignment to Customer Group]** を `Yes` に設定し、必要に応じて次のフィールドに入力します。

   - **[!UICONTROL Default Group]**
   - **[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]**
   - **[!UICONTROL Show VAT Number on Storefront]**

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

#### 手順 4:VAT ID と所在国の設定

1. 左側のパネルで「**[!UICONTROL General]**」を展開し、その下の「**[!UICONTROL General]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Store Information]**」セクションを展開します。

   ![ 店舗情報 ](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. **[!UICONTROL Country]** を選択します。

1. **[!UICONTROL VAT Number]** を入力し、「**[!UICONTROL Validate VAT Number]**」をクリックします。

   結果がすぐに表示されます。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

#### ステップ 5:EU 加盟国リストの検証

1. _一般_ 設定ページで続行して、「![」セクションの ](../assets/icon-display-expand.png) 展開セレクター **[!UICONTROL Countries Options]** を展開します。

   ![ 国オプション ](../configuration-reference/general/assets/general-country-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL European Union Countries]** リストで、EU の各メンバー国が選択されていることを確認します。

   デフォルト設定を変更するには、「**システム値を使用**」チェックボックスをオフにします。 Ctrl キー（PC）または Command キー（Mac）を押しながら、追加または削除する国をそれぞれクリックします。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
