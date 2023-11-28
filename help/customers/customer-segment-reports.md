---
title: 顧客セグメントレポート
description: 顧客セグメントレポートには、各セグメントの顧客数に関する情報が表示されます。
exl-id: a767ee80-7b6e-4acd-9772-2f8adcf3233e
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 1%

---

# 顧客セグメントレポート

{{ee-feature}}

顧客セグメントレポートは、各セグメントの顧客数に関する情報を提供します。

![顧客セグメントレポート](assets/customer-segments-reports.png){width="700" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| **[!UICONTROL Select]** | アクションの対象となる各セグメントのチェックボックスを選択するか、列ヘッダーの選択コントロールを使用します。 オプション： `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| **[!UICONTROL ID]** | 各セグメントに割り当てられる一意の数値識別子 |
| **[!UICONTROL Segment]** | セグメント名 |
| **[!UICONTROL Status]** | セグメントのステータス。 オプション： `Active` / `Inactive` |
| **[!UICONTROL Website]** | セグメントが割り当てられる Web サイト |
| **[!UICONTROL Customers]** | セグメントに割り当てられた顧客の数 |

{style="table-layout:auto"}

セグメント内の顧客のリストにドリルダウンして、データを書き出すことができます。

![顧客データの詳細](assets/customer-segment-drilldown.png){width="600" zoomable="yes"}

最新のデータを確実に取得するには、セグメントデータを更新する必要があります。 セグメントデータが使用できない場合や古い場合は、 **[!UICONTROL Refresh Segment Data]** をクリックします。

1. の場合 **[!UICONTROL Export to]**、書き出し形式を選択します。

   * CSV — プレーンテキストデータを含む、値をコンマで区切ったファイル。
   * Excel XML - XML ベースのスプレッドシートデータ形式。

1. クリック **[!UICONTROL Export]**.

   | 列 | 説明 |
   |--- |--- |
   | **[!UICONTROL ID]** | 各ユーザーに割り当てられる一意の数値識別子 |
   | **[!UICONTROL Name]** | 顧客名 |
   | **[!UICONTROL Email]** | 登録顧客の電子メールアドレス |
   | **[!UICONTROL Group]** | 顧客が割り当てられる顧客グループ |
   | **[!UICONTROL Phone]** | 顧客の電話番号 |
   | **[!UICONTROL ZIP]** | 顧客の所在地の郵便番号 |
   | **[!UICONTROL Country]** | 顧客の所在地の国 |
   | **[!UICONTROL State/Province]** | 顧客の所在地の州または都道府県 |
   | **[!UICONTROL Customer Since]** | 顧客アカウントが作成された日時 |

   {style="table-layout:auto"}

1. 生成されたファイルは、ローカルマシンに自動的に保存されます。
