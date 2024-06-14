---
title: Commerce アカウントの転送
description: Commerce アカウントを別の所有者またはメールアドレスに転送する方法について説明します。
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 59a88468dabfd1042b664f658225de2504b66b1b
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 0%

---

# Commerce アカウントの転送

業務上の責任が変わると、既存のCommerce アカウントの所有権を新しい所有者または別のメールアドレスに転送する必要が生じる場合があります。 この転送では、アカウントに関連付けられたプライマリユーザーのメールを変更する必要があります。

次に、Commerce（MAGEID）アカウントを転送するプロセスについて説明します。 クラウドアカウント（クラウドプロジェクトまたはNew Relic）の所有権の変更は含まれません。 クラウドプロジェクトへのアクセスについて詳しくは、 [ユーザーアクセスの管理](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) が含まれる _クラウドインフラストラクチャー上のCommerce ガイド_.

## 転送タイプの識別

この移行の完了方法は、次のどのシナリオでアカウントの現在の所有者および新しい所有者（E メール アドレス）がアカウントを移行する状況を説明しているかによって異なります。

| 転送タイプ | 現在の所有者 | 新しい所有者 |
| ------------- | ------------- | --------- |
| [新しいAdobe IDとメールの変更](#new-adobe-id-and-email-change) | には、次のようなマギッドがあります **_未接続_** （Adobeログインアカウントを使用）。 | MAGEID を持たず、Adobeログインアカウントに接続されていません。 |
| [メールの変更](#email-change) | には、次のようなマギッドがあります **_接続_** その他のAdobe製品やサービスが関連付けられていないAdobeログインアカウント。 | MAGEID を持たず、Adobeログインアカウントに接続されていません。 |
| [Adobe IDスイッチ](#adobe-id-account-switch) | には、次のようなマギッドがあります **_接続_** その他のAdobe製品やサービスが関連付けられていないAdobeログインアカウント。 | MAGEID を持ち、他のAdobe商品/サービスが関連付けられていないAdobeログインアカウントに接続されている。 |

{style="table-layout:auto"}

>[!NOTE]
>
>Adobe Commerceは他のAdobeソリューションとの統合を続けるため、Commerce アカウント（MAGEID）にはAdobeログインとの関連付けが必要になりました。 このAdobe IDは、Commerce アカウントに接続されているのと同じメールアドレスを使用します。

>[!NOTE]
>
>現在のオーナーまたは新しいオーナーが、他のAdobe製品またはサービスに関連付けられているAdobeログインアカウントを持っている場合は、 [サポートチケット](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) Commerce アカウントを別のAdobe IDに転送する方法については、こちらを参照してください。

## 新しいAdobe IDとメールの変更

>[!IMPORTANT]
>
>をレビュー [転送タイプ](#identify-your-transfer-type) また、この一連の手順の前提条件を満たしていることを確認してください。

この転送タイプでは、関連するAdobe IDを作成してから、そのアカウントを新しいオーナーのメールアドレスに変更する必要があります。

1. に移動 [Commerce アカウント](https://account.magento.com/customer/account/login/).

1. クリック **[!UICONTROL Sign in with Adobe ID]**.

1. クリック **[!UICONTROL Create an account]**.

1. 現在の所有者のメールアドレスとパスワードを入力します。

1. クリック **[!UICONTROL Continue]**.

   これにより、Adobe IDが作成され、現在のCommerce アカウント（MAGEID）にリンクされます。 このアカウントリンクを使用すると、 _[!UICONTROL Email]_フィールドはすべての変更からブロックされます。 関連付けられているメールアドレスは、Adobe ID アカウントで管理されます。

1. に移動します。 [account.adobe.com](https://account.adobe.com/).

1. クリック **[!UICONTROL Change Email]**.

1. 新しい所有者のメールアドレスを入力します。

1. クリック **[!UICONTROL Change]**.

   これにより、新しいメールアドレスに送信される確認メールが生成されます。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しいメールアドレスに送信された確認コードを入力します。

1. クリック **[!UICONTROL Verify]**.

## メールの変更

>[!IMPORTANT]
>
>をレビュー [転送タイプ](#identify-your-transfer-type) また、この一連の手順の前提条件を満たしていることを確認してください。

1. に移動します。 [account.adobe.com](https://account.adobe.com/) Adobeログインを完了します。

1. アカウント名とアバターの下で、 **[!UICONTROL Change Email]**.

1. ダイアログで、新しい所有者のメールアドレスを入力します。

1. クリック **[!UICONTROL Change]**.

   これにより、新しいメールアドレスに送信される確認メールが生成されます。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しいメールアドレスに送信された確認コードを入力します。

1. クリック **[!UICONTROL Verify]**.

## Adobe ID アカウント切り替え

>[!IMPORTANT]
>
>をレビュー [転送タイプ](#identify-your-transfer-type) また、この一連の手順の前提条件を満たしていることを確認してください。

現在のオーナーと新しいオーナーに既存のAdobeID がある場合、両方のアカウントは残りますが、メールアドレスを切り替える必要があります。 これには、 _一時的_ 有効だが、およびAdobe IDに関連付けられていないメールアドレス。

### 一時アカウントへの変更

現在のオーナーは、これらの手順を完了して、Adobe IDを別の一時的なメールアドレスに関連付けます。

1. に移動します。 [account.adobe.com](https://account.adobe.com/) Adobeログインを完了します。

1. アカウント名とアバターの下で、 **[!UICONTROL Change Email]**.

1. ダイアログで、Adobe IDで使用されない有効な一時メールアドレスを入力します。

   確認コードが記載されたメールを取得できるように、メールアドレスにアクセスできる必要があります。

1. クリック **[!UICONTROL Change]**.

   これにより、一時的なメールアドレスに送信される確認メールが生成されます。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 一時メールアドレスに送信される確認コードを入力します。

1. クリック **[!UICONTROL Verify]**.

1. Adobeアカウントからログアウトします。

### 新しい所有者手順

現在の所有者が一時的なメールアドレスへの転送を完了したら、次の手順を実行してアカウントを現在の所有者に変更します。

1. に移動します。 [account.adobe.com](https://account.adobe.com/) Adobeログインを完了します。

1. アカウント名とアバターの下で、 **[!UICONTROL Change Email]**.

1. ダイアログで、現在の所有者の元のメールアドレスを入力します。

1. クリック **[!UICONTROL Change]**.

   これにより、そのメールアドレスに送信される確認メールが生成されます。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 現在の所有者に送信された確認コードを入力します。

1. クリック **[!UICONTROL Verify]**.

1. Adobeアカウントからログアウトします。

### フォローアップ手順

新しいオーナーがAdobeアカウントを現在の（現在は以前の）オーナーに正常に転送した後、次の手順を実行してオーナーを転送します。

1. に移動します。 [account.adobe.com](https://account.adobe.com/) （一連の手順で使用される最初のアカウント）を選択し、Adobeログインを完了します。

   このログインでは、一時メールアドレスの使用が必要です。

1. アカウント名とアバターの下で、 **[!UICONTROL Change Email]**.

1. ダイアログで、新しい所有者のメールアドレスを入力します。

1. クリック **[!UICONTROL Change]**.

   これにより、そのメールアドレスに送信される確認メールが生成されます。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しい所有者に送信される確認コードを入力します。

1. クリック **[!UICONTROL Verify]**.

1. **サポートリクエストを送信** アカウント所有者のメールアドレスを更新したことをサポートチームに通知します。

のメールアドレスの更新など、サポートで実行する追加手順があります [Commerce Marketplace](https://commercemarketplace.adobe.com/) プロファイル。
