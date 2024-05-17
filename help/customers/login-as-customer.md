---
title: 買い物客への支援の提供
description: 「顧客としてログイン」機能を使用すると、顧客に表示される内容を確認し、顧客に代わって更新を行うことができます。
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 買い物客への支援の提供

顧客は注文に関するヘルプが必要になる場合があります。 ストア管理者が使用できる _顧客としてログイン_&#x200B;を使用すると、顧客に表示される内容を確認し、更新を行って支援することができます。

ユーザーとしてログインした際に実行されたすべてのアクションは、実際のお客様のアカウントに適用されます。

に対して有効になっている場合 _Admin_ ユーザー、 _[!UICONTROL Login as Customer]_ボタンが複数のページに表示される：

* [顧客編集ページ](../customers/update-account.md)
* [注文ビューページ](../stores-purchase/order-processing.md)
* [「請求書ビュー」ページ](../stores-purchase/invoices.md)
* [「出荷ビュー」ページ](../stores-purchase/shipments.md)
* [「クレジット・メモ表示」ページ](../stores-purchase/credit-memo-create.md)

![顧客としてログイン](assets/login-as-customer.png){width="600" zoomable="yes"}

## 顧客としてログインを有効にする

有効化 _顧客としてログイン_ Commerce インスタンスでこの機能を有効にし、ユーザーロール権限で管理者ユーザーのアクセスを有効にする必要があります。

### 機能の有効化

1. 管理サイドバーで、に移動します。  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します  **[!UICONTROL Login as Customer]**.

   ![設定オプション – 顧客としてログイン](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enable Login as Customer]** 対象： `Yes`.

1. _（オプション）_ を設定 **[!UICONTROL Disable Page Cache for Admin User]** 対象： `No` 管理者ユーザーがユーザーとしてログインした際にページキャッシュを有効にする場合。

   >[!WARNING]
   >
   > ページキャッシュの無効化（`Yes` - デフォルト）を使用すると、ユーザーとしてログインした際に、キャッシュされていない新しいデータを取得できます。

1. _（オプション）_ を設定 **[!UICONTROL Store View to Log in]** 対象： `Manual Selection` マルチサイトまたはマルチストアの設定があり、管理者ユーザーが顧客としてログインした際にストア表示を選択できるようにする場合。

1. 完了したら、 **[!UICONTROL Save Config]**.

### 管理者ユーザーのアクセスを有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _権限_ > **[!UICONTROL User Roles]**.

1. リストで役割をクリックします。

1. が含まれる [!UICONTROL _役割に関する情報_] 左のパネル、をクリック **[!UICONTROL Role Resources]**.

1. 変更 **[!UICONTROL Role Resources]** ～するページに載っている `Custom`.

   >[!INFO]
   >
   > このオプションを選択すると、リソース階層がページに表示されます。

1. スクロール先：  **[!UICONTROL Customers]** 親項目と **[!UICONTROL Login as Customer]** その下の項目。 次に、役割に対して有効にするリソースを選択します。

   * **[!UICONTROL Allow Login as Customer]**  – 管理者ユーザーがを使用することを許可します _顧客としてログイン_ 機能
   * **[!UICONTROL View Login as Customer Log]**  – 管理者ユーザーに対し、このプロパティの表示を許可します _顧客としてログイン_ ログ。

   ![ロールリソース – 顧客としてログイン](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. クリック **[!UICONTROL Save Role]**.

## 管理者から顧客としてログインします

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > [!UICONTROL _すべての顧客_].

1. ユーザーを編集モードで開きます。

1. が含まれる **[!UICONTROL Customer Information]** パネルで、 **[!UICONTROL Account Information]** セクション。

1. を **[!UICONTROL Allow remote shopping assistance]** 対象： `Yes`.

   >[!INFO]
   >
   >管理者は、ストアフロントからの許可なしでユーザーとしてログインできるようになりました。

## リモート ショッピング アシスタンスの顧客アカウント権限

管理者がストアサポートスタッフのアカウントアクセスを有効にするには、お客様は自分のアカウントでこの機能を有効にする必要があります。

1. 顧客は次の場所に移動します。 **[!UICONTROL Account Information]** ページ。

1. 選択します。 **[!UICONTROL Allow remote shopping assistance]** チェックボックス。

1. 顧客のクリック数 **[!UICONTROL Save]**.

![アカウント情報ページ](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>この権限がない場合、管理者ユーザーはこの顧客としてログインできません。

## 顧客としてログインを使用

>[!INFO]
>
>使用目的 _顧客としてログイン_&#x200B;管理者が前述のように設定されていることを確認してください。

_顧客としてログイン_ を使用すると、顧客と同様にサイトを表示でき、トラブルシューティングや顧客向けの他のアクションを実行できます。 必要な権限を持つユーザーの役割が割り当てられている場合：

1. 次のいずれかをクリックできます。 **[!UICONTROL Login as Customer]** 前のセクションにリストされたページで。
1. 「顧客としてログイン」アクションは、「アクション」レポートで使用できます。

>[!WARNING]
>
>ログイン中に実行されたアクション [!UICONTROL _顧客として_] （製品の追加や削除など）は、実際の顧客の注文に適用されます。 ストアフロントには、次の場合にバナーが表示されます `logged in as customer_name` 特別な状態を思い出させる。

## カスタマーログとしてログイン

{{ee-feature}}

Adobe Commerceには、のログが用意されています _顧客としてログイン_ アクション。 管理者ユーザーが機能にアクセスするすべてのセッションが一覧表示されます。 ログに記録されたアクションにアクセスするには、 [管理アクションレポート](../systems/action-log-report.md).

レポート設定をフィルタリングできます **[!UICONTROL Action Group]** 対象： `Login As Customer` ページの上部との **[!UICONTROL Search]**.

![アクションレポートのフィルタリング](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
