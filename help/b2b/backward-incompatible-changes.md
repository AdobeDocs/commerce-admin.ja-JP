---
title: Adobe Commerce B2B に後方互換性のない変更
description: カスタムコードの更新が必要になる可能性のあるAdobe Commerce B2B リリースの変更点について説明します。
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Adobe Commerce B2B に後方互換性のない変更

Adobe Commerce リリース向け B2B における後方互換性のないすべての変更点について、概要を参照してください。 大きな影響があり、詳細な説明と特別な手順が必要な、互換性のない変更については、ハイライトの節を参照してください。

## ハイライト

### 1.4.2 ～ 1.5.0

複数会社の割り当てを追加すると、会社のユーザーアカウントに複数の `company_id` 値を設定できるようになりました。 `Magento\Company\Api\Data\CompanyCustomerInterface` は、ユーザーのデフォルト `company_id` を設定するように更新されました。 デフォルトでは、会社のユーザーアカウントに最初に割り当てられた会社が設定されます。

以前のリリースからアップグレードする場合、Adobeでは `Magento\Company\Api\Data\CompanyCustomerInterface` を使用するクラスに次のメソッドを実装することをお勧めします。

- Magento\Company\Api\Data\CompanyCustomerInterface::getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface::setIsDefault

## 参照

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
