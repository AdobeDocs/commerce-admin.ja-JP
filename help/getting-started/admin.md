---
title: 管理者とは
description: 詳しくは、 [!DNL Commerce] 管理：マーチャントが製品やプロモーションを設定し、注文を管理し、その他の管理タスクを実行する場所。
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: b657db7e486fec591d5a6239d554376f00707e8c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 管理者とは

ストア _管理者_ はパスワードで保護されたバックオフィスで、マーチャントは、製品とプロモーションの設定、注文の管理、その他の管理タスクを実行できます。 すべての基本的な設定タスクとストア管理操作は、 _管理者_.

セキュリティを強化するには、 _管理者_ ログインは次の方法で保護されています： [二段階認証](../systems/security-two-factor-authentication.md)を設定し、 [CAPTCHA](../systems/security-captcha.md). 詳しくは、 [管理セキュリティの設定](../systems/security-admin.md).

![管理者のサイドバーとダッシュボード](./assets/admin-dashboard.png){width="700" zoomable="yes"}

初期 [サインイン](admin-signin.md) 資格情報は、Adobe CommerceまたはMagento Open Sourceのインストール中に設定されました。 パスワードを忘れた場合は、アカウントに関連付けられた電子メールアドレスに一時的なパスワードを送信できます。 セキュリティを強化するには、大文字と小文字を区別するユーザー名と強力なパスワードをストアに必要とするように設定します。

デフォルトの管理者ユーザーアカウントに加えて、お客様のビジネスでは、 [その他のアカウント](../systems/permissions-users-all.md) ストアとサポートの顧客アカウントを管理する必要がある。 各アカウントは、 [役割](../systems/permissions-user-roles.md) ビジネスに基づく、およびアクセスレベル _知る必要がある_. 各管理者ユーザーアカウントに関連付けられている電子メールアドレスは、一意である必要があります。

{{ims-admin-note}}

## 使用状況データの収集

初めて _管理者_&#x200B;を使用する場合は、すべての管理者Adobeの使用状況データを収集するためのユーザー権限を付与するよう求められます。 管理者使用状況データの収集を許可することで、AdobeはAdobe Commerce Admin、および関連する製品やサービスの使用経験を向上できます。

![管理者使用状況データ収集を許可](./assets/admin-usage-data.png){width="600"}

個々のユーザーは、使用状況データでは識別されません。 お使いのデータ収集設定は、 [管理使用状況](../configuration-reference/advanced/admin.md#admin-usage) 設定。

Adobe Commerceの場合、データ収集を許可すると、 _製品内ガイダンス_( インタラクティブコンテンツを _管理者_. ヘルプ、ツールヒント、ウォークスルーガイド、オンボーディング情報、機能に関するお知らせなどを提供します。
