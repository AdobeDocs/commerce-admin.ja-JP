---
title: Adobe IDとのCommerce管理者統合を無効にする
description: Adobe Commerce管理者とAdobe IMSの連携を無効にする場合は、次のオプション手順に従います。
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/KL6Cx3ymElo7ROx5SUJtlqtKivnw7-heqPWGksGP-pg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 351
ht-degree: 0%

---

# Adobe IDとのCommerce管理者統合を無効にする

{{ee-feature}}

Commerce インスタンスをAdobe IMS認証ワークフローと統合したマーチャントは、このオプション統合を無効にする必要がある場合があります。

Commerceのデプロイメントは、IMS統合が無効になった後、デフォルトのCommerce認証ワークフローとパスワードポリシーに戻ります。 この統合が有効または無効になっている場合は、管理者ユーザーワークフローのみが影響を受けます。

Commerce管理者ログインの概要については、[管理者アカウント ](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html)を参照してください。

## 手順1：統合を無効にする

管理者からこの統合を無効にすることはできません。 CommerceとのAdobe IMS統合を無効にし、Commerce認証をデフォルトの状態に戻すには、コマンドラインインターフェイスから統合を無効にする必要があります。

統合を無効にするには：

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerceでは、正常に終了すると次のメッセージが表示されます。

```
Admin Adobe IMS integration is disabled.
```

## 手順2:Commerce パスワードの作成または取得

統合を無効にした後、管理者ユーザーはCommerce パスワードを使用して管理者にログインする必要があります。

* 既存のCommerce パスワード（つまり、IMS統合前に作成されたCommerce パスワード）を覚えているCommerce管理者ユーザーは、このパスワードを使用して管理者にログインできます。

* 既存のCommerce パスワードを持っていない、または忘れたCommerce管理者ユーザーは、新しいパスワードを作成する必要があります。 新しいパスワードを作成するには、管理者ユーザーはCommerce ログインページの[!UICONTROL Forgot your password?]機能を使用して新しいパスワードを作成できます。 [顧客パスワードのリセット ](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html)を参照してください。 Commerceでは、空のパスワードフィールドは使用できません。

## 統合を無効にした後

IMS統合が無効になった後、デフォルトのCommerce認証ワークフローが再開され、管理者ユーザーにパスワードの入力を再度求めるメッセージが表示されます。

IMS統合を無効にすると、統合が有効になったときに入力された資格情報（`Organization ID`、`Client ID`および`Client Secret`値）がCommerce設定ファイルから削除されます。
