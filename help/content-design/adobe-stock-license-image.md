---
title: Adobe Stock画像のライセンスを取得
description: 法的なアクセス権を持ち、Adobe Stockの透かしを排除するには、Adobe Stock画像のライセンスを取得します。
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Adobe Stock画像のライセンスを取得

実稼動Adobe CommerceおよびMagento Open Sourceストアに使用するAdobe Stock アセットには、ライセンスが必要です。 このライセンスにより、画像への法的アクセスが可能になり、すべてに存在するAdobe Stockの透かしを排除できます [画像プレビュー][save-preview]. 画像のライセンスを取得したり、既にライセンスを取得した画像を保存したりするには、Adobeアカウントにログインする必要があります。

新しい [[!DNL Media Gallery]](media-gallery.md) は、Adobe Stockと直接統合できるので、ギャラリーページから直接イメージのライセンスを簡単に取得できます。

## 前提条件

この機能には、 [Adobe Stockの統合][adobe-stock-integration] モジュールと設定。 ライセンス [Adobe Stock][adobe-stock] 画像を使用するには、有料のAdobe Stock プランおよびが必要です。 [Adobeアカウント][adobe-signin].

## 新しいから画像のライセンスを取得 [!DNL Media Gallery]

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. の手順に従います [Adobe Stock画像の使用][using-adobe-stock] にログインしてプレビューイメージを保存するには [メディアストレージ][media-storage].

   ![保存されたプレビュー画像](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. 画像の下の 3 つのドットをクリックします（![アセットメニューアイコン](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}）を選択し、 **[!UICONTROL License]**.

   ![Adobe Stock画像アクション](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >ログインしていない場合は、ログインフォームが表示されます。 ログインの詳細については、を参照してください。 [Adobe Stock画像の使用][using-adobe-stock].

1. ライセンスの確認ダイアログで、 **[!UICONTROL Confirm]** ：画像のライセンスを取得します。

   ![ライセンスの確認](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >利用可能である必要があります [Adobe Stock クレジット][stock-credits] アカウントでをクリックして、画像のライセンスを取得します。

## 標準メディアストレージからの画像のライセンス取得

1. [Adobe Stock検索グリッドへのアクセス][access-search].

1. 終了 [画像の詳細の表示][view-details]で、検索グリッド内の画像を順にクリックします。

1. イメージの現在のライセンス ステータスに応じて、次のいずれかの操作を行います。

   - 画像がライセンス済みの場合は、 **[!UICONTROL Save]**.

   - 画像がの場合 _ではない_ ライセンス済み、クリック **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >利用可能である必要があります [Adobe Stock クレジット][stock-credits] アカウントでをクリックして、画像のライセンスを取得します。

   この操作を実行すると、イメージをに保存するために使用するファイル名を指定するようプロンプトが表示されます [メディアストレージ][media-storage]. デフォルトのファイル名が提供されますが、この名前は好みに合わせてカスタマイズできます。

   ![Adobe Stockのライセンス画像を保存](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. クリック **[!UICONTROL Confirm]**.

   ページがメディアストレージにリダイレクトされ、保存されたプレビューが表示されます。

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
