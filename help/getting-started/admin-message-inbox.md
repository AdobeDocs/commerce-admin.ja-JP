---
title: 管理メッセージインボックス
description: Adobeやシステムからの重要で有用なメッセージを提供する、管理メッセージインボックスについて説明  [!DNL Commerce]  ます。
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# 管理メッセージインボックス

あなたの店はAdobeから定期的にメッセージを受け取ります。 メッセージは重要度で評価され、システムのアップデート、パッチ、新しいリリース、予定されているメンテナンス、今後のイベントなどを参照します。 ヘッダーのベルアイコンは、インボックス内の未読メッセージの数を示します。

![&#x200B; 管理者 – 受信メッセージ &#x200B;](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

_[!UICONTROL Notifications]_&#x200B;のページには、日付別にランク付けされたすべてのメッセージがリストされます。_[!UICONTROL Action]_ のコマンドを使用して、個々のメッセージを読み取り済みとしてマークしたり、詳細情報を表示したり、インボックスからメッセージを削除したりできます。

設定によって、インボックスの更新頻度とメッセージの配信方法が決定されます。 ストア管理者にセキュア URL がある場合、通知は HTTPS で配信する必要があります。

## 新しい受信メッセージの表示

1. ヘッダーの **[!UICONTROL Notification]** アイコンをクリックして、概要を読みます。

1. 次のいずれかの操作を行います。

   - 必要に応じて、メッセージをクリックして全文を表示します。
   - メッセージを削除するには、メッセージの右側にある削除アイコンをクリックします。
   - 通知の一覧をすべて表示するには、[**[!UICONTROL See All]**] をクリックします。

## 重要なメッセージに対処する

重要なメッセージの場合は、次のいずれかの操作を行います。

- 「**[!UICONTROL Read Details]**」をクリックします。
- 警告ボックスを閉じてもメッセージをアクティブのままにするには、[**[!UICONTROL Close]**] をクリックします。

## 通知の管理

1. 次のいずれかの操作をおこなって、通知ページを開きます。

   - ヘッダーの「**[!UICONTROL Notification]**」アイコンをクリックします。 新しいメッセージが 1 つ以上表示されている場合は、[**[!UICONTROL See All]**] をクリックします。

   - _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Other Settings]_/**[!UICONTROL Notifications]**&#x200B;に移動します。

1. **[!UICONTROL Action]** 列で、次のいずれかの操作を行います。

   - 詳細については、「**[!UICONTROL Read Details]**」をクリックして、リンクされたページを新しいウィンドウで開きます。

   - 受信トレイにメッセージを保持するには、[**[!UICONTROL Mark As Read]**] をクリックします。

     ![&#x200B; 管理者 – 選択した通知を既読としてマーク &#x200B;](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - メッセージを削除するには、「削 **[!UICONTROL Remove]**」をクリックします。

1. 複数のメッセージにアクションを適用するには、次のいずれかの操作を行います。

   - 管理する各メッセージの最初の列のチェックボックスを選択します。
   - 複数のメッセージを選択するには、必要に応じて **[!UICONTROL Mass Actions]** コントロールを設定します。

1. **[!UICONTROL Actions]** コントロールを次のいずれかに設定します。

   - `Mark as Read`
   - `Remove`

1. 「**[!UICONTROL Submit]**」をクリックしてプロセスを完了します。

## 通知の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のナビゲーションパネルで **[!UICONTROL Advanced]** を展開し、「**[!UICONTROL System]**」を選択します。

1. ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)**[!UICONTROL Notifications]** のセクションを展開します。

   ![&#x200B; 通知の設定 &#x200B;](./assets/system-notifications.png){width="600"}

1. ストア管理者が [&#x200B; セキュア URL](../stores-purchase/store-urls.md) 上で実行する場合は、**[!UICONTROL Use HTTPS to Get Feed]** を `Yes` に設定します。

1. **[!UICONTROL Update Frequency]** を設定して、インボックスの更新頻度を決定します。

   間隔は、1～24 時間の範囲で指定できます。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

[!UICONTROL System] 設定オプションについて詳しくは、[_設定リファレンスガイド_](../configuration-reference/advanced/system.md) を参照してください。
