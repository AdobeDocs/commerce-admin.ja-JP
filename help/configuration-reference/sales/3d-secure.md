---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Commerce Admin の [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] ページで設定を確認します。
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] は、安全なオンライントランザクションを促進するために、[!DNL Visa] によって開発されました。 カードネットワークで作成され [!DNL 3-D Secure] ソリューションの例は、[!DNL Visa]、[!DNL Mastercard SecureCode]、[!DNL American Express SafeKey]、[!DNL CardinalCommerce Consumer Authentication] によって検証されています。 [!DNL CardinalCommerce] は、デジタルトランザクション認証の世界的リーダーであり、[!DNL Visa] の完全子会社です。

[!DNL 3-D Secure] バージョン 2.0 では、高度な認証方法や認証フロー、マーチャントと発行者の間のデータ共有の向上など、多数の機能強化がサポートされています。

>[!NOTE]
>
>[Braintree](../../stores-purchase/braintree.md) 支払いゲートウェイは [!DNL 3-D Secure] の確認もサポートしています。

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Environment] | Web サイト | [!DNL CardinalCommerce] アカウントの動作モードを示します。 テスト環境で実行している場合は、「サンドボックス」を選択します。 オプション：サンドボックス /実稼動（デフォルト） |
| [!UICONTROL Org Unit ID] | Web サイト | [!DNL CardinalCommerce] マーチャントアカウントからの組織単位 ID。 |
| [!UICONTROL API Key] | Web サイト | [!DNL CardinalCommerce] マーチャントアカウントの API キー。 |
| [!UICONTROL API Identifier] | Web サイト | [!DNL CardinalCommerce] マーチャントアカウントの API 識別子。 |
| [!UICONTROL Debug] | Web サイト | オプション：`Yes` / `No` |

{style="table-layout:auto"}
