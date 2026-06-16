---
title: ストアビュー
description: ストアビューを追加および編集する方法について説明します。
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
TQID: https://experienceleague.adobe.com/2VMBTnzG3lqsNEyx-e46rqDs1wHofaDeHL3j3SuqxOE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 284
ht-degree: 0%

---

# ストアビュー

ストアビューは、通常、ストアを様々なロケールで利用できるようにするために使用されます。 買い物客は、ストアのヘッダーにある言語選択ツールを使用して、ストアビューを変更できます。

![範囲 – 複数のストアビュー](./assets/scope-multiview.svg){width="550"}

## ストアビューを追加

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**に移動します。

   ![すべての店舗](./assets/stores-all.png){width="700" zoomable="yes"}

1. **[!UICONTROL Create Store View]**&#x200B;をクリックします。

   ![ ストアビューを作成](./assets/create-store-view.png){width="600" zoomable="yes"}

1. このビューの親ストアに&#x200B;**[!UICONTROL Store]**&#x200B;を設定します。

1. このストアビューの&#x200B;**[!UICONTROL Name]**&#x200B;を入力してください。

   名前は、ストアヘッダーの言語選択に表示されます。 例：`Spanish`。

1. **[!UICONTROL Code]**&#x200B;に、ビューを識別するコード（小文字）を入力します。

   例：`spanish`。

1. ビューをアクティブにするには、**[!UICONTROL Status]**&#x200B;を`Enabled`に設定します。

1. （オプション）このビューが他のビューと共に表示されるシーケンスを決定するには、**[!UICONTROL Sort Order]**&#x200B;番号を入力します。

1. **[!UICONTROL Save Store View]**&#x200B;をクリックします。

## ストアビューの編集

ビュー名は言語選択に表示されるので、最終的にはデフォルトのビューの名前をより説明的なものに変更する必要がある場合があります。 _名前_ フィールドは単なるラベルであり、簡単に変更できます。

Adobe CommerceまたはMagento Open Sourceのインストール環境にマルチサイトまたはマルチストア設定がある場合は、`index.php` ファイルで値が参照されていないことを確認せずに、ストアコード フィールドを変更しないでください。 ファイルを調べるためにサーバーにアクセスできない場合は、開発者に助けを求めてください。

| フィールド | 元の値 | 更新された値 |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**に移動します。

1. グリッドの&#x200B;_[!UICONTROL Store View]_列で、編集するビューの名前をクリックします。

   既定のビューを編集する際、_[!UICONTROL Store]_および_[!UICONTROL Status]_ フィールドは使用できません。

   ![ ストアビュー – デフォルトビューを編集](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. 必要に応じて、次のフィールドを更新します。

   - **[!UICONTROL Store]** （デフォルト以外のビューのみ）
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** （`index.php`で使用されていない場合のみ）
   - **[!UICONTROL Status]** （デフォルト以外のビューのみ）
   - **[!UICONTROL Sort Order]**

1. **[!UICONTROL Save Store View]**&#x200B;をクリックします。
