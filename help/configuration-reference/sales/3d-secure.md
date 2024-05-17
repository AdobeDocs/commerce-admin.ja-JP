---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: の設定を確認します。 [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] コマース管理者のページ。
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] は、次によって開発されました： [!DNL Visa] 安全なオンライントランザクションを促進する。 例 [!DNL 3-D Secure] カードネットワークで作成されたソリューションは、次によって検証されます [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey]、および [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] は、デジタルトランザクション認証のグローバルリーダーで、の完全子会社です [!DNL Visa].

[!DNL 3-D Secure] バージョン 2.0 では、高度な認証方法や認証フロー、マーチャントと発行者の間のデータ共有の向上など、多数の機能強化がサポートされています。

>[!NOTE]
>
>この [Braintree](../../stores-purchase/braintree.md) 支払いゲートウェイもサポート [!DNL 3-D Secure] 検証。

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Environment] | Web サイト | の動作モードを示します [!DNL CardinalCommerce] アカウント。 テスト環境で実行している場合は、「サンドボックス」を選択します。 オプション：サンドボックス /実稼動（デフォルト） |
| [!UICONTROL Org Unit ID] | Web サイト | からの組織単位 ID [!DNL CardinalCommerce] マーチャントアカウント。 |
| [!UICONTROL API Key] | Web サイト | の API キー [!DNL CardinalCommerce] マーチャントアカウント。 |
| [!UICONTROL API Identifier] | Web サイト | からの API 識別子 [!DNL CardinalCommerce] マーチャントアカウント。 |
| [!UICONTROL Debug] | Web サイト | オプション： `Yes` / `No` |

{style="table-layout:auto"}
