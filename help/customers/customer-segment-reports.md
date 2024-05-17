---
title: 顧客セグメントレポート
description: 顧客セグメントレポートは、各セグメントの顧客数に関する情報を提供します。
exl-id: a767ee80-7b6e-4acd-9772-2f8adcf3233e
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

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
| **[!UICONTROL Status]** | セグメントステータス。 オプション： `Active` / `Inactive` |
| **[!UICONTROL Website]** | セグメントが割り当てられている web サイト |
| **[!UICONTROL Customers]** | セグメントに割り当てられた顧客の数 |

{style="table-layout:auto"}

セグメント内の顧客のリストにドリルダウンし、データを書き出すことができます。

![顧客データへのドリルダウン](assets/customer-segment-drilldown.png){width="600" zoomable="yes"}

最新のデータを確実に入手するには、セグメントデータを更新する必要があります。 セグメントデータが使用できない場合や古い場合は、 **[!UICONTROL Refresh Segment Data]** をクリックします。

1. の場合 **[!UICONTROL Export to]**&#x200B;で、書き出し形式を選択します。

   * CSV - プレーンテキストデータを含む、コンマ区切り値ファイル。
   * Excel XML - XML ベースのスプレッドシートデータ形式。

1. クリック **[!UICONTROL Export]**.

   | 列 | 説明 |
   |--- |--- |
   | **[!UICONTROL ID]** | 各ユーザーに割り当てられる一意の数値識別子 |
   | **[!UICONTROL Name]** | 顧客名 |
   | **[!UICONTROL Email]** | 登録された顧客の E メール アドレス |
   | **[!UICONTROL Group]** | 顧客が割り当てられている顧客グループ |
   | **[!UICONTROL Phone]** | 顧客の電話番号 |
   | **[!UICONTROL ZIP]** | 顧客の住所の郵便番号 |
   | **[!UICONTROL Country]** | 顧客が所在する国 |
   | **[!UICONTROL State/Province]** | 顧客が所在する都道府県 |
   | **[!UICONTROL Customer Since]** | 顧客アカウントが作成された日時 |

   {style="table-layout:auto"}

1. 生成されたファイルは、ローカルマシンに自動的に保存されます。
