---
title: Google reCAPTCHA Enterprise
description: Google reCAPTCHA Enterprise を設定して、Adobe Commerce as a Cloud Service ストアフロントをボットや不正アクティビティから保護する方法を説明します。
role: Admin
feature: Configuration, Security
source-git-commit: 5181e6dcbffdca87dd6c376c36f7c9d0a3fbc015
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) は、適応型リスク分析と機械学習を使用して人間のユーザーとボットを区別することにより、Adobe Commerce as a Cloud Service ストアフロントの高度なボット保護機能を提供します。 これは、サイトでの不正なアクティビティ、スパム、および不正使用を防ぐのに役立ちます。

>[!NOTE]
>
>この機能は、管理者の reCAPTCHA サポートを提供するものではありません。

Google reCAPTCHA の他のバージョンの設定について詳しくは、&lbrace;0[Google reCAPTCHA V3 および V2 を参照してください。](security-google-recaptcha.md)

## 機能

Google reCAPTCHA Enterprise には、以下の機能があります。

- **高度なボット検出**:Google Cloud の機械学習モデルを使用して、優れたボット検出を行います
- **リスクスコア分析**：各インタラクションの詳細なリスクスコア（0.0～1.0）を提供します
- **設定可能なしきい値**：テナントごとの最小許容リスクスコアを設定します
- **マルチテナントのサポート**：分離されたGoogle Cloud プロジェクトを使用した、テナントごとの設定
- **暗号化された資格情報**: データベースに暗号化されて保存されたサービスアカウントの資格情報
- **フォームの保護**：ログイン、チェックアウト、商品レビューなど、標準のCommerce フォームをすべて保護します。

## 前提条件

Adobe Commerce as a Cloud Service ストアフロントにGoogle reCAPTCHA Enterprise を設定するには、次のリソースが必要です。

- reCAPTCHA Enterprise が有効になっている、アクティブなGoogle Cloud アカウント。
- reCAPTCHA エンタープライズキーを作成および管理するためのGoogle Cloud Console にアクセスします。

マルチテナントのAdobe Commerce as a Cloud Service インストールでは、各テナントに独自のGoogle Cloud プロジェクトと reCAPTCHA Enterprise キーが必要です。

## 手順 1:Google reCAPTCHA Enterprise の設定

次の一般的な手順に従って、ストアフロントにGoogle reCAPTCHA Enterprise を設定します。 手順について詳しくは、[Google reCAPTCHA Enterprise ドキュメント &#x200B;](https://docs.cloud.google.com/recaptcha/docs/overview) を参照してください。

1. reCAPTCHA Enterprise 実装用の [Google クラウドプロジェクトを作成 &#x200B;](https://developers.google.com/workspace/guides/create-project) します。

1. [reCAPTCHA Enterprise API](https://docs.cloud.google.com/recaptcha/docs/prepare-environment) を有効にします。

1. スコアベースの reCAPTCHA Enterprise[&#x200B; サイトキー &#x200B;](https://docs.cloud.google.com/recaptcha/docs/choose-key-type) を作成します。

1. `roles/recaptchaenterprise.admin` の IAM 役割を持つサービス アカウントを作成します。

1. サービスアカウント JSON キーファイルをダウンロードします。このファイルには、Google reCAPTCHA Enterprise でAdobe Commerce as a Cloud Service ストアフロントを認証するために必要な資格情報が含まれています。

## 手順 2：ストアフロントのGoogle reCAPTCHA を設定する

1. _[!UICONTROL Security]_&#x200B;の下の左パネルで、「**[!UICONTROL Google reCAPTCHA Storefront]**」を選択します。

1. **[!UICONTROL reCAPTCHA Enterprise]** の節を次のように完了します。

   - **[!UICONTROL Site Key]** しくは、reCAPTCHA Enterprise サイトキーをGoogle Cloud コンソールからコピー&amp;ペーストします。

   - **[!UICONTROL Google Cloud Project ID]** しくは、プロジェクト ID をGoogle Cloud プロジェクトからコピー&amp;ペーストします。

   - **[!UICONTROL Service Account JSON]** しくは、[&#x200B; 手順 1:Google reCAPTCHA Enterprise の設定 &#x200B;](#step-1-set-up-google-recaptcha-enterprise) でダウンロードしたサービスアカウント JSON キーファイルの内容をコピーします。

   - **[!UICONTROL Minimum Score Threshold]**：最小スコア（0.0～1.0）を入力すると、ユーザーインタラクションが潜在的なリスクとしてフラグ付けされるタイミングを識別できます。ここで、1.0 は一般的なユーザーインタラクションで、0.0 はボットである可能性があります。

   - **[!UICONTROL Badge Position]** しくは、各ページの非表示の reCAPTCHA バッジの位置を選択します。 オプション：`Inline`/`Bottom Right`/`Bottom Left`。

   - **[!UICONTROL Theme]** しくは、`Light Theme` （デフォルト）または `Dark Theme` を選択して、Google reCAPTCHA ボックスのスタイルを決定します。

   - **[!UICONTROL Language Code]** しくは、Google reCAPTCHA テキストおよびメッセージングで使用する言語を指定する [2 文字のコード &#x200B;](https://developers.google.com/recaptcha/docs/language) を入力します。

   - **[!UICONTROL Validation Failure Message]**：検証に失敗した場合にストアフロントに表示されるメッセージをオプションで変更できます。


1. **[!UICONTROL Storefront]** セクションを展開し、保護する各ストアフロントフォームを **[!UICONTROL reCAPTCHA Enterprise]** に設定します。

   {{recaptcha-forms-list}}

   ![&#x200B; ストアフロントオプションの設定 &#x200B;](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 手順 3：設定を保存する

1. 設定が完了したら、「**[!UICONTROL Save Config]**」をクリックします。

1. ワークスペースの上部にあるメッセージで、「**[!UICONTROL Cache Management]**」をクリックし、無効な各キャッシュを更新します。
