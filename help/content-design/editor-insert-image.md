---
title: エディターでの画像の挿入
description: WYSIWYG エディターを使用すると、メディアストレージから画像を簡単に挿入したり、別のサーバーにある画像にリンクしたり、Adobe Stock アセットを使用したりできます。
exl-id: 591830c9-6dba-4738-a6e7-cf5f93b3c319
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/0SlAN-Ija-mUYhkTfmC4QEfuGPw73szU5-7dqwcFKtc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
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
source-wordcount: 374
ht-degree: 0%

---

# エディターでの画像の挿入

エディターから、次の3つのソースタイプを使用して画像を挿入できます。

- [&#x200B; メディアストレージ &#x200B;](media-storage.md)にアップロードされた画像を追加します
- 別のサーバーにある画像へのリンク
- Adobe Stockとの統合を使用して、Adobe Stock アセットを検索および使用する

![&#x200B; メディアストレージ &#x200B;](./assets/media-storage.png){width="650" zoomable="yes"}

1. 編集モードでページ、ブロック、またはダイナミックブロックを開きます。

1. _[!UICONTROL Content]_&#x200B;セクションに移動し、エディターをサポートする任意の要素をクリックします。

1. 画像を表示する位置にカーソルを置きます。

1. エディターツールバーで、_画像を挿入_ アイコンをクリックします。

   ![画像を挿入アイコン &#x200B;](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   このアクションにより、_[!UICONTROL Insert/edit image]_&#x200B;ダイアログが開きます。

1. **Source**&#x200B;の場合、_検索_ アイコンをクリックし、使用する画像アセットの場所と一致するメソッドを使用します。

   ![検索アイコンの選択](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

   - **新しい画像をアップロード**：この方法を使用して、新しい画像ファイルをアップロードします。

      - 新しい画像ファイルを追加するツリー内のフォルダーを選択します。

      - **[!UICONTROL Choose Files]**&#x200B;をクリックします。

      - 画像ファイルを探して選択します。

      - 新しいファイルのサムネールをクリックし、**[!UICONTROL Add Selected]**&#x200B;をクリックします。

   - **既存のアセットを選択**：この方法を使用して、メディアストレージ/ギャラリーから既存の画像アセットを選択します。

      - ツリーを使用して画像に移動します。

      - サムネールをクリックし、**[!UICONTROL Add Selected]**&#x200B;をクリックします。

   - **Adobe Stock画像を検索して選択**：この方法を使用して、Adobe Stockから画像を検索します。

     >[!NOTE]
     >
     >この方法では、管理者用に設定された[Adobe Stock統合](adobe-stock.md)が必要です。

      - **[!UICONTROL Search Adobe Stock]**&#x200B;をクリックし、画像を検索します。

      - プレビューまたはライセンスされた画像をギャラリーに保存します。

        [Adobe Stock](https://stock.adobe.com) アセットの操作について詳しくは、[Adobe Stock Images](adobe-stock-manage.md)の使用を参照してください。

      - ギャラリーでアセットのサムネールを選択し、**[!UICONTROL Add Selected]**&#x200B;をクリックします。

1. **[!UICONTROL Image Description]**&#x200B;に、画像の簡単な説明を入力します。

1. ページ上に画像をレンダリングするために、幅と高さ&#x200B;**[!UICONTROL Dimensions]**&#x200B;をピクセル単位で入力します。

   画像の縦横比を自動的に維持するには、**[!UICONTROL Constrain proportions]** チェックボックスを選択したままにします。

1. **[!UICONTROL Insert]**&#x200B;をクリックしてプロセスを完了します。
