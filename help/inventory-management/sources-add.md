---
title: 在庫ソースの追加
description: 倉庫、実店舗、配送センター、ドロップ荷主などの場所のソースを作成する方法を説明します。
exl-id: 1bff9986-8722-4fb5-ac83-41de82325f7b
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# ソースを追加

カスタムソースを使用して、複数の場所からの在庫と注文のフルフィルメントを管理します。 倉庫、実店舗、配送センター、配送業者など、各場所のソースを作成します。 ソースの割り当てと製品ごとの数量の更新

デフォルトのSourceを編集する場合、名前とコードを除くすべての設定を編集できます。 シングルソースマーチャントは、場所に合わせて情報を追加することをお勧めします。

## 在庫ソースの追加

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Inventory]_/**[!UICONTROL Sources]**&#x200B;に移動します。

1. 「**[!UICONTROL Add New Source]**」をクリックします。

   ![ ソースの管理 ](assets/inventory-sources.png)

1. **[!UICONTROL General]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   - 在庫ソースを識別するには、一意の **[!UICONTROL Name]** を入力します。

   - 一意の **[!UICONTROL Code]** を入力します。

     このコードでは、大文字、小文字、数字、ダッシュ、アンダースコアを使用できます。 コードは、在庫への割り当てやデータの書き出しと読み込みの際に使用される一意の ID です。

   - この在庫ソースを使用する準備ができている場合は、**[!UICONTROL Is Enabled]** を `Yes` に設定します。

   - この場所の簡単な **[!UICONTROL Description]** を入力して、クイックリファレンスや追加の詳細を確認します。

   - **[!UICONTROL Latitude]** と **[!UICONTROL Longitude]** には、施設の位置の GPS （全地球測位システム）座標を入力します。

     [Google マップ ][1] で GPS 座標を検索するには、検索ボックスに住所を入力します。 マップ上のマーカーを右クリックし、[**[!UICONTROL What's here?]**] を選択します。 GPS 座標が、住所の下の詳細ボックスに表示されます。

     ![ 一般的なソースオプション ](assets/inventory-source-general.png)

   - この在庫ソースが集荷場所の場合は、**[!UICONTROL Use as Pickup Location]** を `Yes` に設定します。

     既定のSourceは、店舗の集荷注文の集荷場所として使用できません。

1. **[!UICONTROL Contact Info]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   - **[!UICONTROL Contact Name]**：その場所のプライマリ連絡先の氏名を入力します。

   - 場所に連絡するための **[!UICONTROL Email]** アドレスを入力します。

   - **[!UICONTROL Phone]**：市外局番と電話番号を入力します。

   - **[!UICONTROL Fax]**: FAX の市外局番と電話番号（使用可能な場合）を入力します。

     ![ 連絡先情報 ](assets/inventory-source-contact-info.png)

1. **[!UICONTROL Address Data]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   - **[!UICONTROL Country]** を選択します。

   - **[!UICONTROL State/Province]**：州または都道府県の標準省略形を入力します。

   - **[!UICONTROL City]** を入力します。

   - 物理 **[!UICONTROL Street]** アドレスを入力します。

   - **[!UICONTROL Postcode]**：郵便番号を入力します。

     ![ アドレスデータ ](assets/inventory-source-address.png)

1. 前の手順でソースをピックアップ場所として設定した場合は、![ 拡張セレクター ](../assets/icon-display-expand.png) の **[!UICONTROL Pickup Location]** のセクションを展開し、その場所に関する説明情報を指定します。

   - 集荷場所の **[!UICONTROL Frontend Name]** を入力します。

   - 集荷場所の **[!UICONTROL Frontend Description]** を入力します。 このテキスト ボックスを使用して、店舗の営業時間、他のランドマークに対する相対的な場所、または顧客が正しい集荷場所を選択するのに役立つその他の役に立つ情報を表示します。

     ![ 受け取り場所 ](assets/inventory-pickup-location.png)

   ソースを集荷場所として使用する際のメール通知の設定方法について詳しくは、[ 設定リファレンスガイド _の ](../configuration-reference/sales/sales-emails.md) 販売メール_ を参照してください。

1. 作業内容を保存するには、次のいずれかの操作を行います。

   - 作業内容を保存して編集を続行するには、「**[!UICONTROL Save & Continue]**」をクリックします。

   - 作業内容を保存して「ソースの管理」ページに戻るには、下向き矢印（![ メニュー矢印 ](../assets/icon-menu-down-arrow-red.png)）をクリックして「**[!UICONTROL Save & Close]**」を選択します。

   - 現在のソース レコードに対する作業内容を保存し、新しいソースを入力するには、[**[!UICONTROL Save & New]**] を選択します。

## ボタンバー

| ボタン | 説明 |
|--|--|
| [!UICONTROL Back] | ソースの管理ページに戻ります。 |
| [!UICONTROL Reset] | フォーム内のすべてのフィールドを、最後の保存時の値に復元します。 |
| [!UICONTROL Save & Continue] | すべての変更を保存し、さらに編集するためにフォームを開いたままにします。 下向き矢印をクリックして追加のオプションを表示します。<br/>**[!UICONTROL Save & Close]**– 現在のレコードに対する変更を保存し、フォームを閉じて、ソースの管理ページに戻ります。<br/>**[!UICONTROL Save & New]** – 変更を保存し、現在のレコードを閉じて、新しい空白のフォームを開きます。 |

## フィールドの説明

| フィールド | 説明 |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | （必須）管理者ユーザーの在庫ソースを識別する一意の名前。 |
| [!UICONTROL Code] | （必須）在庫ソースを識別するためにシステムで使用される一意の英数字コード。 コードは、大文字、小文字、数字（スペースを入れない）のいずれかまたは両方で入力してください。 必要に応じて、スペースの代わりにハイフンまたはアンダースコアを使用できます。 ソースの作成後にコードを編集することはできません。 これは、在庫にソースを割り当て、製品データの書き出しや読み込みを行う際に使用される一意の ID です。 |
| [!UICONTROL Is Enabled] | 在庫ソースを使用できるかどうかを決定します。 オプション：はい/いいえ |
| [!UICONTROL Description] | 在庫ソース場所の簡単な説明。 管理者ユーザーに役立つ詳細を含めます。 |
| [!UICONTROL Latitude] | GPS のインベントリ ソースの緯度の座標を指定します。 必要に応じて、値を数字で入力し、先頭にプラス記号またはマイナス記号を付けます。 度記号と文字は使用できません。 例：Latitude 32.7555 |
| [!UICONTROL Longitude] | GPS の在庫ソースの経度座標を指定します。 必要に応じて、値を数字で入力し、先頭にプラス記号またはマイナス記号を付けます。 度記号と文字は使用できません。 例：`-97.3308` |
| **[!UICONTROL Contact Info]** | |
| [!UICONTROL Contact Name] | 在庫ソースの場所の主要連絡先の名前。 |
| [!UICONTROL Email] | プライマリ連絡先の電子メール。 |
| [!UICONTROL Phone] | 希望する形式を使用した、プライマリ連絡先の市外局番と電話番号。 例：`(123) 456-7890` または `123-456-7890` |
| [!UICONTROL Fax] | プライマリ連絡先の市外局番と FAX 番号。 |
| **[!UICONTROL Address Data]** | |
| [!UICONTROL Country] | （必須）在庫ソースが存在する国。 |
| [!UICONTROL State/Province] | 在庫ソースが存在する都道府県。 |
| [!UICONTROL City] | 在庫ソースが所在する市区町村。 |
| [!UICONTROL Street] | 在庫ソースの住所。 |
| [!UICONTROL Postcode] | （必須）在庫ソースの郵便番号。 |
| **[!UICONTROL Pickup Location]** | |
| [!UICONTROL Frontend Name] | ストアフロントに表示されるソースのピックアップ場所の名前。 |
| [!UICONTROL Frontend Description] | ストアフロントに表示されるソースの集荷場所の説明。 添付された画像を含めることができます。 |

[1]: https://www.google.com/maps
