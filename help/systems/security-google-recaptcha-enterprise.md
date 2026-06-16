---
title: Google reCAPTCHA Enterprise
description: ボットや不正なアクティビティからAdobe Commerce as a Cloud Service ストアフロントを保護するようにGoogle reCAPTCHA Enterpriseを設定する方法について説明します。
role: Admin
feature: Configuration, Security
badgeSaas: label="SaaSのみ" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service プロジェクト（Adobeで管理されるSaaS インフラストラクチャ）にのみ適用されます。"
exl-id: 2c88488c-8ff1-41db-b81b-89ad164e134d
TQID: https://experienceleague.adobe.com/oMZleuJsp2QiDD7IsMDV647LWKm938lNvY4--o6G3c8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eb30f47f-d87a-400f-8f78-63ce7979ff56id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform)は、アダプティブリスク分析とマシンラーニングを使用して人間のユーザーとボットを区別することで、Adobe Commerce as a Cloud Service ストアフロントに高度なボット保護を提供します。 これにより、サイトでの不正行為、スパム、悪用を回避できます。

>[!NOTE]
>
>この機能は、管理者に対するreCAPTCHA サポートを提供しません。

[reCAPTCHA統合](https://experienceleague.adobe.com/developer/commerce/storefront/dropins/user-auth/recaptcha/)では、reCAPTCHA Enterpriseのサポートをストアフロントに追加する方法について説明します。

Google reCAPTCHAの他のバージョンの設定について詳しくは、[Google reCAPTCHA V3およびV2](security-google-recaptcha.md)を参照してください。

## 機能

Google reCAPTCHA Enterpriseには、次の機能が含まれています。

- **高度なボット検出**:Google Cloudのマシンラーニングモデルを使用して、優れたボット検出を実現
- **リスクスコア分析**：各インタラクションの詳細なリスクスコア（0.0 ～ 1.0）を提供します
- **設定可能なしきい値**: テナントごとに許容可能な最小リスクスコアを設定します
- **マルチテナントサポート**：分離されたGoogle Cloud プロジェクトを使用したテナントごとの設定
- **暗号化された資格情報**: データベースに暗号化されて保存されたサービス アカウントの資格情報
- **フォーム保護**: ログイン、チェックアウト、商品レビューなど、すべての標準Commerce フォームを保護します。

## 前提条件

Adobe Commerce as a Cloud Service ストアフロント用にGoogle reCAPTCHA Enterpriseを設定するには、次のリソースが必要です。

- reCAPTCHA Enterpriseが有効になっているアクティブなGoogle Cloud アカウント。
- Google Cloud Consoleにアクセスして、reCAPTCHA Enterprise キーを作成および管理します。

マルチテナント Adobe Commerce as a Cloud Serviceのインストールでは、各テナントに独自のGoogle Cloud プロジェクトとreCAPTCHA Enterprise キーが必要です。

## 手順1:Google reCAPTCHA Enterpriseの設定

次の一般的な手順に従って、ストアフロントにGoogle reCAPTCHA Enterpriseを設定します。 詳細な手順については、[Google reCAPTCHA Enterprise ドキュメント ](https://docs.cloud.google.com/recaptcha/docs/overview)を参照してください。

1. reCAPTCHA Enterprise実装用に[Google Cloud プロジェクト ](https://developers.google.com/workspace/guides/create-project)を作成します。

1. [reCAPTCHA Enterprise API](https://docs.cloud.google.com/recaptcha/docs/prepare-environment)を有効にします。

1. スコアベースのreCAPTCHA Enterprise [ サイトキー](https://docs.cloud.google.com/recaptcha/docs/choose-key-type)を作成します。

1. `roles/recaptchaenterprise.admin` IAMの役割を持つサービス アカウントを作成します。

1. サービスアカウント JSON キーファイルをダウンロードします。このファイルには、Adobe Commerce as a Cloud Service ストアフロントとGoogle reCAPTCHA Enterpriseの認証に必要な資格情報が含まれています。

## 手順2：ストアフロント用にGoogle reCAPTCHAを設定する

1. Adobe Commerce _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL Security]_を展開し、**[!UICONTROL Google reCAPTCHA Storefront]**を選択します。

1. **[!UICONTROL reCAPTCHA Enterprise]** セクションまで下にスクロールし、次のように設定を完了します。

   - **[!UICONTROL Site Key]**&#x200B;の場合は、Google Cloud ConsoleからreCAPTCHA Enterprise サイトキーをコピーして貼り付けます。

   - **[!UICONTROL Google Cloud Project ID]**&#x200B;の場合は、Google Cloud プロジェクトからプロジェクト IDをコピーして貼り付けます。

   - **[!UICONTROL Service Account JSON]**&#x200B;の場合、[でダウンロードしたサービスアカウント JSON キーファイルの内容をコピーします。手順1: Google reCAPTCHA Enterpriseの設定](#step-1-set-up-google-recaptcha-enterprise)。

   - **[!UICONTROL Minimum Score Threshold]**&#x200B;について、ユーザーとのやり取りが潜在的なリスクとしてフラグ付けされるタイミングを特定するために、最小スコア（0.0 ～ 1.0）を入力します。 スコアが1.0は一般的なユーザーインタラクション、0.0はボットである可能性が高いです。

   - **[!UICONTROL Badge Position]**&#x200B;で、各ページの非表示のreCAPTCHA バッジの位置を選択します。 オプション：`Inline` / `Bottom Right` / `Bottom Left`。

   - **[!UICONTROL Theme]**&#x200B;で、`Light Theme` （デフォルト）または`Dark Theme`のいずれかを選択して、Google reCAPTCHA ボックスのスタイルを決定します。

   - **[!UICONTROL Language Code]**&#x200B;の場合、Google reCAPTCHA テキストとメッセージに使用する言語を指定する[2文字コード ](https://developers.google.com/recaptcha/docs/language)を入力します。

   - **[!UICONTROL Validation Failure Message]**&#x200B;の場合、検証が成功しない場合にストアフロントに表示されるメッセージをオプションで変更します。


1. **[!UICONTROL Storefront]** セクションを展開し、保護する各ストアフロントフォームを&#x200B;**[!UICONTROL reCAPTCHA Enterprise]**&#x200B;に設定します。

   {{recaptcha-forms-list}}

   ![ ストアフロントオプション設定](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 手順3：設定の保存

1. 設定が完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

1. ワークスペースの上部にあるメッセージで「**[!UICONTROL Cache Management]**」をクリックし、無効なキャッシュを1つずつ更新します。
