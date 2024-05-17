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

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Password Options]** セクション。

   ![パスワードオプション](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. を **[!UICONTROL Password Reset Protection Type]** パスワードリセットリクエストの確認に使用するメソッドに対して：

   - `By IP and Email`  – 特定の電子メールまたは特定の IP からパスワードをリセットしようとしたことがないかどうかを確認します。
   - `By IP`  – 特定の IP からパスワードのリセットが前回試行されたかどうかを確認します。
   - `By Email`  – 特定の E メールに対してパスワードのリセットが過去に試行されていないか確認します。
   - `None`  – 保護が無効（パスワードのリセットに制限なし）。

   この **[!UICONTROL Max Number of Password Reset Requests]** および **[!UICONTROL Min Time Between Password Reset Requests]** はこの設定に基づいて計算されます。

1. 1 時間あたりに送信されるパスワードリセット要求の数を制限するには、次の操作を行います。

   - の場合 **[!UICONTROL Max Number of Password Reset Requests]**&#x200B;に設定し、1 時間あたりに送信できるパスワードリセットリクエストの最大数を入力します。

   - の場合 **[!UICONTROL Min Time Between Password Reset Requests]**&#x200B;は、リクエストから次のリクエストまでの最小時間（分）を入力します。

1. パスワードリセットメール通知を設定するには、次の手順を実行します。

   - を設定 **[!UICONTROL Forgot Email Template]** パスワードを忘れた顧客に送信されるメールに使用されるテンプレート。

   - を設定 **[!UICONTROL Remind Email Template]** を、管理者ユーザーが顧客パスワードをリセットする際に使用するテンプレートに変更します。

   - を設定 **[!UICONTROL Reset Password Template]** を、顧客がパスワードを変更する際に使用するテンプレートに変更します。

   - を設定 **[!UICONTROL Password Template Email Sender]** に [店舗の連絡先](../getting-started/store-details.md) パスワード関連の通知の送信者として表示されます。

1. 次のパスワードリセットセキュリティオプションを入力します。

   - の場合 **[!UICONTROL Recovery Link Expiration Period (hours)]**：パスワード回復リンクの有効期限が切れるまでの時間数を入力します。

   - 顧客ログインおよびパスワードを忘れた場合のフォームのフィールドを以前の入力内容から自動的に入力する場合は、次のように設定します **[!UICONTROL Enable Autocomplete on login/forgot password forms]** 対象： `Yes`.

   - の場合 **[!UICONTROL Number of Required Character Classes]**：次の文字クラスに基づいて、パスワードに含める必要がある様々な文字タイプの数を入力します。

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - の場合 **[!UICONTROL Maximum Login Failures to Lockout Account]**&#x200B;を入力し、カスタマーアカウントがロックされるまでログインが失敗した回数を入力します。 試行回数を制限しない場合は、ゼロ（`0`）に設定します。

   - の場合 **[!UICONTROL Minimum Password Length]**：パスワードで使用できる最小文字数を入力します。 数値は 0 より大きくなければなりません。

   - の場合 **[!UICONTROL Lockout Time (minutes)]**：ログインの試行に失敗した回数が多すぎた場合に顧客アカウントがロックされる時間（分）を入力します。

1. 完了したら、 **[!UICONTROL Save Config]**.
