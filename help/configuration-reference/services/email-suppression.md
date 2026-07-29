---
title: '[!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]'
description: Commerce管理者の[!UICONTROL Adobe Services] > [!UICONTROL Email Suppression] ページで設定を確認します。
feature: Configuration, Communications
badgeSaas: label="SaaSのみ" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud ServiceおよびAdobe Commerce Optimizer プロジェクト（Adobeが管理するSaaS インフラストラクチャ）にのみ適用されます。"
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f4d7033067a99421224ab2159b1b95775e5e949f
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]

{{config}}

[!UICONTROL Email Suppression]を使用すると、管理者は、ストアの残りのメールに影響を与えたり、開発者の関与を必要としたりすることなく、特定のカテゴリの自動システムメールをオフにできます。 この機能を使用すると、データ移行時の注文メールやマーケティングメールなど、特定の通知を一時的または完全に停止できます。

>[!IMPORTANT]
>
>二段階認証コードや管理者パスワードリセットのメールなど、セキュリティ関連の管理者通知は、この機能によって抑制されることはありません。

このページの設定は[&#x200B; ストアビュー](../../getting-started/websites-stores-views.md#scope-settings)ごとに適用されるため、異なるストアフロントに対して異なるメールカテゴリを抑制できます。

>[!NOTE]
>
>抑制をオフにすると、通常のメール配信は直ちに復元されますが、抑制期間中に送信されたメールはキューに入れられません。

## [!UICONTROL Email Suppression]

![電子メール抑制](./assets/email-suppression.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Email Suppression] | ストアビュー | 機能のマスターオン/オフスイッチ。 `No`に設定すると（デフォルト）、このページの他のすべての設定が無視され、すべてのメールが正常に送信されます。 |
| [!UICONTROL Disabled Functional Areas] | ストアビュー | 電子メールを除外する1つ以上のビジネス カテゴリを選択します。 各カテゴリに含まれる内容については、[&#x200B; ビジネス カテゴリ &#x200B;](#business-categories)を参照してください。 |
| [!UICONTROL Disabled Template IDs] | ストアビュー | カテゴリーに関係なく、個別に抑制する特定のメールテンプレートのコンマ区切りリスト（オプション）。 管理者で作成したカスタムテンプレートのテンプレートコード （例：`customer_password_forgot_email_template`）または数値テンプレート IDを使用します。 |

{style="table-layout:auto"}

### 業種 {#business-categories}

| カテゴリ | 一般的なメールが含まれています |
|--- |--- |
| 顧客アカウント | アカウント作成、パスワードリセット、アカウント情報の変更。 |
| Order Management | 注文確認、請求書、発送、クレジットメモ、注文キャンセル。 |
| 返品（RMA） | 商品の承認通知を返す。 |
| チェックアウトと支払い | チェックアウトや有料リンク関連のメール： |
| マーケター | ニュースレター、商品アラート、ウィッシュリスト共有、友達へのメール、リマインダー、招待状、ギフトレジストリ。 |
| ストアクレジット&amp;リワード | ギフトカード、リワードポイント、ストアクレジット残高の変更。 |
| B2B | 会社、交渉可能な見積もり、および発注通知。 |
| システム通知 | 定期インポート、エクスポート、問い合わせフォームのメールなどの運用通知。 |

{style="table-layout:auto"}
