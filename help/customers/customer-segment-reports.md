---
title: 顧客セグメントレポート
description: 顧客セグメントレポートは、各セグメントの顧客数に関する情報を提供します。
exl-id: a767ee80-7b6e-4acd-9772-2f8adcf3233e
TQID: https://experienceleague.adobe.com/asBYmrf5lkWyfH6xf8o-OxZwK25rr4okrtsyON3Fv1s
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# 顧客セグメントレポート

{{ee-feature}}

顧客セグメントレポートには、各セグメントの顧客数に関する情報が表示されます。

![顧客セグメントレポート &#x200B;](assets/customer-segments-reports.png){width="700" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| **[!UICONTROL Select]** | アクションの対象となる各セグメントのチェックボックスを選択するか、列ヘッダーの選択コントロールを使用します。 オプション：`Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| **[!UICONTROL ID]** | 各セグメントに割り当てられる一意の数値識別子 |
| **[!UICONTROL Segment]** | セグメント名 |
| **[!UICONTROL Status]** | セグメントステータス： オプション：`Active` / `Inactive` |
| **[!UICONTROL Website]** | セグメントが割り当てられているWeb サイト |
| **[!UICONTROL Customers]** | セグメントに割り当てられた顧客の数 |

{style="table-layout:auto"}

セグメント内の顧客のリストにドリルダウンして、データを書き出すことができます。

![顧客データにドリルダウン &#x200B;](assets/customer-segment-drilldown.png){width="600" zoomable="yes"}

最新のデータを使用するには、セグメントデータを更新する必要があります。 セグメントデータが利用できないか、古い場合は、ボタンバーの「**[!UICONTROL Refresh Segment Data]**」をクリックして更新します。

1. **[!UICONTROL Export to]**&#x200B;の場合、書き出し形式を選択します。

   * CSV - プレーンテキストデータを含むコンマ区切りの値ファイル。
   * Excel XML - XML ベースのスプレッドシート データ形式。

1. **[!UICONTROL Export]**&#x200B;をクリックします。

   | 列 | 説明 |
   |--- |--- |
   | **[!UICONTROL ID]** | 各ユーザーに割り当てられる一意の数値識別子 |
   | **[!UICONTROL Name]** | 企業名 |
   | **[!UICONTROL Email]** | 登録済みのお客様のメールアドレス |
   | **[!UICONTROL Group]** | 顧客が割り当てられている顧客グループ |
   | **[!UICONTROL Phone]** | 顧客の電話番号 |
   | **[!UICONTROL ZIP]** | お客様が所在する郵便番号 |
   | **[!UICONTROL Country]** | 顧客が所在する国 |
   | **[!UICONTROL State/Province]** | 顧客が所在する州または都道府県 |
   | **[!UICONTROL Customer Since]** | 顧客アカウントが作成された日時 |

   {style="table-layout:auto"}

1. 生成されたファイルは、ローカルマシンに自動的に保存されます。
