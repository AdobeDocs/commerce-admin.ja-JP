---
title: 管理メッセージインボックス
description: Adobeおよび [!DNL Commerce] システム。
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 管理メッセージインボックス

ストアは定期的にAdobeからメッセージを受け取ります。 メッセージは重要度が高く評価され、システムの更新、パッチ、新しいリリース、定期メンテナンス、または今後のイベントを指す場合があります。 ヘッダーのベルのアイコンは、インボックス内の未読メッセージの数を示します。

![管理 — 受信メッセージ](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

The _[!UICONTROL Notifications]_ページには、すべてのメッセージが日付順にランク付けされて表示されます。 The_[!UICONTROL Action]_ コマンドを使用して、個々のメッセージを既読としてマークしたり、詳細情報を表示したり、インボックスからメッセージを削除したりできます。

設定によって、インボックスの更新頻度と、メッセージの配信方法が決まります。 ストア管理者がセキュア URL を持っている場合、通知は HTTPS で配信する必要があります。

## 新しい受信メッセージを表示

1. 次をクリック： **[!UICONTROL Notification]** アイコンをクリックし、概要を読み取ります。

1. 次のいずれかの操作を行います。

   - 必要に応じて、メッセージをクリックして全文を表示します。
   - メッセージを削除するには、メッセージの右側にある削除アイコンをクリックします。
   - すべての通知リストを表示するには、 **[!UICONTROL See All]**.

## 重要なメッセージの処理

重要なメッセージに対して、次のいずれかの操作を行います。

- クリック **[!UICONTROL Read Details]**.
- メッセージをアクティブにしたままアラートボックスを閉じるには、 **[!UICONTROL Close]**.

## 通知の管理

1. 次のいずれかの操作を行って、通知ページを開きます。

   - 次をクリック： **[!UICONTROL Notification]** アイコンをクリックします。 1 つ以上の新しいメッセージが表示された場合は、 **[!UICONTROL See All]**.

   - 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**.

1. Adobe Analytics の **[!UICONTROL Action]** 」列で、次のいずれかの操作を行います。

   - 詳しくは、 **[!UICONTROL Read Details]** をクリックすると、リンクされたページが新しいウィンドウで開きます。

   - メッセージをインボックスに保持するには、 **[!UICONTROL Mark As Read]**.

     ![管理 — 選択した通知を既読としてマーク](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - メッセージを削除するには、 **[!UICONTROL Remove]**.

1. 複数のメッセージにアクションを適用するには、次のいずれかの操作を行います。

   - 管理する各メッセージの最初の列にあるチェックボックスを選択します。
   - 複数のメッセージを選択するには、 **[!UICONTROL Mass Actions]** 必要に応じてコントロールします。

1. を設定します。 **[!UICONTROL Actions]** コントロールを次のいずれかに設定します。

   - `Mark as Read`
   - `Remove`

1. クリック **[!UICONTROL Submit]** をクリックしてプロセスを完了します。

## 通知の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png)の **[!UICONTROL Notifications]** 」セクションに入力します。

   ![通知の設定](./assets/system-notifications.png){width="600"}

1. ストア管理者が [セキュア URL](../stores-purchase/store-urls.md)，設定 **[!UICONTROL Use HTTPS to Get Feed]** から `Yes`.

1. 設定 **[!UICONTROL Update Frequency]** を使用して、インボックスの更新頻度を決定します。

   間隔は 1 ～ 24 時間にすることができます。

1. 完了したら、「 **[!UICONTROL Save Config]**.

詳しくは、 [!UICONTROL System] 設定オプション ( [_設定リファレンスガイド_](../configuration-reference/advanced/system.md).
