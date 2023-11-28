---
title: 購買依頼リストの最大値の構成
description: 各顧客アカウントで維持可能な最大数を制御する購買依頼リスト設定について説明します。
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 購買依頼リストの最大値の構成

購買依頼リスト機能が有効な場合、顧客は、頻繁に購入した品目の複数のリストを作成し、それらのリストを注文の配置に使用できます。 ログインしているユーザーとゲストの両方で利用できます。 購買依頼リストは、次の場合に有効にできます。 [B2B 機能の設定](enable-basic-features.md).

顧客は、様々なベンダー、購入者、チーム、キャンペーン、または共通のワークフローを効率化するその他の製品に焦点を当てる複数のリストを持つことができます。 [購買依頼リスト機能](requisition-lists.md) はウィッシュリストに似ていますが、次の点が異なります。

- 買い物かごに品目を送信した後、購買依頼リストは消去されません。 複数回使用できます。
- 購買依頼リストのユーザー・インタフェースでは、多くの品目を表示するためにコンパクト・ビューが使用されます。

デフォルトでは、顧客は自分のアカウントの最大 999 件の購買依頼リストを維持できます。 ただし、設定を変更し、小さい数値を指定すると、ストアの負荷を軽減できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Requisition Lists]**.

   ![購買依頼リスト — 一般設定](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Number of Requisition Lists]**」には、各顧客アカウントで維持可能な購買依頼リストの最大数を入力します。

   最小数は次のとおりです。 `2`の場合、最大値は `999`.

1. 完了したら、「 **[!UICONTROL Save Config]**.
