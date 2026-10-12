---
title: ニュースレターと購読
description: ニュースレターと、この機能を低コストのプロモーションツールとして有効にする方法について説明します。
exl-id: ad4488c2-1b8b-4326-8486-743c75c5b9a6
feature: Customers, Communications
TQID: 'https://experienceleague.adobe.com/riYrvqQTvcEa2p9EQXv-oy3juefmg4pch20aOHDOoEQ'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: bb03f6c4-cab9-560e-9d02-5816e1808d17
    internal-label: Communications
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%
---
# ニュースレターと購読

定期的なニュースレターの公開は、利用可能な最も強力で手頃なマーケティングツールのひとつであると考えられています。 Commerceなら、購読している顧客にニュースレターを配信します。さらに、ニュースレターの作成、購読者リストの作成と管理、コンテンツの制作、ストアへのトラフィックの増加を実現するツールも利用できます。 また、[ ページ階層](../content-design/page-hierarchy.md)を使用して、過去の問題のアーカイブを作成することもできます。

>[!NOTE]
>
>Commerce インスタンスをサードパーティのニュースレターサービスプロバイダーと統合し、拡張機能を追加することで、機能を追加できます。 詳しくは、[Commerce Marketplace](../getting-started/commerce-marketplace.md)を参照してください。

ニュースレターを作成する最初の手順は、サイトのニュースレター設定を設定することです。 電子メールで送信された確認リンクをクリックして、サブスクリプションを確認するように顧客に要求できます。 このダブルオプトイン方式では、顧客がニュースレターを受け取ることを2回確認する必要があり、迷惑メールとみなされる可能性を低減します。

## ニュースレターの有効化

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Newsletter]**&#x200B;を選択します。

1. **[!UICONTROL General Options]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. ストアビューの範囲でニュースレターを有効にするには、**[!UICONTROL Enabled]**&#x200B;を`Yes`に設定します。

ニュースレター機能を有効にすると、_[!UICONTROL Subscription Options]_セクションが表示されます。

## サブスクリプションオプションの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Newsletter]**&#x200B;を選択します。

1. 必要に応じて、[設定スコープ ](../getting-started/websites-stores-views.md#scope-settings)を変更して、特定のサイト/ストアビューにニュースレター設定の変更を適用します。

1. **[!UICONTROL Subscription Options]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![顧客設定 – ニュースレター購読](../configuration-reference/customers/assets/newsletter-subscription-options.png){width="600" zoomable="yes"}

   - 購読者に送信される次の各メールメッセージのメールテンプレートと送信者を確認します。

     - [!UICONTROL Success email]
     - [!UICONTROL Confirmation email]
     - [!UICONTROL Unsubscribe email]

   - ダブルオプトインプロセスを使用してサブスクリプションを確認するには、**[!UICONTROL Need to Confirm]**&#x200B;を`Yes`に設定します。

   - ストアのアカウントを持たないユーザーにニュースレターの購読を許可するには、**[!UICONTROL Allow Guest Subscription]**&#x200B;を`Yes`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
