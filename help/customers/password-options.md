---
title: 顧客パスワードのオプション
description: 顧客パスワードオプションは、ストアの様々な顧客対応機能のセキュリティレベルを決定します。
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/ttWsiKhuvquDE2oQRWLF9rTDTZ64BHkKD0Lbv-EDnHs
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 0%

---

# 顧客パスワードのオプション

お客様のパスワードオプションは、パスワードリセット要求に使用されるセキュリティレベル、お客様への通知に使用されるメールテンプレート、パスワード回復リンクの有効期間を決定します。 顧客が自分のパスワードを変更できるようにしたり、ストア管理者のみが変更できるようにすることを要求したりできます。

## お客様のパスワードオプションの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Customer Configuration]**&#x200B;を選択します。

1. **[!UICONTROL Password Options]** セクションを展開します。

   ![ パスワードオプション ](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. パスワード リセット リクエストのチェックに使用するメソッドに&#x200B;**[!UICONTROL Password Reset Protection Type]**&#x200B;を設定します。

   - `By IP and Email` – 特定の電子メールまたは特定のIPからパスワードをリセットする以前の試みを確認します。
   - `By IP` – 特定のIPからパスワードをリセットする以前の試みを確認します。
   - `By Email` – 特定の電子メールのパスワードをリセットする以前の試みを確認します。
   - `None` – 保護が無効です（パスワードのリセットに制限はありません）。

   **[!UICONTROL Max Number of Password Reset Requests]**&#x200B;と&#x200B;**[!UICONTROL Min Time Between Password Reset Requests]**&#x200B;は、この設定に基づいて計算されます。

1. 1時間あたりのパスワードリセット要求の送信数を制限するには、次の操作を行います。

   - **[!UICONTROL Max Number of Password Reset Requests]**&#x200B;の場合、1時間に送信できるパスワード リセット要求の最大数を入力します。

   - **[!UICONTROL Min Time Between Password Reset Requests]**&#x200B;に対して、リクエスト間で経過する必要がある最小分数を入力します。

1. パスワードリセットのメール通知を設定するには、次の操作を行います。

   - パスワードを忘れた顧客に送信する電子メールに使用するテンプレートに&#x200B;**[!UICONTROL Forgot Email Template]**&#x200B;を設定します。

   - 管理者ユーザーが顧客パスワードをリセットする際に使用するテンプレートに&#x200B;**[!UICONTROL Remind Email Template]**&#x200B;を設定します。

   - 顧客がパスワードを変更する際に使用されるテンプレートに&#x200B;**[!UICONTROL Reset Password Template]**&#x200B;を設定します。

   - パスワード関連の通知の送信者として表示される[ ストア連絡先](../getting-started/store-details.md)に&#x200B;**[!UICONTROL Password Template Email Sender]**&#x200B;を設定します。

1. 次のパスワードリセットセキュリティオプションを実行します。

   - **[!UICONTROL Recovery Link Expiration Period (hours)]**&#x200B;の場合、パスワード回復リンクの有効期限が切れるまでの時間数を入力します。

   - 顧客ログインのフィールドと、パスワードを忘れたフォームを以前のエントリから自動的に入力する場合は、**[!UICONTROL Enable Autocomplete on login/forgot password forms]**&#x200B;を`Yes`に設定します。

   - **[!UICONTROL Number of Required Character Classes]**&#x200B;の場合、パスワードに含める必要がある様々な文字タイプの数を、次の文字クラスに基づいて入力します。

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - **[!UICONTROL Maximum Login Failures to Lockout Account]**&#x200B;に、顧客アカウントがロックされるまでログイン試行が失敗した回数を入力します。 無制限の試行の場合は、ゼロ （`0`）を入力します。

   - **[!UICONTROL Minimum Password Length]**&#x200B;に、パスワードで使用できる最小文字数を入力します。 数値は0より大きくなければなりません。

   - **[!UICONTROL Lockout Time (minutes)]**&#x200B;に対して、ログインに失敗した回数が多すぎる場合に顧客アカウントがロックされる分数を入力します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
