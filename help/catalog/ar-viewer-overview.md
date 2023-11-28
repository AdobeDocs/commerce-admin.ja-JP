---
title: '''[!DNL AR Viewer] Adobe Commerceの'
description: 詳しくは、 [!DNL AR Viewer] は、Adobe Commerceインスタンスと、拡張機能のオンボーディングとセットアップに成功する方法に役立ちます。
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!DNL AR Viewer] Adobe Commerce

Augmented Reality(AR) は、デバイスのカメラからライブビューに 2D または 3D 要素を追加し、それらの要素が実際の世界に存在するように見えるようにするユーザーエクスペリエンスを表します。

The [!DNL AR Viewer] Adobe Commerce用拡張機能を使用すると、レンダリングされた 3D グラフィックをユーザーに表示するように設計されたシームレスなエクスペリエンスを実現できます。

このガイドの情報は、 [!DNL AR Viewer] Adobe Commerceで [!DNL AR Viewer] は、ユーザーにメリットを与え、そのジャーニーに従うためのベストプラクティスを提供します。

Pixar が開発した。 [ユニバーサルシーンの説明 (USD)](https://www.pixar.com/usd){target=_blank} は、非常に協調性の高いワークフローを促進しながら、様々なアセット、ソース、アニメーションで構成される 3D シーンを堅牢かつ拡張可能に交換できる、初のオープンソースソフトウェアです。 この USD は、 `.USDZ` ファイル。 この `.USDZ` ファイルは、AR および 3D コンテンツをユーザーのデバイスに配信します。

>[!NOTE]
>
> The [!DNL AR Viewer] のみをサポート `.USDZ` ファイル。

## [!DNL AR Viewer] 要件

The [!DNL AR Viewer] は、次の両方と互換性があります [!DNL Magento Open Source] Adobe Commerce 詳しくは、 [ライフサイクルポリシー](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} を参照してください。

詳しくは、 [をインストールします。 [!DNL AR Viewer] 拡張](../catalog/ar-viewer-setup.md) を参照してください。

を使用するには [!DNL AR Viewer]を使用する場合は、お使いのインスタンスで以下を使用できる必要があります。

* PHP 8.1.0
* Adobe Commerceバージョン 2.4.4 以降
* Magento Open Source(CE) バージョン 2.4.x

## 互換性の制限

[!DNL AR Viewer] 既存の互換性の制限：

* `.USDZ` のみ：この機能は、次のもののみをサポートします。 `.USDZ` ファイル。
* `qr-code`：が必要です `endroid/qr-code` バージョン 4.5。
* `Catalog module`：が必要です `magento/module-catalog` バージョン 104.0.0。
