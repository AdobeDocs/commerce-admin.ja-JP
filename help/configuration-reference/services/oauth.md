---
title: '[!UICONTROL Services] > [!UICONTROL OAuth]'
description: Commerce管理者の[!UICONTROL Services] > [!UICONTROL OAuth] ページで設定を確認します。
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/gwRxAaSnEul4D-LjjoGIcEiUCLl8ZrKjcSaMTvlGUKY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![&#x200B; アクセストークンの有効期限](./assets/oauth-token-expire.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | グローバル | 顧客API トークンの有効期限が切れるまでの時間を時間単位で指定します。 フィールドが空の場合、顧客トークンは期限切れになりません。 デフォルト値：`1` |
| [!UICONTROL Admin Token Lifetime (hours)] | グローバル | 管理者API トークンの有効期限が切れるまでの時間を時間単位で指定します。 フィールドが空の場合、管理者トークンは期限切れになりません。 デフォルト値：`4` |

{style="table-layout:auto"}

>[!NOTE]
>
>ベアラー顧客と管理者API トークンの有効期間と暗号化アルゴリズムは、[JWT認証](magento-web-api.md#jwt-authentication)の設定設定によって制御されます。

## [!UICONTROL Cleanup Settings]

![&#x200B; クリーンアップ設定](./assets/oauth-cleanup.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | グローバル | クリーンアップを開始する前のOAuth要求の数を指定します。 クリーンアップを無効にするには、`0`を入力しないでください。 |
| [!UICONTROL Enable WSDL Cache] | グローバル | エントリをクリーニングする前に、エントリの経過時間を数分で決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Consumer Settings]

![&#x200B; コンシューマー設定](./assets/oauth-consumer-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | グローバル | 顧客が資格情報を投稿したときにシステムがタイムアウトするまでの時間を秒単位で指定します。 |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | グローバル | コンシューマー資格情報の投稿に関連するリダイレクトの最大数を指定します。 |
| [!UICONTROL Expiration Period] | グローバル | 未使用のキー/秘密鍵がOAuth トークン交換の開始後に期限切れになるまでの秒数を指定します。 |

{style="table-layout:auto"}

## [!UICONTROL Authentication Locks]

![認証ロック &#x200B;](./assets/oauth-locks.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | グローバル | アカウントをロックアウトするための認証エラーの最大数を指定します。 |
| [!UICONTROL Lockout Time (seconds)] | グローバル | アカウントのロックを解除するまでの時間（秒単位）を指定します。 |

{style="table-layout:auto"}
