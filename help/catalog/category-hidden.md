---
title: 非表示のカテゴリ
description: 内部の目的で非表示のカテゴリを使用する方法や、ナビゲーションメニューに含まれていないカテゴリにリンクする方法について説明します。
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# 非表示のカテゴリ

非表示のカテゴリを使用する方法は多数あります。 独自の内部目的のために追加のカテゴリレベルを作成し、上位レベルのカテゴリのみを顧客に表示する場合があります。 または、ナビゲーションメニューに含まれていないカテゴリにリンクすることもできます。

## 非表示のカテゴリを作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. カテゴリツリーで、非表示にするカテゴリを選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Is Active]** 対象： `Yes`.
   - を設定 **[!UICONTROL Include in Menu]** 対象： `No`.

1. が含まれる **[!UICONTROL Display Settings]** セクション、設定 **[!UICONTROL Anchor]** 対象： `No`.

   ![非表示のカテゴリ](./assets/hidden-categories.png){width="600" zoomable="yes"}

   非表示のカテゴリはアクティブですが、トップメニューや階層的なナビゲーションには表示されません。

1. サブカテゴリを作成するには、非表示の各サブカテゴリに対して次の設定を行います。

   >[!NOTE]
   >
   >カテゴリは非表示ですが、その下にサブカテゴリを作成してアクティブにすることができます。

   - を設定 **[!UICONTROL Enable Category]** 対象： `Yes`.
   - が含まれる **[!UICONTROL Display Settings]** セクション、設定 **[!UICONTROL Anchor]** 対象： `Yes`.

   アクティブなカテゴリとして、ストア内の他の場所からリンクできるようになりましたが、メニューには表示されません。

1. 完了したら、 **[!UICONTROL Save]**.
