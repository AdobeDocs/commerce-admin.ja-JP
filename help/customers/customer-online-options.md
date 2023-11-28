---
title: 顧客セッションの有効期間
description: 顧客セッションの有効期間は、顧客のショッピングセッションの有効期間を決定します。
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# 顧客セッションの有効期間

顧客のショッピングセッションの有効期間は、サーバーセッションの長さ、 [永続的な買い物かご](../stores-purchase/cart-persistent.md)、およびブラウザーに保存される情報の有効期間。 これらは同じ顧客体験に関連していますが、それぞれが異なる有効期限イベントとライフタイムを持つ別々のプロセスです。

| プロセス | 説明 |
| --- | --- |
| セッション | 買い物かごの内容など、サーバーに保存される情報。 Cookie の有効期限が切れる前にサーバーセッションの有効期限が切れた場合、顧客は買い物かごの内容を失い、セキュリティリスクを軽減する可能性があります。 |
| セッション Cookie | 数字または文字列としてブラウザーに保存される情報です。 セッション Cookie の有効期限がサーバーセッションより前に切れた場合、お客様はログアウトされます。 顧客がブラウザーウィンドウを閉じると、セッション cookie は削除されます。 デフォルトでは、cookie の有効期間は 3600 秒または 1 時間に設定されています。 その間にキーボードアクティビティがない場合、現在のセッションは終了し、顧客が買い物を続行するにはアカウントに再度ログインする必要があります。 |

{style="table-layout:auto"}

次の場合 [買い物かごの持続](../stores-purchase/cart-persistent.md) が有効な場合、顧客が次回アカウントにサインインする際に使用する買い物かごの内容は保存されます。 永続的な買い物かごを使用する場合は、サーバーセッションの有効期間とセッション cookie の有効期間を長期間に設定することをお勧めします。

サーバー上のセッションの長さは、 `php.ini` ファイルと複数の変数。 現在、Adobe Commerceにはサーバーセッションの長さを制御する管理者設定はありません。

## cookie の有効期間の設定

1. 次の日： _管理者_ サイドバー、移動 [!UICONTROL **ストア**] > _[!UICONTROL Settings]_>[!UICONTROL **設定**].

1. 複数のストアがある場合、 **[!UICONTROL Store View]** 設定を適用するストアの右上隅の「選択」。

1. の下の左側のパネル **[!UICONTROL General]**&#x200B;を選択します。 **[!UICONTROL Web]**.

1. を展開します。 **[!UICONTROL Default Cookie Settings]** 」セクションに入力します。

   ![デフォルトの Cookie 設定](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. デフォルトを変更するには、 **[!UICONTROL Use system value]** チェックボックスに新しい値を秒単位で入力します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 設定 _自分を記憶する_ 機能

ログインを容易にするには、 **[!UICONTROL Remember Me]** 関数を使用すると、ユーザーアカウント所有者は、ストアフロントに入るたびに資格情報を入力するのを防ぐことができます。 セキュリティ上の理由から、永続化機能はデフォルトで無効になっています。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Persistent Shopping Cart]**.

1. を展開します。 **[!UICONTROL General Options]** 」セクションに入力します。

1. の場合 **[!UICONTROL Enable Persistence]**、に設定 `Yes`. ( **[!UICONTROL Use system value]** チェックボックスをオンにして、デフォルト設定の変更を許可します。)

1. の場合 **[!UICONTROL Enable "Remember Me"]**、に設定 `Yes` または `No` 必要に応じて変更します。

1. 完了したら、「 **[!UICONTROL Save Config]**.
