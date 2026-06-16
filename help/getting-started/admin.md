---
title: 管理者とは
description: 販売者が製品とプロモーションを設定し、注文を管理し、その他の管理タスクを実行する場所である [!DNL Commerce] 管理者について説明します。
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
TQID: https://experienceleague.adobe.com/A0DuYohA907-EHXQ6fyy2Sz83Y6cFZ7PDY5SmtBa14Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 324
ht-degree: 0%

---

# 管理者とは

ストア _管理者_&#x200B;は、パスワードで保護されたバックオフィスです。ここでは、販売者として、製品とプロモーションの設定、注文の管理、その他の管理タスクを行います。 すべての基本的な設定タスクとストア管理操作は、_管理者_&#x200B;から実行されます。

セキュリティを強化するため、_管理者_&#x200B;のログインは[二段階認証](../systems/security-two-factor-authentication.md)によって保護され、[CAPTCHA](../systems/security-captcha.md)を必要とするように設定できます。 詳しくは、[管理者セキュリティの設定](../systems/security-admin.md)にアクセスしてください。

![管理者サイドバーとダッシュボード &#x200B;](./assets/admin-dashboard.png){width="700" zoomable="yes"}

最初の[&#x200B; ログイン &#x200B;](admin-signin.md)資格情報は、Adobe CommerceまたはMagento Open Sourceのインストール中に設定されました。 パスワードを忘れた場合は、アカウントに関連付けられているメールアドレスに一時的なパスワードを送信できます。 セキュリティを強化するには、大文字と小文字を区別するユーザー名と強力なパスワードを必要とするようにストアを設定します。

デフォルトの管理者ユーザーアカウントに加えて、ストアの管理とカスタマーアカウントのサポートに必要な追加アカウントを[個](../systems/permissions-users-all.md)作成できます。 各アカウントは、ビジネス _の必要な知識_&#x200B;に基づいて、特定の[役割](../systems/permissions-user-roles.md)およびアクセスレベルに関連付けることができます。 各管理者ユーザーアカウントに関連付けられている電子メールアドレスは、一意である必要があります。

{{ims-admin-note}}

## 利用状況データの収集

_管理者_&#x200B;に初めてログインする場合は、すべての管理者ユーザーの使用状況データを収集するためのAdobe権限を付与するように求められます。 管理者の使用状況データの収集を許可することで、AdobeでAdobe Commerce管理者および関連製品やサービスの使用体験を向上させることができます。

![管理者使用データ収集を許可](./assets/admin-usage-data.png){width="600"}

使用状況データでは、個々のユーザーは識別されません。 ユーザーのデータ収集設定は、[管理者使用状況](../configuration-reference/advanced/admin.md#admin-usage)設定からいつでも変更できます。

Adobe Commerceの場合、データ収集を許可すると、_製品内ガイダンス_&#x200B;も有効になります。このガイダンスは、_管理者_&#x200B;にインタラクティブコンテンツを提供するように設計されています。 ヘルプ、ツールのヒント、チュートリアル ガイド、オンボーディング情報、機能のお知らせなどを提供します。
