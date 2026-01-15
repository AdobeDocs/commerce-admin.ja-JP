---
title: 階層の価格
description: 階層価格を使用して、製品リストまたは製品ページから数量割引を提供する方法を説明します。
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# 階層の価格

階層価格を使用すると、ストアフロントの商品リストまたは商品ページから数量割引を提供できます。 割引は、特定のストア表示、顧客グループ、共有カタログに適用できます。

更新する製品が多数ある場合は、階層価格の変更を個別に入力するのではなく、インポートするのが最も効率的です。 詳しくは、[ 階層価格のインポート ](../systems/data-import-price-tier.md) を参照してください。

![ ストアフロント製品ページの階層価格 ](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

製品ページで数量割引が計算され、次のようなメッセージが表示されます。

`Buy 6 for $5.95 each and save 15%`

ストアフロントの価格は、高い数量から低い数量まで優先されます。 数量 `5` に階層価格があり、`10` に 1 があり、顧客が買い物かごに 5 個、6 個、7 個、8 個、または 9 個の品目を追加すると、顧客は数量 `5` 階層分の割引価格を受け取ります。 顧客が 10 番目の品目を追加すると、数量 `10` 層に指定された割引価格が `5` の数量の層を置き換え、`10` の割引価格が適用されます。

## 製品の価格階層の追加

1. 製品を編集モードで開きます。

1. 「_[!UICONTROL Price]_」フィールドの下にある「**[!UICONTROL Advanced Pricing]**」をクリックします。

1. 「_[!UICONTROL Tier Price]_」セクションで、「**[!UICONTROL Add]**」をクリックします。

   複数の価格の階層を作成する場合は、追加のレベルごとに **[!UICONTROL Add]** をクリックして、すべての階層を同時に作業できるようにします。 グループ内の各層の web サイトと顧客グループまたは共有カタログの割り当ては同じですが、数量と価格が異なります。

## 価格層の設定

1. ストアに複数の web サイトがある場合は、階層の価格が適用される **[!UICONTROL Website]** を選択します。

1. 必要に応じて、**[!UICONTROL Customer Group]** または **[!UICONTROL Shared Catalog]** を選択して、価格レベルの利用を制限します（![Adobe Commerce B2B](../assets/b2b.svg) [Adobe Commerce B2B](./b2b/../introduction.md) でのみ利用可能）。

1. **[!UICONTROL Qty]**：割引を受け取るために注文する必要がある数量を入力します。

   - **方法 1:** 価格を固定金額で入力する

     **[!UICONTROL Price]** を `Fixed` に設定し、その階層の 1 単位の調整済み価格を入力します。

     ![ 固定金額としての階層価格 ](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **方法 2:** 価格をパーセンテージで入力します。

     **[!UICONTROL Price]** を `Discount` に設定し、割引価格を製品の基本価格に対するパーセンテージとして入力します。

     例えば、15% の割引の場合は、`15` という数値を入力します。 （価格は `15.00` のように小数点以下 2 桁で保存されます。）

     >[!NOTE]
     >
     >割引価格を取得するには、定義済みの割合を、_[!UICONTROL Price]_フィールドではなく、_[!UICONTROL Special Price]_ フィールドで定義された値に対して計算します。

     ![ 階層価格（割合） ](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## 価格設定の完了

1. 別の web サイトまたは顧客グループに別の階層料金セットを追加するには、前の手順を繰り返します。

1. 完了したら、「**[!UICONTROL Done]**」をクリックし、次に「**[!UICONTROL Save]**」をクリックします。

>[!NOTE]
>
>**_最終_** 製品価格は、次の式を使用して **_最小_** 関連価格として計算されます。<br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定価格_** 製品カスタマイズ可能なオプションは、グループ価格、階層価格、特別価格、カタログ価格ルールの影響を _受けません_。

## カタログ価格ルールの階層価格を有効にする

[!BADGE SaaS のみ ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service プロジェクトにのみ適用されます（Adobeで管理される SaaS インフラストラクチャ）。"}

[!BADGE  サンドボックス ]{type=Caution tooltip="リストされた項目は、現在、サンドボックス環境でのみ使用できます。 Adobeでは、最初にサンドボックス環境で新しいリリースを使用できるようにして、リリースが実稼動環境で使用できるようになる前に、今後の変更をテストするための時間を提供します。"}

以前のバージョンのCommerceでは、カタログ価格ルールと組み合わせて階層価格を使用することはできませんでした。 カタログルールでは、階層価格の設定が無視され、元の基本価格からのみ計算された割引が無視されました。 Adobe Commerce as a Cloud Serviceを使用して、カタログ価格ルールの計算に階層価格を含めることができるようになりました。

この機能を有効にするには：

1. **[!UICONTROL Stores]**/*[!UICONTROL Settings]*/**[!UICONTROL Configuration]**/**[!UICONTROL Sales]**/**[!UICONTROL Sales]**/**[!UICONTROL Promotions]** に移動し、「**[!UICONTROL Apply Catalog Price Rule on Grouped Price]**」フィールドを「**[!UICONTROL Yes]**」に設定します。

   ![ カタログ価格ルールの階層価格を有効にする ](../configuration-reference/sales/assets/sales-promotions-settings.png){width="700" zoomable="yes"}

1. カタログ価格ルールでターゲットにする特定の顧客グループまたは共有カタログ（`1`、`Wholesale`、またはマーチャント定義のグループなど）ごとに、`Retail` 数の階層価格を定義します。 この目的には、`ALL GROUPS` 顧客グループ `Default` 共有カタログは使用できません。 階層の価格は、`1` の数量で定義された階層価格を持たないグループでは有効になっていません。

1. 必要に応じて、数量が `1` を超える追加の階層価格を定義します。 これらの追加階層価格は、顧客が商品の数量を買い物かごに追加した場合に、通常どおり適用されます。 カタログ価格ルールは、これらの追加の階層価格には適用されません。

単一の製品を購入する際に階層価格がカタログ価格ルールとどのように連動するかを示すために、次の例を考えてみます。

- 製品の標準基本価格は 100 USD です。
- 階層価格は、数量が `Wholesale` で固定価格が 90 USD の `1` 顧客グループに対して定義されます。
- カタログ価格ルールを使用すると、`Wholesale` 顧客グループに 10% の割引が適用されます。

カタログ価格ルールに対して階層価格設定が使用可能な場合、システムでは次のフローを使用して最終価格を計算します。

1. ユーザーがログインする前に、製品価格は 100 USD （標準の基本価格）と表示されます。

1. 顧客が `Wholesale` グループのメンバーとしてログインした後、製品価格は 90 USD （`Wholesale` グループの階層価格）に調整されます。

1. カタログ価格ルールが適用され、階層価格が 90 USD から 10% 割引になり、最終的に 81 USD になります。

次の表に、カタログ価格ルールに対して階層価格設定が使用可能な場合に、すべての顧客グループに対して 10% の値引が提供される価格計算を要約します。

商品：標準価格$100 （単品購入）

| 顧客グループ | 階層価格（数量=1） | 新しい基本価格 | 最終価格 |
|---|---|---|---|
| すべてのグループ | 未設定 | 100 ドル | $100 - 10% = $90 |
| 卸売 | 固定：$85 | $85 | $85 - 10% = 76.50 ドル |
| Retailer | 20% 割引 | $80 | $80～10% = 72.00 ドル |
| VIP | 15% 割引 | $85 | $85 - 10% = 76.50 ドル |
