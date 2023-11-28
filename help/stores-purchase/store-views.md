---
title: ストア表示
description: ストアビューを追加および編集する方法について説明します。
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 1%

---

# ストア表示

ストアビューは、通常、別のロケールでストアを使用できるようにするために使用されます。 買い物客は、ストアのヘッダーで言語選択を使用して、ストアの表示を変更できます。

![範囲 — 複数のストア表示](./assets/scope-multiview.svg){width="550"}

## ストアビューを追加

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![すべてのストア](./assets/stores-all.png){width="700" zoomable="yes"}

1. クリック **[!UICONTROL Create Store View]**.

   ![ストア表示を作成](./assets/create-store-view.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Store]** をこのビューの親ストアに追加します。

1. を入力します。 **[!UICONTROL Name]** （このストア表示用）。

   名前は、ストアヘッダーの言語選択で表示されます。 例： `Spanish`.

1. の場合 **[!UICONTROL Code]**」に、ビューを識別するコード（小文字）を入力します。

   例： `spanish`.

1. ビューをアクティブにするには、 **[!UICONTROL Status]** から `Enabled`.

1. （オプション） **[!UICONTROL Sort Order]** このビューが他のビューと共に表示される順序を決定する番号。

1. クリック **[!UICONTROL Save Store View]**.

## ストア表示の編集

ビュー名は言語選択で表示されるので、最終的にはデフォルトビューの名前をよりわかりやすい名前に変更する必要が生じる場合があります。 The _名前_ フィールドは単なるラベルで、簡単に変更できます。

Adobe CommerceまたはMagento Open Sourceのインストールにマルチサイトまたはマルチストアが設定されている場合、 `index.php` ファイル。 サーバーにアクセスしてファイルを調べる権限がない場合は、開発者に問い合わせてください。

| フィールド | 元の値 | 更新された値 |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** >  _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Adobe Analytics の _[!UICONTROL Store View]_グリッドの列で、編集するビューの名前をクリックします。

   デフォルトのビューを編集する場合、 _[!UICONTROL Store]_および_[!UICONTROL Status]_ フィールドは使用できません。

   ![ストア表示 — デフォルト表示の編集](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. 必要に応じて、次のフィールドを更新します。

   - **[!UICONTROL Store]** （デフォルト以外の表示のみ）
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** （で使用されない場合のみ） `index.php`)
   - **[!UICONTROL Status]** （デフォルト以外の表示のみ）
   - **[!UICONTROL Sort Order]**

1. クリック **[!UICONTROL Save Store View]**.
