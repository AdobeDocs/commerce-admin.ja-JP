---
title: ザ  [!DNL Media Gallery]
description: メディアギャラリーを使用して、サーバー上のメディアファイルを整理および管理します。
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/PL80USg-GVh-vlWwoYCuWRzJdO-FzHDFmFSDjxhavo8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# ザ [!DNL Media Gallery]

Adobe CommerceまたはMagento Open Source 2.4では、新しい&#x200B;_enhanced_ [!DNL Media Gallery]を使用して、サーバー上のメディアファイルを整理および管理できます。 この新しい[!DNL Media Gallery]には、既存のメディアストレージと同じ機能が含まれていますが、改善されたユーザーインターフェイスと[Adobe Stock](https://stock.adobe.com)との緊密な統合が含まれています。

![&#x200B; メディアギャラリーグリッドに表示される画像](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>[_[!UICONTROL Images and Videos]_&#x200B;製品セクション &#x200B;](../catalog/product-image.md#upload-an-image)に追加された製品画像は、[!DNL Media Gallery]によって管理されません。 新しい[!DNL Media Gallery]では、_[!UICONTROL Content]_&#x200B;製品セクション フィールドで使用されている画像のみが表示され、フィルタリングされます。

## 新しい[!DNL Media Gallery]を有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を展開し、**[!UICONTROL System]**&#x200B;を選択します。

1. ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**&#x200B;を展開します。

   ![詳細設定 – [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable Old Media Gallery]**&#x200B;を`No`に設定します。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

1. プロンプトが表示されたら、システムメッセージの&#x200B;**[!UICONTROL Cache Management]** リンクをクリックし、無効なキャッシュを更新します。

   [[!UICONTROL Content] メニュー](/help/content-design/content-menu.md)に新しい&#x200B;_[!UICONTROL Media Gallery]_&#x200B;オプションが表示されるようになりました。

>[!NOTE]
>
>新しい[!DNL Media Gallery]の完全な機能を使用するには、`media.gallery.synchronization`および`media.content.synchronization` キューのコンシューマーを最初の同期のために開始する必要があります。 詳しくは、_設定ガイド_&#x200B;の「[&#x200B; メッセージキューの管理](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html)」を参照してください。

## 新しい[!DNL Media Gallery]にアクセス

新しい[!DNL Media Gallery]は、コンテンツ メニューから、または[&#x200B; ページを追加または編集](/help/content-design/page-add.md)するときにアクセスできます。 また、[&#x200B; カテゴリを作成または編集する場合](/help/catalog/category-create.md)や、[&#x200B; コンテンツエディター](/help/content-design/editor-insert-image.md)を使用して画像を挿入する場合にもアクセスできます。

[!UICONTROL Content] メニューから新しい[!UICONTROL Media Gallery]にアクセスするには：

- _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**&#x200B;に移動します。

ページの追加または編集時に新しいメディアギャラリーにアクセスするには：

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**&#x200B;に移動します。

1. **[!UICONTROL Add a New Page]**&#x200B;をクリックします。

   既存のページを編集する場合は、_[!UICONTROL Action]_&#x200B;列を使用して&#x200B;**[!UICONTROL Select]**&#x200B;をクリックし、**[!UICONTROL Edit]**&#x200B;を選択できます。

1. **[!UICONTROL Content]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   - [&#x200B; ページビルダーが有効になっている](../page-builder/setup.md)場合は、**[!UICONTROL Media]** パネルを展開し、**[!UICONTROL Image]** プレースホルダーをターゲットコンテナにドラッグします。 次に、**[!UICONTROL Select from Gallery]**&#x200B;をクリックします。

     ![画像をステージにドラッグ &#x200B;](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - [WYSIWYG エディターが有効になっている](/help/content-design/editor.md)場合は、**[!UICONTROL Show/Hide Editor]**&#x200B;をクリックし、**[!UICONTROL Insert Image]**&#x200B;をクリックします。

## [!DNL Media Gallery] デモ

[!DNL Media Gallery]について詳しくは、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12&learn=on)
