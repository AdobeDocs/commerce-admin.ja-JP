---
title: Adobe IDとのCommerce管理者の統合を無効にする
description: Adobe Commerce Admin とAdobe IMSの統合を無効にするには、次のオプションの手順に従います。
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Adobe IDとのCommerce管理者の統合を無効にする

{{ee-feature}}

Commerce インスタンスをAdobe IMS認証ワークフローと統合したマーチャントは、このオプションの統合を無効にする必要が生じる場合があります。

Commerce デプロイメントは、IMS 統合が無効になった後、デフォルトのCommerce認証ワークフローおよびパスワードポリシーに戻ります。 この統合が有効または無効の場合は、管理者ユーザーワークフローのみが影響を受けます。

参照： [管理者アカウント](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) Commerce管理者のログインの概要については、を参照してください。

## 手順 1：統合を無効にする

管理者からこの統合を無効にすることはできません。 CommerceとのAdobe IMS統合を無効にし、Commerce認証をデフォルトステートに戻すには、コマンドラインインターフェイスから統合を無効にする必要があります。

統合を無効にするには：

```bash
bin/magento admin:adobe-ims:disable
```

成功すると、Adobe Commerceに次のメッセージが表示されます。

```terminal
Admin Adobe IMS integration is disabled.
```

## 手順 2:Commerce パスワードを作成または取得する

統合を無効にした後、管理者ユーザーはCommerce パスワードを使用して管理者にログインする必要があります。

* Commerce管理者ユーザーは、既存のCommerce パスワード（IMS 統合前に作成されたCommerce パスワード）を覚えている場合は、そのパスワードを使用して管理者にログインできます。

* Commerce管理者ユーザーが、Commerceの既存のパスワードを持っていない場合や忘れた場合は、新しいパスワードを作成する必要があります。 新しいパスワードを作成するために、管理者ユーザーはを使用できます [!UICONTROL Forgot your password?] Commerceのログインページで新しいパスワードを作成するための機能です。 参照： [顧客パスワードのリセット](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerceでは、空のパスワードフィールドを使用できません。

## 統合を無効にした後

IMS 統合が無効になると、デフォルトのCommerce認証ワークフローが再開され、管理者ユーザーにはパスワードの入力を求められます。

IMS 統合を無効にすると、統合が有効（`Organization ID`, `Client ID`、および `Client Secret` 値）を含めることができます。（Commerce設定ファイルから）
