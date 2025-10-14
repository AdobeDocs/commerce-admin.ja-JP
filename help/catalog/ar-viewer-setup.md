---
title: 'Adobe Commerce設定の [!DNL AR Viewer]'
description: 製品リストで拡張機能を使用して 3D モデルアセットを管理す  [!DNL AR Viewer]  方法について説明します。
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Adobe Commerce [!DNL AR Viewer] を使用した製品 3D モデルの管理

製品ごとに、AR および 3D モデルを製品リストで使用できるようにする `.USDZ` ファイルをアップロードできます。

[!DNL AR Viewer] は `.USDZ` ファイルのみをサポートします。

## 拡張機能のインストール

[!DNL AR Viewer] は、[Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank} から拡張機能としてインストールされています。

拡張機能のインストールプロセスについて詳しくは、[_インストールガイド_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html?lang=ja) を参照してください。

[!DNL AR Viewer] 拡張機能をインストールして設定すると、管理者ユーザーは、製品リストを設定、カスタマイズ、管理して 3D モデルを含めることができます。

## 3D モデルの追加

1. 製品を編集モードで開きます。

1. 特定のストア表示を操作するには、**[!UICONTROL Store View]** 選択を該当する表示に設定します。

   >[!NOTE]
   >
   >新しい製品 3D モデルは _常に_ アップロードされ、`All Store Views` スコープがアップロードに使用されない場合でも _すべて_ ストアビューに表示されます。 <br/><br/> 特定のストア表示で製品 3D モデルを非表示にするには、そのストア表示に切り替えて、3D モデルの「**[!UICONTROL Hide from Product Page]**」チェックボックスをオンにし、「**[!UICONTROL Save]**」をクリックする必要があります。

1. 下にスクロールして、「_[!UICONTROL Product 3D Model]_」セクションを展開します。

   ![&#x200B; メニューポップアップ &#x200B;](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. 製品の 3D モデル（`.USDZ` ファイル）を追加します。

1. 「**[!UICONTROL Save]**」をクリックします。

### 3D モデルの削除

製品の詳細から 3D モデルを削除するには：

1. 「**[!UICONTROL Delete]**」をクリックします。

1. 「**[!UICONTROL Save]**」をクリックします。

## 製品の 3D モデルを表示

製品の詳細が 3D モデルで更新された場合：

1. [!DNL AR Viewer] は、AR ファイルをエンコードする QR コードを製品説明内に生成します。

1. お客様は、この QR コードを製品ページで確認できます。

1. 顧客がモバイルデバイスで QR コードをスキャンすると、モバイルデバイスで AR エクスペリエンスがレンダリングされます。

>[!NOTE]
>
> 製品に 3d モデルを追加するユーザーの一連のデモビデオについては、_CommerceのビデオとTutorials[&#x200B; の &#x200B;](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html?lang=ja)Adobe Commerceの AR ビューア_ を参照してください。
