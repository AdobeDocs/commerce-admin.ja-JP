---
title: 'Adobe Commerceの [!DNL AR Viewer]'
description: がAdobe Commerce インスタンスに与えるメリット  [!DNL AR Viewer] 、拡張機能を正常にオンボーディングおよび設定する方法について説明します。
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Adobe Commerceの [!DNL AR Viewer]

AR （Augmented Reality）とは、デバイスのカメラからライブビューに 2D または 3D の要素を追加し、それらの要素が現実世界に存在するように見せるユーザーエクスペリエンスを表します。

[!DNL AR Viewer] for Adobe Commerce拡張機能は、レンダリングされた 3D グラフィックをユーザーに表示するように設計されたシームレスなエクスペリエンスを強化します。

このガイドでは、Adobe Commerceでの [!DNL AR Viewer] ーザーのオンボーディングエクスペリエンスの概要と [!DNL AR Viewer] のメリットのほか、このジャーニーに従うためのベストプラクティスについて説明します。

Pixar が開発した [Universal Scene Description （USD） ](https://openusd.org/release/index.html){target=_blank} は、非常に共同作業の多いワークフローを促進しながら、多くの異なるアセット、ソース、アニメーションで構成される 3D シーンを確実かつスケーラブルに交換できる最初のオープンソースソフトウェアです。 この USD は `.USDZ` ファイル内で使用されます。 この `.USDZ` ファイルは、ユーザーのデバイスに AR および 3D コンテンツを配信します。

>[!NOTE]
>
> [!DNL AR Viewer] は `.USDZ` ファイルのみをサポートします。

## [!DNL AR Viewer] 要件

[!DNL AR Viewer] は、[!DNL Magento Open Source] とAdobe Commerceの両方と互換性があります。 サポートされるバージョンの詳細については、[ ライフサイクル ポリシー ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} を参照してください。

詳しくは、[ 拡張機能のインスト  [!DNL AR Viewer]  ル ](../catalog/ar-viewer-setup.md) を参照してください。

[!DNL AR Viewer] を使用するには、お使いのインスタンスで以下が可能である必要があります。

* PHP 8.1.0
* Adobe Commerce バージョン 2.4.4 以降
* Magento Open Source（CE）バージョン 2.4.x

## 互換性の制限

既存 [!DNL AR Viewer] 互換性に関する制限事項は次のとおりです。

* `.USDZ` のみ：この機能は `.USDZ` ファイルのみをサポートします。
* `qr-code`:`endroid/qr-code` バージョン 4.5 が必要です。
* `Catalog module`:`magento/module-catalog` バージョン 104.0.0 が必要です。
