---
title: 管理者とは何ですか？
description: について説明します [!DNL Commerce] 管理者：マーチャントが製品やプロモーションの設定、注文の管理、その他の管理タスクを実行する場所です。
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: b657db7e486fec591d5a6239d554376f00707e8c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 管理者とは何ですか？

ストア _Admin_ は、マーチャントとして製品やプロモーションの設定、注文の管理、その他の管理タスクを実行する、パスワードで保護されたバックオフィスです。 すべての基本的な設定タスクとストア管理操作は、 _Admin_.

セキュリティを強化するには、 _Admin_ ログインは次によって保護されています： [二要素認証](../systems/security-two-factor-authentication.md)、およびを必須として設定できる [CAPTCHA](../systems/security-captcha.md). 詳細については、次を参照してください： [Admin Security の設定](../systems/security-admin.md).

![管理サイドバーとダッシュボード](./assets/admin-dashboard.png){width="700" zoomable="yes"}

最初の [ログイン](admin-signin.md) 資格情報は、Adobe CommerceまたはMagento Open Sourceのインストール中に設定されました。 パスワードを忘れた場合、一時的なパスワードをアカウントに関連付けられているメールアドレスに送信できます。 セキュリティを強化するには、大文字と小文字を区別するユーザー名と強力なパスワードを要求するようにストアを設定します。

デフォルトの管理者ユーザーアカウントに加えて、ビジネスは以下を作成できます [追加アカウント](../systems/permissions-users-all.md) store の管理とカスタマーアカウントのサポートに必要な情報。 各アカウントは、特定のに関連付けることができます [役割](../systems/permissions-user-roles.md) ビジネスに基づくアクセス・レベル _知る必要がある_. 各管理者ユーザーアカウントに関連付けられているメールアドレスは、一意である必要があります。

{{ims-admin-note}}

## 使用状況データの収集

に初めてログインしたとき _Admin_&#x200B;を選択した場合は、すべての管理者Adobeの使用状況データを収集するユーザーアクセス権を付与するように求められます。 管理者の使用状況データ収集を許可することで、AdobeはAdobe Commerce Admin および関連する製品とサービスを使用するエクスペリエンスを向上させることができます。

![管理者による使用状況データの収集を許可](./assets/admin-usage-data.png){width="600"}

使用状況データでは個々のユーザーは識別されません。 データ収集の設定は、 [Admin Usage](../configuration-reference/advanced/admin.md#admin-usage) 設定。

Adobe Commerceの場合、データ収集を許可すると次も可能になります。 _製品内ガイダンス_&#x200B;これは、インタラクティブコンテンツをに提供するように設計されています。 _Admin_. ヘルプ、ツールヒント、ウォークスルーのガイド、オンボーディング情報、機能のお知らせなどを提供します。
