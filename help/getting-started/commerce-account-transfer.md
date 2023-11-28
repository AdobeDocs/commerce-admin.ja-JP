---
title: コマースアカウントの転送
description: コマースアカウントを別の所有者または電子メールアドレスに転送する方法を説明します。
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: dd8ccda17b0ef83cb4b0ce130fdc9315026733b1
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 1%

---

# コマースアカウントの転送

ビジネス上の責任が変わると、既存の Commerce アカウントの所有権を新しい所有者または別の電子メールアドレスに転送する必要が生じる場合があります。 この転送では、アカウントに関連付けられたプライマリユーザー E メールを変更する必要があります。

次に、コマース (MAGEID) アカウントを転送するプロセスを説明します。 クラウドアカウント（クラウドプロジェクト）の所有権に関する変更は含まれません。 クラウドプロジェクトへのアクセスについて詳しくは、 [ユーザーアクセスを管理](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) （内） _Commerce on Cloud Infrastructure ガイド_.

## 転送タイプを特定します。

この転送を完了する方法は、アカウントの現在の所有者と、アカウントの転送先の新しい所有者（電子メールアドレス）の状況を次のどちらのシナリオで示すかによって異なります。

| 転送タイプ | 現在の所有者 | 新しい所有者 |
| ------------- | ------------- | --------- |
| [新しいAdobe IDと E メールの変更](#new-adobe-id-and-email-change) | 次の MAGEID を持つ： **_未接続_** にログインAdobeを設定します。 | MAGEID がなく、Adobeログインアカウントに接続されていません。 |
| [メールの変更](#email-change) | 次の MAGEID を持つ： **_接続済み_** にログインし、他のAdobe製品/サービスが関連付けられていないAdobeログインアカウントを設定する。 | MAGEID がなく、Adobeログインアカウントに接続されていません。 |
| [Adobe IDスイッチ](#adobe-id-account-switch) | 次の MAGEID を持つ： **_接続済み_** にログインし、他のAdobe製品/サービスが関連付けられていないAdobeログインアカウントを設定する。 | MAGEID を持ち、他のAdobe製品/サービスが関連付けられていないAdobeログインアカウントに接続されている。 |

{style="table-layout:auto"}

>[!NOTE]
>
>Adobe Commerceは他のAdobeソリューションと引き続き統合されるので、コマースアカウント (MAGEID) にはログインとの関連付けが必要になりました。 このAdobe IDは、お使いのコマースアカウントに接続されているのと同じ電子メールアドレスを使用します。

>[!NOTE]
>
>現在または新規の所有者が、他のAdobeの製品/サービスに関連付けられたAdobeログインアカウントを持っている場合、 [サポートチケット](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) コマースアカウントを別のAdobe IDに移行する際のサポートが必要です。

## 新しいAdobe IDと E メールの変更

>[!IMPORTANT]
>
>以下を確認します。 [転送タイプ](#identify-your-transfer-type) をクリックし、この一連の手順の前提条件を満たしていることを確認します。

この転送タイプでは、まず関連するAdobe IDを作成し、そのアカウントを新しい所有者の電子メールアドレスに変更する必要があります。

1. 次の場所に移動します。 [コマースアカウント](https://account.magento.com/customer/account/login/).

1. クリック **[!UICONTROL Sign in with Adobe ID]**.

1. クリック **[!UICONTROL Create an account]**.

1. 現在の所有者の電子メールアドレスとパスワードを入力します。

1. クリック **[!UICONTROL Continue]**.

   これにより、Adobe IDが作成され、現在の Commerce アカウント (MAGEID) にリンクされます。 このアカウントリンクを使用すると、 _[!UICONTROL Email]_フィールドは変更からブロックされています。 関連する電子メールアドレスは、Adobe IDアカウントで管理されます。

1. に移動します。 [account.adobe.com](https://account.adobe.com/).

1. クリック **[!UICONTROL Change Email]**.

1. 新しい所有者の電子メールアドレスを入力します。

1. クリック **[!UICONTROL Change]**.

   これにより、新しい E メールアドレスに送信された検証 E メールが生成されます。 電子メールには、電子メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しい電子メールアドレスに送信する確認コードを入力します。

1. クリック **[!UICONTROL Verify]**.

## メールの変更

>[!IMPORTANT]
>
>以下を確認します。 [転送タイプ](#identify-your-transfer-type) をクリックし、この一連の手順の前提条件を満たしていることを確認します。

1. に移動します。 [account.adobe.com](https://account.adobe.com/) をクリックし、Adobeログインを完了します。

1. アカウント名とアバターで、「 **[!UICONTROL Change Email]**.

1. ダイアログで、新しい所有者の電子メールアドレスを入力します。

1. クリック **[!UICONTROL Change]**.

   これにより、新しい E メールアドレスに送信された検証 E メールが生成されます。 電子メールには、電子メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しい電子メールアドレスに送信する確認コードを入力します。

1. クリック **[!UICONTROL Verify]**.

## Adobe IDアカウントの切り替え

>[!IMPORTANT]
>
>以下を確認します。 [転送タイプ](#identify-your-transfer-type) をクリックし、この一連の手順の前提条件を満たしていることを確認します。

現在の所有者と新しい所有者に既存のAdobeID がある場合、両方のアカウントを残す必要がありますが、電子メールアドレスを切り替える必要があります。 これには、 _一時的_ 有効で、とAdobe IDに関連付けられていない電子メールアドレス。

### 一時的なアカウントに変更

現在の所有者は、Adobe IDを別の一時的な電子メールアドレスに関連付けるために、これらの手順を完了します。

1. に移動します。 [account.adobe.com](https://account.adobe.com/) をクリックし、Adobeログインを完了します。

1. アカウント名とアバターで、「 **[!UICONTROL Change Email]**.

1. ダイアログで、Adobe IDで使用されていない有効な一時的な E メールアドレスを入力します。

   確認コードで E メールを取得できるように、E メールアドレスへのアクセス権が必要です。

1. クリック **[!UICONTROL Change]**.

   これにより、一時的な E メールアドレスに送信された検証 E メールが生成されます。 電子メールには、電子メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 一時的な E メールアドレスに送信する確認コードを入力します。

1. クリック **[!UICONTROL Verify]**.

1. Adobe・アカウントからログアウト

### 新しい所有者の手順

現在の所有者が一時的な E メールアドレスへの転送を完了したら、次の手順を実行して、アカウントを現在の所有者に変更します。

1. に移動します。 [account.adobe.com](https://account.adobe.com/) をクリックし、Adobeログインを完了します。

1. アカウント名とアバターで、「 **[!UICONTROL Change Email]**.

1. ダイアログで、現在の所有者の元の電子メールアドレスを入力します。

1. クリック **[!UICONTROL Change]**.

   これにより、その電子メールアドレスに送信された検証用電子メールが生成されます。 電子メールには、電子メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 現在の所有者に送信される確認コードを入力します。

1. クリック **[!UICONTROL Verify]**.

1. Adobe・アカウントからログアウト

### 手順に従います

新しい所有者がAdobeアカウントを現在の（現在の）所有者に正常に転送した後、所有権を転送するには、以下の手順を実行します。

1. に移動します。 [account.adobe.com](https://account.adobe.com/) （一連の手順で使用する最初のアカウント）を選択し、Adobeログインを完了します。

   このログインには、一時的な E メールアドレスを使用する必要があります。

1. アカウント名とアバターで、 **[!UICONTROL Change Email]**.

1. ダイアログで、新しい所有者の電子メールアドレスを入力します。

1. クリック **[!UICONTROL Change]**.

   これにより、その電子メールアドレスに送信された検証用電子メールが生成されます。 電子メールには、電子メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しい所有者に送信する確認コードを入力します。

1. クリック **[!UICONTROL Verify]**.

1. **サポートリクエストを送信** アカウント所有者の電子メールアドレスを更新したことをサポートチームに知らせるため。

サポートが実行する必要のある追加の手順は、 [Commerce Marketplace](https://commercemarketplace.adobe.com/) プロファイル。
