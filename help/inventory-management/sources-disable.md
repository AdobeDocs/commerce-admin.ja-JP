---
title: 在庫ソースの無効化
description: ソースを無効にする方法と、情報（場所や連絡先など）を変更する方法について説明します。
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# ソースを無効にする

すべての注文データが [!DNL Commerce] に保持されていることを確認するために、ソースを削除することはできません。 ソース、注文および出荷は相互に直接接続されています。 ソースを無効にしたり、場所や連絡先などの情報を変更したりできます。

場所のステータスに応じて、ソースを無効にした方がよいでしょう。 無効なソースでは、在庫および製品ごとのすべての割り当てが保持されますが、在庫および注文についてはアクセスされません。

ソースが無効の場合：

- [!DNL Inventory Management] は、出荷または受注処理のソースを無視し、リストしません。
- 在庫は、集計された在庫合計のソースからの在庫数量にアクセスしません。
- 無効な場所には注文出荷を割り当てることができません。

デフォルトのSourceは無効にできません。 [!DNL Commerce] では、このソースを、読み込まれたすべての製品、バンドル製品、サードパーティのシステムサポートに使用します。 カスタムソースはいつでも有効または無効にできます。

ソースを `disabled` に設定すると、次の状況で役立ちます。

- 店舗または倉庫の追加 – 新しい店舗を開いたり、新しい倉庫および出荷場所をオンラインにしたりする際に、インポートを使用して製品在庫を設定し、潜在在庫に接続するためのソース エントリを追加します。
- 季節の出荷 – 休日は年の忙しい時間になる可能性があります。 倉庫などの特定の出荷場所からのみ出荷を制限して、実店舗の場所を十分に在庫し、地元の買い物客に焦点を当てたい場合があります。 または、新しい出荷場所を期間限定で追加して、より高い割合の販売および入荷オーダーを処理することもできます。
- 事業所のクローズ：事業所を新規の施設に移動するためにクローズする場合、または永続的にクローズする場合は、事業所からの新規出荷を停止できないようにします。

## 1 つ以上のカスタムソースを無効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Inventory]_/**[!UICONTROL Sources]**&#x200B;に移動します。

1. 無効にする有効なカスタムソースごとにチェックボックスを選択します。

1. 左上隅の _アクション_ メニューをクリックして、「**[!UICONTROL Disable]**」を選択します。

   ![[!DNL Inventory Management] ソース – アクションメニュー ](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. 確認ダイアログで、「**[!UICONTROL OK]**」をクリックします。

## 単一のカスタムソースを有効または無効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Inventory]_/**[!UICONTROL Sources]**&#x200B;に移動します。

1. カスタムソースを見つけて、「**[!UICONTROL Edit]**」をクリックします。

1. 「![ 拡張セレクター ](../assets/icon-display-expand.png) 「_一般_」セクションを展開し、**[!UICONTROL Is Enabled]** を変更します。

   | オプション | 説明 |
   | ----- | ----- |
   | `Yes` | Sourceは有効です。 数量が「販売可能数量」に加算されます。 注文を出荷する際の現在の数量を含むソース リスト。 Source Selection Algorithm は、出荷用のソースをチェックします。 |
   | `No` | Sourceは無効です。 数量は、販売可能数量には追加されません。 注文を出荷する際にソースがリストされない。 このソースは配送オプションによってスキップされます。 |

1. 「**[!UICONTROL Save and Close]**」をクリックします。
