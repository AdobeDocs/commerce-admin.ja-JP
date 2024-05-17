---
title: 統合
description: サードパーティ統合用の OAuth 資格情報とリダイレクト URL の設定方法を説明します。
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# 統合

Commerce管理者で統合を定義すると、サードパーティ統合用の OAuth 資格情報とリダイレクト URL の場所が設定され、統合に必要な使用可能な API リソースが特定されます。 統合登録プロセスの詳細については、を参照してください。 [OAuth ベースの認証](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) Commerce開発者向けドキュメント

![統合](./assets/integrations.png){width="700" zoomable="yes"}

## オンボーディングワークフロー

1. **統合を承認**  – に移動します **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**をページ表示し、関連する統合を見つけて認証します。
1. **ログインの検証と確立** - プロンプトが表示されたら、リクエストされたアクセスを承認します。 サードパーティにリダイレクトされた場合は、システムにログインするか、アカウントを作成します。 ログインに成功したら、統合ページに戻ります。
1. **承認された統合の確認を受信** - システムは、統合が正常に承認されたことを示す通知を送信します。 統合を設定して資格情報を受け取ると、アクセスまたはリクエストトークンを呼び出す必要はなくなります。

## 統合の追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

   ![新しい統合](./assets/integration-new.png){width="600" zoomable="yes"}

1. 次の統合情報を入力します。

   - を入力 **[!UICONTROL Name]** の統合および連絡先 **[!UICONTROL Email]** 住所。

   - を入力 **[!UICONTROL Callback URL]** トークン交換に OAuth を使用する場合は、OAuth 認証情報を送信できます。 使用 `https://` を強くお勧めします。

   - を入力 **[!UICONTROL Identity Link URL]** をクリックして、これらのAdobe CommerceまたはMagento Open Source統合資格情報を持つサードパーティアカウントにユーザーをリダイレクトします。

   >[!NOTE]
   >
   > この `Integration not secure` 警告ラベルは、の各統合名の近くに表示されます [!UICONTROL Integrations] https URL がに保存されるまでのリマインダーとしてのグリッド [!UICONTROL Callback URL] および [!UICONTROL Identity Link URL] フィールド。

   - プロンプトが表示されたら、パスワードを入力して ID を確認します。

1. 左パネルで、を選択します。 **[!UICONTROL API]** 次の手順を実行します。

   - を設定 **[!UICONTROL Resource Access]** を次のいずれかに変更します。

      - `All`
      - `Custom`

   - カスタムアクセスの場合は、必要な各リソースのチェックボックスをオンにします。

     ![統合 – 利用可能な API](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.

## 統合のアクティブ化

デフォルトでは、保存済みの統合はでグリッドに表示されます `Inactive` ステータス。 有効にするには、次の手順を実行します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. 新しく作成した統合を見つけて、 **[!UICONTROL Activate]** リンク。

1. 右上隅のをクリックします。 **[!UICONTROL Allow]**.

   拡張機能の統合トークンを表示します。 この情報を暗号化された安全な場所にコピーして、統合で使用できるようにします。

   ![拡張機能の統合トークン](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. 右上隅のをクリックします。 **[!UICONTROL Done]**.

## 統合の再認証

新しい統合アクセストークンおよびアクセストークン秘密鍵を生成するには、管理者から統合を再認証しました。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. との統合の検索 **[!UICONTROL Active]** ステータス。

1. 対象： _[!UICONTROL Activate]_列で、**[!UICONTROL Reauthorize]**.

1. クリック **[!UICONTROL Reauthorize]** API リソースへのアクセスを承認します。

1. 拡張機能の新しい統合トークンを保存し、 **[!UICONTROL Done]**.

## API ゲストアクセスのセキュリティ設定の変更

デフォルトでは、CMS、カタログ、その他のストアリソースへの匿名ゲストアクセスは許可されません。 設定を変更する必要がある場合は、次の操作を行います。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Services]** を選択します **[!UICONTROL Magento Web API]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Web API Security Setting]** セクション。

   ![サービスの設定 – web API セキュリティ設定](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Allow Anonymous Guest Access]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

詳しくは、を参照してください [匿名 Web API へのアクセスの制限](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) Commerce開発者向けドキュメント

## 統合の削除

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. 既存の統合を見つけて、アイコン（ ![ごみ箱アイコン](../assets/icon-delete-trashcan-solid.png) ） **[!UICONTROL Delete]** 列。

1. アクションを確定するには、 **[!UICONTROL OK]**.
