---
title: ダイナミック ブロック
description: 動的ブロックを使用して、価格ルールと顧客セグメントからのロジックによって駆動される、リッチでインタラクティブなコンテンツを作成します。
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# ダイナミック ブロック

{{ee-feature}}

[&#x200B; 価格ルール &#x200B;](../merchandising-promotions/introduction.md#price-rules) および [&#x200B; 顧客セグメント &#x200B;](../customers/customer-segments.md) のロジックによって駆動される、リッチでインタラクティブなコンテンツを作成します。 既存の [&#x200B; ダイナミック ブロック &#x200B;](../page-builder/dynamic-block.md) を [!DNL Page Builder] ージ [&#x200B; ステージ &#x200B;](../page-builder/workspace.md) に直接追加できます。 ダイナミック ブロックを使用する詳細な手順の例については、[&#x200B; チュートリアル 2: ブロック &#x200B;](../page-builder/2-blocks.md) を参照してください。

>[!NOTE]
>
>[[!UICONTROL Content] メニューの _[!UICONTROL Banner]_&#x200B;オプションは &#x200B;](content-menu.md)2.3.1 で非推奨となり、2.4.0 で削除されました。その機能はダイナミック ブロックに置き換えられています。

![[!DNL Page Builder] – 価格ルールと顧客セグメントを含むダイナミックブロック &#x200B;](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## 手順 1：ダイナミックブロックの作成

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Dynamic Blocks]**&#x200B;に移動します。

   ![&#x200B; ダイナミック ブロック リスト &#x200B;](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. 右上隅の「**[!UICONTROL Add Dynamic Block]**」をクリックします。

   ![&#x200B; 新規ダイナミック ブロック &#x200B;](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. 必要に応じて、動的ブロックを表示する特定のストア表示に **[!UICONTROL Store View]** を設定します。

1. ダイナミック ブロックをアクティブにするには、**[!UICONTROL Enable Dynamic Block]** を `Yes` に設定します。

1. 内部参照の場合は、わかりやすい **[!UICONTROL Dynamic Block Name]** を入力します。

1. ダイナミックブロックを表示するページの領域に **[!UICONTROL Dynamic Block Type]** を設定し、「**[!UICONTROL Done]**」をクリックします。

   ![&#x200B; ダイナミック ブロック タイプを設定する &#x200B;](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. **[!UICONTROL Customer Segment]** リストで、動的ブロックを表示する各セグメントのチェックボックスをオンにし、「**[!UICONTROL Done]**」をクリックして設定を保存します。

   ![&#x200B; 顧客セグメントの選択 &#x200B;](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- セグメントが作成されない場合、ダイナミック ブロックはすべてのユーザに表示されます。
   >- 顧客がどのセグメントにも属しておらず、ダイナミック ブロックがすべてのセグメントに対して作成されている場合、ダイナミック ブロックのコンテンツは表示されたままになります。
   >- 動的ブロックに割り当てられたすべての顧客セグメントが削除されると、そのコンテンツは全員に表示されます。

### 動的ブロックでのReal-Time CDP オーディエンスの使用

[!DNL Audience Activation] 拡張機能を [&#x200B; インストール &#x200B;](../customers/audience-activation.md#install-the-extension) および [&#x200B; 設定 &#x200B;](../customers/audience-activation.md#configure-the-extension) した場合は、「**[!UICONTROL Audiences]**」というセクションが表示されます。

![Real-Time CDP オーディエンスを選択 &#x200B;](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

**[!UICONTROL Real-Time CDP Audience]** リストで、動的ブロックを表示する各オーディエンスのチェックボックスをオンにし、「**[!UICONTROL Done]**」をクリックして設定を保存します。

## 手順 2：コンテンツを完了する

[!DNL Page Builder] [&#x200B; ワークスペース &#x200B;](../page-builder/workspace.md) を使用して、コンテンツを完了します。

![[!DNL Page Builder] - ダイナミック ブロック ワークスペース &#x200B;](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## 手順 3：関連プロモーションの選択

1. 下にスクロールして、![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)**[!UICONTROL Related Promotions]** を展開します。

1. ダイナミックブロックに関連付けるプロモーションのタイプをクリックします。

   - **[!UICONTROL Add Cart Price Rules]** （[&#x200B; 買い物かご価格ルール &#x200B;](../merchandising-promotions/price-rules-cart.md)）

   - **[!UICONTROL Add Catalog Price Rules]** （[&#x200B; カタログ価格ルール &#x200B;](../merchandising-promotions/price-rules-catalog.md)）

   >[!NOTE]
   >
   >カタログ価格ルールは、Real-Time CDP オーディエンスではサポートされていません。

1. 使用可能なルールのリストで、使用する各ルールのチェックボックスをオンにし、「**[!UICONTROL Add Selected]**」をクリックします。

1. ダイナミック ブロックが完成したら、[**[!UICONTROL Save]**] をクリックします。

## 手順 4：ページへの動的ブロックの追加

1. ダイナミックブロックを表示するページを開きます。

1. [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) コンテンツタイプを使用して、動的ブロックをステージに追加します。

## フィールドとツールの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Store View] | ダイナミック ブロックを使用できるストア ビューを指定します。 |
| [!UICONTROL Enable Dynamic Block] | ダイナミック ブロックをアクティブまたは非アクティブにします。 オプション：はい/いいえ |
| [!UICONTROL Dynamic Block Name] | 管理画面で動的ブロックを識別するわかりやすい名前。 |
| [!UICONTROL Dynamic Block Type] | ダイナミック ブロックが配置される [&#x200B; 標準ページ レイアウト &#x200B;](layout-updates.md) 内の場所を識別します。 オプション：<br/>**[!UICONTROL Content Area]**- ページのメイン [&#x200B; コンテンツ領域 &#x200B;](layout-updates.md) に動的ブロックを配置します。<br/>**[!UICONTROL Footer]** - ページに動的ブロックを配置します [&#x200B; フッター &#x200B;](page-setup.md#footer)。 <br/>**[!UICONTROL Header]**- ページに動的ブロックを配置します [&#x200B; ヘッダー &#x200B;](page-setup.md#header)。<br/>**[!UICONTROL Left Column]** - 2 列または 3 列のレイアウトの [&#x200B; 左側のサイドバー &#x200B;](page-layout.md#standard-page-layouts) に動的ブロックを配置します。 <br/>**[!UICONTROL Right Column]**- 2 列または 3 列のレイアウトの [&#x200B; 右側のサイドバー &#x200B;](page-layout.md#standard-page-layouts) にダイナミックブロックを配置します。 |
| 顧客セグメント | 顧客セグメントを動的ブロックに関連付けて、どの顧客に表示できるかを決定します。 |
| Real-Time CDP オーディエンス | [Real-Time CDP オーディエンス &#x200B;](../customers/audience-activation.md) を動的ブロックに関連付けて、どの顧客に表示できるかを決定します。 |

{style="table-layout:auto"}

### 目次

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Layout] | 行、列、タブをステージに追加します。 |
| [!UICONTROL Elements] | ステージ上の任意のレイアウトコンテナにテキスト、見出し、ボタン、区切り文字、HTML コードを追加できます。 |
| [!UICONTROL Media] | 画像、ビデオ、バナー、スライダー、Googleマップを、ステージ上の既存のレイアウトコンテナに追加します。 |
| [!UICONTROL Add Content] | 既存のブロック、ダイナミック ブロック、および製品をステージに追加します。 |

{style="table-layout:auto"}

### 関連するプロモーション

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]** – 既存の [&#x200B; 買い物かご価格ルール &#x200B;](../merchandising-promotions/price-rules-cart.md) を動的ブロックにプロモーションとして関連付けます。 |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]** – 既存の [&#x200B; カタログ価格ルール &#x200B;](../merchandising-promotions/price-rules-catalog.md) をプロモーションとして動的ブロックに関連付けます。 |

{style="table-layout:auto"}
