---
title: 非表示のカテゴリ
description: 非表示のカテゴリを内部的な目的で使用する方法、またはナビゲーションメニューに含まれていないカテゴリにリンクする方法について説明します。
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# 非表示のカテゴリ

非表示のカテゴリを使用する方法は多数あります。 独自の内部目的で追加のカテゴリレベルを作成し、上位のカテゴリのみを顧客に表示する場合があります。 または、ナビゲーションメニューに含まれていないカテゴリにリンクすることもできます。

## 非表示のカテゴリを作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. カテゴリツリーで、非表示にするカテゴリを選択し、次の操作を行います。

   - 設定 **[!UICONTROL Is Active]** から `Yes`.
   - 設定 **[!UICONTROL Include in Menu]** から `No`.

1. Adobe Analytics の **[!UICONTROL Display Settings]** セクション、設定 **[!UICONTROL Anchor]** から `No`.

   ![非表示のカテゴリ](./assets/hidden-categories.png){width="600" zoomable="yes"}

   非表示のカテゴリはアクティブですが、上部のメニューやレイヤーナビゲーションには表示されません。

1. サブカテゴリを作成するには、非表示のサブカテゴリごとに次の設定を実行します。

   >[!NOTE]
   >
   >カテゴリは非表示ですが、その下にサブカテゴリを作成してアクティブにすることができます。

   - 設定 **[!UICONTROL Enable Category]** から `Yes`.
   - Adobe Analytics の **[!UICONTROL Display Settings]** セクション、設定 **[!UICONTROL Anchor]** から `Yes`.

   アクティブなカテゴリは、ストア内の他の場所からリンクできるようになりましたが、メニューには表示されません。

1. 完了したら、「 **[!UICONTROL Save]**.
