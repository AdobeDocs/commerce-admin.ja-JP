---
title: CommerceのExperience Manager Assets統合
description: Experience Manager Assetsをインスタンスと統合して  [!DNL Commerce]  ストアで使用する無数のメディアアセットにアクセスする方法を説明します。
feature: CMS, Media, Configuration, Integration
source-git-commit: fafe8d46931cc00e58d0888639fd8e739a170f8a
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# CommerceのExperience Manager Assets統合

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

CommerceとAdobe Experience Manager（AEM）Assetsの統合は、AEM as a Digital Asset Management （DAM）システムの堅牢な機能とAdobe Commerceを組み合わせて、e コマースエクスペリエンスを強化します。 この統合では、AEMの強力なアセット管理機能を活用して、コマースストアフロント全体でアセットを管理および配信するための、シームレスでスケーラブルかつ効率的な方法を提供します。

**主な特長**

- **一元的なアセット管理**

   - **AEM Assets as a Single Source of Truth**-AEM Assetsは、すべてのデジタルアセットの中央リポジトリとして機能し、すべての e コマースプラットフォームがオンブランドの承認済みアセットにアクセスできるようにします。

   - **一括アセット管理** AEMの堅牢なアセット管理機能により、組織は大量のアセットを効率的に管理できます。 これにより、マーケターとマーチャンダイザーは、新しい製品ライン用に大量の画像セットを効率的にマッピングできます。

- **パーソナライズされたCommerce エクスペリエンス** - AEMの GenAI サービスを使用すると、パーソナライズされた e コマースエクスペリエンスに対して何百万種類もの製品バリエーションを生成できます。 マーケターやマーチャンダイザーは、これらの画像を使用して、製品のローンチや季節的なキャンペーンのための動的なストアフロントを作成し、エンゲージメントを強化し、コンバージョン率を高めることができます。

- **自動アセットマッチング** – この統合には、SKU またはその他の主要な属性に基づいてAEM内のアセットをAdobe Commerce内の製品に自動的に照合するルールエンジンサービスが含まれています。 このサービスにより、最新の製品アセットとバリエーションが、e コマースストアフロントで常に利用できるようになります。 また、アセットの管理に必要な手動の手間を軽減し、より戦略的なアクティビティに時間を解放します。

- **事務の合理化**
   - **Commerce管理から統合を有効にして設定します** – 管理者と開発者は、使い慣れたツールとプロセスを使用して、Adobe Commerceから統合をインストールして設定できます。
   - **動的な更新** – アセット管理システムの最新の変更に合わせて製品画像を最新の状態に保ちます。 これらの自動更新により、コマースストアフロントに常に最新の製品情報が保持されるようになります。
   - **効率的なカタログ管理** - アセットのクリーンアップと更新を自動化することで、製品カタログのメンテナンスを簡素化します。

## 統合を有効にすると変更される内容

製品リスト – 新しいフィールド [!UICONTROL Remote Media URL]

商品詳細ページ - AEM DAM から取得されるアセットが表示される以外、変更はありません


## CommerceとExperience Manager Assetsの統合

>[!BEGINSHADEBOX]

**前提条件**

- Adobe Commerceは、割り当てられた組織 ID を持つ ](/help/getting-started/adobe-ims-config.md)0}Commerce管理者とAdobe IDの統合で設定される必要があります。[
- Experience Manager Assetsは、同じ組織 ID に商品として割り当てられている必要があります。
- 統合を設定するユーザーには、Adobe CommerceおよびExperience Manager Assetsにアクセスするための管理者権限を持つ、同じ組織のアカウントが必要です。

>[!ENDSHADEBOX]


CommerceとExperience Manager Assetsの統合を有効にするには、次の 3 つの手順を実行します。

1. [Experience Manager Assets プロジェクトを設定してCommerce アセットを管理します ](aem-assets-configure-aem.md)。

1. [Experience Manager Assets Integration 拡張機能のインストールとAdobe Commerceの設定](aem-assets-configure-aem.md)

1. [同期サービスの設定](aem-assets-setup-synchronization.md)

