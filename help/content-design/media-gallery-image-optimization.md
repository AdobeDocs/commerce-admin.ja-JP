---
title: メディアギャラリー画像の最適化
description: ' [!DNL Commerce]  メディアアセットに画像の最適化を使用する方法について説明します。'
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/BTjXX6X70q2Mwm0xPNx-t429R5m93VprCHBDcYgQNpY
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
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 211
ht-degree: 0%

---

# メディアギャラリー画像の最適化

新しい[&#x200B; メディアギャラリー](media-gallery.md)では、_画像最適化_&#x200B;機能が提供され、ストアフロントのパフォーマンスが向上し、メディアファイルのサイズが小さくなります。 この最適化はデフォルトで有効になっており、ストア設定で変更できます。

## 画像の最適化の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を展開し、**[!UICONTROL System]**&#x200B;を選択します。

1. ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]**&#x200B;を展開し、次の操作を行います。

   - **[!UICONTROL Enable Image Optimization]**&#x200B;を`Yes`に設定します。
   - 必要に応じて&#x200B;**[!UICONTROL Maximum Width]**&#x200B;と&#x200B;**[!UICONTROL Maximum Height]**&#x200B;の値（ピクセル単位）を入力します。

## 動作

メディアギャラリーの画像最適化機能が有効になっている場合、最適化された画像のコピーが、元のファイルではなく[&#x200B; メディアギャラリー](media-gallery.md)のコンテンツに自動的に挿入されます。

設定で&#x200B;_最大幅_&#x200B;と&#x200B;_最大高さ_&#x200B;の値が変更されると、以前に挿入された既存の最適化された画像がすべて更新されます。

Media Gallery Image Optimizationでは、構成が変更されたときに最適化された画像を再生成するために、`media.gallery.renditions.update` キューのコンシューマーが実行されている必要があります。 詳しくは、_設定ガイド_&#x200B;の「[&#x200B; メッセージキューの管理](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html)」を参照してください。

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

<!-- Last updated from includes: 2024-01-30 15:43:39 -->
