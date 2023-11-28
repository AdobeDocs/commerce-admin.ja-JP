---
title: 統合
description: サードパーティ統合用の OAuth 資格情報とリダイレクト URL の設定方法について説明します。
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# 統合

コマース管理で統合を定義すると、サードパーティ統合の OAuth 資格情報とリダイレクト URL の場所が設定され、統合に必要な使用可能な API リソースが特定されます。 統合登録プロセスの詳細については、 [OAuth ベースの認証](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) （ Commerce 開発者向けドキュメント）を参照してください。

![統合](./assets/integrations.png){width="700" zoomable="yes"}

## オンボーディングワークフロー

1. **統合を認証**  — に移動します。 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**ページで、関連する統合を見つけて、認証します。
1. **ログインの確認と確立**  — 要求されたアクセスを受け入れます。 サードパーティにリダイレクトされた場合は、システムにログインするか、アカウントを作成します。 正常にログインしたら、統合ページに戻ります。
1. **認証済み統合の確認を受け取る**  — 統合が正常に承認されたことを示す通知をシステムが送信します。 統合を設定し、資格情報を受け取った後は、のアクセスやリクエストトークンの呼び出しをおこなう必要がなくなりました。

## 統合の追加

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

   ![新しい統合](./assets/integration-new.png){width="600" zoomable="yes"}

1. 次の統合情報を入力します。

   - 次を入力します。 **[!UICONTROL Name]** 統合と連絡先の **[!UICONTROL Email]** 住所。

   - 次を入力します。 **[!UICONTROL Callback URL]** ここでは、OAuth をトークン交換に使用する際に OAuth 資格情報を送信できます。 使用 `https://` を強くお勧めします。

   - 次を入力します。 **[!UICONTROL Identity Link URL]** をクリックして、Adobe CommerceまたはMagento Open Source統合資格情報を使用して、ユーザーをサードパーティのアカウントにリダイレクトします。

   >[!NOTE]
   >
   > The `Integration not secure` 警告ラベルは、 [!UICONTROL Integrations] グリッド (HTTPS URL が [!UICONTROL Callback URL] および [!UICONTROL Identity Link URL] フィールド。

   - プロンプトが表示されたら、ID を確認するためのパスワードを入力します。

1. 左側のパネルで、を選択します。 **[!UICONTROL API]** 次の操作を実行します。

   - 設定 **[!UICONTROL Resource Access]** を次のいずれかに変更します。

      - `All`
      - `Custom`

   - カスタムアクセスの場合、必要な各リソースのチェックボックスをオンにします。

     ![統合 — 使用可能な API](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save]**.

## 統合のアクティブ化

デフォルトでは、保存された統合は、 `Inactive` ステータス。 アクティブ化するには、次の手順を実行します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. 新しく作成した統合を見つけ、 **[!UICONTROL Activate]** リンク。

1. 右上隅で、 **[!UICONTROL Allow]**.

   このアクションは、拡張機能の統合トークンを表示します。 この情報を暗号化された安全な場所にコピーして、統合で使用します。

   ![拡張機能の統合トークン](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. 右上隅で、 **[!UICONTROL Done]**.

## 統合の再認証

新しい統合アクセストークンとアクセストークン秘密鍵を生成するには、管理者から統合を再認証します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. との統合を見つける **[!UICONTROL Active]** ステータス。

1. In _[!UICONTROL Activate]_列で、**[!UICONTROL Reauthorize]**.

1. クリック **[!UICONTROL Reauthorize]** をクリックして、API リソースへのアクセスを承認します。

1. 拡張機能用の新しい統合トークンを保存し、 **[!UICONTROL Done]**.

## API ゲストによるアクセスセキュリティ設定の変更

デフォルトでは、CMS、カタログ、その他のストアリソースへの匿名のゲストによるアクセスは許可されません。 設定を変更する必要がある場合は、次の操作を行います。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Services]** を選択します。 **[!UICONTROL Magento Web API]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Web API Security Setting]** 」セクションに入力します。

   ![サービスの設定 — Web API セキュリティ設定](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Allow Anonymous Guest Access]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

詳しくは、 [匿名 Web API へのアクセスの制限](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) （ Commerce 開発者向けドキュメント）を参照してください。

## 統合の削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. 既存の統合を見つけて、アイコン ( ![ごみ箱アイコン](../assets/icon-delete-trashcan-solid.png) ) を **[!UICONTROL Delete]** 列。

1. アクションを確定するには、 **[!UICONTROL OK]**.
