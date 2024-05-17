---
title: 管理メッセージインボックス
description: Adobeやフォームからの重要で有用なメッセージを提供する、管理メッセージインボックスについて説明します [!DNL Commerce] システム。
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# 管理メッセージインボックス

あなたの店はAdobeから定期的にメッセージを受け取ります。 メッセージは重要度で評価され、システムのアップデート、パッチ、新しいリリース、予定されているメンテナンス、今後のイベントなどを参照します。 ヘッダーのベルアイコンは、インボックス内の未読メッセージの数を示します。

![管理者 – 受信メッセージ](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

この _[!UICONTROL Notifications]_ページには、日付別にランク付けされたすべてのメッセージがリストされます。 この_[!UICONTROL Action]_ コマンドを使用すると、個々のメッセージを開封済みとしてマークしたり、詳細情報を表示したり、インボックスからメッセージを削除したりできます。

設定によって、インボックスの更新頻度とメッセージの配信方法が決定されます。 ストア管理者にセキュア URL がある場合、通知は HTTPS で配信する必要があります。

## 新しい受信メッセージの表示

1. 「」をクリックします **[!UICONTROL Notification]** アイコンをクリックし、概要を確認します。

1. 次のいずれかの操作を行います。

   - 必要に応じて、メッセージをクリックして全文を表示します。
   - メッセージを削除するには、メッセージの右側にある削除アイコンをクリックします。
   - 通知リスト全体を表示するには、 **[!UICONTROL See All]**.

## 重要なメッセージに対処する

重要なメッセージの場合は、次のいずれかの操作を行います。

- クリック **[!UICONTROL Read Details]**.
- 警告ボックスを閉じてもメッセージをアクティブのままにするには、 **[!UICONTROL Close]**.

## 通知の管理

1. 次のいずれかの操作をおこなって、通知ページを開きます。

   - 「」をクリックします **[!UICONTROL Notification]** アイコンがヘッダーに表示されます。 1 つ以上の新規メッセージが表示されている場合は、 **[!UICONTROL See All]**.

   - 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**.

1. が含まれる **[!UICONTROL Action]** 列で、次のいずれかの操作を行います。

   - 詳細については、をクリックしてください。 **[!UICONTROL Read Details]** をクリックして、リンクされたページを新しいウィンドウで開きます。

   - メッセージを受信トレイに保持するには、 **[!UICONTROL Mark As Read]**.

     ![Admin - Mark selected notifications as read](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - メッセージを削除するには、 **[!UICONTROL Remove]**.

1. 複数のメッセージにアクションを適用するには、次のいずれかの操作を行います。

   - 管理する各メッセージの最初の列のチェックボックスを選択します。
   - 複数のメッセージを選択するには、 **[!UICONTROL Mass Actions]** 必要に応じて制御します。

1. を **[!UICONTROL Actions]** 次のいずれかに制御します。

   - `Mark as Read`
   - `Remove`

1. クリック **[!UICONTROL Submit]** をクリックしてプロセスを完了します。

## 通知の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルでを展開します。 **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png)この **[!UICONTROL Notifications]** セクション。

   ![通知設定](./assets/system-notifications.png){width="600"}

1. ストア管理者がを経由している場合 [セキュア URL](../stores-purchase/store-urls.md)、設定 **[!UICONTROL Use HTTPS to Get Feed]** 対象： `Yes`.

1. を設定 **[!UICONTROL Update Frequency]** インボックスが更新される頻度を判断します。

   間隔は、1～24 時間の範囲で指定できます。

1. 完了したら、 **[!UICONTROL Save Config]**.

について [!UICONTROL System] 設定オプションについては、を参照してください [_設定リファレンスガイド_](../configuration-reference/advanced/system.md).
