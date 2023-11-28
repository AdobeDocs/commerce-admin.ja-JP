---
title: 製品設定 — [!UICONTROL Customizable Options]
description: 製品の場合、 [!UICONTROL Customizable Options] 設定では、テキスト、選択、日付の入力タイプを含む様々なオプションを提供できます。
exl-id: 7d23c5c5-2b2a-4f2a-b843-9c27b851be5f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# 製品設定 — [!UICONTROL Customizable Options]

カスタマイズ可能なオプションを製品に追加すると、テキスト、選択、日付の入力タイプを含む様々なオプションを簡単に提供できます。 在庫のニーズが簡単な場合は、カスタマイズ可能なオプションを使用すると良いソリューションが得られます。 ただし、単一の SKU のバリエーションに基づいているので、在庫の管理や価格ルール条件の基準として使用することはできません。 同じオプションを持つ複数の製品がある場合は、1 つの製品を設定し、そのオプションを他の製品に読み込むことができます。

顧客がカスタマイズ可能なオプションを含む製品を購入すると、選択した各オプションの説明が製品の説明の下に表示され、関連するマークアップ (Markdown) が自動的に品目の価格に適用されます。

![カスタマイズ可能なオプションを含む製品の詳細](./assets/storefront-customizable-option-product-detail.png){width="700" zoomable="yes"}

買い物かごの価格ルールが購入によってトリガーされる場合、最初の計算は製品価格に適用され、2 番目に行項目価格に適用されます。その際、適用可能なカスタマイズ可能なオプションの調整が必要になります。 次の例では、顧客が$74.00 のダッフルバッグに加え、モノグラム用のカスタマイズ可能なオプションを購入します。 基本製品価格に$14.80 のマークアップが適用され、調整された価格は$88.80 と表示されます。この場合、ダッフルバッグの購入は、製品 SKU に基づいて買い物かごの価格ルールをトリガーし、購入に割引を適用し、さらに送料も無料です。 買い物かごの価格ルールは、カスタマイズ可能なオプションでトリガーされませんが、カートの内容に割引が適用されます。これには、カスタマイズ可能なオプションのマークアップが含まれます。

![カスタマイズ可能なオプションと価格ルールを含む買い物かご](./assets/storefront-customizable-option-cart-price-rule.png){width="700" zoomable="yes"}

>[!NOTE]
>
>カタログ価格ルールの割引は、固定価格のカスタマイズ可能なオプションには適用されません。

## カスタマイズ可能なオプションの作成

1. 製品を編集モードで開きます。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Customizable Options]_」セクションに入力します。

1. クリック **[!UICONTROL Add Option]**.

   ![カスタマイズ可能なオプション](./assets/product-customizable-options.png){width="600" zoomable="yes"}

1. 新しいオプション設定を入力します。

   - の場合 **[!UICONTROL Option Title]**」で、オプションの名前を入力します。

   - を設定します。 **[!UICONTROL Option Type]** 」をクリックします。

   - 製品の購入にオプションが不要な場合は、「 **[!UICONTROL Required]** チェックボックス。

1. データ入力タイプに従って、フィールドに入力します。

   - の場合 **[!UICONTROL Title]**」で、このオプションの名前を入力します。

   - （オプション）の場合 **[!UICONTROL Price]**」で、このオプションに適用される基本製品価格から任意のマークアップまたは Markdown を入力します。

   - 設定 **[!UICONTROL Price Type]** を次のいずれかに変更します。

      - `Fixed` ・変動価格は、基本製品の価格と異なり、$1 などの固定金額。
      - `Percentage`  — バリエーションの価格は、基本製品の価格と、10%などの割合で異なります。

   - （オプション） **[!UICONTROL SKU]** を選択します。 オプション SKU は、製品 SKU に追加されるサフィックスです。

   - 次の場合、 _[!UICONTROL Option Type]_次に該当 `File`、ファイルのパラメーターを設定します。 の場合&#x200B;**[!UICONTROL Compatible File Extensions]**の場合は、有効な拡張子をコンマ区切り値 ( `png, jpg, gif`) をクリックします。 の場合&#x200B;**[!UICONTROL Maximum Image Size]**に値を入力する場合は、最大画像サイズをピクセル単位で入力します。 テキスト入力の場合は、**[!UICONTROL Maximum Characters]**.

   ![「Add Values for customization」オプション](./assets/product-customizable-options-add-values.png){width="600" zoomable="yes"}

1. （オプション）カスタマイズ可能な他のオプションを追加する場合は、 **[!UICONTROL Add Option]**.

   - 以前と同様に設定を完了します。

   - オプションの順序を変更するには、 _[!UICONTROL Order]_![並べ替え順アイコン](../assets/icon-sort-order.png) アイコンをクリックし、リスト内の新しい位置にオプションをドラッグします。

   追加する各オプションに対して、この手順を繰り返します。

1. 完了したら、「 **[!UICONTROL Save]**.

## 読み込みのカスタマイズ可能なオプション

1. Adobe Analytics の _カスタマイズ可能なオプション_ セクションで、 **[!UICONTROL Import Options]**.


1. カスタマイズ可能なオプションを持つすべての製品がグリッドに表示されます。

1. リストで、読み込むオプションを含む製品のチェックボックスを選択します。

1. クリック **[!UICONTROL Import]**.

1. 完了したら、引き続きカスタムオプションを追加するか、 **[!UICONTROL Save and Close]**.

## 入力タイプ

| タイプ | 説明 |
|---------------------|---------------|
| [!UICONTROL Text] | 顧客が必要な情報を入力できる入力行またはテキストボックス。 オプション：<br />**[!UICONTROL Field]**— テキストの 1 行の入力フィールド。<br />**[!UICONTROL Area]**  — 複数行の入力フィールド。 このタイプは、HTMLなどの高度な書式設定をサポートしていません。 「最大文字数」を使用して、入力できるテキストの長さを制限し、入力したテキストが管理者で正しく表現されるようにします。 |
| [!UICONTROL File] | ユーザーがファイルをアップロードできるようにします。 |
| [!UICONTROL Select] | お客様が、使用する入力タイプに応じて、1 つまたは複数のオプションを選択できるようにします。 オプション：<br />**[!UICONTROL Drop-down]**- 1 つの選択のみ可能なオプションのドロップダウンリスト。<br />**[!UICONTROL Radio Buttons]** - 1 つの選択のみを許可する一連のオプション。<br />**[!UICONTROL Checkbox]**— チェックボックスは、はい/いいえのオプションのバリエーションです。 製品に複数のチェックボックスがある場合は、複数の選択を行うことができます。<br />**[!UICONTROL Multiple Select]**  — 複数の選択を受け入れるオプションのドロップダウンリストボックス。 複数のオプションを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。 |
| [!UICONTROL Date] | 顧客が日付や時刻を入力したり、カレンダーから値を選択したりできます。 オプション： <br />**[!UICONTROL Date]**— 日付値の入力フィールド。 日付は、フィールドに直接入力することも、リストまたはカレンダーから選択することもできます。 入力方法と形式は、 [日付と時間のオプション](attributes-input-types.md#date-and-time-options) 設定。<br />**[!UICONTROL Date & Time]**  — 日付と時刻の値の入力フィールド。<br />**[!UICONTROL Time]**— 時間値の入力フィールド。 |

{style="table-layout:auto"}
