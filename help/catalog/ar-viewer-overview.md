---
title: Adobe Commerce用[!DNL AR Viewer]
description: ' [!DNL AR Viewer] がAdobe Commerce インスタンスにどのようなメリットをもたらすのか、拡張機能のオンボーディングとセットアップを成功させる方法について説明します。'
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
TQID: https://experienceleague.adobe.com/ofebqdDS0exPDKJMLB-mpE0eVjRKT5ck91Fm2-7CVjA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# Adobe Commerce用[!DNL AR Viewer]

AR （拡張現実）とは、デバイスのカメラからライブビューに2Dまたは3D要素を追加し、それらの要素を現実世界に住んでいるように見せるユーザーエクスペリエンスを指します。

Adobe Commerce用[!DNL AR Viewer]拡張機能は、ユーザーにレンダリングされた3D グラフィックを表示するように設計されたシームレスなエクスペリエンスを強化します。

このガイドでは、Adobe Commerceの[!DNL AR Viewer]のオンボーディングエクスペリエンスの概要と、[!DNL AR Viewer]がユーザーにどのようなメリットをもたらすのか、また、そのジャーニーに沿って従うべきベストプラクティスについて説明します。

Pixarが開発した[Universal Scene Description （USD） &#x200B;](https://openusd.org/release/index.html){target=_blank}は、非常に協力的なワークフローを促進しながら、様々なアセット、ソース、アニメーションで構成される3D シーンを堅牢かつスケーラブルに交換できる最初のオープンソースソフトウェアです。 このUSDは`.USDZ` ファイル内で使用されます。 この`.USDZ` ファイルは、ユーザーのデバイスにARおよび3D コンテンツを配信します。

>[!NOTE]
>
> [!DNL AR Viewer]は`.USDZ`個のファイルのみをサポートしています。

## [!DNL AR Viewer]要件

[!DNL AR Viewer]は[!DNL Magento Open Source]とAdobe Commerceの両方と互換性があります。 サポートされているバージョンについて詳しくは、[&#x200B; ライフサイクルポリシー](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank}を参照してください。

詳しくは、[拡張機能をインストール  [!DNL AR Viewer] するを参照してください。](../catalog/ar-viewer-setup.md)

[!DNL AR Viewer]を使用するには、インスタンスで次の機能を利用できる必要があります。

* PHP 8.1.0
* Adobe Commerce バージョン 2.4.4以降
* Magento Open Source（CE）バージョン 2.4.x

## 互換性の制限

[!DNL AR Viewer]の既存の互換性の制限：

* `.USDZ`のみ：この機能は`.USDZ` ファイルのみをサポートします。
* `qr-code`: `endroid/qr-code` バージョン 4.5が必要です。
* `Catalog module`: `magento/module-catalog` バージョン 104.0.0が必要です。

