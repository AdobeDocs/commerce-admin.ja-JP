---
title: 会社アカウント
description: Adobe Commerceストアで管理されている会社アカウントを使用して、同じ会社に属する複数の購入者を 1 つの会社アカウントに参加させる方法を説明します。
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# 会社アカウント

B2B 会社のアカウントをストアに組み込むと、会社が組織内のユーザーの役割に基づいて柔軟な権限を持つ複数のサブアカウントを作成できるので、企業の買い物を簡略化できます。 会社によっては、店舗管理者がニーズに合わせてプロモーションや価格を調整し、買い物客の要望に応じて高度にカスタマイズされたオファーを作成し、注文を増やすことができます。 標準への会社アカウントの関連付けの追加 [個人版](../customers/account-create.md) 顧客が、会社に定義された特定の購入ワークフローを使用できるようにします。

会社アカウントの利点：

- 無制限のオファー [会社のユーザー](account-company-users.md) 追加のアカウントを作成し、企業での購入を簡素化します。

- のサポートを含む _スマート_ 異なる会社アカウント階層 [役割と権限](account-company-roles-permissions.md) 注文を行う場合。

- 商人が以下を提供することで収入を増やす仕組みを提供 [会社店舗クレジット](credit-company.md) 支払い方法として。

- をサポートします。 [管理](account-company-manage.md) 」という名前に変更されました。

## 会社アカウントを表示

The _会社_ グリッドには、ステータスの設定に関係なく、すべてのアクティブな会社アカウントと保留中のリクエストが一覧表示されます。 また、 [作成中](account-company-create.md) および [管理](account-company-manage.md) 会社アカウント。 標準のグリッドコントロールを使用して、リストをフィルタし、列のレイアウトを調整します。 列の説明のリストについては、 _列の説明_ のセクション [会社アカウントの管理](account-company-manage.md).

顧客はストアフロントから会社アカウントを作成することも、マーチャントが管理者からアカウントを作成することもできます。 デフォルトでは、ストアフロントから会社アカウントを作成する機能が有効になっています。 設定で許可されている場合、ストアの訪問者は会社のアカウントのオープンをリクエストできます。 会社アカウントが承認されると、会社の管理者は、様々なレベルの権限を持つ会社構造およびユーザーを設定できます。

Adobe Analytics の _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![企業グリッド](./assets/companies-grid.png){width="700" zoomable="yes"}

The [!UICONTROL Companies] グリッドには、ステータスに関係なく、すべての会社が一覧表示されます。 次の例は、「ACME」会社と「Vandelay」会社の 2 つの会社のアカウントを示しています。

## 会社の管理者

次の例は、 _顧客_ グリッドに、最初の会社管理者アカウントを表示します。

![会社の管理者アカウントを含む顧客グリッド](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

会社の管理者としての役割を持つ人物が社内で複数の役割を持つ可能性があります。 会社管理者用に別の電子メールアドレスを入力した場合、初期の会社構造には、会社管理者と、会社管理者名の個々のユーザーアカウントが含まれます。 この場合、会社の管理者は、会社または個々のユーザーとしてアカウントにログインできます。

アカウントの作成後、会社の管理者がの会社構造を定義します。 [チーム](account-company-structure.md)、を設定します。 [会社のユーザー](account-company-users.md)，確立している [役割と権限](account-company-roles-permissions.md) を設定します。

### 初めてログインする前に会社の管理者パスワードを設定する

1. 会社の管理者が、ストアから歓迎の電子メールを検索します。

   ![お知らせメールの例](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >E メールアドレスのターゲットと E メールのコンテンツは、 [会社のメールオプション](email-company-configuration.md) 設定。

1. 手順に従って、をクリックします。 [!UICONTROL **リンク**] パスワードを設定します。

1. 次の項目に入る [!UICONTROL **新しいパスワード**] アカウントを更新し、再度確認する必要があります。

   パスワードには、次の文字タイプのうち少なくとも 3 つを含める必要があります。

   - 小文字 (abc...)
   - 大文字 (ABC...)
   - 数値 (1234567890)
   - 特殊文字 (!@#$...)

1. クリック数 [!UICONTROL **新しいパスワードの設定**].

   ![顧客ログイン — 会社管理者](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. 次の場合に [!UICONTROL Customer Login] ページが表示され、顧客が [!UICONTROL **電子メール**] および [!UICONTROL **パスワード**].

1. クリック数 [!UICONTROL **ログイン**] をクリックして、アカウントダッシュボードにアクセスします。

   ![アカウントダッシュボード — 会社](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## 会社構造

会社アカウントは、ビジネスの構造を反映するように設定できます。 最初は、会社の管理者のみが会社の構造に含まれますが、ユーザーのチームを含めるように拡張できます。 ユーザーは、チームに関連付けることも、社内の部署や部門の階層内で整理することもできます。 この構造は、 [承認ルール](account-dashboard-approval-rules.md) 対象： [発注書](purchase-order-flow.md) 会社アカウントに関連付けられた（発注）。

![部門を持つ会社構造](./assets/company-structure-diagram.svg){width="450"}

会社管理者のアカウントダッシュボードでは、会社構造はツリーとして表され、最初は会社管理者のみで構成されます。

![会社管理者との会社構造](./assets/company-structure-tree-admin.png){width="600"}

アカウントを作成すると、会社の管理者は会社の電子メールアドレスを使用したり、別の電子メールアドレスを割り当てたりできます。

次の例では、最初の会社構造に、会社管理者と、会社管理者の名前の個々のユーザーアカウントが含まれています。 ただし、会社の管理者の機能（会社の構造や承認ルールなど）は、会社の管理者として指定されたユーザーアカウントにログインしている場合にのみ使用できます。

![管理者およびユーザーアカウントを使用した会社構造](./assets/company-structure-tree-admin-user.png){width="600"}
