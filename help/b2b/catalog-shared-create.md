---
title: 共有カタログの作成
description: 共有カタログの作成と、既存の共有カタログの複製について説明します。
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# 共有カタログの作成

条件 [共有カタログ](catalog-shared.md) が作成されると、システムによって自動的に [顧客グループ](account-company-customer-group.md) 同じ名前で。 例えば、という共有カタログを作成するとします。 _ABC カタログ_&#x200B;対応するも作成されます _ABC カタログ_ 顧客グループ。 共有カスタムカタログに会社を割り当てる手順は、基本的に顧客グループに会社を割り当てる手順と同じです。

新しい共有カタログには、製品、カスタム価格、会社の関連付けは含まれません。 公開カタログは、共有カタログが有効な場合に作成されるデフォルトの共有カタログであり、自動的にゲストと、会社に関連付けられていない顧客に割り当てられます。

![共有カタログ](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

共有カタログを使用するには、次の点を設定する必要があります。

- カタログ範囲
- 製品の選択
- カスタム価格
- 会社の割り当て

## 価格範囲

マルチサイトをインストールしている場合は、共有カタログを作成する前に必ず価格範囲を設定してください。 この [価格範囲](../catalog/catalog-price-scope.md) はに設定できます。 `Global` または `Website`. ただし、設定プロセスの最初にのみ設定できます。 Web サイト選択は、の手順 2 で表示されます [shared catalog setup](catalog-shared-pricing-structure.md).

![Web サイトの選択](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **カタログ** を選択します **カタログ** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **価格** セクション。

1. を設定 **カタログの価格スコープ** 対象： `Website`.

   ![カタログの価格スコープ](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

## 手順 1：共有カタログの作成

共有カタログを作成する方法は 2 つあります。 いずれかのタイプの共有カタログを作成するか、既存の共有カタログを複製できます。 新しい共有カタログには製品が含まれておらず、まだ会社に割り当てられていません。

### 方法 1：新しい共有カタログを追加する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Shared Catalog]** 次の手順を実行します。

   - を入力 **[!UICONTROL Name]** を共有カタログ用に使用します。

     割り当てた名前は、共有カタログを参照するために、管理者および顧客ダッシュボード全体で使用されます（該当する場合）。 対応する顧客グループの名前にもなります。

   - を選択 **[!UICONTROL Type]** : `Custom` または `Public`.

   - 適切なを選択します **[!UICONTROL Customer Tax Class]** これは、共有カタログから行われた購入に適用されます。

     税金区分の設定と定義の詳細は、次を参照してください。 [税クラス](../stores-purchase/tax-class.md).

     次の例は、特定の卸売顧客の新しいカスタムカタログを示しています。

     ![新しい共有カタログ](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - Enter **[!UICONTROL Description]**

1. 完了したら、 **[!UICONTROL Save]**.

   新しいカタログがに表示されます _[!UICONTROL Shared Catalogs]_グリッド。

### 方法 2：既存の共有カタログを複製する

重複するカスタムカタログには、元の価格モデルと構造が保持されますが、会社の関連付けは保持されません。 対応する顧客グループも、重複するカタログと同じ名前で作成されます。 デフォルトでは、重複するカタログの名前はです _次の重複_ 元のカタログ。

公開共有カタログが複製されると、複製されたカタログのタイプがに変わります。 `custom`.

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 複製するグリッド内の共有カタログについて、 **[!UICONTROL Action]** 列と選択 **[!UICONTROL General Settings]**.

1. ページ上部のオプションで、 **[!UICONTROL Duplicate]**.

   ![共有カタログを複製](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. 新しいカタログに対して次のフィールドを更新します。

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. 完了したら、 **[!UICONTROL Save]**.

   複製がに表示されます _[!UICONTROL Shared Catalogs]_一意の ID を持つグリッド。

## 手順 2：設定の完了

新しい共有カタログを作成した後、適切な製品選択を使用して新しい共有カタログを設定する必要があります。 [会社の割り当て](catalog-shared-assign-companies.md)、および [カテゴリ権限](../catalog/category-permissions.md). 続行するには、を参照してください [価格と構造の設定](catalog-shared-pricing-structure.md).

>[!NOTE]
>
>**[B2B リリース 1.3.0](release-notes.md#b2b-v130) 以降**  – 共有カタログを作成する場合、次の各項目 [カテゴリ権限](../catalog/category-permissions.md) カタログがに設定されている場合 _[!UICONTROL Allow for the Display Product Prices]_および_[!UICONTROL Add to Cart]_ カタログ権限設定でこのアクセス権が割り当てられている顧客グループの場合。 以前は、これらの設定は、自動的にに設定されていました `Deny` カタログの権限がに設定されている場合でも `Allow`.

## 共有カタログのデモ

共有カタログ管理のデモを見るには、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/344446?quality=12&learn=on)

## 共有カタログページの参照

### ボタンバー

| ボタン | 説明 |
|--- |--- |
| [!UICONTROL Back] | 新しい共有カタログを保存せずに、共有カタログ ページに戻ります。 |
| [!UICONTROL Reset] | 未保存の変更のフォームをクリアし、元のカタログの詳細情報を復元します。 |
| [!UICONTROL Save and Continue Edit] | すべての変更を保存し、フォームを編集モードで開いたままにします。 |
| [!UICONTROL Save] | 変更を保存し、フォームを閉じて、共有カタログ ページに戻ります。 |

{style="table-layout:auto"}

### カタログの詳細

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Name] | 管理者全体、および共有カタログが使用可能な顧客アカウントで共有カタログを識別します。 カタログ名は、説明的で 32 文字以下にする必要があります。 同じ名前の 2 つの共有カタログを持つことはできません。 最大文字数：32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]**  – 割り当てられている特定の会社のみが使用できるカスタム価格のカタログを識別します。<br/>**[!UICONTROL Public]**– すべてのゲスト訪問者と、ログインした企業に関連付けられていない顧客が使用できる共有カタログを識別します。 デフォルトの公開共有カタログは、次の場合に作成されます [!DNL Adobe Commerce B2B] はインストールされますが、ストア管理者が設定する必要があります。 一度に存在できる公開共有カタログは 1 つだけです。 |
| [!UICONTROL Customer Tax Class] | カタログから行われた購入に使用する税クラスを決定します。 オプションには、使用可能なすべての税金クラスが含まれます。 |
| [!UICONTROL Description] | カタログの使用方法の簡単な説明。 |

{style="table-layout:auto"}

### グリッド列

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL ID] | 共有カタログエンティティに割り当てられる一意の数値識別子。 |
| [!UICONTROL Name] | 共有カタログの名前。 |
| [!UICONTROL Type] | 共有カタログのタイプを示します。 次になることができます `Public` または `Custom`. |
| [!UICONTROL Created At] | 共有カタログがシステムに作成された日付。 |
| [!UICONTROL Created By] | 共有カタログを作成した管理者ユーザーの名前。 |
| [!UICONTROL Action] | アクションのリスト。 オプション： `Set Pricing and Structure`, `Assign Companies`, `General Settings`, `Delete`. |

{style="table-layout:auto"}
