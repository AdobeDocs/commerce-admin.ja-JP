---
title: '[!UICONTROL My Quote Templates]'
description: ストアフロントアカウントダッシュボードで使用できる見積もりテンプレートのカスタマーエクスペリエンスについて説明します。
feature: B2B, Companies, Quotes
source-git-commit: c2cb4db24effa764996b0fb77fbda67727392efe
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---


# [!UICONTROL My Quote Templates]

見積が有効になっている場合、顧客アカウント・ダッシュボードの「_[!UICONTROL My Quotes Template]_」セクションには、顧客アカウントに関連付けられているすべての見積テンプレートがリストされます。 権限に応じて、会社の代わりに購入を行う購入者のみが見積もりテンプレートをリクエストし、繰り返し注文の見積もり価格と条件を交渉できます。

![ 自分の見積もりテンプレート ](./assets/account-dashboard-quote-templates-list.png){width="700" zoomable="yes"}

見積テンプレートのリストには、ステータス別にテンプレートが表示されます。

- **[!UICONTROL Active Quote Templates]** では、ネゴシエートされ、使用が承認されたテンプレートがリストされます。 ネゴシエーション・プロセス中にこれらのオプションが構成された場合は、最小見積合計と発注が含まれます。 購入者は、テンプレートからリンクされた見積もりを生成し、見積もり条件に基づいて注文を送信できます。

- **[!UICONTROL In Review]** は、現在のステータスを示し、テンプレートを開くためのリンクを提供するネゴシエーション・プロセスのテンプレートをリストします。

- **[!UICONTROL Inactive]** には、バイヤーが許可された数のコミット済み注文を使い果たしたため、期限切れ、キャンセル済み、または無効になったテンプレートが一覧表示されます。

買い手にとって、*[!UICONTROL My Quotes Templates]* ページは、ネゴシエートプロセス中の買い手と売り手の間のすべての通信の焦点です。

売り手によって提供された交渉済み条件に同意する買い手は、テンプレートを受け入れ、それを使用して注文に使用できる承認済みのリンクされた見積もりを生成できます。

- 見積もりテンプレートの管理に関連するアクション：

   - テンプレートのキャンセル
   - 確認のために販売者に送信
   - 見積もりテンプレートの承認
   - 見積テンプレートの有効期限の変更
   - 配送先住所を追加

- ネゴシエーション・プロセス中に見積テンプレート詳細を更新するための処理：

   - 品目の価格と更新を確認します。
   - 見積テンプレートに数量しきい値が設定されている場合は、最小値と最大値を調整します。
   - [!UICONTROL Comments] および [!UICONTROL History] のセクションからネゴシエーション・プロセスを追跡します。
   - テンプレートがレビュー中の場合、購入者は品目を削除することで見積テンプレートを変更できます。
   - 品目レベルおよび見積レベルでメモを追加して、販売者と連絡を取り、交渉します。

  変更を加えた後、買い手はレビューのために売り手にテンプレートを返します。

- ネゴシエーション中の一般的なアクション：

   - 確認のために販売者に見積テンプレートを送信
   - 見積もりテンプレートの承認
   - ネゴシエーションを終了して見積をクローズする場合は「取消」

次の例は、購入者によって更新され、レビューのために販売者に送り返された見積もりテンプレートを示しています。

![ 見積テンプレートの購買担当ビュー ](./assets/account-dashboard-my-quote-template-detailed.png){width="700" zoomable="yes"}

`Submitted` ステータスのテンプレートは、販売者がテンプレートをレビューおよび更新し、購入者に返すまでロックされます。

## 見積もりテンプレートの作成

購買担当は、次のいずれかの方法を使用して見積テンプレートのネゴシエーション・プロセスを開始できます。

- アクションをクリックして、既存の Quote からテンプレート **[!UICONTROL Create quote template]** 作成します。

- ストアフロントから見積依頼を送信し、営業担当者に見積依頼から見積テンプレートを作成するように依頼するコメントを追加します。

## 見積もりテンプレートの表示

1. 購入者が自分のアカウントにログインします。

1. 左側のパネルで、「**[!UICONTROL My Quote Templates]**」を選択します。

1. リストで見積テンプレートを検索し、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL View]**をクリックします。

## 配送先住所を追加

購入者は、配送先住所が記載されるまで見積テンプレートを受け入れることができません。

1. 購入者が自分のアカウントにログインします。

1. 左側のパネルで、「**[!UICONTROL My Quote Templates]**」を選択します。

1. 必要な見積もりテンプレートを選択します。

1. 「**[!UICONTROL Shipping Information]**」セクションで、「**[!UICONTROL Add New Address]**」をクリックします。

1. 新しいアドレスの詳細を入力します。

1. **[!UICONTROL Save Address]** をクリックします。

購入者が住所を追加した後、テンプレートをレビュー用に販売者に送り返します。 売り手は出荷と配達のオプションを提供します。 これらの更新は、交渉された見積もり価格に影響を与える可能性があります。 配送オプションはチェックアウト時にロックされます。

## リンクされた見積もりを生成

バイヤーは見積テンプレートを受け入れた後、それを使用して、*[!UICONTROL My Quote Templates dashboard]* ーザーまたは見積テンプレートから **[!UICONTROL Generate a quote]** 処理を使用して、承認済のリンク済の見積を生成できます。

リンクされた見積もりには、承認され、チェックアウトの準備が整ったことを示す通知が含まれています。 また、ヘッダー情報に見積もりテンプレートへのリンクも表示されます。

![ 引用テンプレートから生成されたリンク済み引用 ](./assets/quote-templates-linked-quote.png){width="700" zoomable="yes"}

見積テンプレートが注文しきい値で設定されている場合、リンクされた見積が生成されるとカウントが増分されます。

購入者は、リンクされた見積もりから次のアクションを完了できます。

- 見積に数量しきい値が設定されている場合は、明細品目の受注数量を調整します。
- チェックアウトに進み、注文を送信します。
- 見積もりを削除または印刷します。
- 見積の生成に使用する見積テンプレートを開きます。

## 見積もりテンプレートのキャンセル

見積テンプレート ページで、[**[!UICONTROL Cancel Quote Template]**] をクリックします。

見積テンプレートが取り消され、見積の状態が `Closed` に変わります。 クローズド引用符は、*[!UICONTROL Inactive]* の引用符のリストに残り、管理者の _[!UICONTROL Quote Templates]_グリッドにも残ります。



