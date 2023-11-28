---
title: Adobe Stockイメージのライセンス
description: 法的なアクセス権を持ち、Adobe Stockの透かしを排除するには、Adobe Stock画像のライセンスを取得します。
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Adobe Stockイメージのライセンス

実稼動用のAdobe CommerceおよびMagento Open Sourceストアに使用するAdobe Stockアセットのライセンスが必要です。 このライセンスを使用すると、画像に法的にアクセスでき、すべての画像に存在するAdobe Stockの透かしを排除できます [画像のプレビュー][save-preview]. 画像のライセンスを取得したり、ライセンスを取得済みの画像を保存するには、Adobeアカウントにログインする必要があります。

新しい [[!DNL Media Gallery]](media-gallery.md) はAdobe Stockと直接統合され、ギャラリーページから直接画像のライセンスを取得しやすくします。

## 前提条件

この機能を使用するには、 [Adobe Stock統合][adobe-stock-integration] モジュールと設定。 ライセンス [Adobe Stock][adobe-stock] 画像には有料のAdobe Stockプランと [Adobeアカウント][adobe-signin].

## 新しい [!DNL Media Gallery]

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. 次の手順に従います。 [Adobe Stock Images の使用][using-adobe-stock] にログインしてプレビュー画像を保存するには、以下を実行します。 [メディアストレージ][media-storage].

   ![保存されたプレビュー画像](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. 画像の下の 3 つのドット (![アセットメニューアイコン](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) をクリックし、次に「 **[!UICONTROL License]**.

   ![Adobe Stock画像アクション](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >ログインしていない場合は、ログインフォームが表示されます。 ログインについて詳しくは、 [Adobe Stock Images の使用][using-adobe-stock].

1. ライセンスの確認ダイアログで、 **[!UICONTROL Confirm]** をクリックして、画像のライセンスを取得します。

   ![ライセンスの確認](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >使用可能である必要があります [Adobe Stock単位][stock-credits] 」をクリックして、画像のライセンスを取得します。

## 標準のメディアストレージから画像のライセンスを取得

1. [Adobe Stock Search グリッドへのアクセス][access-search].

1. 宛先 [画像の詳細を表示][view-details]」で、検索グリッドの画像を順にクリックします。

1. イメージの現在のライセンス状態に応じて、次のいずれかの操作を行います。

   - 画像が既にライセンスされている場合は、 **[!UICONTROL Save]**.

   - 画像が _not_ ライセンス済み、クリック **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >使用可能である必要があります [Adobe Stock単位][stock-credits] 」をクリックして、画像のライセンスを取得します。

   この操作を実行すると、イメージを [メディアストレージ][media-storage]. デフォルトのファイル名が指定されますが、設定に合わせて名前をカスタマイズできます。

   ![Adobe Stockライセンス画像を保存](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. クリック **[!UICONTROL Confirm]**.

   ページはメディアストレージにリダイレクトされ、保存したプレビューが表示されます。

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
