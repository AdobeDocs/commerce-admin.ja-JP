---
title: カタログ強化ブランドルールの作成
description: カタログエンリッチメントのブランドガバナンスルールを作成および管理する方法、製品コピー要件を定義する方法、カタログエンリッチメントジョブにルールを適用する方法について説明します。
role: Admin, User, Leader
source-git-commit: 9d7a4f4e98fe2d2d51261d96a2e072c28925babd
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%
---
# カタログ強化ブランドルールの作成

ブランドガバナンスおよびブランドガバナンスルールは、カタログ強化でのみ使用できます。 これらはPDP エンリッチメントには適用されません。 これらのルールは、[!DNL Commerce Catalog Agent]によって生成される製品名と説明の要件を定義します。 デフォルトのブランド標準のデフォルトルールを編集または設定してから、特定のキャンペーン、製品カテゴリ、サブブランドのカスタムルールを作成します。 [&#x200B; カタログ強化](catalog-enrichment.md) ジョブを作成するときにルールを選択します。

## オープンなブランドガバナンス

1. 管理画面で、**[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**&#x200B;に移動します。
1. 「**[!UICONTROL Brand Governance]**」タブを開きます。

「**ブランドガバナンス**」タブには、デフォルトルールと、作成したカスタムルールが含まれています。 ルールを検索したり、ルールのテーブルをフィルタリングしたりできます。

各行には、**ルール名**、**フィールド**、**トーン**、**最終更新日**、および&#x200B;**ステータス**&#x200B;が表示されます。 既定のルールは&#x200B;**[!UICONTROL Default]**&#x200B;とマークされています。

**[!UICONTROL Needs your attention]**&#x200B;領域では、設定が必要なドラフトや競合のあるルールなど、作業が必要なルールがハイライト表示されます。 ルールの詳細を確認し、**[!UICONTROL Finish setup]**&#x200B;や&#x200B;**[!UICONTROL Fix conflict]**&#x200B;など、使用可能なアクションを使用します。

## ルールタイプについて

カタログのエンリッチメントでは、デフォルトのルールとカスタムルールをサポートしています。

### デフォルトルール

各[!DNL Adobe Commerce] インスタンスには、デフォルト ルールが1つずつ存在します。 [!DNL Adobe Commerce]は、空のフィールドを含むこのルールを作成します。 名前は&#x200B;**[!UICONTROL Global]**&#x200B;に固定されています。 ルールは編集できますが、削除することはできません。

[!DNL Adobe Commerce]は、カスタム ルールを選択せずにカタログ強化ジョブを作成する場合、既定で既定のルールを適用します。 デフォルトのルールは、カタログのエンリッチメントのベースラインガバナンスを提供します。

### カスタムルール

キャンペーン、製品カテゴリ、サブブランドに対して、任意の数のカスタムルールを作成できます。 カスタムルールは自動的には適用されません。 カタログエンリッチメントジョブを作成する際に選択します。

カスタムルールは、デフォルトのルールから値を継承しません。 カスタムルールを作成する場合は、デフォルトのルールの現在の値を1回限りの開始点としてコピーできます。 後でデフォルトのルールに変更しても、カスタムルールは更新されません。

ユーザーがカスタムルールを選択しない場合に適用する標準のデフォルトルールを使用します。 異なる要件を持つキャンペーンまたはカテゴリのカスタムルールを作成します。 カスタムルールはグローバル値を継承しないため、カスタムルールに必要なグローバル要件を追加します。

## カスタムルールの作成

この節では、ブランドガバナンスルールを作成する方法を説明します。

![&#x200B; ブランドガバナンスルールの作成](./assets/brand-gov-create-rule.png)

1. 「**ブランドガバナンス**」タブで、**[!UICONTROL Create Rule]**&#x200B;をクリックします。
1. ルールの開始方法を選択します。
   - **[!UICONTROL Blank]**：すべての値を自分で設定します。
   - **[!UICONTROL Copy Global enrichment]**：現在のデフォルト ルール値を1回限りのコピーとして開始します。
   - **[!UICONTROL Draft with AI]**: （**近日リリース予定**）ブランドボイスを記述して、提案されたルール値を取得します。
1. キャンペーン、カテゴリ、サブブランドなど、目的を特定する&#x200B;**ルール名**&#x200B;を入力します。
1. **強化するフィールド**&#x200B;で、製品名と製品説明の要件を設定します。

   製品名と説明を別々に設定します。 各フィールドには、独自のイネーブルスイッチとガバナンス要件があります。

1. **製品名の長さ**&#x200B;を設定します。

   強化された製品名の最小および最大の名前の長さの範囲を設定します。 例えば、ルールには最低20文字、最大200文字が必要な場合があります。

1. **大文字と小文字** オプションを設定します。

   - **[!UICONTROL Sentence case]**: `Waterproof hiking boots`
   - **[!UICONTROL Title Case]**: `Waterproof Hiking Boots`
   - **[!UICONTROL As written]**: ソーステキストの大文字と小文字を保持します。

1. **ブランドトーン**&#x200B;について説明します。 ガイダンスについては、[&#x200B; ブランドトーンの設定](#set-brand-tone)を参照してください。
1. 必須フレーズと除外フレーズの設定

   **[!UICONTROL Must include]** フレーズを追加します。
   **[!UICONTROL Never use]** フレーズを追加します。

1. **[!UICONTROL Save as draft]**&#x200B;をクリックして後で終了するか、**[!UICONTROL Publish rule]**&#x200B;をクリックして、カタログ強化ルールを作成する際にルールを選択できるようにします。 **[!UICONTROL Cancel]**&#x200B;をクリックすると、保存せずに終了します。

1. ルールを[&#x200B; カタログ強化](catalog-enrichment.md) ジョブに適用できるようになりました。

### ブランドトーンを設定

複数行&#x200B;**[!UICONTROL Brand tone]** フィールドにガイダンスを入力して、強化された名前の音声とスタイルを説明します。

**説明**&#x200B;に使用できるトーンの例を次に示します。

- **B2B industrial**: `Write for the operator and the buyer. Open with what the unit does and where it fits in the kitchen, then throughput, utility requirements, footprint, and certifications. Plain, technical language. Mention cleaning and maintenance, because total cost of ownership drives the decision. No lifestyle language.`
- **高級ファッション**: `Quiet confidence. Lead with craftsmanship and provenance (atelier, tannery, technique), then how the piece wears and ages. Short, measured sentences. Sensory detail is fine. Never compare to other brands or mention price or value.`
- **家電製品**: `Clear and benefit-led. Turn every spec into what it does for the user. Scannable short paragraphs or bullets. Put compatibility and what's in the box up front. Don't make performance claims without a source, and don't use comparative claims like "fastest"`
- **スペシャルティフードと食料品**: `Warm and appetizing, but honest. Describe taste, texture, and aroma in concrete terms, then origin and how it's made, then serving ideas. Plain, friendly language. Put allergens and dietary attributes in a consistent closing line. Don't make health claims.`
- **家具**: `Inviting and practical. Open with how the piece is used, then dimensions, materials, and care. Help the shopper picture it in their space without overselling. Always mention assembly, delivery, and weight, since those drive returns.`
