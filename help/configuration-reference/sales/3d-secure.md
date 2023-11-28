---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: 次のページで設定を確認します： [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] コマース管理のページ。
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] は次のように開発されました： [!DNL Visa] 安全なオンライントランザクションを促進する。 例： [!DNL 3-D Secure] カードネットワークで作成されたソリューションは、 [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey]、および [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] は、デジタルトランザクション認証の世界的なリーダーであり、 [!DNL Visa].

[!DNL 3-D Secure] バージョン 2.0 は、高度な認証方法や認証フロー、およびマーチャントと発行者間のデータ共有の改善など、多数の機能強化をサポートしています。

>[!NOTE]
>
>The [Braintree](../../stores-purchase/braintree.md) また、支払いゲートウェイもサポートします [!DNL 3-D Secure] 検証。

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Environment] | Web サイト | の動作モードを示します。 [!DNL CardinalCommerce] アカウント。 テスト環境で実行している場合は、「サンドボックス」を選択します。 オプション：サンドボックス/実稼動（デフォルト） |
| [!UICONTROL Org Unit ID] | Web サイト | の組織単位 ID。 [!DNL CardinalCommerce] マーチャントアカウント。 |
| [!UICONTROL API Key] | Web サイト | の API キー [!DNL CardinalCommerce] マーチャントアカウント。 |
| [!UICONTROL API Identifier] | Web サイト | からの API 識別子 [!DNL CardinalCommerce] マーチャントアカウント。 |
| [!UICONTROL Debug] | Web サイト | オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
