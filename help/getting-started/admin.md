---
title: 管理者とは何ですか？
description: マーチャントが製品やプロモーションの設定、注文の管理、その他の管理タスクを実行する場所である  [!DNL Commerce] Admin について説明します。
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: a6b293dca673808bbc7f37cb468c6e316fddb735
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---


# 管理者とは何ですか？

ストア _管理者_ は、マーチャントとして製品やプロモーションの設定、注文の管理、その他の管理タスクを実行する、パスワードで保護されたバックオフィスです。 すべての基本的な設定タスクとストアの管理操作は、_管理者_ から実行されます。

セキュリティを強化するために、_Admin_ ログインは [2 要素認証 &#x200B;](../systems/security-two-factor-authentication.md) で保護されており、[CAPTCHA](../systems/security-captcha.md) を必要とするように設定できます。 詳しくは、[Admin Security の設定 &#x200B;](../systems/security-admin.md) を参照してください。

![&#x200B; 管理サイドバーとダッシュボード &#x200B;](./assets/admin-dashboard.png){width="700" zoomable="yes"}

最初の [&#x200B; ログイン &#x200B;](admin-signin.md) 資格情報は、Adobe CommerceまたはMagento Open Sourceのインストール中に設定されました。 パスワードを忘れた場合、一時的なパスワードをアカウントに関連付けられているメールアドレスに送信できます。 セキュリティを強化するには、大文字と小文字を区別するユーザー名と強力なパスワードを要求するようにストアを設定します。

デフォルトの管理者ユーザーアカウントに加えて、ビジネスでは、ストアの管理とカスタマーアカウントのサポートに必要な数の [&#x200B; 追加アカウント &#x200B;](../systems/permissions-users-all.md) を作成できます。 各アカウントは、ビジネス [&#x200B; 知る必要がある &#x200B;](../systems/permissions-user-roles.md) に基づいて、特定の _役割_ およびアクセスレベルに関連付けることができます。 各管理者ユーザーアカウントに関連付けられているメールアドレスは、一意である必要があります。

{{ims-admin-note}}

## 使用状況データの収集

_管理者_ に初めてログインすると、すべての管理者ユーザーの使用状況データを収集するAdobe権限を付与するよう求められます。 管理者の使用状況データの収集を許可すると、AdobeがAdobe Commerce Admin および関連する製品とサービスを使用する際の操作性を向上させることができます。

![&#x200B; 管理者による使用状況データの収集を許可 &#x200B;](./assets/admin-usage-data.png){width="600"}

使用状況データでは個々のユーザーは識別されません。 データ収集の設定は、「[&#x200B; 管理者の使用状況 &#x200B;](../configuration-reference/advanced/admin.md#admin-usage) 設定からいつでも変更できます。

Adobe Commerceの場合、データ収集を許可すると、インタラクティブコンテンツを _管理者_ に提供するように設計された _製品内ガイダンス_ も有効になります。 ヘルプ、ツールヒント、ウォークスルーのガイド、オンボーディング情報、機能のお知らせなどを提供します。
