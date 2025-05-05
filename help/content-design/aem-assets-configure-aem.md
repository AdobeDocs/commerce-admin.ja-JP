---
title: Commerce用AEM Assets パッケージのインストール
description: CommerceのAEM Assets統合を有効にして、Adobe Commerce プロジェクトとExperience Manager Assets プロジェクトの間でアセットを同期するために必要なアセットメタデータを追加します。
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
source-git-commit: d7125774dbf6fb2796ccabc6df8e574455e1e968
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 0%

---

# AEM Assets パッケージのインストール

Adobeは、Experience Manager Assets as a Cloud Service環境設定にCommerce名前空間およびメタデータスキーマリソースを追加するプロジェクトテンプレート `commerce-assets` を提供します。 このテンプレートを Maven パッケージとして環境にデプロイします。 次に、AEM Assets オーサリング環境でCommerce メタデータを設定して、設定を完了します。

このテンプレートにより、次のリソースがAEM Assets オーサリング環境に追加されます。

- Commerce関連のプロパティを識別するた `Commerce` の [ カスタム名前空間 ](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json)。

- Adobe Commerce プロジェクトに関連付けられたCommerce アセットにタグ付けするた `Eligible for Commerce` のラベルが付いたカスタムメタデータタイプ `commerce:isCommerce`。

- カスタムメタデータタイプ `commerce:productmetadata` と、*[!UICONTROL Product Data]* スタムプロパティを追加するための対応する UI コンポーネント。 商品データには、Commerce アセットを商品 SKU に関連付けたり、アセットの画像 `role` と `position` 属性を指定したりするためのメタデータプロパティが含まれています。

  ![ カスタム製品データ UI コントロール ](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- Commerce アセットにタグ付けするための `Eligible for Commerce?` フィールドと `Product Data` フィールドを含む、Commerce タブを持つメタデータスキーマフォーム このフォームには、AEM Assets UI の `roles` および `order` （位置）フィールドを表示または非表示にするオプションも用意されています。

  ![AEM Assets メタデータスキーマフォームの「Commerce」タブ ](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- 最初のアセットの同期をサポートするための [ タグ付けされた承認済みCommerce アセット ](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml) サンプル `equipment_6.jpg`。 AEM AssetsからAdobe Commerceに同期できるのは、承認済みのCommerce アセットのみです。

>[!NOTE]
>`commerce-assets` AEM プロジェクトテンプレートについて詳しくは、[Readme](https://github.com/ankumalh/assets-commerce) を参照してください。

このAEM プロジェクトを使用して環境設定を更新するには、次のリソースと権限が必要です。

- プログラムおよびデプロイメントマネージャーの役割を使用して [AEM Assets Cloud Manager プログラムおよび環境にアクセス ](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo) します。

- [ ローカル AEMローカル開発環境 ](https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) およびAEM開発プロセスに精通していること。

- [AEM プロジェクト構造 ](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) およびCloud Managerを使用してカスタムコンテンツパッケージをデプロイする方法を理解します。

## `commerce-assets` パッケージのインストール

1. 必要に応じて、Cloud Managerから、AEM Assets プロジェクトの実稼動環境とステージング環境を作成します。

1. 必要に応じて、デプロイメントパイプラインを設定します。

1. GitHub で、[Commerce - Assets AEM プロジェクト ](https://github.com/ankumalh/assets-commerce) からボイラープレートコードをダウンロードします。

1. [ ローカル AEM開発環境 ](https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) から、カスタムコードをAEM Assets環境設定に Maven パッケージとしてインストールするか、既存のプロジェクト設定に手動でコードをコピーします。

1. 変更をコミットし、ローカル開発ブランチをCloud Manager Git リポジトリにプッシュします。

1. Cloud Managerから [ コードをデプロイしてAEM環境を更新します ](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager)。

## メタデータプロファイルの設定

AEM Assets オーサー環境で、メタデータプロファイルを作成して、Commerce アセットメタデータのデフォルト値を設定します。 次に、新しいプロファイルをAEM Asset フォルダーに適用すると、これらのデフォルトが自動的に使用されます。 この設定により、手動の手順が減ることでアセット処理が合理化されます。

メタデータプロファイルを設定する場合、次のコンポーネントを設定するだけで済みます。

- 「Commerce」タブを追加します。 このタブでは、テンプレートによって追加されたCommerce固有の設定を有効にします
- 「`Eligible for Commerce`」フィールドを「Commerce」タブに追加します。

テンプレートに基づいて、製品データ UI コンポーネントが自動的に追加されます。

### メタデータプロファイルの設定

1. Adobe Experience Manager オーサー環境にログインします。

1. Adobe Experience Manager Workspace から、Adobe Experience Manager アイコンをクリックして、AEM Assetsのオーサーコンテンツ管理ワークスペースに移動します。

   ![AEM Assetsの作成 ](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. ハンマーアイコンを選択して、管理者ツールを開きます。

   ![AEM オーサー管理者によるメタデータプロファイルの管理 ](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Metadata Profiles]**」をクリックして、プロファイル設定ページを開きます。

1. Commerce統合用のメタデータプロファイルを **[!UICONTROL Create]** 定します。

   ![AEM オーサー管理者によるメタデータプロファイルの追加 ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Commerce メタデータ用のタブを追加します。

   1. 左側で、「**[!UICONTROL Settings]**」をクリックします。

   1. タブ セクションの [**[!UICONTROL +]**] をクリックし、**[!UICONTROL Tab Name]**、`Commerce` を指定します。

1. `Eligible for Commerce` フィールドをフォームに追加します。

   ![AEM オーサー管理者のプロファイルにメタデータフィールドを追加 ](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

   - 「**[!UICONTROL Build form]**」をクリックします。

   - 「`Single Line text`」フィールドをフォームにドラッグします。

   - 「」をクリックして、ラベルの `Eligible for Commerce` のテキストを追加 **[!UICONTROL Field Label]** ます。

   - 「設定」タブで、ラベルテキストを **フィールドラベル** に追加します。

   - プレースホルダーテキストを `yes` に設定します。

   - **[!UICONTROL Map to Property]** フィールドで、次の値をコピーして貼り付けます

     ```terminal
     ./jcr:content/metadata/commerce:isCommerce
     ```

1. オプション。 承認済みのCommerce アセットをAEM Assets環境にアップロードする際に自動的に同期させるには、「`Basic`」タブの「_[!UICONTROL Review Status]_」フィールドのデフォルト値を `approved` に設定します。

1. 更新を保存します。

#### メタデータプロファイルのCommerce assets ソースフォルダーへの適用

1. [!UICONTROL &#x200B; Metadata Profiles] ページで、「Commerce統合」プロファイルを選択します。

1. アクションメニューから「**[!UICONTROL Apply Metadata Profiles to Folders]**」を選択します。

1. Commerce アセットを含むフォルダーを選択します。

   Commerce フォルダーが存在しない場合は作成します。

1. 「**[!UICONTROL Apply]**」をクリックします。

## 次の手順

[Adobe Commerce パッケージのインストール](aem-assets-configure-commerce.md)
