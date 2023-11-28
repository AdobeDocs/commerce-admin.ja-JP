---
title: 顧客のパスワードオプション
description: お客様のパスワードオプションによって、お客様が店舗で利用する様々な機能のセキュリティレベルが決まります。
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 顧客のパスワードオプション

お客様のパスワードオプションによって、パスワードリセット要求に使用するセキュリティのレベル、お客様への通知に使用する電子メールテンプレート、およびパスワード回復リンクの有効期間が決まります。 顧客が自分のパスワードを変更することを許可したり、ストア管理者のみが変更できるように要求したりできます。

## 顧客のパスワードオプションの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Password Options]** 」セクションに入力します。

   ![パスワードオプション](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. を設定します。 **[!UICONTROL Password Reset Protection Type]** を、パスワードリセット要求の確認に使用するメソッドに追加します。

   - `By IP and Email`  — 特定の電子メールのパスワードをリセットしようとしたか、特定の IP からパスワードをリセットしようとしたかを確認します。
   - `By IP`  — 特定の IP からパスワードをリセットする前の試行を確認します。
   - `By Email`  — 特定の電子メールのパスワードをリセットする前の試行を確認します。
   - `None`  — 保護が無効です（パスワードのリセットに制限はありません）。

   The **[!UICONTROL Max Number of Password Reset Requests]** および **[!UICONTROL Min Time Between Password Reset Requests]** は、この設定に基づいて計算されます。

1. 1 時間に送信されるパスワードリセット要求の数を制限するには、次の手順を実行します。

   - の場合 **[!UICONTROL Max Number of Password Reset Requests]**、1 時間に送信できるパスワードリセット要求の最大数を入力します。

   - の場合 **[!UICONTROL Min Time Between Password Reset Requests]**」には、リクエストの間隔の最小値を入力します。

1. パスワードリセットの電子メール通知を設定するには、以下の手順を実行します。

   - 設定 **[!UICONTROL Forgot Email Template]** を、パスワードを忘れた顧客に送信する電子メールに使用されるテンプレートに追加する必要があります。

   - 設定 **[!UICONTROL Remind Email Template]** を、管理者ユーザーが顧客パスワードをリセットしたときに使用するテンプレートに追加します。

   - 設定 **[!UICONTROL Reset Password Template]** を、顧客がパスワードを変更したときに使用するテンプレートに追加します。

   - 設定 **[!UICONTROL Password Template Email Sender]** から [ストア連絡先](../getting-started/store-details.md) パスワード関連の通知の送信者として表示される

1. 次のパスワードリセットセキュリティオプションを設定します。

   - の場合 **[!UICONTROL Recovery Link Expiration Period (hours)]**」には、パスワード回復リンクの有効期限が切れるまでの時間数を入力します。

   - 顧客ログインとパスワードを忘れた場合のフォームを、前のエントリから自動的に入力する場合は、 **[!UICONTROL Enable Autocomplete on login/forgot password forms]** から `Yes`.

   - の場合 **[!UICONTROL Number of Required Character Classes]**、次の文字クラスに基づいて、パスワードに含める必要がある異なる文字タイプの数を入力します。

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - の場合 **[!UICONTROL Maximum Login Failures to Lockout Account]**&#x200B;に設定した場合は、顧客アカウントがロックされるまでのログイン失敗回数を入力します。 試行回数を制限しない場合は、ゼロ (`0`) をクリックします。

   - の場合 **[!UICONTROL Minimum Password Length]**」には、1 つのパスワードに使用できる最小文字数を入力します。 0 より大きい数値を指定する必要があります。

   - の場合 **[!UICONTROL Lockout Time (minutes)]**&#x200B;に値を入力しない場合は、ログインに失敗した回数が多すぎた後に、顧客アカウントがロックされる時間（分）を入力します。

1. 完了したら、「 **[!UICONTROL Save Config]**.
