---
title: '''[!DNL AR Viewer] (Adobe Commerce設定用 )'
description: を使用した 3D モデルアセットの管理について説明します。 [!DNL AR Viewer] 製品リストの拡張機能。
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# を使用して製品 3D モデルを管理する [!DNL AR Viewer] Adobe Commerce

各製品について、 `.USDZ` 製品リストで AR および 3D モデルを使用できるファイル。

The [!DNL AR Viewer] のみがサポート `.USDZ` ファイル。

## 拡張機能のインストール

[!DNL AR Viewer] は、 [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

詳しくは、 [_インストールガイド_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) を参照してください。

次の期間の後に [!DNL AR Viewer] 拡張機能がインストールおよび設定されていると、管理者ユーザーは、3D モデルを含めるための製品リストの設定、カスタマイズ、管理をおこなうことができます。

## 3D モデルを追加する

1. 製品を編集モードで開きます。

1. 特定のストア表示を操作するには、 **[!UICONTROL Store View]** 適用可能なビューに対する選択。

   >[!NOTE]
   >
   >新しい製品 3D モデルは、 _常に_ アップロードされて表示される _すべて_ ビューを保存 ( `All Store Views` 範囲はアップロードに使用されません。 <br/><br/>特定のストア表示から製品 3D モデルを非表示にするには、そのストア表示に切り替える必要があります。次に、 **[!UICONTROL Hide from Product Page]** 3D モデルのチェックボックスをオンにし、 **[!UICONTROL Save]**.

1. 下にスクロールして、 _[!UICONTROL Product 3D Model]_」セクションに入力します。

   ![メニューポップアップ](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. 3D モデルの追加 (`.USDZ` ファイル ) に含まれている必要があります。

1. クリック **[!UICONTROL Save]**.

### 3D モデルを削除する

製品の詳細から 3D モデルを削除するには：

1. クリック **[!UICONTROL Delete]**.

1. クリック **[!UICONTROL Save]**.

## 製品 3D モデルの表示

製品の詳細が 3D モデルで更新された場合：

1. The [!DNL AR Viewer] は、AR ファイルをエンコードする製品の説明に QR コードを生成します。

1. 顧客は、製品ページでこの QR コードを確認できます。

1. 顧客がモバイルデバイスで QR コードをスキャンすると、AR エクスペリエンスがモバイルデバイスでレンダリングされます。

>[!NOTE]
>
> 製品に 3d モデルを追加するユーザのデモビデオのシリーズについては、 [Adobe Commerce用 AR ビューア](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) ページ内 _コマースのビデオとTutorials_.
