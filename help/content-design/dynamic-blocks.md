---
title: ダイナミック ブロック
description: 動的ブロックを使用して、価格ルールと顧客セグメントからのロジックによって駆動される、リッチでインタラクティブなコンテンツを作成します。
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 0%

---

# ダイナミック ブロック

{{ee-feature}}

からのロジックによって駆動される、リッチでインタラクティブなコンテンツの作成 [価格ルール](../merchandising-promotions/introduction.md#price-rules) および [顧客セグメント](../customers/customer-segments.md). 既存 [ダイナミック ブロック](../page-builder/dynamic-block.md) に直接追加できます [!DNL Page Builder] [ステージ](../page-builder/workspace.md). ダイナミック ブロックを使用する詳細な手順の例については、を参照してください。 [チュートリアル 2: ブロック](../page-builder/2-blocks.md).

>[!NOTE]
>
>この _[!UICONTROL Banner]_のオプション [[!UICONTROL Content] メニュー](content-menu.md) は 2.3.1 で非推奨となり、2.4.0 で削除されました。その機能はダイナミック ブロックに置き換えられています。

![[!DNL Page Builder]  – 価格ルールと顧客セグメントを含むダイナミックブロック](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## 手順 1：ダイナミックブロックの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![ダイナミック ブロック リスト](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. 右上隅のをクリックします。 **[!UICONTROL Add Dynamic Block]**.

   ![新規ダイナミック ブロック](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. 該当する場合、を設定します **[!UICONTROL Store View]** を指定して、ダイナミック ブロックが表示される特定のストア ビューを表示します。

1. ダイナミック ブロックをアクティブにするには、を設定します **[!UICONTROL Enable Dynamic Block]** 対象： `Yes`.

1. 内部参照の場合は、説明的なを入力します **[!UICONTROL Dynamic Block Name]**.

1. を設定 **[!UICONTROL Dynamic Block Type]** をクリックして、ダイナミックブロックを表示するページの領域に移動し、 **[!UICONTROL Done]**.

   ![ダイナミック ブロック タイプを設定する](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. が含まれる **[!UICONTROL Customer Segment]** リストで、ダイナミックブロックを表示する各セグメントのチェックボックスを選択し、をクリックします **[!UICONTROL Done]** 設定を保存します。

   ![顧客セグメントの選択](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- セグメントが作成されない場合、ダイナミック ブロックはすべてのユーザに表示されます。
   >- 顧客がどのセグメントにも属しておらず、ダイナミック ブロックがすべてのセグメントに対して作成されている場合、ダイナミック ブロックのコンテンツは表示されたままになります。
   >- 動的ブロックに割り当てられたすべての顧客セグメントが削除されると、そのコンテンツは全員に表示されます。

### 動的ブロックでのReal-Time CDP オーディエンスの使用

次の場合： [installed](../customers/audience-activation.md#install-the-extension) および [設定済み](../customers/audience-activation.md#configure-the-extension) この [!DNL Audience Activation] 拡張機能には、というセクションが表示されます。 **[!UICONTROL Audiences]**.

![Real-Time CDP オーディエンスを選択](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

が含まれる **[!UICONTROL Real-Time CDP Audience]** リストで、動的ブロックを表示する各オーディエンスのチェックボックスをオンにし、クリックします。 **[!UICONTROL Done]** 設定を保存します。

## 手順 2：コンテンツを完了する

の使用 [!DNL Page Builder] [workspace](../page-builder/workspace.md) をクリックしてコンテンツを完了します。

![[!DNL Page Builder] - ダイナミックブロックワークスペース](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## 手順 3：関連プロモーションの選択

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. ダイナミックブロックに関連付けるプロモーションのタイプをクリックします。

   - **[!UICONTROL Add Cart Price Rules]** （を参照） [買い物かご価格ルール](../merchandising-promotions/price-rules-cart.md)）

   - **[!UICONTROL Add Catalog Price Rules]** （を参照） [カタログ価格ルール](../merchandising-promotions/price-rules-catalog.md)）

   >[!NOTE]
   >
   >カタログ価格ルールは、Real-Time CDP オーディエンスではサポートされていません。

1. 使用可能なルールのリストで、使用する各ルールのチェックボックスをオンにし、 **[!UICONTROL Add Selected]**.

1. ダイナミック ブロックが完成したら、 **[!UICONTROL Save]**.

## 手順 4：ページへの動的ブロックの追加

1. ダイナミックブロックを表示するページを開きます。

1. の使用 [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) コンテンツタイプを使用して、動的ブロックをステージに追加します。

## フィールドとツールの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Store View] | ダイナミック ブロックを使用できるストア ビューを指定します。 |
| [!UICONTROL Enable Dynamic Block] | ダイナミック ブロックをアクティブまたは非アクティブにします。 オプション：はい/いいえ |
| [!UICONTROL Dynamic Block Name] | 管理画面で動的ブロックを識別するわかりやすい名前。 |
| [!UICONTROL Dynamic Block Type] | 内の場所を識別 [標準ページレイアウト](layout-updates.md) ダイナミック ブロックが配置される場所。 オプション： <br/>**[!UICONTROL Content Area]**- ダイナミック ブロックをメインに配置します [コンテンツ領域](layout-updates.md) を表示します。<br/>**[!UICONTROL Footer]** - ダイナミックブロックをページに配置します [フッター](page-setup.md#footer). <br/>**[!UICONTROL Header]**- ダイナミックブロックをページに配置します [ヘッダー](page-setup.md#header).<br/>**[!UICONTROL Left Column]**  – 動的ブロックを [左サイドバー](page-layout.md#standard-page-layouts) （2 カラムまたは 3 カラムのレイアウト）。 <br/>**[!UICONTROL Right Column]**– 動的ブロックを [右側のサイドバー](page-layout.md#standard-page-layouts) （2 列または 3 列のレイアウト）。 |
| 顧客セグメント | 顧客セグメントを動的ブロックに関連付けて、どの顧客に表示できるかを決定します。 |
| Real-Time CDP オーディエンス | を関連付けます [Real-Time CDP オーディエンス](../customers/audience-activation.md) を動的ブロックに置き換えて、どの顧客に表示するかを決定します。 |

{style="table-layout:auto"}

### 目次

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Layout] | 行、列、タブをステージに追加します。 |
| [!UICONTROL Elements] | ステージ上の任意のレイアウトコンテナにテキスト、見出し、ボタン、区切り文字、HTMLコードを追加できます。 |
| [!UICONTROL Media] | 画像、ビデオ、バナー、スライダー、Googleマップを、ステージ上の既存のレイアウトコンテナに追加します。 |
| [!UICONTROL Add Content] | 既存のブロック、ダイナミック ブロック、および製品をステージに追加します。 |

{style="table-layout:auto"}

### 関連するプロモーション

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]**  – 既存のを関連付ける [買い物かご価格ルール](../merchandising-promotions/price-rules-cart.md) プロモーションとしてダイナミックブロックを使用します。 |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]**  – 既存のを関連付ける [カタログ価格ルール](../merchandising-promotions/price-rules-catalog.md) プロモーションとしてダイナミックブロックを使用します。 |

{style="table-layout:auto"}
