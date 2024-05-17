---
title: ニュースレター購読者の管理
description: アクティブな購読の単純なリストを使用して、ニュースレターの購読者を管理する方法を説明します。
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# ニュースレター購読者の管理

ベストプラクティスとして、購読リストを定期的に管理し、購読解除のリクエストを必ず処理してください。 一部の管轄区域では、登録解除のリクエストが特定の期間内に処理されることが法律で義務付けられています。

アクティブな購読の単純なリストを使用して、購読者を簡単に管理できます。 顧客が登録解除リクエストを送信した際は、 _購読解除_ 選択した 1 つ以上のサブスクリプションに対するアクション。

複数のストア表示を使用した単一サイトの設定では、顧客アカウントの購読を特定のストア表示に関連付けることができます。

グローバルなマルチストアおよびマルチサイト設定 [顧客アカウントの範囲](../customers/customer-account-scope.md)の場合、1 つの顧客アカウントで複数のサイトやストアのニュースレターを購読できます。 この場合、顧客アカウントを編集して購読のグループを管理したり、特定のサイト/ストアの購読をキャンセルしてリクエストに応じることができます。

サードパーティのサービスを使用してニュースレターを送信する場合は、購読リストを CSV または XML ファイルとして書き出すことができます。

## 顧客の購読の管理

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. グリッドで顧客を見つけて、 **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. クリック **[!UICONTROL Newsletter]** 左側のパネルで次の操作を行います。

1. サイト/ストアの設定に応じて、顧客の購読を変更します。

   単一サイト/単一ストアを設定する場合は、を選択またはクリアするだけで済みます **[!UICONTROL Subscribed to Newsletter]** チェックボックス。

   ![シングルストア顧客ニュースレター購読チェックボックス](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   単一サイト/マルチストアを設定する場合は、を選択または選択解除できます。 **[!UICONTROL Subscribed to Newsletter]** チェックボックスとセット **[!UICONTROL Subscribed on Store View]** をサブスクリプションの正しいストア表示に変更します。

   ![マルチストア顧客ニュースレター購読チェックボックスとストア表示セレクター](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   グローバル顧客アカウント範囲を使用したマルチサイト/マルチストア設定の場合、ページには、すべてのサイトの購読ステータスが表示されます。 を選択またはクリアできます **[!UICONTROL Subscribed]** チェックボックスをオンまたはオフにする **[!UICONTROL Store View]** サブスクリプション。

   ![マルチサイト顧客ニュースレター購読チェックボックスとストア表示セレクター](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. クリック **[!UICONTROL Save Customer]**.

## サブスクライバーリストからのサブスクリプションのキャンセル

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

   一部の顧客が複数のサイトの購読を持っているマルチサイト設定の場合、各購読はグリッドに行項目として表示されます。

1. グリッドで購読者を見つけ、最初の列のチェックボックスを選択します。

   >[!NOTE]
   >
   >一括登録解除の場合は、キャンセルする各購読者のチェックボックスを選択します。

1. を _[!UICONTROL Action]_コントロール先&#x200B;**[!UICONTROL Unsubscribe]**をクリックして、**[!UICONTROL Submit]**.

   ![ニュースレターの登録解除](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   レコードのステータスが「」に変わります `Unsubscribed`.

## サブスクライバーのリストのエクスポート

1. から _[!UICONTROL Newsletter Subscribers]_リスト、フィルタ コントロールを使用して、のレコードのみを含める_&#x200B;ステータス&#x200B;_件中 `Subscribed` 該当する web サイト、ストアまたはストア表示の場合はおよびを使用します。

1. を **[!UICONTROL Export to]** 次のいずれかに制御します。

   - `CSV`
   - `XML`

1. クリック **[!UICONTROL Export]** そして、画面の下部にあるプロンプトを探して、ファイルを保存します。

   ![ニュースレター購読者の書き出し](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## サブスクライバーリストからサブスクライバーを削除します

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

1. グリッドで購読者を見つけ、最初の列のチェックボックスを選択します。

1. を _[!UICONTROL Action]_コントロール先&#x200B;**[!UICONTROL Delete]**をクリックして、**[!UICONTROL Submit]**.

1. 確認を求められたら、 **[!UICONTROL OK]**.
