---
title: ニュースレターと購読
description: ニュースレターの概要と、この機能を低コストのプロモーションツールとして有効にする方法について説明します。
exl-id: ad4488c2-1b8b-4326-8486-743c75c5b9a6
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# ニュースレターと購読

通常のニュースレターを公開することは、利用可能な最も強力で手頃な価格のマーケティングツールの 1 つと考えられています。 Commerceには、購読している顧客にニュースレターを公開および配布する機能に加え、ニュースレターを作成し、購読者のリストを作成および管理し、コンテンツを開発し、ストアへのトラフィックを促進するツールが用意されています。 を使用することもできます。 [ページ階層](../content-design/page-hierarchy.md) 過去のイシューのアーカイブを作成する

>[!NOTE]
>
>Commerce インスタンスをサードパーティのニュースレターサービスプロバイダーと統合したり、拡張機能を追加したりすることで、に対応能力を追加できます。 詳しくは、 [Commerce Marketplace](../getting-started/commerce-marketplace.md).

ニュースレターを作成する最初の手順は、サイトのニュースレター設定を指定することです。 メールで送信される確認リンクをクリックして購読を確認するように、顧客に求めることができます。 このダブルオプトイン方法では、顧客はニュースレターを受信することを 2 回確認する必要があり、スパムと見なされる可能性が低くなります。

## ニュースレターの有効化

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Newsletter]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL General Options]** セクション。

1. ストア表示範囲のニュースレターを有効にするには、次を設定します **[!UICONTROL Enabled]** 対象： `Yes`.

ニュースレター機能を有効にした後、 _[!UICONTROL Subscription Options]_セクションが表示されます。

## 購読オプションの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Newsletter]**.

1. 必要に応じて、 [設定スコープの変更](../getting-started/websites-stores-views.md#scope-settings) ニュースレター設定の変更を特定のサイト/ストア表示に適用します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Subscription Options]** を選択し、次の操作を実行します。

   ![顧客設定 – ニュースレターの購読](../configuration-reference/customers/assets/newsletter-subscription-options.png){width="600" zoomable="yes"}

   - 購読者に送信される次の各メールメッセージのメールテンプレートと送信者を確認します。

      - [!UICONTROL Success email]
      - [!UICONTROL Confirmation email]
      - [!UICONTROL Unsubscribe email]

   - ダブルオプトインプロセスを使用して購読を確認するには、を設定します **[!UICONTROL Need to Confirm]** 対象： `Yes`.

   - ストアのアカウントを持っていないユーザーがニュースレターを購読できるようにするには、を設定します **[!UICONTROL Allow Guest Subscription]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.
