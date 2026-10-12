---
title: AEM Assetsの使用
description: AEM Assetsでストアメディアアセットを管理しましょう。
feature: CMS, Media
exl-id: 55144019-8ba2-4392-b5dd-216e2ee9daf2
TQID: 'https://experienceleague.adobe.com/c9tgs7PAobBnFZUKX0Zkpik9-kt5O5RXSTYQ61l2sBc'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ddbd0f6e-b569-5a04-8a70-55058777c373
    internal-label: CMS
  - id: 4ca54350-01cb-5b22-8966-5f2873dc6d90
    internal-label: Media
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%
---
# AEM Assetsの使用

<!--In ACAP-844, this topic was linked to from the Commerce Admin products images and videos when the Assets integration is enabled. If the URL to the topic changes, be sure to add a redirect.-->

## アセットの更新

AEM Assetsでアセットを編集した後、アセットを承認して再処理することで、更新をCommerceに送信します。 承認済みのアセットのみがCommerce インスタンスに送信されます。 アセットを再処理することで、アセットがAdobe Commerceに送信される前に、最終的な変更やメタデータの更新が確実に取得されます。

詳しくは、次のAEM Assets ドキュメントを参照してください。

- [デジタルアセットの再処理](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/reprocessing)

- [アセットの承認](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/approve-assets)

## カテゴリへのアセットの追加コンテンツ

AEM Assets統合を有効にして設定すると、アセットをカタログカテゴリのコンテンツに追加できます。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**&#x200B;に移動します。

1. **[!UICONTROL Content]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![ カテゴリーコンテンツ ](./assets/aem-assets-manage-categories.png){width="600" zoomable="yes"}

1. ページの上部に&#x200B;**[!UICONTROL Category Image]**&#x200B;を表示するには、**[!UICONTROL Select from Assets]**&#x200B;をクリックして、AEM Assets フォルダーの画像を使用します。

1. **[!UICONTROL Save]**&#x200B;をクリックして続行します。

   カテゴリを作成する方法の詳細については、[ カテゴリのコンテンツを完了](../catalog/category-create.md#step-3-complete-the-category-content)するを参照してください。

