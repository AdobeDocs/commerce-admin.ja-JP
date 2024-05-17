---
title: '[!DNL Google Analytics]'
description: の使用方法を説明します [!DNL Google Analytics] Commerce サイトに役立つ指標を収集できます。
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] では、追加のカスタムディメンションおよび指標を定義してトラッキングし、オフラインおよびモバイルアプリのインタラクションをサポートし、継続的な更新にアクセスできるようにします。 [!DNL Google Analytics] 4 はGoogleの次世代型計測ソリューションで、 [!DNL Universal Analytics]. 2023 年 7 月 1 日（PT）に、標準の Universal Analytics プロパティは、新しいヒットの処理を停止します。

>[!NOTE]
>
>ビジネスが、次のようなプライバシー規制の対象となる場合 [EU 一般データ保護規則](../getting-started/compliance-gdpr.md) および/または [カリフォルニア消費者プライバシー法](../getting-started/compliance-ccpa.md)を参照してください [Google プライバシー設定](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>を有効にする場合 [Cookie 制限モード](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] は、Cookie を受け入れない限り、訪問者に関するデータを収集しません。

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### 手順 1：の設定 [!UICONTROL Google Analytics] 4

まだない場合は、 [!DNL Google Analytics] 4 サイトの設定は、次のいずれかの方法で行います。

- [初めて Analytics データ収集を設定](https://support.google.com/analytics/answer/9304153)
- [を使用してサイトにGoogle Analytics 4 を追加する [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### 手順 2:Commerceの設定を完了する

1. Commerce ストアの管理者にログインします。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Google API]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Google GTag]** セクション。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Google Analytics4]** およびを参照し、次の操作を行います。

   - を設定 **[!UICONTROL Enable]** 対象： `Yes`.

   - を残す **[!UICONTROL Account type]** as `Google Analytics4`.

   - を入力 **[!UICONTROL Measurement ID]**. 詳しくは、 [Google Analyticsヘルプ](https://support.google.com/analytics/answer/9539598).

   - A/B テストやその他のパフォーマンステストをコンテンツに対して実行する場合は、を設定します **コンテンツ実験** 対象： `Yes`.

   ![Sales configuration - Google Analytics4 用Google API](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>2023 年 7 月 1 日（PT）をもって、標準のユニバーサルアナリティクス プロパティはデータを処理しなくなります。 まだ依存している場合 [!DNL Universal Analytics]を使用する場合は、を使用することをお勧めします [Google Analytics4 の使用準備](https://support.google.com/analytics/answer/10759417) 先に進む。

### 手順 1:Google Universal Analytics の設定

Googleの web サイトにアクセスして、 [Google Universal Analytics][1] アカウント。

### 手順 2:Commerceの設定を完了する

1. Commerce ストアの管理者にログインします。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Google API]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Google Analytics]** を選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Enable]** 対象： `Yes`.

   - を入力 [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - A/B テストやその他のパフォーマンステストをコンテンツに対して実行する場合は、を設定します **[!UICONTROL Content Experiments]** 対象： `Yes`.

   ![Sales configuration - Google API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

## E コマースの強化

Enhanced E コマースは以下のプラグインです。 [!DNL Google Universal Analytics] これにより、顧客の買い物や購入行動に関するインサイトを得ることができます。 E コマースの強化機能を使用すると、顧客が買い物かごに商品を追加したタイミング、チェックアウトプロセスを開始したタイミング、購入を完了したタイミングなど、顧客の主要なアクティビティに関するレポートを作成できます。 また、購入せずに買い物かごを放棄した買い物客のパターンを特定し、分析することもできます。

次の手順に、設定方法を示します [!DNL Google Tag Manager] （を使用） [!DNL Universal Analytics] 強化された E コマースデータおよびレポートを生成する

### 手順 1. Google アカウントへの新規登録

1. に新規登録 [Google Tag Manager](google-tag-manager.md) アカウントを作成し、Commerceの設定を完了します。

1. 新規登録 [Google Universal Analytics][1] アカウント。

### 手順 2. Enhanced Ecommerce の設定

1. Google Universal Analytics アカウントにログインします。

1. 次の設定を使用して、Enhanced Ecommerce Analytics のプロパティを作成します。

   - 状態：オン
   - 関連製品：オン
   - E コマースレポートの強化機能を有効にする：オン
   - チェックアウトラベル：（必須ではありません）

1. 完了したら、 **[!UICONTROL Submit]**.

### 手順 3. タグとトリガーの作成

1. にログイン [!DNL Google Tag Manager] 次のトリガーをアカウントに追加して作成します。

   | 名前 | イベントタイプ | フィルター |
   |--- |--- |--- |
   | `addToCart` | カスタムイベント |  |
   | `checkout` | カスタムイベント |  |
   | `checkout only` | ページビュー | ページ URL が正規表現/checkout/に一致します。* |
   | `checkoutOption` | カスタムイベント |  |
   | `gtm.dom` | カスタムイベント |  |
   | `productClick` | カスタムイベント |  |
   | `promotionClick` | カスタムイベント |  |
   | `removeFromCart` | カスタムイベント |  |

   >[!NOTE]
   >
   >この [!UICONTROL Checkout] イベントは、組み込みのCommerceの基本的な支払い方法に対してのみトリガーされます `Check / Money Order` および `Cash On Delivery Payment`）に設定します。 このイベントは、に対しては実行されません `PayPal checkout` 外部リソースからチェックアウトへのリダイレクトを使用する、およびその他の外部支払い方法。

1. 同じ基本設定で次の Universal Analytics タグを作成します。

   - Universal Analytics タグ

     | 名前 | タイプ | トリガーの実行 |
     |--- |--- |--- |
     | `Add to cart tracking` | ユニバーサルアナリティクス | addToCart |
     | `Checkout option tracking` | ユニバーサルアナリティクス | checkoutOption |
     | `Checkout tracking` | ユニバーサルアナリティクス | チェックアウト |
     | `Pageview tracking` | ユニバーサルアナリティクス | gtm.dom |
     | `Product click tracking` | ユニバーサルアナリティクス | productClick |
     | `Promo click tracking` | ユニバーサルアナリティクス | promotionClick |
     | `Remove from cart tracking` | ユニバーサルアナリティクス | removeFromCart |

   - タグの基本設定

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | ユニバーサルアナリティクス |
     | [!UICONTROL Tracking ID] | UA-XXX （ユニバーサルアナリティクスアカウントのトラッキング ID） |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | True |
     | [!UICONTROL Use data layer] | True |
     | [!UICONTROL Use Debug version] | True |

1. 個々のトラッキング設定を完了します。

   - 以下を入力します **[!UICONTROL Add to Cart]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | イベント |
     | [!UICONTROL Category] | E コマース |
     | [!UICONTROL Action] | カートに追加 |
     | [!UICONTROL Trigger] | addToCart |

   - 以下を入力します **[!UICONTROL Checkout option]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | イベント |
     | [!UICONTROL Category] | E コマース |
     | [!UICONTROL Action] | チェックアウトオプション |
     | [!UICONTROL Trigger] | checkoutOption |

   - 以下を入力します **[!UICONTROL PageView]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | ページビュー |
     | [!UICONTROL Trigger] | gtm.dom |

   - 次の手順を実行します **[!UICONTROL Product Click]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | イベント |
     | [!UICONTROL Category] | E コマース |
     | [!UICONTROL Action] | 製品クリック |
     | [!UICONTROL Trigger] | productClick |

   - 次の手順を実行します **[!UICONTROL Promotion Click]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | イベント |
     | [!UICONTROL Category] | E コマース |
     | [!UICONTROL Action] | プロモーションをクリック |
     | [!UICONTROL Trigger] | promotionClick |

   - 次の手順を実行します **[!UICONTROL Remove from Cart]** トラッキング設定：

     | 設定 | 値 |
     |--- |--- |
     | [!UICONTROL Track Type] | イベント |
     | [!UICONTROL Category] | E コマース |
     | [!UICONTROL Action] | カートから削除 |
     | [!UICONTROL Trigger] | removeFromCart |

1. 完了したら、 **[!UICONTROL Preview]** そして、タグが正しく機能することを確認します。

1. 設定を確認したら、 **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
