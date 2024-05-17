---
title: '''[!DNL AR Viewer] Adobe Commerce用'
description: 詳細を見る [!DNL AR Viewer] お使いのAdobe Commerce インスタンスで、拡張機能を正常にオンボーディングしてセットアップする方法に役立つ場合があります。
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# [!DNL AR Viewer] Adobe Commerceの場合

AR （Augmented Reality）とは、デバイスのカメラからライブビューに 2D または 3D の要素を追加し、それらの要素が現実世界に存在するように見せるユーザーエクスペリエンスを表します。

この [!DNL AR Viewer] for Adobe Commerce extension は、レンダリングされた 3D グラフィックをユーザーに表示するように設計されたシームレスなエクスペリエンスを強化します。

このガイドの情報では、のオンボーディングエクスペリエンスの概要を説明します [!DNL AR Viewer] Adobe Commerceとその方法 [!DNL AR Viewer] そのジャーニーに沿うためのベストプラクティスと共に、ユーザーにメリットがあります。

Pixar が開発、 [ユニバーサル シーンの説明（USD）](https://www.pixar.com/usd){target=_blank} は、非常に共同作業の多いワークフローを促進しながら、さまざまなアセット、ソース、アニメーションで構成される 3D シーンを確実かつスケーラブルに交換できる最初のオープンソース ソフトウェアです。 この USD は以下で使用されます `.USDZ` ファイル。 この `.USDZ` ファイルは、ユーザーのデバイスに AR および 3D コンテンツを配信します。

>[!NOTE]
>
> この [!DNL AR Viewer] サポートのみ `.USDZ` ファイル。

## [!DNL AR Viewer] 要件

この [!DNL AR Viewer] は、次の両方と互換性があります [!DNL Magento Open Source] とAdobe Commerce。 参照： [ライフサイクルポリシー](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} サポートされているバージョンについて詳しくは、こちらを参照してください。

参照： [のインストール [!DNL AR Viewer] 拡張子](../catalog/ar-viewer-setup.md) を参照してください。

を使用するには [!DNL AR Viewer]インスタンスで次を利用できる必要があります。

* PHP 8.1.0
* Adobe Commerce バージョン 2.4.4 以降
* Magento Open Source（CE）バージョン 2.4.x

## 互換性の制限

[!DNL AR Viewer] 既存の互換性の制限：

* `.USDZ` のみ：この機能は、 `.USDZ` ファイル。
* `qr-code`：が必要 `endroid/qr-code` バージョン 4.5。
* `Catalog module`：が必要 `magento/module-catalog` バージョン 104.0.0。
