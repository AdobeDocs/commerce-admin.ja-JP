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

顧客ショッピング セッションの有効期間は、サーバーセッションの長さ、[&#x200B; 永続的な買い物かごの使用 &#x200B;](../stores-purchase/cart-persistent.md)、ブラウザーに保存されている情報の有効期間など、いくつかの要因によって決定されます。 これらは同じ顧客体験に関連していますが、有効期限イベントと有効期間が異なる別個のプロセスです。

| プロセス | 説明 |
| --- | --- |
| Session | 買い物かごのコンテンツなど、サーバーに保存される情報。 Cookie の有効期限が切れる前にサーバーセッションの有効期限が切れると、お客様が買い物かごの中身を失い、セキュリティリスクが軽減される可能性があります。 |
| セッション Cookie | 数値または文字列としてブラウザーに保存される情報です。 サーバーセッションより前にセッション cookie の有効期限が切れた場合、顧客はログアウトされます。 ユーザーがブラウザーウィンドウを閉じると、セッション Cookie は削除されます。 デフォルトでは、cookie の有効期間は 3600 秒（1 時間）に設定されています。 その間にキーボードアクティビティがない場合、現在のセッションは終了し、顧客が買い物を続行するにはアカウントにログインし直す必要があります。 |

{style="table-layout:auto"}

[&#x200B; 永続的な買い物かご &#x200B;](../stores-purchase/cart-persistent.md) が有効になっている場合、顧客が次回アカウントにログインする際に備えて、買い物かごの内容が保存されます。 永続的な買い物かごを使用する場合、サーバーセッションとセッション cookie の有効期間を長い期間に設定することをお勧めします。

サーバーでは、セッションの長さは `php.ini` ファイルといくつかの変数によって制御されます。 現在、Adobe Commerceには、サーバーセッションの長さを制御する管理者設定がありません。

## cookie の有効期間の設定

1. _管理者_ サイドバーで、[!UICONTROL **ストア**]/_[!UICONTROL Settings]_/[!UICONTROL **設定**]に移動します。

1. 複数のストアがある場合は、右上隅の **[!UICONTROL Store View]** 選択を、設定が適用されるストアに設定します。

1. **[!UICONTROL General]** の下の左パネルで、「**[!UICONTROL Web]**」を選択します。

1. 「**[!UICONTROL Default Cookie Settings]**」セクションを展開します。

   ![&#x200B; デフォルトの Cookie 設定 &#x200B;](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. デフォルト値を変更するには、「**[!UICONTROL Use system value]**」チェックボックスをオフにして、新しい値（秒単位）を入力します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## _記憶する_ 機能の設定

ログインを容易にするために、**[!UICONTROL Remember Me]** 機能を使用すると、ユーザーアカウント所有者は、ストアフロントに入るたびに資格情報を入力するのを回避できます。 セキュリティ上の理由から、永続性機能はデフォルトで無効になっています。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Persistent Shopping Cart]**」を選択します。

1. 「**[!UICONTROL General Options]**」セクションを展開します。

1. **[!UICONTROL Enable Persistence]** の場合は、`Yes` に設定します。 （デフォルト設定の変更を許可する場合は、「**[!UICONTROL Use system value]**」チェックボックスをオフにします）。

1. **[!UICONTROL Enable "Remember Me"]** の場合は、要件に応じて `Yes` または `No` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
