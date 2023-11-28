---
title: アクションログレポート
description: アクションログレポートを表示、フィルタリング、および書き出す方法について説明します。このレポートには、ログが有効なすべての管理者アクションの詳細な記録が記録されます。
exl-id: f2be5852-9185-4f14-b0bb-44d779b40819
feature: Logs, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# アクションログレポート

{{ee-feature}}

The _アクションログ_ レポートには、ログに対して有効なすべての管理者アクションの詳細が表示されます。 各レコードにはタイムスタンプが付き、IP アドレスとユーザーの名前が記録されます。 ログの詳細には、管理者ユーザーデータと、アクション中に加えられた関連する変更が含まれます。

レポートに表示するアクションは、 [管理アクションのログ](action-log.md) 画面を開きます。 アクションタイプがオン（有効）になっている場合、それらのタイプの管理アクションがアクションログレポートに表示されます。

レポートは、各列のオプションを使用してフィルタリングできます。 単一のフィルターオプションを設定するか、複数の列にフィルターオプションを設定して、特定のアクションをリストするようにレポートを絞り込むことができます。 また、レポートデータを CSV 形式または Excel XML 形式で書き出すこともできます。

アクションログレポートには、次の情報が含まれます。

- **[!UICONTROL Time]**  — アクションが発生した日時
- **[!UICONTROL Action Group]**  — 有効なアクションと相関するアクションタイプを表示します。 _管理アクションのログ_ ストア設定の画面
- **[!UICONTROL Action]**  — ログに記録されたアクションを表示します
- **[!UICONTROL IP Address]**  — アクションが実行されたマシンの IP アドレスを表示します
- **[!UICONTROL Username]**  — アクションを実行したユーザーのログイン ID を表示します
- **[!UICONTROL Result]**  — ユーザーのアクションの成功または失敗を表示します
- **[!UICONTROL Full Action Name]**  — バックエンドのアクション名を表示します
- **[!UICONTROL Details]**  — バックエンドのアクションカテゴリを表示します
- **[!UICONTROL Full Details]**  — 管理アクションのログに記録されたすべての詳細を表示します

## アクションログレポートの表示

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Report]**.

   ![アクションログ](./assets/action-log-report.png){width="600" zoomable="yes"}

1. リストに表示された管理者アクションの詳細を表示するには、 **[!UICONTROL View]**.

   ![アクションログエントリの詳細](./assets/action-log-report-view.png){width="600" zoomable="yes"}

## アクションログレポートのフィルタリング

フィルターオプションフィールドを定義して、 **[!UICONTROL Search]** をクリックして、表示されるアクションを絞り込みます。

フィルターオプションをクリアしてフルレポートに戻るには、 **[!UICONTROL Reset Filter]**.

![アクションログレポートフィルター](./assets/action-log-report-filters.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Time] | In **[!UICONTROL From]**」をクリックして、動的カレンダーから日付を選択し、フィルターの開始日を定義します。 In **[!UICONTROL To]**」、「 」をクリックして日付を選択し、フィルターの終了日を定義します。 |
| [!UICONTROL Action Group] | アクショングループを選択します。 |
| [!UICONTROL Action] | アクションを選択します。 |
| [!UICONTROL IP Address] | アクションに使用するマシンの IP アドレスを入力します。 |
| [!UICONTROL Username] | ユーザー名を選択します。 デフォルトはです。 `All Users`. |
| [!UICONTROL Result] | 「成功」または「失敗」を選択します。 |
| [!UICONTROL Full Action Name] | フィールドに、一致する検索のテキストを入力します。 |
| [!UICONTROL Details] | フィールドに、一致する検索のテキストを入力します。 |

{style="table-layout:auto"}

## アクションログレポートのエクスポート

1. の場合 **[!UICONTROL Export to]**、書き出し形式を選択します。

   - `CSV`  — プレーンテキストデータを含む、値をコンマで区切ったファイル
   - `Excel XML` - XML ベースのスプレッドシートデータ形式

1. クリック **[!UICONTROL Export]**.

   生成されたファイルは、指定されたフォルダーに自動的に保存され、ダウンロード用に保存されます。

   ![アクションログレポートのエクスポート](./assets/action-log-report-export.png){width="200"}
