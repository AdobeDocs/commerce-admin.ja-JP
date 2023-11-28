---
title: ニュースレター購読者の管理
description: アクティブな購読の単純なリストを使用して、ニュースレター購読者を管理する方法を説明します。
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# ニュースレター購読者の管理

ベストプラクティスとして、定期的に購読リストを管理し、購読解除のリクエストを必ず処理するようにしてください。 一部の管轄地域では、登録解除のリクエストが特定の期間内に処理されることが法律で義務付けられています。

アクティブな購読の単純なリストを使用すると、購読者を簡単に管理できます。 顧客が購読解除リクエストを送信すると、 _配信停止_ 選択した 1 つ以上の購読に対するアクション。

複数のストア表示を持つ単一サイトの設定では、顧客アカウントのサブスクリプションを特定のストア表示に関連付けることができます。

グローバルを使用したマルチストアおよびマルチサイトの設定 [顧客アカウントの範囲](../customers/customer-account-scope.md)の場合、顧客アカウントを複数のサイト/ストアのニュースレターに購読登録できます。 この場合、顧客アカウントを編集してサブスクリプションのグループを管理したり、特定のサイトやストアのサブスクリプションをキャンセルしてリクエストを受け入れたりできます。

サードパーティのサービスを使用してニュースレターを送信する場合は、購読リストを CSV または XML ファイルとして書き出すことができます。

## 顧客の購読を管理

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. グリッド内の顧客を検索し、 **[!UICONTROL Edit]** （内） _[!UICONTROL Action]_列。

1. クリック **[!UICONTROL Newsletter]** をクリックします。

1. サイト/ストアの設定に従って、顧客のサブスクリプションを変更します。

   単一のサイト/シングルストアの設定では、 **[!UICONTROL Subscribed to Newsletter]** チェックボックス。

   ![単一ストアの顧客ニュースレター購読チェックボックス](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   単一のサイト/マルチストアの設定では、 **[!UICONTROL Subscribed to Newsletter]** チェックボックスとセット **[!UICONTROL Subscribed on Store View]** をサブスクリプションの正しいストア表示に追加します。

   ![マルチストア顧客ニュースレターの購読チェックボックスとストア表示セレクター](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   グローバルな顧客アカウント範囲を持つマルチサイト/マルチストアの設定の場合、ページにはすべてのサイトの購読ステータスが表示されます。 選択またはクリアできる **[!UICONTROL Subscribed]** チェックボックスをオンにして、 **[!UICONTROL Store View]** 購読の

   ![マルチサイト顧客ニュースレター購読チェックボックスとストア表示セレクター](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. クリック **[!UICONTROL Save Customer]**.

## 購読者リストからの購読のキャンセル

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

   複数のサイトのサブスクリプションを持つ顧客がいるマルチサイト設定の場合、各サブスクリプションはグリッドの行項目として表示されます。

1. グリッドで購読者を見つけ、最初の列のチェックボックスをオンにします。

   >[!NOTE]
   >
   >一括購読解除の場合、キャンセルする各購読者のチェックボックスをオンにします。

1. を設定します。 _[!UICONTROL Action]_～を制御する&#x200B;**[!UICONTROL Unsubscribe]**をクリックします。**[!UICONTROL Submit]**.

   ![ニュースレターを購読解除](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   レコードのステータスは、 `Unsubscribed`.

## 購読者のリストをエクスポート

1. 次から： _[!UICONTROL Newsletter Subscribers]_リストを表示するには、フィルタコントロールを使用して、_&#x200B;ステータス&#x200B;_/ `Subscribed` およびは、適切な web サイト、ストア、またはストア表示に対して使用します。

1. を設定します。 **[!UICONTROL Export to]** コントロールを次のいずれかに設定します。

   - `CSV`
   - `XML`

1. クリック **[!UICONTROL Export]** 画面の下部にあるプロンプトを探し、ファイルを保存します。

   ![ニュースレターの購読者を書き出し](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## 購読者リストから購読者を削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

1. グリッドで購読者を見つけ、最初の列のチェックボックスをオンにします。

1. を設定します。 _[!UICONTROL Action]_～を制御する&#x200B;**[!UICONTROL Delete]**をクリックします。**[!UICONTROL Submit]**.

1. 確認するメッセージが表示されたら、「 **[!UICONTROL OK]**.
