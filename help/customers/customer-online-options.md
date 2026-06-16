---
title: 顧客セッションの有効期間
description: 顧客セッションの有効期間は、顧客のショッピングセッションの有効期間を決定します。
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/cJ8Rv5zMkTvZMfrl-nj-3xy3guSPDlxa7HZ-ZG7kLFw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# 顧客セッションの有効期間

顧客ショッピングセッションの有効期間は、サーバーセッションの長さ、[永続的なカート ](../stores-purchase/cart-persistent.md)の使用、ブラウザーに保存される情報の有効期間など、いくつかの要因によって決まります。 これらは同じ顧客体験に関連していますが、有効期限や有効期間が異なる個別のプロセスです。

| プロセス | 説明 |
| --- | --- |
| セッション | ショッピングカートの内容など、サーバーに保存される情報。 Cookieの有効期限が切れる前にサーバーセッションが終了すると、顧客はカートの内容を失い、セキュリティリスクを軽減する可能性があります。 |
| セッション Cookie | ブラウザーに保存される情報は、文字数または文字列です。 セッションクッキーがサーバーセッションの前に期限切れになると、お客様はログアウトされます。 お客様がブラウザーウィンドウを閉じると、セッション Cookieは削除されます。 デフォルトでは、Cookieの有効期間は3600秒、つまり1時間に設定されています。 その間にキーボード操作がない場合、現在のセッションは終了し、顧客はアカウントにログインしてショッピングを続ける必要があります。 |

{style="table-layout:auto"}

[永続的なカート ](../stores-purchase/cart-persistent.md)が有効になっている場合、次回の顧客がアカウントにサインインしたときに、カートの内容が保存されます。 永続的なカートを使用する場合は、サーバーセッションとセッション Cookieの有効期間を長い期間に設定することをお勧めします。

サーバーでは、セッションの長さは`php.ini` ファイルと複数の変数によって制御されます。 現在、Adobe Commerceには、サーバーセッションの長さを制御する管理者設定はありません。

## Cookieの有効期間の設定

1. _管理者_ サイドバーで、[!UICONTROL **ストア**] > _[!UICONTROL Settings]_>[!UICONTROL **構成**]に移動します。

1. 複数のストアがある場合は、右上隅の&#x200B;**[!UICONTROL Store View]** セレクターを、設定が適用されるストアに設定します。

1. **[!UICONTROL General]**&#x200B;の下の左側のパネルで、**[!UICONTROL Web]**&#x200B;を選択します。

1. **[!UICONTROL Default Cookie Settings]** セクションを展開します。

   ![既定のCookie設定](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. デフォルトを変更するには、**[!UICONTROL Use system value]** チェックボックスをオフにし、新しい値を秒単位で入力します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## _Remember Me_&#x200B;機能の設定

ログインを簡単にするために、**[!UICONTROL Remember Me]**&#x200B;機能を使用すると、ユーザーアカウント所有者は、ストアフロントに入るたびに資格情報を入力せずに済みます。 セキュリティ上の理由から、永続性機能はデフォルトで無効になっています。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Persistent Shopping Cart]**&#x200B;を選択します。

1. **[!UICONTROL General Options]** セクションを展開します。

1. **[!UICONTROL Enable Persistence]**&#x200B;の場合は、`Yes`に設定します。 （**[!UICONTROL Use system value]** チェックボックスをオフにして、デフォルト設定の変更を許可します）。

1. **[!UICONTROL Enable "Remember Me"]**&#x200B;の場合は、要件に応じて`Yes`または`No`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
