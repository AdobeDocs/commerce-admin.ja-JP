---
title: 顧客パスワードオプション
description: カスタマーパスワードオプションは、ストアの様々な顧客対応機能のセキュリティレベルを決定します。
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 顧客パスワードオプション

顧客パスワード オプションでは、パスワード リセット要求に使用するセキュリティのレベル、顧客への通知に使用する電子メール テンプレート、およびパスワード回復リンクの有効期間を指定します。 顧客が自分のパスワードを変更することを許可したり、ストア管理者のみが変更できるようにすることを要求したりできます。

## 顧客パスワードオプションの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Customer Configuration]**」を選択します。

1. 「**[!UICONTROL Password Options]**」セクションを展開します。

   ![&#x200B; パスワードオプション &#x200B;](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. パスワードリセットリクエストの確認に使用するメソッドの **[!UICONTROL Password Reset Protection Type]** を設定します。

   - `By IP and Email` – 特定の E メールまたは特定の IP からパスワードをリセットしようとした回数を確認します。
   - `By IP` – 特定の IP からパスワードのリセットが前回試行されていないか確認します。
   - `By Email` – 特定の E メールに対してパスワードのリセットが過去に試行されていないか確認します。
   - `None` – 保護が無効（パスワードのリセットに制限なし）。

   **[!UICONTROL Max Number of Password Reset Requests]** と **[!UICONTROL Min Time Between Password Reset Requests]** は、この設定に基づいて計算されます。

1. 1 時間あたりに送信されるパスワードリセット要求の数を制限するには、次の操作を行います。

   - **[!UICONTROL Max Number of Password Reset Requests]**:1 時間あたりに送信できるパスワードリセットリクエストの最大数を入力します。

   - **[!UICONTROL Min Time Between Password Reset Requests]**：要求間の経過に必要な最小分数を入力します。

1. パスワードリセットメール通知を設定するには、次の手順を実行します。

   - パスワードを忘れた顧客に送信されるメールに使用されるテンプレートに **[!UICONTROL Forgot Email Template]** を設定します。

   - 管理者ユーザーが顧客パスワードをリセットする際に使用するテンプレートに **[!UICONTROL Remind Email Template]** を設定します。

   - 顧客がパスワードを変更する際に使用するテンプレートに **[!UICONTROL Reset Password Template]** を設定します。

   - パスワード関連の通知の送信者として表示される [&#x200B; ストアの連絡先 &#x200B;](../getting-started/store-details.md) に **[!UICONTROL Password Template Email Sender]** を設定します。

1. 次のパスワードリセットセキュリティオプションを入力します。

   - **[!UICONTROL Recovery Link Expiration Period (hours)]**: パスワード回復リンクの有効期限が切れるまでの時間数を入力します。

   - 顧客ログインおよびパスワードを忘れた場合のフォームのフィールドを以前の入力内容から自動的に入力する場合は、「**[!UICONTROL Enable Autocomplete on login/forgot password forms]**」を「`Yes`」に設定します。

   - **[!UICONTROL Number of Required Character Classes]**：次の文字クラスに基づいて、パスワードに含める必要がある様々な文字タイプの数を入力します。

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - **[!UICONTROL Maximum Login Failures to Lockout Account]**: カスタマーアカウントがロックされるまでログインが失敗した回数を入力します。 試行回数に制限のない場合は、ゼロ（`0`）を入力します。

   - **[!UICONTROL Minimum Password Length]**: パスワードで使用できる最小文字数を入力します。 数値は 0 より大きくなければなりません。

   - **[!UICONTROL Lockout Time (minutes)]**: ログインの試行に失敗した回数が多すぎた場合に顧客アカウントがロックされる時間（分）を入力します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
