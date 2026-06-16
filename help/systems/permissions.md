---
title: 管理者権限
description: 管理者ユーザーアカウントと、ストア管理機能へのアクセス権を付与するために役割を使用する方法について説明します。
exl-id: 54e4a322-4747-4472-b60b-cfe84c109f86
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
TQID: https://experienceleague.adobe.com/7xyouYohAbOKbwVCxZPamD-7gEiqGrqEAAg9FDm8z-U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# 管理者権限

Adobe CommerceとMagento Open Sourceでは、ロールと権限を使用して、管理者に対する様々なレベルのアクセス権を設定します。 ストアを最初に設定すると、完全な権限を持つ管理者ロールの一連のログイン資格情報が届きます。 ただし、サイトで作業する他のユーザーの「知る必要がある」基準で、権限のレベルを制限できます。 たとえば、デザインチームのメンバーには、コンテンツデザインツールのみにアクセス権を与え、顧客や注文情報のある領域にはアクセス権を与えることはできません。

さらに、特定のサイトまたは一連のサイトとその関連データに対する管理者アクセスのみを制限できます。 同じCommerce インストールに複数のブランドまたは事業部が別々のストアを持つ場合は、各事業部に管理者アクセス権を付与しながら、他の管理者ユーザーからデータを非表示にしたり保護したりできます。

管理者ユーザーのアクセスが特定のweb サイトまたはストアに制限されている場合、許可されていないサイトは表示されないか、グレー表示になります。 許可されたweb サイトおよびストアの販売およびその他のデータのみがユーザーに表示されます。

- ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）デフォルトでは、ユーザーがストアに変更を適用したときに実行したすべてのアクションが自動的に記録（記録）されます。 管理者アクションは、[&#x200B; アクションログレポート &#x200B;](action-log-report.md)で確認できます。 ストアの高度な管理者設定で[管理者アクション ログ &#x200B;](action-log.md)へのログインを設定します。

![管理者 – すべてのユーザーアカウント &#x200B;](./assets/users-all.png){width="700" zoomable="yes"}
