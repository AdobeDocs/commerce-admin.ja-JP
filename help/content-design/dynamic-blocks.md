---
title: 動的ブロック
description: 動的ブロックを使用して、価格ルールや顧客セグメントのロジックによって駆動される、リッチでインタラクティブなコンテンツを作成します。
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# 動的ブロック

{{ee-feature}}

次のロジックに基づいて駆動される、リッチでインタラクティブなコンテンツを作成 [価格ルール](../merchandising-promotions/introduction.md#price-rules) および [顧客セグメント](../customers/customer-segments.md). 既存 [動的ブロック](../page-builder/dynamic-block.md) は、 [!DNL Page Builder] [ステージ](../page-builder/workspace.md). 動的ブロックの詳細な手順の例については、 [チュートリアル 2：ブロック](../page-builder/2-blocks.md).

>[!NOTE]
>
>The _[!UICONTROL Banner]_オプションを [[!UICONTROL Content] メニュー](content-menu.md) は 2.3.1 で廃止され、2.4.0 で削除されました。その機能はダイナミックブロックに置き換えられます。

![[!DNL Page Builder]  — 価格ルールと顧客セグメントを含む動的ブロック](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## 手順 1：ダイナミックブロックを作成する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![動的ブロックリスト](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. 右上隅で、 **[!UICONTROL Add Dynamic Block]**.

   ![新しいダイナミックブロック](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. 該当する場合は、 **[!UICONTROL Store View]** ダイナミックブロックを表示する特定のストアビューに追加します。

1. ダイナミックブロックをアクティブにするには、 **[!UICONTROL Enable Dynamic Block]** から `Yes`.

1. 内部参照の場合は、 **[!UICONTROL Dynamic Block Name]**.

1. 設定 **[!UICONTROL Dynamic Block Type]** ダイナミックブロックを表示するページ領域にドラッグし、 **[!UICONTROL Done]**.

   ![ダイナミックブロックタイプの設定](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Customer Segment]** リストで、動的ブロックを表示する各セグメントのチェックボックスを選択し、 **[!UICONTROL Done]** をクリックして設定を保存します。

   ![顧客セグメントの選択](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- セグメントが作成されていない場合、動的ブロックは全員に表示されます。
   >- 顧客がどのセグメントにも属していない場合で、すべてのセグメントに対して動的ブロックが作成された場合でも、動的ブロックのコンテンツは表示されます。
   >- ダイナミックブロックに割り当てられているすべての顧客セグメントが削除された場合、その内容は全員に表示されます。

### 動的ブロックでのReal-Time CDPオーディエンスの使用

次の場合、 [インストール済み](../customers/audience-activation.md#install-the-extension) および [設定済み](../customers/audience-activation.md#configure-the-extension) の [!DNL Audience Activation] 拡張機能には、 **[!UICONTROL Audiences]**.

![Real-Time CDPオーディエンスを選択](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

Adobe Analytics の **[!UICONTROL Real-Time CDP Audience]** リストで、動的ブロックを表示する各オーディエンスのチェックボックスを選択し、 **[!UICONTROL Done]** をクリックして設定を保存します。

## 手順 2：コンテンツの完了

以下を使用します。 [!DNL Page Builder] [workspace](../page-builder/workspace.md) をクリックして、コンテンツを完了します。

![[!DNL Page Builder]  — 動的ブロックワークスペース](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## 手順 3：関連するプロモーションの選択

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. 動的ブロックに関連付けるプロモーションのタイプをクリックします。

   - **[!UICONTROL Add Cart Price Rules]** ( [買い物かごの価格ルール](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** ( [カタログ価格ルール](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >カタログ価格ルールは、Real-Time CDPオーディエンスではサポートされていません。

1. 使用可能なルールのリストで、使用する各ルールのチェックボックスを選択し、 **[!UICONTROL Add Selected]**.

1. ダイナミックブロックが完了したら、 **[!UICONTROL Save]**.

## 手順 4：ページにダイナミックブロックを追加する

1. ダイナミックブロックを表示するページを開きます。

1. 以下を使用します。 [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) ステージにダイナミックブロックを追加するコンテンツタイプ。

## フィールドとツールの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Store View] | ダイナミックブロックを使用できるストアビューを指定します。 |
| [!UICONTROL Enable Dynamic Block] | ダイナミックブロックをアクティブまたは非アクティブにします。 オプション：はい/いいえ |
| [!UICONTROL Dynamic Block Name] | 管理者内の動的ブロックを識別するわかりやすい名前。 |
| [!UICONTROL Dynamic Block Type] | 内の場所を識別します。 [標準ページレイアウト](layout-updates.md) ダイナミックブロックが配置されている場所。 オプション： <br/>**[!UICONTROL Content Area]**— ダイナミックブロックをメインに配置します [コンテンツ領域](layout-updates.md) 」と入力します。<br/>**[!UICONTROL Footer]**  — 動的ブロックをページに配置します [フッター](page-setup.md#footer). <br/>**[!UICONTROL Header]**— 動的ブロックをページに配置します [ヘッダー](page-setup.md#header).<br/>**[!UICONTROL Left Column]**  — ダイナミックブロックを [左サイドバー](page-layout.md#standard-page-layouts) 2 列または 3 列のレイアウトの <br/>**[!UICONTROL Right Column]**— ダイナミックブロックを [右サイドバー](page-layout.md#standard-page-layouts) 2 列または 3 列のレイアウトの |
| 顧客セグメント | 顧客セグメントを動的ブロックに関連付けて、どの顧客が表示できるかを決定します。 |
| Real-Time CDP Audience | を関連付けます。 [Real-Time CDPオーディエンス](../customers/audience-activation.md) 動的ブロックを使用して、どの顧客に表示できるかを決定します。 |

{style="table-layout:auto"}

### 内容

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Layout] | ステージに行、列またはタブを追加します。 |
| [!UICONTROL Elements] | ステージ上の任意のレイアウトコンテナに、テキスト、見出し、ボタン、HTML、区切り文字および配置コードを追加します。 |
| [!UICONTROL Media] | 画像、ビデオ、バナー、スライダーおよびGoogleマップを、ステージ上の既存のレイアウトコンテナに追加します。 |
| [!UICONTROL Add Content] | 既存のブロック、動的ブロック、製品をステージに追加します。 |

{style="table-layout:auto"}

### 関連するプロモーション

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]**  — 既存の [買い物かごの価格ルール](../merchandising-promotions/price-rules-cart.md) をプロモーションとして使用します。 |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]**  — 既存の [カタログ価格ルール](../merchandising-promotions/price-rules-catalog.md) をプロモーションとして使用します。 |

{style="table-layout:auto"}
