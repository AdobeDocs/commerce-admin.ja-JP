---
title: 買い物かご価格ルールの予定変更
description: キャンペーンの一環としてスケジュールに従って買い物かごの価格ルールを適用し、他のコンテンツの変更と共にグループ化する方法を説明します。
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 買い物かご価格ルールの予定変更

{{ee-feature}}

買い物かごの価格ルールは、キャンペーンの一環としてスケジュールに従って適用し、他のコンテンツの変更と共にグループ化できます。 価格ルールに対するスケジュール済みの変更に基づいてキャンペーンを作成したり、変更を既存のキャンペーンに適用したりできます。

![買い物かごの価格ルール — 予定変更](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>スケジュールされたすべての更新が連続して適用されます。 つまり、どのエンティティも、一度に 1 つのスケジュール済み更新のみを持つことができます。 スケジュールされた更新は、その期間内のすべてのストアビューに適用されます。 その結果、異なるストア表示に対して、エンティティが異なるスケジュール済み更新を同時に持つことはできません。 現在のスケジュール済み更新の影響を受けない、すべてのストア表示内のすべてのエンティティ属性値は、以前のスケジュール済み更新の値ではなく、デフォルト値から取得されます。

同じキャンペーンで複数の価格ルールが実行されている場合、 _[!UICONTROL Priority]_価格ルールの設定によって、どのルールが優先されるかが決まります。 詳しくは、 [コンテンツのステージング](../content-design/content-staging.md).

次の注意事項に注意してください。

- 価格ルールを含むキャンペーンが終了日なしで最初に作成された場合、キャンペーンを後から編集して終了日を含めることはできません。 キャンペーンの作成時に終了日を追加するか、既存のキャンペーンのバージョンを複製して、必要に応じて終了日を複製に追加することをお勧めします。
- スケジュールされた更新を使用して終了日の買い物かごの価格ルールを有効にする場合、ルールは必ず最初は無効だった状態で設定してください。 既にアクティブなルールは終了日を考慮しません。
- クーポンは、買い物かごの価格ルールに接続されません。 スケジュールされた更新では、 _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_、および_[!UICONTROL Uses per Customer]_ フィールド _[!UICONTROL Rule Information]_タブをクリックします。 また、_[!UICONTROL Manage Coupon Codes]_ タブは使用できません。

>[!IMPORTANT]
>
>Campaign **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** は、 **_デフォルト_** 管理者のタイムゾーン。各 Web サイトのローカルタイムゾーンから変換されます。 異なるタイムゾーンに複数の Web サイトがあり、米国のタイムゾーンに基づいてキャンペーンを開始したい場合を考えてみましょう。 この場合、ローカルタイムゾーンごとに個別に更新をスケジュールし、 **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** 各ローカル Web サイトのタイムゾーンからデフォルトの管理タイムゾーンに変換されます。
