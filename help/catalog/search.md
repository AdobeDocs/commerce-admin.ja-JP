---
title: カタログ検索について
description: 顧客がストアフロントで商品を検索するために使用できる、クイック検索ツールと高度な検索ツールについて説明します。
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
TQID: https://experienceleague.adobe.com/PV3ZrkqHaUZw-2LFHCNKUeDcvJmkvFcuoR3ZxxURP54
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 541
ht-degree: 0%

---

# カタログ検索について

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=ja)は、高速で非常に関連性の高い直感的な検索体験を提供し、Adobe Commerceで追加料金なしで利用できます。 この節では、[!DNL Live Search]とは異なる可能性のある標準検索機能について説明します。

調査によると、検索機能を利用する人々は、ナビゲーションだけを利用する顧客よりも購入する可能性が高いことが明らかになっています。 実際、一部の調査によると、検索連動型広告を利用する人は、購入する可能性がほぼ2倍になります。

次の節では、基本的なカタログ検索機能について説明します。 ネイティブカタログ検索機能を設定およびカスタマイズする方法について詳しくは、次を参照してください。

- [カタログ検索の設定](search-configuration.md)
- [検索結果](search-results.md)
- [検索語を管理](search-terms.md)

>[!NOTE]
>
>Commerceのネイティブ検索機能では、完全一致の検索結果が表示されます。 Adobe Commerce内のインストールとイネーブルメントに使用できるオプションモジュールである[!DNL Live Search]は異なる方法で実装され、その結果は正確な検索文字列に限定されません。 例えば、_Omega_&#x200B;の数値ラベルが付いた10個の製品がある場合、`Omega 1`を検索すると、_Omega 1_&#x200B;とネイティブ検索機能が1つ一致します。 しかし、ライブ検索によって提供される同じ検索文字列が、複数の項目（_オメガ 1_&#x200B;と&#x200B;_オメガ 10_）に一致します。

## クイック検索

>[!NOTE]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)がインストールされ、[[!DNL Storefront Popover]](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/storefront-popover) ウィジェットが有効になっている場合、検索ボックスに「入力時に検索」の結果がポップオーバーで表示されます。

ストアのヘッダーにある検索ボックスは、訪問者がカタログ内の商品を見つけるのに役立ちます。 検索テキストには、製品名の全部または一部、または製品を説明するその他の単語またはフレーズを使用できます。 ユーザーが製品を検索するために使用する検索キーワードは、管理者から管理できます。

1. **[!UICONTROL Search]**&#x200B;の場合、顧客は検索する内容の最初の数文字を入力します。

   カタログ内の一致はすべて下に表示され、見つかった結果の数が表示されます。

1. お客様はEnter キーを押すか、一致する製品のリストで結果をクリックします。

   ![検索](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## 高度な検索

>[!NOTE]
>
>ここで説明する高度なフォーム検索機能は、[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=ja)には適用されません。

高度な検索により、買い物客はフォームに入力された値にもとづいてカタログを検索できます。 フォームには複数のフィールドが含まれているため、1回の検索で複数のパラメーターを含めることができます。 この結果は、カタログ内のすべての商品のリストで、条件に一致します。 ストアのフッターに、高度な検索へのリンクがあります。

![詳細検索](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

フォームの各フィールドは、製品カタログの属性に対応します。 フィールドを追加するには、属性のフロントエンドプロパティを`Include in Advanced Search`に設定します。 ベストプラクティスとして、顧客が商品を見つける可能性が最も高いフィールドのみを含めるようにしましょう。フィールドの数が多すぎると、検索が遅くなります。

1. ストアのフッターで、顧客は&#x200B;**[!UICONTROL Advanced Search]**&#x200B;をクリックします。

1. _詳細検索_ フォームで、必要な数のフィールドに完全または部分的な値を追加します。

1. **[!UICONTROL Search]**&#x200B;をクリックして結果を表示します。

   ![検索結果](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. 顧客が検索結果で探しているものが表示されない場合、顧客は&#x200B;**[!UICONTROL Modify your search]**&#x200B;をクリックし、別の条件の組み合わせを試みます。
