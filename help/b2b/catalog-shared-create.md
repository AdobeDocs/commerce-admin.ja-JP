---
title: 共有カタログの作成
description: 共有カタログの作成と既存の共有カタログの複製について説明します。
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
TQID: https://experienceleague.adobe.com/UaH40o7aZu8AYc1TuOfvXqxHebFod-rmGg0tobIKzjg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 872
ht-degree: 0%

---

# 共有カタログの作成

[共有カタログ &#x200B;](catalog-shared.md)が作成されると、同じ名前の[顧客グループ &#x200B;](account-company-customer-group.md)が自動的に作成されます。 例えば、_ABC カタログ_&#x200B;という名前の共有カタログを作成すると、対応する&#x200B;_ABC カタログ_&#x200B;の顧客グループも作成されます。 共有カスタムカタログに会社を割り当てることは、基本的に顧客グループに会社を割り当てることと同じです。

新しい共有カタログには、商品、カスタム価格、企業関連は含まれません。 共有カタログが有効になっている場合に作成されるデフォルトの共有カタログである公開カタログは、会社に関連付けられていないゲストと顧客に自動的に割り当てられます。

![共有カタログ &#x200B;](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

共有カタログを使用する前に、共有カタログの次の側面を設定する必要があります。

- カタログの範囲
- 製品の選定
- カスタム価格
- 会社の割り当て

## 価格範囲

マルチサイトをインストールしている場合は、共有カタログを作成する前に、必ず価格範囲を設定してください。 [価格範囲](../catalog/catalog-price-scope.md)は`Global`または`Website`に設定できます。 ただし、設定プロセスの最初にのみ設定できます。 Web サイト選択ツールは、[共有カタログ設定](catalog-shared-pricing-structure.md)の手順2で表示されます。

![Web サイト選択](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**カタログ**」を展開し、下の「**カタログ**」を選択します。

1. **価格** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **カタログ価格範囲**&#x200B;を`Website`に設定します。

   ![&#x200B; カタログ価格範囲](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

## 手順1：共有カタログの作成

共有カタログを作成するには、2つの方法があります。 タイプの共有カタログを作成するか、既存の共有カタログを複製できます。 新しい共有カタログには製品が含まれず、まだ会社に割り当てられていません。

### 方法1：新しい共有カタログを追加する

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add Shared Catalog]**」をクリックし、次の操作を行います。

   - 共有カタログの&#x200B;**[!UICONTROL Name]**&#x200B;を入力します。

     割り当てた名前は、管理者および顧客ダッシュボード全体で使用され、該当する場合は共有カタログを参照します。 対応する顧客グループの名前にもなります。

   - **[!UICONTROL Type]** : `Custom`または`Public`を選択してください。

   - 共有カタログから行われた購入に適用される適切な&#x200B;**[!UICONTROL Customer Tax Class]**&#x200B;を選択します。

     税区分の設定と定義について詳しくは、[税区分](../stores-purchase/tax-class.md)を参照してください。

     次の例は、特定の卸売顧客向けの新しいカスタムカタログを示しています。

     ![新しい共有カタログ &#x200B;](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - **[!UICONTROL Description]**&#x200B;を入力

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

   新しいカタログが&#x200B;_[!UICONTROL Shared Catalogs]_&#x200B;グリッドに表示されます。

### 方法2：既存の共有カタログを複製する

重複したカスタムカタログは、元の価格モデルと構造を保持しますが、会社の関連付けは保持されません。 対応する顧客グループも、重複カタログと同じ名前で作成されます。 デフォルトでは、重複したカタログには、元のカタログの&#x200B;_個の_&#x200B;重複という名前が付けられます。

公開されている共有カタログが複製されると、複製されたカタログの種類は`custom`に変更されます。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**&#x200B;に移動します。

1. 複製するグリッド内の共有カタログの場合は、**[!UICONTROL Action]**&#x200B;列に移動し、**[!UICONTROL General Settings]**&#x200B;を選択します。

1. ページ上部のオプションで、**[!UICONTROL Duplicate]**&#x200B;をクリックします。

   ![共有カタログを複製](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. 新しいカタログの次のフィールドを更新します。

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

   重複が一意のIDを持つ&#x200B;_[!UICONTROL Shared Catalogs]_&#x200B;グリッドに表示されます。

## 手順2：設定の完了

新しい共有カタログを作成したら、適切な製品選択、[会社割り当て](catalog-shared-assign-companies.md)、[&#x200B; カテゴリ権限](../catalog/category-permissions.md)を使用して設定する必要があります。 続行するには、[価格と構造の設定](catalog-shared-pricing-structure.md)を参照してください。

>[!NOTE]
>
>**[B2B リリース 1.3.0](release-notes.md#b2b-v130)以降** – 共有カタログを作成する場合、カタログの各[&#x200B; カテゴリ権限](../catalog/category-permissions.md)は、カタログ権限設定でこのアクセスが割り当てられている顧客グループに対して&#x200B;_[!UICONTROL Allow for the Display Product Prices]_&#x200B;および&#x200B;_[!UICONTROL Add to Cart]_&#x200B;に設定されます。 以前は、カタログ権限が`Allow`に設定されていても、これらの設定は自動的に`Deny`に設定されていました。

## 共有カタログのデモ

共有カタログ管理のデモについては、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/3410755?captions=jpn&quality=12&learn=on)

## 共有カタログページ参照

### ボタンバー

| ボタン | 説明 |
|--- |--- |
| [!UICONTROL Back] | 新しい共有カタログを保存せずに、共有カタログページに戻ります。 |
| [!UICONTROL Reset] | 保存されていない変更のフォームを消去し、元のカタログの詳細情報を復元します。 |
| [!UICONTROL Save and Continue Edit] | すべての変更を保存し、フォームを編集モードで開いたままにします。 |
| [!UICONTROL Save] | 変更を保存し、フォームを閉じて、共有カタログ ページに戻ります。 |

{style="table-layout:auto"}

### カタログの詳細

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Name] | 管理者全体および利用可能な顧客アカウント内の共有カタログを識別します。 カタログ名は説明的で、32文字以下にする必要があります。 同じ名前の2つの共有カタログを持つことはできません。 最大文字数：32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** – 割り当てられた特定の企業のみが利用できるカスタム価格設定のカタログを識別します。<br/>**[!UICONTROL Public]**– すべてのゲスト訪問者と、会社に関連付けられていないログイン顧客が利用できる共有カタログを識別します。 既定のパブリック共有カタログは、[!DNL Adobe Commerce B2B]のインストール時に作成されますが、ストア管理者が設定する必要があります。 一度に存在できる公開共有カタログは1つだけです。 |
| [!UICONTROL Customer Tax Class] | カタログから作成された購入に使用される税区分を指定します。 オプションには、使用可能なすべての税区分が含まれます。 |
| [!UICONTROL Description] | カタログの使用方法を簡単に説明します。 |

{style="table-layout:auto"}

### グリッド列

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL ID] | 共有カタログエンティティに割り当てられる一意の数値識別子。 |
| [!UICONTROL Name] | 共有カタログの名前。 |
| [!UICONTROL Type] | 共有カタログのタイプを示します。 `Public`または`Custom`を指定できます。 |
| [!UICONTROL Created At] | 共有カタログがシステムで作成された日付。 |
| [!UICONTROL Created By] | 共有カタログを作成した管理者ユーザーの名前。 |
| [!UICONTROL Action] | アクションのリスト。 オプション：`Set Pricing and Structure`、`Assign Companies`、`General Settings`、`Delete`。 |

{style="table-layout:auto"}
