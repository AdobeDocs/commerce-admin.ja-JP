---
title: '[!DNL Google Analytics]'
description: 使用方法 [!DNL Google Analytics] コマースサイトに役立つ指標を収集する。
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] では、オフラインおよびモバイルアプリのインタラクションをサポートし、継続的な更新にアクセスできるように、追跡用の追加のカスタムディメンションおよび指標を定義できます。 [!DNL Google Analytics] 4 はGoogleの次世代測定ソリューションであり、代わりとなる [!DNL Universal Analytics]. 2023 年 7 月 1 日に、標準のユニバーサルアナリティクスプロパティは、新しいヒットの処理を停止します。

>[!NOTE]
>
>お客様のビジネスが [EU 一般データ保護規則](../getting-started/compliance-gdpr.md) および/または [カリフォルニア州消費者プライバシー法](../getting-started/compliance-ccpa.md)を参照してください。 [Google Privacy Settings](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>以下を有効にした場合、 [Cookie 制限モード](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] では、cookie を受け入れない限り訪問者に関するデータを収集しません。

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### 手順 1：セットアップ [!UICONTROL Google Analytics] 4

まだ [!DNL Google Analytics] 4 サイトのセットアップは、次のいずれかの方法でおこないます。

- [Analytics データ収集の初回セットアップ](https://support.google.com/analytics/answer/9304153)
- [Google Analytics4 を [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### 手順 2：コマース設定の完了

1. コマースストアの管理者にログインします。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Google API]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Google GTag]** 」セクションに入力します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Google Analytics4]** サブセクションで、以下の操作を実行します。

   - 設定 **[!UICONTROL Enable]** から `Yes`.

   - を残します。 **[!UICONTROL Account type]** as `Google Analytics4`.

   - を入力します。 **[!UICONTROL Measurement ID]**. 詳しくは、 [Google Analyticsヘルプ](https://support.google.com/analytics/answer/9539598).

   - コンテンツに対して A/B テストや他のパフォーマンステストを実行する場合は、 **コンテンツ実験** から `Yes`.

   ![セールス設定 —Google Analytics4 用Google API](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>2023 年 7 月 1 日 (PT) に、標準のユニバーサルアナリティクスプロパティはデータを処理しなくなります。 依然として [!DNL Universal Analytics]を使用する場合は、 [Google Analytics4 を使用する準備](https://support.google.com/analytics/answer/10759417) 前に進む。

### 手順 1:Google Universal Analytics のセットアップ

Googleの Web サイトにアクセスし、 [Google Universal Analytics][1] アカウント。

### 手順 2：コマース設定の完了

1. コマースストアの管理者にログインします。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Google API]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Google Analytics]** 」セクションで次の操作を実行します。

   - 設定 **[!UICONTROL Enable]** から `Yes`.

   - を入力します。 [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - コンテンツに対して A/B テストや他のパフォーマンステストを実行する場合は、 **[!UICONTROL Content Experiments]** から `Yes`.

   ![セールス設定 — Google API -Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

## e コマースの強化

拡張 e コマースは、 [!DNL Google Universal Analytics] 顧客の買い物行動や購入行動を把握できます。 拡張 e コマースを使用すると、顧客が品目を買い物かごに追加した場合、チェックアウトプロセスを開始する場合、購入を完了する場合など、主要な顧客アクティビティに関するレポートを作成できます。 また、買い物かごを放棄した買い物客のパターンを購入せずに特定し、分析することもできます。

次の手順は、 [!DNL Google Tag Manager] 次を使用 [!DNL Universal Analytics] e コマースのデータおよびレポートを拡張しました。

### 手順 1. Googleアカウントに新規登録

1. 新規登録： [Google Tag Manager](google-tag-manager.md) アカウントを作成し、コマース設定を完了します。

1. 新規登録 [Google Universal Analytics][1] アカウント。

### 手順 2. 拡張 e コマースの設定

1. Google Universal Analytics アカウントにログインします。

1. 次の設定を使用して、拡張 e コマース分析用のプロパティを作成します。

   - ステータス：オン
   - 関連製品：オン
   - 拡張 e コマースレポートを有効にする：オン
   - チェックアウトのラベル付け： （必須ではありません）

1. 完了したら、「 **[!UICONTROL Submit]**.

### 手順 3. タグとトリガーの作成

1. ログイン先： [!DNL Google Tag Manager] アカウントを作成し、次のトリガーを作成します。

   | 名前 | イベントタイプ | フィルター |
   |--- |--- |--- |
   | `addToCart` | カスタムイベント |  |
   | `checkout` | カスタムイベント |  |
   | `checkout only` | ページビュー | ページ URL は RegEx /checkout/に一致します。* |
   | `checkoutOption` | カスタムイベント |  |
   | `gtm.dom` | カスタムイベント |  |
   | `productClick` | カスタムイベント |  |
   | `promotionClick` | カスタムイベント |  |
   | `removeFromCart` | カスタムイベント |  |

   >[!NOTE]
   >
   >The [!UICONTROL Checkout] イベントは、組み込みの Commerce 基本支払い方法 ( `Check / Money Order` および `Cash On Delivery Payment`) をクリックします。 このイベントは、 `PayPal checkout` 外部リソースからのチェックアウトへのリダイレクトを使用する、その他の外部支払い方法。

1. 同じ基本設定で次の Universal Analytics タグを作成します。

   - Universal Analytics タグ

     | 名前 | タイプ | 実行トリガー |
     |--- |--- |--- |
     | `Add to cart tracking` | ユニバーサル分析 | addToCart |
     | `Checkout option tracking` | ユニバーサル分析 | checkoutOption |
     | `Checkout tracking` | ユニバーサル分析 | checkout |
     | `Pageview tracking` | ユニバーサル分析 | gtm.dom |
     | `Product click tracking` | ユニバーサル分析 | productClick |
     | `Promo click tracking` | ユニバーサル分析 | promotionClick |
     | `Remove from cart tracking` | ユニバーサル分析 | removeFromCart |

   - 基本タグ設定

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | ユニバーサル分析 |
     | [!UICONTROL Tracking ID] | UA-XXX （Universal Analytics アカウントからのトラッキング ID） |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | True |
     | [!UICONTROL Use data layer] | True |
     | [!UICONTROL Use Debug version] | True |

1. 個々のトラッキング設定を完了します。

   - 次を入力します。 **[!UICONTROL Add to Cart]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | イベント |
     | [!UICONTROL Category] | e コマース |
     | [!UICONTROL Action] | 買い物かごに追加 |
     | [!UICONTROL Trigger] | addToCart |

   - 次を入力します。 **[!UICONTROL Checkout option]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | イベント |
     | [!UICONTROL Category] | e コマース |
     | [!UICONTROL Action] | チェックアウトオプション |
     | [!UICONTROL Trigger] | checkoutOption |

   - 次を入力します。 **[!UICONTROL PageView]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - 次の手順を実行します。 **[!UICONTROL Product Click]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | イベント |
     | [!UICONTROL Category] | e コマース |
     | [!UICONTROL Action] | 製品のクリック |
     | [!UICONTROL Trigger] | productClick |

   - 次の手順を実行します。 **[!UICONTROL Promotion Click]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | イベント |
     | [!UICONTROL Category] | e コマース |
     | [!UICONTROL Action] | プロモーションクリック |
     | [!UICONTROL Trigger] | promotionClick |

   - 次の手順を実行します。 **[!UICONTROL Remove from Cart]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | イベント |
     | [!UICONTROL Category] | e コマース |
     | [!UICONTROL Action] | 買い物かごから削除 |
     | [!UICONTROL Trigger] | removeFromCart |

1. 完了したら、「 **[!UICONTROL Preview]** タグが正しく機能することを確認します。

1. 設定を確認したら、 **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
