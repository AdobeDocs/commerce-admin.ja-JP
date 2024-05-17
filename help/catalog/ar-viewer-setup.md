---
title: '[!DNL AR Viewer] Adobe Commerceの設定の場合'
description: を使用した 3D モデルアセットの管理について説明します [!DNL AR Viewer] 製品リストの拡張機能。
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# を使用した製品 3D モデルの管理 [!DNL AR Viewer] Adobe Commerceの場合

製品ごとに、 `.USDZ` 製品リストで AR および 3D モデルを使用できるようにするファイル。

この [!DNL AR Viewer] のみをサポート `.USDZ` ファイル。

## 拡張機能のインストール

[!DNL AR Viewer] は、から拡張機能としてインストールされます [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

を参照してください。 [_インストールガイド_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) 拡張機能のインストールプロセスについて詳しくは、を参照してください。

後 [!DNL AR Viewer] 拡張機能がインストールおよび設定されると、管理者ユーザーは、製品リストを設定、カスタマイズ、管理して 3D モデルを含めることができます。

## 3D モデルの追加

1. 製品を編集モードで開きます。

1. 特定のストア表示を使用するには、 **[!UICONTROL Store View]** 該当するビューを選択します。

   >[!NOTE]
   >
   >新製品の 3D モデルは次のとおりです _常に_ アップロードしてに表示 _all_ ビューの保存（例： `All Store Views` 範囲は、アップロードには使用されません。 <br/><br/>特定のストア ビューで製品 3D モデルを非表示にするには、そのストア ビューに切り替えて、 **[!UICONTROL Hide from Product Page]** 3D モデルのチェックボックスをオンにして、 **[!UICONTROL Save]**.

1. 下にスクロールして、 _[!UICONTROL Product 3D Model]_セクション。

   ![メニューポップアップ](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. 3D モデルを追加（`.USDZ` ファイル）を選択します。

1. クリック **[!UICONTROL Save]**.

### 3D モデルの削除

製品の詳細から 3D モデルを削除するには：

1. クリック **[!UICONTROL Delete]**.

1. クリック **[!UICONTROL Save]**.

## 製品の 3D モデルを表示

製品の詳細が 3D モデルで更新された場合：

1. この [!DNL AR Viewer] ar ファイルをエンコードする QR コードを製品説明内に生成します。

1. お客様は、この QR コードを製品ページで確認できます。

1. 顧客がモバイルデバイスで QR コードをスキャンすると、モバイルデバイスで AR エクスペリエンスがレンダリングされます。

>[!NOTE]
>
> 製品に 3d モデルを追加する様子を示す一連のデモビデオについては、を参照してください。 [Adobe Commerceの AR ビューア](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) のページ _CommerceのビデオとTutorials_.
