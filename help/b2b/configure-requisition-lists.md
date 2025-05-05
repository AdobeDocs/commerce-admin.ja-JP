---
title: 最大購買要求リストのコンフィギュレーション
description: 各顧客アカウントで維持可能な最大数を制御する購買依頼リストの構成について説明します。
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 最大購買要求リストのコンフィギュレーション

購買依頼リスト機能が使用可能な場合、顧客は頻繁に購入する品目の複数のリストを作成し、それらのリストを発注に使用できます。 ログインしているユーザーとゲストの両方が利用できます。 [B2B 機能の構成 ](enable-basic-features.md) 時に、購買依頼リストを使用可能にできます。

顧客は、様々なベンダー、購入者、チーム、キャンペーンなど、一般的なワークフローを効率化する要素の製品に焦点を当てた複数のリストを持つことができます。 [ 購買依頼リスト機能 ](requisition-lists.md) は、ウィッシュ・リストに似ていますが、次の点が異なります。

- 品目を買い物かごに送信した後、要求リストがクリアされません。 複数回使用できます。
- 購買依頼リストのユーザー・インタフェースでは、多数の品目を表示するためにコンパクト・ビューが使用されます。

デフォルトでは、顧客は自分のアカウントに対して最大 999 件の購買依頼リストを保守できます。 ただし、設定を変更し、より小さい数を指定して、ストアの負荷を軽減することができます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Requisition Lists]**」を選択します。

   ![ 購買依頼リスト – 一般設定 ](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. **[!UICONTROL Number of Requisition Lists]** に、各顧客アカウントで保守できる購買依頼リストの最大数を入力します。

   最小値は `2`、最大値は `999` です。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
