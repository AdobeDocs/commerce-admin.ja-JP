---
title: ビューを保存
description: ストア表示を追加および編集する方法について説明します。
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# ビューを保存

ストア表示は、通常、様々なロケールでストアを使用できるようにするために使用されます。 買い物客は、ストアのヘッダーにある言語選択を使用して、ストア表示を変更できます。

![範囲 – 複数のストア表示](./assets/scope-multiview.svg){width="550"}

## ストア表示の追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![すべてのストア](./assets/stores-all.png){width="700" zoomable="yes"}

1. クリック **[!UICONTROL Create Store View]**.

   ![ストア表示を作成](./assets/create-store-view.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Store]** を、このビューの親ストアに追加します。

1. を入力 **[!UICONTROL Name]** このストア表示の場合。

   この名前は、ストアヘッダーの言語選択に表示されます。 例： `Spanish`.

1. の場合 **[!UICONTROL Code]**&#x200B;で、ビューを識別するコードを小文字で入力します。

   例： `spanish`.

1. ビューをアクティブにするには、を設定します **[!UICONTROL Status]** 対象： `Enabled`.

1. （任意） a と入力します **[!UICONTROL Sort Order]** このビューが他のビューと共に一覧表示されるシーケンスを決定する番号。

1. クリック **[!UICONTROL Save Store View]**.

## ストア表示の編集

ビュー名は言語選択に表示されるため、最終的には既定のビューの名前をわかりやすい名前に変更する必要が生じる場合があります。 この _名前_ フィールドは単なるラベルであり、簡単に変更できます。

Adobe CommerceまたはMagento Open Sourceのインストールでマルチサイトまたはマルチストアの設定を使用している場合は、の値が参照されていないことを確認し、ストアコード フィールドを変更しないでください `index.php` ファイル。 ファイルを調べるサーバーにアクセスできない場合は、開発者に問い合わせてください。

| フィールド | 元の値 | 更新された値 |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** >  _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. が含まれる _[!UICONTROL Store View]_グリッドの列で、編集するビューの名前をクリックします。

   デフォルトのビューを編集する場合、 _[!UICONTROL Store]_および_[!UICONTROL Status]_ フィールドは使用できません。

   ![ストア表示 – デフォルト表示を編集](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. 必要に応じて、次のフィールドを更新します。

   - **[!UICONTROL Store]** （非デフォルトビューのみ）
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** （で使用されていない場合のみ `index.php`）
   - **[!UICONTROL Status]** （非デフォルトビューのみ）
   - **[!UICONTROL Sort Order]**

1. クリック **[!UICONTROL Save Store View]**.
