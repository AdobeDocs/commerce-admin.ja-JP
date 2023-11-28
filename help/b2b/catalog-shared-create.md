---
title: 共有カタログを作成
description: 共有カタログを作成し、既存の共有カタログを複製する方法を説明します。
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# 共有カタログを作成

When a [共有カタログ](catalog-shared.md) が作成された場合、システムは自動的に [顧客グループ](account-company-customer-group.md) 同じ名前で 例えば、 _ABC カタログ_&#x200B;を使用する場合、システムは、 _ABC カタログ_ 顧客グループとして割り当てられます。 共有カスタムカタログに会社を割り当てる操作は、顧客グループに会社を割り当てる操作と基本的に同じです。

新しい共有カタログには、製品、カスタム価格、企業関連の情報は含まれません。 公開カタログは、共有カタログが有効になったときに作成されるデフォルトの共有カタログで、会社に関連付けられていないゲストや顧客に自動的に割り当てられます。

![共有カタログ](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

共有カタログを使用する前に、次の要素を設定する必要があります。

- カタログの範囲
- 製品の選択
- カスタム価格
- 会社の割り当て

## 価格の範囲

マルチサイトインストールを行う場合は、共有カタログを作成する前に価格範囲を設定してください。 The [価格範囲](../catalog/catalog-price-scope.md) に設定できます。 `Global` または `Website`. ただし、設定プロセスの最初にのみ設定できます。 Web サイトの選択は、 [共有カタログ設定](catalog-shared-pricing-structure.md).

![Web サイトの選択](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **カタログ** を選択します。 **カタログ** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **価格** 」セクションに入力します。

1. 設定 **カタログ価格範囲** から `Website`.

   ![カタログ価格範囲](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

## 手順 1：共有カタログを作成する

共有カタログを作成する方法は 2 つあります。 いずれかのタイプの共有カタログを作成するか、既存の共有カタログを複製することができます。 新しい共有カタログには製品が含まれず、まだ会社に割り当てられていません。

### 方法 1：新しい共有カタログを追加する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 右上隅で、 **[!UICONTROL Add Shared Catalog]** 次の操作を実行します。

   - を入力します。 **[!UICONTROL Name]** 共有カタログの

     割り当てた名前は、管理者ダッシュボードと顧客ダッシュボード（該当する場合）全体で、共有カタログを参照するために使用されます。 また、対応する顧客グループの名前になります。

   - 選択 **[!UICONTROL Type]** : `Custom` または `Public`.

   - 適切な **[!UICONTROL Customer Tax Class]** 共有カタログからの購入に適用されます。

     税区分の設定と定義の詳細は、 [税区分](../stores-purchase/tax-class.md).

     次の例は、特定の卸売顧客の新しいカスタムカタログを示しています。

     ![新しい共有カタログ](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - 入力 **[!UICONTROL Description]**

1. 完了したら、「 **[!UICONTROL Save]**.

   新しいカタログが _[!UICONTROL Shared Catalogs]_グリッド。

### 方法 2：既存の共有カタログを複製する

重複するカスタムカタログには、元のの価格モデルと構造が保持されますが、会社関連の価格モデルと構造は保持されません。 また、重複したカタログと同じ名前で、対応する顧客グループも作成されます。 デフォルトでは、重複したカタログには _複製_ 元のカタログ。

公開共有カタログが複製されると、重複するカタログの種類が `custom`.

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 複製するグリッド内の共有カタログについて、 **[!UICONTROL Action]** 列と選択 **[!UICONTROL General Settings]**.

1. ページ上部のオプションで、「 **[!UICONTROL Duplicate]**.

   ![共有カタログを複製](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. 新しいカタログの次のフィールドを更新します。

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. 完了したら、「 **[!UICONTROL Save]**.

   重複が _[!UICONTROL Shared Catalogs]_グリッドに含まれる一意の ID を持ちます。

## 手順 2：設定の完了

新しい共有カタログを作成した後、適切な製品を選択して設定する必要があります。 [会社割り当て](catalog-shared-assign-companies.md)、および [カテゴリ権限](../catalog/category-permissions.md). 続行するには、 [価格と構造の設定](catalog-shared-pricing-structure.md).

>[!NOTE]
>
>**[B2B リリース 1.3.0](release-notes.md#b2b-v130) およびその後**  — 共有カタログを作成する場合、 [カテゴリ権限](../catalog/category-permissions.md) ( カタログが _[!UICONTROL Allow for the Display Product Prices]_および_[!UICONTROL Add to Cart]_ カタログ権限設定でこのアクセス権を割り当てられた顧客グループの場合。 以前は、これらの設定は自動的に `Deny` （カタログ権限がに設定されている場合も） `Allow`.

## 共有カタログのデモ

共有カタログ管理のデモを見るには、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/344446?quality=12&learn=on)

## 共有カタログページの参照

### ボタンバー

| ボタン | 説明 |
|--- |--- |
| [!UICONTROL Back] | 新しい共有カタログを保存せずに、共有カタログページに戻ります。 |
| [!UICONTROL Reset] | 未保存の変更のフォームをクリアし、元のカタログの詳細情報を復元します。 |
| [!UICONTROL Save and Continue Edit] | すべての変更を保存し、フォームを編集モードで開いたままにします。 |
| [!UICONTROL Save] | 変更を保存し、フォームを閉じて、[ 共有カタログ ] ページに戻ります。 |

{style="table-layout:auto"}

### カタログの詳細

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Name] | 管理者全体および使用可能な顧客アカウント内で共有カタログが特定されます。 カタログ名は説明的で、32 文字以内にしてください。 同じ名前の 2 つの共有カタログを持つことはできません。 最大文字数： 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]**  — 割り当て先の特定の会社にのみ利用可能なカスタム価格でカタログを識別します。<br/>**[!UICONTROL Public]**— すべてのゲスト訪問者と、会社に関連していないログイン済み顧客が使用できる共有カタログを識別します。 デフォルトの公開共有カタログは、 [!DNL B2B for Adobe Commerce] がインストールされているが、ストア管理者が設定する必要がある。 一度に存在できる公開共有カタログは 1 つだけです。 |
| [!UICONTROL Customer Tax Class] | カタログからの購入に使用される税区分を決定します。 オプションには、使用可能な税区分がすべて含まれます。 |
| [!UICONTROL Description] | カタログの使用方法に関する簡単な説明です。 |

{style="table-layout:auto"}

### グリッド列

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL ID] | 共有カタログエンティティに割り当てられる一意の数値識別子。 |
| [!UICONTROL Name] | 共有カタログの名前。 |
| [!UICONTROL Type] | 共有カタログの種類を示します。 次のことが可能です。 `Public` または `Custom`. |
| [!UICONTROL Created At] | 共有カタログがシステムで作成された日付。 |
| [!UICONTROL Created By] | 共有カタログを作成した管理者ユーザーの名前。 |
| [!UICONTROL Action] | アクションのリスト。 オプション： `Set Pricing and Structure`, `Assign Companies`, `General Settings`, `Delete`. |

{style="table-layout:auto"}
