---
title: 在庫ソースの無効化
description: ソースを無効にし、場所や連絡先などの情報を変更する方法について説明します。
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
TQID: https://experienceleague.adobe.com/l-S7b-E9rREgJ4AX5Zd6nneSDJe-OioeD-vk8YeSAak
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 406
ht-degree: 0%

---

# ソースを無効にする

すべての注文データが[!DNL Commerce]に保持されるようにするには、ソースを削除できません。 ソース、注文、出荷は互いに直接接続されています。 ソースを無効にし、場所や連絡先などの情報を変更できます。

場所のステータスに応じて、ソースを無効にすることができます。 無効なソースでは、在庫と製品ごとにすべての割り当てが保持されますが、在庫と注文に対してはアクセスされません。

ソースが無効になっている場合：

- [!DNL Inventory Management]は出荷または注文処理のソースを無視し、リストしません。
- 在庫は、集計在庫合計のためにソースから在庫量にアクセスしません。
- 注文出荷を無効な場所に割り当てることはできません。

デフォルトのSourceを無効にすることはできません。 [!DNL Commerce]は、すべての新しいインポート済み製品、バンドル製品、およびサードパーティ製システムのサポートに、このソースを使用します。 カスタムソースはいつでも有効または無効にできます。

ソースを`disabled`に設定すると、次のような場合に役立ちます。

- ストアや倉庫の追加 – 新しいストアフロントを開いたり、新しい倉庫や出荷の場所をオンラインで持ち込んだりする際に、ソースエントリを追加して、インポートを使用して商品の在庫を設定し、潜在的な在庫に接続します。
- 季節的な出荷 – 休日は年の忙しい時期になる可能性があります。 実店舗を適切に在庫し、地元の買い物客に焦点を当てるために、倉庫などの特定の配送場所からのみ出荷を制限することをお勧めします。 または、期間限定で新しい出荷場所を追加して、より高い販売率と受注を処理することもできます。
- 場所を閉じる – 新しい施設への移動または永続的な移動のために場所を閉じる場合、その場所から新しい出荷を停止するには無効にします。

## 1つ以上のカスタムソースを無効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**に移動します。

1. 無効にする有効なカスタムソースごとにチェックボックスを選択します。

1. 左上隅の&#x200B;_アクション_ メニューをクリックし、**[!UICONTROL Disable]**&#x200B;を選択します。

   ![[!DNL Inventory Management] ソース – アクション メニュー](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. 確認ダイアログで、**[!UICONTROL OK]**&#x200B;をクリックします。

## 単一のカスタムソースを有効または無効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**に移動します。

1. カスタムソースを見つけて、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. ![拡張セレクター](../assets/icon-display-expand.png)、_一般_ セクションを展開し、**[!UICONTROL Is Enabled]**&#x200B;を変更します。

   | オプション | 説明 |
   | ----- | ----- |
   | `Yes` | Sourceが有効になっています。 数量が販売可能数量に加算されます。 ソースには、注文の発送時に現在の数量が一覧表示されます。 Source Selection Algorithmは、発送元を確認します。 |
   | `No` | Sourceは無効です。 数量は販売可能数量に追加されません。 注文を出荷する際にソースがリストされない。 配送オプションはこのソースをスキップします。 |

1. **[!UICONTROL Save and Close]**&#x200B;をクリックします。
