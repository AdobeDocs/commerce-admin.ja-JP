---
title: Adobe IDとのコマース管理者の統合を無効にする
description: Adobe Commerce Admin とAdobe IMSの統合を無効にするには、次のオプションの手順に従います。
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# Adobe IDとのコマース管理者の統合を無効にする

{{ee-feature}}

コマースインスタンスをAdobe IMS認証ワークフローと統合したマーチャントは、このオプションの統合を無効にする必要がある場合があります。

コマースのデプロイメントは、IMS 統合が無効になった後、デフォルトの Commerce 認証ワークフローおよびパスワードポリシーに戻ります。 この統合が有効または無効の場合は、管理者ユーザーワークフローのみが影響を受けます。

詳しくは、 [管理者アカウント](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) コマース管理者のログインの概要。

## 手順 1：統合の無効化

管理者からこの統合を無効にすることはできません。 コマースとのAdobe IMS統合を無効にし、コマース認証をデフォルトの状態に戻すには、コマンドラインインターフェイスから統合を無効にする必要があります。

統合を無効にするには：

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerceが成功すると、次のメッセージが表示されます。

```terminal
Admin Adobe IMS integration is disabled.
```

## 手順 2：コマースパスワードを作成または取得する

統合を無効にした後、管理者ユーザーは、コマースパスワードを使用して管理者にログインする必要があります。

* 既存の Commerce パスワード（IMS 統合の前に作成された Commerce パスワード）を記憶している Commerce 管理者ユーザーは、それを使用して管理者にログインできます。

* Commerce の管理者ユーザーで、既存の Commerce パスワードを持っていないか忘れた場合は、新しいパスワードを作成する必要があります。 新しいパスワードを作成する場合、管理者ユーザーは [!UICONTROL Forgot your password?] 新しいパスワードを作成するためのコマースログインページの機能を使用します。 詳しくは、 [顧客パスワードのリセット](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). コマースでは空のパスワードフィールドを使用できません。

## 統合を無効にした後

IMS 統合が無効になると、デフォルトの Commerce 認証ワークフローが再開され、管理者ユーザーは再びパスワードの入力を求められます。

IMS 統合を無効にすると、統合が有効になったときに入力された資格情報が削除されます (`Organization ID`, `Client ID`、および `Client Secret` 値 ) をコマース設定ファイルから取得します。
