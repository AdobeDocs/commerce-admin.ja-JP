---
title: 非表示のカテゴリ
description: 内部目的で非表示のカテゴリを使用する方法や、ナビゲーションメニューに含まれていないカテゴリにリンクする方法を説明します。
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
TQID: https://experienceleague.adobe.com/vXJFiYxeTBcRQxdc4XGrPEPKuBAcqr-mnuUlh1WIskM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 186
ht-degree: 0%

---

# 非表示のカテゴリ

非表示のカテゴリを使用する方法はたくさんあります。 自社の内部目的のために追加のカテゴリーレベルを作成し、顧客に上位レベルのカテゴリのみを表示することをお勧めします。 または、ナビゲーションメニューに含まれていないカテゴリにリンクすることもできます。

## 非表示カテゴリを作成

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**&#x200B;に移動します。

1. カテゴリーツリーで、非表示にするカテゴリを選択し、次の操作を行います。

   - **[!UICONTROL Is Active]**&#x200B;を`Yes`に設定します。
   - **[!UICONTROL Include in Menu]**&#x200B;を`No`に設定します。

1. **[!UICONTROL Display Settings]** セクションで、**[!UICONTROL Anchor]**&#x200B;を`No`に設定します。

   ![非表示カテゴリ &#x200B;](./assets/hidden-categories.png){width="600" zoomable="yes"}

   非表示カテゴリはアクティブですが、トップメニューやレイヤーナビゲーションには表示されません。

1. サブカテゴリを作成するには、非表示の各サブカテゴリに対して次の設定を実行します。

   >[!NOTE]
   >
   >カテゴリは非表示ですが、その下にサブカテゴリを作成してアクティブにすることができます。

   - **[!UICONTROL Enable Category]**&#x200B;を`Yes`に設定します。
   - **[!UICONTROL Display Settings]** セクションで、**[!UICONTROL Anchor]**&#x200B;を`Yes`に設定します。

   アクティブなカテゴリとして、ストア内の他の場所からリンクできるようになりましたが、メニューには表示されません。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。
