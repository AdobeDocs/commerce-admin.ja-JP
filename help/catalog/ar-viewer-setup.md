---
title: Adobe Commerce セットアップ用[!DNL AR Viewer]
description: 製品リストに [!DNL AR Viewer] 拡張機能を使用した3D モデルアセットの管理について説明します。
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
TQID: https://experienceleague.adobe.com/6OlcZ4Psm3INgVm7f-Y9JvqfUdmR6Rg48tcigLAHiaE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 313
ht-degree: 0%

---

# Adobe Commerce用[!DNL AR Viewer]を使用した商品3D モデルの管理

製品ごとに、AR モデルと3D モデルを製品リストで使用できるように`.USDZ` ファイルをアップロードできます。

[!DNL AR Viewer]は`.USDZ`個のファイルのみをサポートしています。

## 拡張機能のインストール

[!DNL AR Viewer]は、[Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}の拡張機能としてインストールされています。

拡張機能のインストールプロセスについて詳しくは、[_インストールガイド_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html)を参照してください。

[!DNL AR Viewer]拡張機能をインストールして設定した後、管理者ユーザーは3D モデルを含めるように製品リストを設定、カスタマイズ、管理できます。

## 3D モデルを追加

1. 製品を編集モードで開きます。

1. 特定のストアビューで作業するには、**[!UICONTROL Store View]**&#x200B;選択範囲を該当するビューに設定します。

   >[!NOTE]
   >
   >新しい製品3D モデルは、`All Store Views` スコープがアップロードに使用されていない場合でも、_常に_ アップロードされ、_すべて_&#x200B;のストアビューに表示されます。 <br/><br/>特定のストアビューから商品3D モデルを非表示にするには、そのストアビューに切り替え、3D モデルの&#x200B;**[!UICONTROL Hide from Product Page]** チェックボックスを選択して、**[!UICONTROL Save]**&#x200B;をクリックする必要があります。

1. 下にスクロールして、_[!UICONTROL Product 3D Model]_&#x200B;セクションを展開します。

   ![&#x200B; メニューポップアップ &#x200B;](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. 製品の3D モデル （`.USDZ` ファイル）を追加します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

### 3D モデルを削除

製品の詳細から3D モデルを削除するには：

1. **[!UICONTROL Delete]**&#x200B;をクリックします。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 製品の3D モデルの表示

製品の詳細が3D モデルで更新された場合：

1. [!DNL AR Viewer]は、AR ファイルをエンコードする製品説明にQR コードを生成します。

1. 顧客は商品ページでこのQR コードを見ることができます。

1. 顧客がモバイルデバイスでQR コードをスキャンすると、AR体験がモバイルデバイスでレンダリングされます。

>[!NOTE]
>
> 3d モデルを製品に追加するユーザーの一連のデモ動画については、_Commerce ビデオとチュートリアル_&#x200B;の[AR Viewer for Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) ページを参照してください。

