---
title: 顧客セッションの有効期間
description: 顧客セッションの有効期間は、顧客の買い物セッションの有効期間を決定します。
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 顧客セッションの有効期間

顧客の買い物セッションの有効期間は、サーバーセッションの長さ、の使用など、いくつかの要因によって決まります。 [永続カート](../stores-purchase/cart-persistent.md)、およびブラウザーに保存される情報の有効期間。 これらは同じ顧客体験に関連していますが、有効期限イベントと有効期間が異なる別個のプロセスです。

| プロセス | 説明 |
| --- | --- |
| Session | 買い物かごのコンテンツなど、サーバーに保存される情報。 Cookie の有効期限が切れる前にサーバーセッションの有効期限が切れると、お客様が買い物かごの中身を失い、セキュリティリスクが軽減される可能性があります。 |
| セッション Cookie | 数値または文字列としてブラウザーに保存される情報です。 サーバーセッションより前にセッション cookie の有効期限が切れた場合、顧客はログアウトされます。 ユーザーがブラウザーウィンドウを閉じると、セッション Cookie は削除されます。 デフォルトでは、cookie の有効期間は 3600 秒（1 時間）に設定されています。 その間にキーボードアクティビティがない場合、現在のセッションは終了し、顧客が買い物を続行するにはアカウントにログインし直す必要があります。 |

{style="table-layout:auto"}

次の場合 [永続カート](../stores-purchase/cart-persistent.md) が有効になっている場合は、顧客が次回アカウントにログインする際に備えて買い物かごの中身が保存されます。 永続的な買い物かごを使用する場合、サーバーセッションとセッション cookie の有効期間を長い期間に設定することをお勧めします。

サーバーでは、セッションの長さは以下によって制御されます。 `php.ini` ファイルおよびいくつかの変数。 現在、Adobe Commerceには、サーバーセッションの長さを制御する管理者設定がありません。

## cookie の有効期間の設定

1. 日 _Admin_ サイドバー、に移動 [!UICONTROL **ストア**] > _[!UICONTROL Settings]_>[!UICONTROL **設定**].

1. 複数のストアがある場合、 **[!UICONTROL Store View]** 設定が適用されるストアの右上隅にある選択。

1. の下の左パネルで **[!UICONTROL General]**、を選択 **[!UICONTROL Web]**.

1. を展開します。 **[!UICONTROL Default Cookie Settings]** セクション。

   ![デフォルトの Cookie 設定](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. デフォルトを変更するには、 **[!UICONTROL Use system value]** チェックボックスをオンにして、新しい値を秒単位で入力します。

1. 完了したら、 **[!UICONTROL Save Config]**.

## 設定 _記録する_ 機能

ログインを容易にするには、 **[!UICONTROL Remember Me]** 機能を使用すると、ユーザーアカウント所有者は、ストアフロントに入るたびに資格情報を入力するのを回避できます。 セキュリティ上の理由から、永続性機能はデフォルトで無効になっています。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Persistent Shopping Cart]**.

1. を展開します。 **[!UICONTROL General Options]** セクション。

1. の場合 **[!UICONTROL Enable Persistence]**、に設定 `Yes`. （をクリア **[!UICONTROL Use system value]** デフォルト設定の変更を許可するチェックボックス）。

1. の場合 **[!UICONTROL Enable "Remember Me"]**、に設定 `Yes` または `No` ご要望に応じて。

1. 完了したら、 **[!UICONTROL Save Config]**.
