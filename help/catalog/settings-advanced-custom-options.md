---
title: 製品設定 – [!UICONTROL Customizable Options]
description: 製品の場合、[!UICONTROL Customizable Options] の設定を使用すると、テキスト、選択、日付入力タイプのオプションを選択できます。
exl-id: 7d23c5c5-2b2a-4f2a-b843-9c27b851be5f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---

# 製品設定 – [!UICONTROL Customizable Options]

製品にカスタマイズ可能なオプションを追加すると、テキスト、選択、日付入力タイプの様々なオプションを簡単に提供できます。 カスタマイズ可能なオプションは、在庫のニーズがシンプルな場合に適したソリューションです。 ただし、これらは単一の SKU のバリエーションに基づいているので、在庫の管理や価格ルール条件の基礎として使用することはできません。 同じオプションを持つ製品が複数ある場合は、1 つの製品を設定して、そのオプションを他の製品に読み込むことができます。

顧客がカスタマイズ可能なオプションを使用して製品を購入すると、選択した各オプションの説明が製品の説明の下に表示され、関連するマークアップ（マークダウン）が項目の価格に自動的に適用されます。

![ 製品の詳細とカスタマイズ可能なオプション ](./assets/storefront-customizable-option-product-detail.png){width="700" zoomable="yes"}

買い物かごの価格ルールが購入によってトリガーされた場合、最初の計算は製品価格に最初に適用され、2 番目は品目価格に適用され、適用可能なカスタマイズ可能なオプションの調整が行われます。 次の例では、顧客はダッフルバッグを 74.00 ドルで購入し、さらにモノグラム用のカスタマイズ可能なオプションを購入します。 ベースの製品価格に$14.80 のマークアップが適用され、調整済みの価格は$88.80 と表示されます。この場合、ダッフルバッグの購入は、商品 SKU に基づいて買い物かご価格ルールをトリガーし、購入に割引を適用し、送料無料を適用します。 買い物かごの価格ルールは、カスタマイズ可能なオプションによってトリガーされませんが、カスタマイズ可能なオプションのマークアップを含む割引を買い物かごのコンテンツに適用します。

![ カスタマイズ可能なオプションと価格ルールを備えた買い物かご ](./assets/storefront-customizable-option-cart-price-rule.png){width="700" zoomable="yes"}

>[!NOTE]
>
>カタログ価格ルール割引は、固定価格のカスタマイズ可能なオプションには適用されません。

## カスタマイズ可能なオプションの作成

1. 製品を編集モードで開きます。

1. 下にスクロールして、「_[!UICONTROL Customizable Options]_」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

1. 「**[!UICONTROL Add Option]**」をクリックします。

   ![ カスタマイズ可能なオプション ](./assets/product-customizable-options.png){width="600" zoomable="yes"}

1. 新しいオプション設定を完了します。

   - **[!UICONTROL Option Title]**：オプションの名前を入力します。

   - データ入力のタイプの **[!UICONTROL Option Type]** を設定します。

   - 製品の購入にオプションが必要ない場合は、「**[!UICONTROL Required]**」チェックボックスの選択を解除します。

1. データ入力タイプに従ってフィールドに入力します。

   - **[!UICONTROL Title]**：このオプションの名前を入力します。

   - （任意） **[!UICONTROL Price]** の場合は、このオプションに適用される基本製品価格からのマークアップまたはマークダウンを入力します。

   - **[!UICONTROL Price Type]** を次のいずれかに設定します。

      - `Fixed` - バリエーションの価格は、基本商品の価格と$1 などの固定金額で異なります。
      - `Percentage` - バリエーションの価格と基本製品の価格が 10% などのパーセンテージで異なります。

   - （オプション）オプションの **[!UICONTROL SKU]** を入力します。 オプション SKU は、製品 SKU に追加されるサフィックスです。

   - _[!UICONTROL Option Type]_が `File` の場合は、ファイルのパラメーターを設定します。**[!UICONTROL Compatible File Extensions]**の場合は、有効な拡張子をコンマ区切り値（`png, jpg, gif` など）で入力します。**[!UICONTROL Maximum Image Size]**しくは、画像の最大サイズをピクセル単位で入力します。 テキスト入力の場合は、**[!UICONTROL Maximum Characters]**の最大値を入力します。

   ![ カスタマイズの値を追加オプション ](./assets/product-customizable-options-add-values.png){width="600" zoomable="yes"}

1. （オプション）別のカスタマイズ可能なオプションを追加する場合は、「**[!UICONTROL Add Option]**」をクリックします。

   - 前と同じように設定を完了します。

   - オプションの順序を変更するには、「並べ替え _[!UICONTROL Order]_順アイコン ![ アイコンをクリックし ](../assets/icon-sort-order.png) リストの新しい位置にオプションをドラッグします。

   追加する各オプションに対して、この手順を繰り返します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## カスタマイズ可能なオプションをインポート

1. [_カスタマイズ可能なオプション_] セクションで、[**[!UICONTROL Import Options]**] をクリックします。


1. カスタマイズ可能なオプションを持つすべての製品がグリッドに表示されます。

1. リストで、読み込むオプションを含む製品のチェックボックスをオンにします。

1. 「**[!UICONTROL Import]**」をクリックします。

1. 完了したら、引き続きカスタムオプションを追加するか、「**[!UICONTROL Save and Close]**」をクリックできます。

## 入力タイプ

| タイプ | 説明 |
|---------------------|---------------|
| [!UICONTROL Text] | 顧客が必要な情報を入力できる入力行またはテキストボックス。 Options:<br />**[!UICONTROL Field]**- テキストの 1 行入力フィールド。<br />**[!UICONTROL Area]** – 複数行の入力フィールド。 このタイプでは、HTMLなどの高度な書式設定はサポートされていません。 最大文字数を使用すると、入力できるテキストの長さを制限でき、管理者で入力したテキストが正しく表示されるようにします。 |
| [!UICONTROL File] | 顧客がファイルをアップロードできるようにします。 |
| [!UICONTROL Select] | 使用する入力タイプに応じて、1 つまたは複数のオプションを選択できるようにします。 Options:<br />**[!UICONTROL Drop-down]**- 1 つの選択のみを許可するオプションのドロップダウンリスト。<br />**[!UICONTROL Radio Buttons]** - 1 つしか選択できない一連のオプション。<br />**[!UICONTROL Checkbox]**- チェックボックスは、yes/no オプションのバリエーションです。 製品に複数のチェックボックスがある場合は、複数の選択を行うことができます。<br />**[!UICONTROL Multiple Select]** – 複数の選択を受け入れるオプションのドロップダウンリストボックス。 複数のオプションを選択するには、Ctrl （PC）キーまたは Command （Mac）キーを押しながら、各オプションをクリックします。 |
| [!UICONTROL Date] | 顧客が日付や時刻を入力したり、カレンダーから値を選択したりできます。 オプション：<br />**[!UICONTROL Date]**– 日付値の入力フィールド。 日付は、フィールドに直接入力することも、リストやカレンダーから選択することもできます。 入力の方法と形式は、「日付と時刻のオプション [ の設定によって決 ](attributes-input-types.md#date-and-time-options) ります。<br />**[!UICONTROL Date & Time]** – 日時の値の入力フィールド。<br />**[!UICONTROL Time]**– 時間値の入力フィールド。 |

{style="table-layout:auto"}
