---
title: Commerce アカウントの転送
description: Commerce アカウントを別の所有者またはメールアドレスに転送する方法について説明します。
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 89637c8f2c4ff725499c27ebe0feb91bf3f9a0ef
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# Commerce アカウントの転送

業務上の責任が変わると、既存のCommerce アカウントの所有権を新しい所有者または別のメールアドレスに転送する必要が生じる場合があります。 この転送では、アカウントに関連付けられたプライマリユーザーのメールを変更する必要があります。

次に、Commerce（MAGEID）アカウントを転送するプロセスについて説明します。 クラウドアカウント（クラウドプロジェクトまたはNew Relic）の所有権の変更は含まれません。 Commerce クラウドプロジェクトのアクセスについて詳しくは、_Cloud Infrastructure ガイドの [ ユーザーアクセスの管理 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) を参照してください_

## 転送タイプの識別

この移行の完了方法は、次のどのシナリオでアカウントの現在の所有者および新しい所有者（E メール アドレス）がアカウントを移行する状況を説明しているかによって異なります。

| 転送タイプ | 現在の所有者 | 新しい所有者 |
| ------------- | ------------- | --------- |
| [ 新しいAdobe IDとメールの変更 ](#new-adobe-id-and-email-change) | Adobeのログインアカウントを使用して **_接続されていない_** MAGEID を持っている。 | MAGEID を持たず、Adobeログインアカウントに接続されていません。 |
| [ メールの変更 ](#email-change) | 他のAdobe商品やサービスが関連付けられていないAdobeログインアカウントを持つ **_接続_** された MAGEID を持っています。 | MAGEID を持たず、Adobeログインアカウントに接続されていません。 |
| [Adobe IDスイッチ ](#adobe-id-account-switch) | 他のAdobe商品やサービスが関連付けられていないAdobeログインアカウントを持つ **_接続_** された MAGEID を持っています。 | MAGEID を持ち、他のAdobe商品/サービスが関連付けられていないAdobeログインアカウントに接続されている。 |

{style="table-layout:auto"}

>[!NOTE]
>
>Adobe Commerceは他のAdobeソリューションとの統合を続けるため、Commerce アカウント（MAGEID）にはAdobeログインとの関連付けが必要になりました。 このAdobe IDは、Commerce アカウントに接続されているのと同じメールアドレスを使用します。

## 新しいAdobe IDとメールの変更

>[!IMPORTANT]
>
>[ 転送タイプ ](#identify-your-transfer-type) をレビューし、この一連の手順の前提条件を満たしていることを確認します。

この転送タイプでは、関連するAdobe IDを作成してから、そのアカウントを新しいオーナーのメールアドレスに変更する必要があります。

1. [Commerce アカウント ](https://account.magento.com/customer/account/login/) に移動します。

1. 「**[!UICONTROL Sign in with Adobe ID]**」をクリックします。

1. 「**[!UICONTROL Create an account]**」をクリックします。

1. 現在の所有者のメールアドレスとパスワードを入力します。

1. 「**[!UICONTROL Continue]**」をクリックします。

   これにより、Adobe IDが作成され、現在のCommerce アカウント（MAGEID）にリンクされます。 このアカウントリンクを使用すると、_[!UICONTROL Email]_フィールドはすべての変更からブロックされます。 関連付けられているメールアドレスは、Adobe ID アカウントで管理されます。

1. [account.adobe.com](https://account.adobe.com/) に移動します。

1. 「**[!UICONTROL Change Email]**」をクリックします。

1. 新しい所有者のメールアドレスを入力します。

1. 「**[!UICONTROL Change]**」をクリックします。

   これにより、新しいメールアドレスに送信される確認メールが生成されます。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しいメールアドレスに送信された確認コードを入力します。

1. 「**[!UICONTROL Verify]**」をクリックします。

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## メールの変更

>[!IMPORTANT]
>
>[ 転送タイプ ](#identify-your-transfer-type) をレビューし、この一連の手順の前提条件を満たしていることを確認します。

1. [account.adobe.com](https://account.adobe.com/) に移動し、Adobeログインを完了します。

1. アカウント名とアバターの下で、「**[!UICONTROL Change Email]**」をクリックします。

1. ダイアログで、新しい所有者のメールアドレスを入力します。

1. 「**[!UICONTROL Change]**」をクリックします。

   これにより、新しいメールアドレスに送信される確認メールが生成されます。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しいメールアドレスに送信された確認コードを入力します。

1. 「**[!UICONTROL Verify]**」をクリックします。

## Adobe ID アカウント切り替え

>[!IMPORTANT]
>
>[ 転送タイプ ](#identify-your-transfer-type) をレビューし、この一連の手順の前提条件を満たしていることを確認します。

現在のオーナーと新しいオーナーに既存のAdobeID がある場合、両方のアカウントは残りますが、メールアドレスを切り替える必要があります。 これには、有効でしかもAdobe IDに関連付けられていない _一時的_ メールアドレスを使用する必要があります。

### 一時アカウントへの変更

現在のオーナーは、これらの手順を完了して、Adobe IDを別の一時的なメールアドレスに関連付けます。

1. [account.adobe.com](https://account.adobe.com/) に移動し、Adobeログインを完了します。

1. アカウント名とアバターの下で、「**[!UICONTROL Change Email]**」をクリックします。

1. ダイアログで、Adobe IDで使用されない有効な一時メールアドレスを入力します。

   確認コードが記載されたメールを取得できるように、メールアドレスにアクセスできる必要があります。

1. 「**[!UICONTROL Change]**」をクリックします。

   これにより、一時的なメールアドレスに送信される確認メールが生成されます。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 一時メールアドレスに送信される確認コードを入力します。

1. 「**[!UICONTROL Verify]**」をクリックします。

1. Adobeアカウントからログアウトします。

### 新しい所有者手順

現在の所有者が一時的なメールアドレスへの転送を完了したら、次の手順を実行してアカウントを現在の所有者に変更します。

1. [account.adobe.com](https://account.adobe.com/) に移動し、Adobeログインを完了します。

1. アカウント名とアバターの下で、「**[!UICONTROL Change Email]**」をクリックします。

1. ダイアログで、現在の所有者の元のメールアドレスを入力します。

1. 「**[!UICONTROL Change]**」をクリックします。

   これにより、そのメールアドレスに送信される確認メールが生成されます。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 現在の所有者に送信された確認コードを入力します。

1. 「**[!UICONTROL Verify]**」をクリックします。

1. Adobeアカウントからログアウトします。

### フォローアップ手順

新しいオーナーがAdobeアカウントを現在の（現在は以前の）オーナーに正常に転送した後、次の手順を実行してオーナーを転送します。

1. [account.adobe.com](https://account.adobe.com/) （一連の手順で使用した最初のアカウント）に移動し、Adobeへのログインを完了します。

   このログインでは、一時メールアドレスの使用が必要です。

1. アカウント名とアバターの下で、「**[!UICONTROL Change Email]**」をクリックします。

1. ダイアログで、新しい所有者のメールアドレスを入力します。

1. 「**[!UICONTROL Change]**」をクリックします。

   これにより、そのメールアドレスに送信される確認メールが生成されます。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しい所有者に送信される確認コードを入力します。

1. 「**[!UICONTROL Verify]**」をクリックします。

>[!IMPORTANT]
>
>サポートリクエストを送信して、アカウント所有者のメールアドレスが更新されたことをサポートチームに通知します。 更新を完了するには、[Commerce Marketplace](https://commercemarketplace.adobe.com/) プロファイルのメールアドレスの更新など、さらに手順を実行する必要があります。 リクエストには、以前のアカウント所有者のメールアドレスを含めます。
