---
title: カタログ検索の概要
description: ストアフロントで製品を見つけるために使用できるクイック検索ツールと詳細検索ツールについて説明します。
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---

# カタログ検索の概要

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) は、迅速で非常に関連性が高く直感的な検索エクスペリエンスを提供し、Adobe Commerceでは追加料金なしで利用できます。 ここでは、とは異なる可能性のある標準の検索機能について説明します [!DNL Live Search].

調査によると、検索を使用するユーザーは、ナビゲーションだけに依存する顧客よりも購入する可能性が高くなります。 実際、一部の調査によると、検索を使用する人は、購入する可能性がほぼ 2 倍です。

次の節では、基本的なカタログ検索機能について説明します。 ネイティブカタログ検索機能の設定とカスタマイズ方法について詳しくは、以下を参照してください。

- [カタログ検索の設定](search-configuration.md)
- [検索結果](search-results.md)
- [検索語句の管理](search-terms.md)

>[!NOTE]
>
>Commerceのネイティブ検索機能は、完全一致の検索結果を提供します。 While [!DNL Live Search]Adobe Commerce内でのインストールとイネーブルメントに使用できるオプションモジュールの実装は異なり、結果は正確な検索文字列に限定されません。 例えば、以下のように数値でラベル付けされた 10 個の製品があるとします _オメガ_：の検索 `Omega 1` 1 回の一致で次に対する結果： _オメガ 1_ ネイティブ検索機能を使用する。 ただし、ライブ検索を利用した同じ検索文字列では、複数の項目が一致します。 _オメガ 1_ および _オメガ 10_.

## クイック検索

>[!NOTE]
>
>条件 [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html) がインストールされている場合、検索ボックスは「入力中に検索」を返し、結果がポップアップで表示されます。

ストアのヘッダーにある検索ボックスは、訪問者がカタログ内の製品を見つけるのに役立ちます。 検索テキストには、製品名の全部または一部や、製品を説明するその他の単語やフレーズを使用できます。 製品を検索するためにユーザーが使用する検索用語は、管理者から管理できます。

1. の場合 **[!UICONTROL Search]**&#x200B;検索する文字列の最初の数文字を入力します。

   カタログ内の一致が以下に表示され、見つかった結果の数が表示されます。

1. 顧客が Enter キーを押すか、一致する製品のリスト内の結果をクリックします。

   ![検索](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## 詳細検索

>[!NOTE]
>
>ここで説明する高度なフォーム検索機能は、に適用されません [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

詳細検索を使用すると、買い物客はフォームに入力された値に基づいてカタログを検索できます。 フォームには複数のフィールドが含まれているので、1 回の検索で複数のパラメーターを指定できます。 結果として、条件に一致するカタログ内のすべての製品のリストが表示されます。 詳細検索へのリンクは、ストアのフッターにあります。

![詳細検索](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

フォーム内の各フィールドは、製品カタログの属性に対応しています。 フィールドを追加するには、属性のフロントエンドプロパティをに設定します `Include in Advanced Search`. ベストプラクティスとして、顧客が製品を見つけるために使用する可能性が最も高いフィールドのみを含めます。多すぎると検索が遅くなるからです。

1. ストアのフッターで、顧客は次をクリックします **[!UICONTROL Advanced Search]**.

1. が含まれる _詳細検索_ フォームでは、必要な数のフィールドに完全な値または部分的な値を追加します。

1. クリック数 **[!UICONTROL Search]** をクリックして結果を表示します。

   ![検索結果](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. 検索結果に探しているものが表示されない場合は、ユーザーがクリックします **[!UICONTROL Modify your search]** そして、別の条件の組み合わせを試します。
