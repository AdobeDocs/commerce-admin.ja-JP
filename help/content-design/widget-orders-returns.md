---
title: 注文と返品のウィジェット
description: 注文と返品ウィジェットを使用して、顧客が注文のステータスを確認し、請求書を印刷し、出荷を追跡できるようにする方法について説明します。
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/jWpFWPBwvKr5EnMXdV5-3zAqagGuzPrvOL6-gMiEw-M
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 382
ht-degree: 0%

---

# 注文と返品のウィジェット

_注文と返品_ ウィジェットを使用すると、ゲストは注文のステータスを確認し、請求書を印刷し、配送を追跡できます。 ウィジェットがストアフロントに追加されると、ゲストとアカウントにログインしていない顧客にのみ表示されます。 ご注文の際には、注文ID、請求先姓、メールアドレスまたは郵便番号を入力します。

![&#x200B; ストアフロントのサイドバーにある注文と返品ウィジェット &#x200B;](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## ストアフロントの注文と返品のウィジェット

1. お客様は、**[!UICONTROL Find Order By]** オプションを使用して、注文を検索するために使用する次のいずれかのパラメーターを選択できます。

   - メールアドレス
   - 郵便番号

1. お客様が&#x200B;**[!UICONTROL Order ID]**&#x200B;と&#x200B;**[!UICONTROL Billing Last Name]**&#x200B;にエントリします。

1. 注文に関連付けられている請求&#x200B;**[!UICONTROL Email Address]**&#x200B;または&#x200B;**[!UICONTROL ZIP Code]**&#x200B;のいずれかを入力します。

1. **[!UICONTROL Search]**&#x200B;をクリックして注文を取得します。

   ![&#x200B; ストアフロントに表示される注文情報](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## 注文と返品ウィジェットの設定

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add Widget]**」をクリックします。

1. _[!UICONTROL Settings]_&#x200B;セクションで、次の操作を行います。

   - **[!UICONTROL Type]**&#x200B;を`Orders and Returns`に設定します。

   - ストアで使用されている&#x200B;**[!UICONTROL Design Theme]**&#x200B;を選択します。

1. **[!UICONTROL Continue]**&#x200B;をクリックします。

1. _[!UICONTROL Storefront Properties]_&#x200B;セクションで、次の操作を行います。

   - 「**[!UICONTROL Widget Title]**」に、ウィジェットの説明的なタイトルを入力します。

     このタイトルは、管理者からのみ表示されます。

   - **[!UICONTROL Assign to Store Views]**&#x200B;で、ウィジェットが表示されているストアビューを選択します。

     特定のストアビュー、または`All Store Views`を選択できます。 複数のビューを選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押しながら、各オプションをクリックします。

   - （オプション） **[!UICONTROL Sort Order]**&#x200B;の場合、ページの同じ部分で他のユーザーと一緒にこの項目を表示する順序を決定する番号を入力します。 （`0` = first, `1` = second, `3` = thirdなど）

1. _[!UICONTROL Layout Updates]_&#x200B;セクションで、**[!UICONTROL Add Layout Update]**&#x200B;をクリックし、次の操作を行います。

   - **[!UICONTROL Display On]**&#x200B;を、ウィジェットを表示するページの種類に設定します。

   - ウィジェットがページ上のどこに表示されるかを判断するには、残りのレイアウト更新情報を完了します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

1. キャッシュの更新を求めるメッセージが表示されたら、ページの上部にあるメッセージ内のリンクをクリックし、指示に従います。
