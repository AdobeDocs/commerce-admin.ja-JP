---
title: Commerce アカウントの転送
description: Commerce アカウントを別の所有者またはメールアドレスに転送する方法について説明します。
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: e44ebfab5b9505098405b005051f110b689c3f4f
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 0%

---

# Commerce アカウントの転送

ビジネス上の責任が変わると、Commerce アカウントを新しい所有者または別のメールアドレスに転送する必要が生じる場合があります。 この転送では、アカウントに関連付けられたプライマリユーザーのメールを変更する必要があります。

次に、Commerce（MAGEID）アカウントを転送するプロセスについて説明します。 クラウドアカウント（クラウドプロジェクトまたはNew Relic）の所有権の変更は含まれません。 Commerce クラウドプロジェクトのアクセスについて詳しくは、_Cloud Infrastructure ガイドの [ ユーザーアクセスの管理 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) を参照してください_

>[!IMPORTANT]
>
>新しいアカウント所有者が共有アクセスを使用して拡張機能を購入した場合、アカウント転送プロセスが開始されるとすぐに、それらの拡張機能へのアクセス権が失われます。 アカウントの移行をリクエストする前に、新しい所有者が [ マーケットプレイスのアカウント ](https://commercemarketplace.adobe.com/sales/order/history/) から購入の注文 ID を取得し、[ マーケットプレイスのチーム ](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) からそれらの拡張機能の払い戻しをリクエストしていることを確認してください。 拡張機能の購入を別のアカウントに転送することはできません。

## 転送タイプの識別

Commerce アカウントの転送の種類は、現在のオーナーと新しいオーナーが使用できるCommerce アカウント資格情報によって異なります。 次のシナリオでは、これらの資格情報に基づく様々な転送タイプについて説明します。

| 転送タイプ | 現在の所有者 | 新しい所有者 |
| ------------- | ------------- | --------- |
| [ 新しいAdobe IDとメールの変更 ](#new-adobe-id-and-email-change) | Adobeのログインアカウントを持つ **_接続されていない_** MAGEID を持っている。 | MAGEID を持たず、Adobe ログインアカウントに接続していない。 |
| [ メールの変更 ](#email-change) | Adobeのログインアカウントで **_接続_** されている MAGEID を持っている。 | MAGEID を持たず、Adobe ログインアカウントに接続していない。 |
| [Adobe IDスイッチ ](#adobe-id-account-switch) | Adobeのログインアカウントで **_接続_** されている MAGEID を持っている。 | MAGEID を持ち、他のAdobe製品/サービスが関連付けられていないAdobe ログインアカウントに接続されている。 |

{style="table-layout:auto"}

>[!NOTE]
>
>Adobe Commerceは他のAdobe ソリューションとの統合を続けるため、Commerce アカウント（MAGEID）にはAdobe ログインとの関連付けが必要になりました。 このAdobe IDは、Commerce アカウントに接続されているのと同じメールアドレスを使用します。

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

   この手順では、Adobe IDを作成し、現在のCommerce アカウント（MAGEID）にリンクします。 このアカウントリンクを使用すると、_[!UICONTROL Email]_フィールドはすべての変更からブロックされます。 関連するメールアドレスの設定は、Adobe ID アカウントから管理されます。

1. [account.adobe.com](https://account.adobe.com/) に移動します。

1. 「**[!UICONTROL Change Email]**」をクリックします。

1. 新しい所有者のメールアドレスを入力します。

1. 「**[!UICONTROL Change]**」をクリックします。

   この手順では、新しいメールアドレスに送信される確認メールを生成します。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しいメールアドレスに送信された確認コードを入力します。

1. 「**[!UICONTROL Verify]**」をクリックします。

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## メールの変更

>[!IMPORTANT]
>
>[ 転送タイプ ](#identify-your-transfer-type) をレビューし、この一連の手順の前提条件を満たしていることを確認します。

1. [account.adobe.com](https://account.adobe.com/) に移動し、Adobeへのログインを完了します。

1. アカウント名とアバターの下で、「**[!UICONTROL Change Email]**」をクリックします。

1. ダイアログで、新しい所有者のメールアドレスを入力します。

1. 「**[!UICONTROL Change]**」をクリックします。

   この手順では、新しいメールアドレスに送信される確認メールを生成します。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しいメールアドレスに送信された確認コードを入力します。

1. 「**[!UICONTROL Verify]**」をクリックします。

## Adobe ID アカウント切り替え

>[!IMPORTANT]
>
>[ 転送タイプ ](#identify-your-transfer-type) をレビューし、この一連の手順の前提条件を満たしていることを確認します。

現在のオーナーと新しいオーナーが既存のAdobe ID を持っている場合、両方のアカウントは残りますが、メールアドレスを切り替える必要があります。 これには、有効でもAdobe IDに関連付けられていない _一時的な_ メールアドレスの使用が必要です。

### 一時アカウントへの変更

現在のオーナーは、これらの手順を完了して、Adobe IDを別の一時的なメールアドレスに関連付けます。

1. [account.adobe.com](https://account.adobe.com/) に移動し、Adobeへのログインを完了します。

1. アカウント名とアバターの下で、「**[!UICONTROL Change Email]**」をクリックします。

1. ダイアログで、Adobe IDで使用されない有効な一時メールアドレスを入力します。

   確認コードが記載されたメールを取得できるように、メールアドレスにアクセスできる必要があります。

1. 「**[!UICONTROL Change]**」をクリックします。

   この手順では、一時的なメールアドレスに送信される確認メールを生成します。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 一時メールアドレスに送信される確認コードを入力します。

1. 「**[!UICONTROL Verify]**」をクリックします。

1. Adobe アカウントからログアウトします。

### 新しい所有者手順

現在の所有者が一時的なメールアドレスへの転送を完了した後、新しい所有者はこれらの手順を完了し、現在の所有者の元のメールアドレスを指すようにアカウント設定を変更する必要があります。

1. [account.adobe.com](https://account.adobe.com/) に移動し、Adobeへのログインを完了します。

1. アカウント名とアバターの下で、「**[!UICONTROL Change Email]**」をクリックします。

1. ダイアログで、現在の所有者の元のメールアドレスを入力します。

1. 「**[!UICONTROL Change]**」をクリックします。

   この手順では、現在の所有者の元のメールアドレスに送信される確認メールを生成します。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 現在の所有者の元の電子メール アドレスに送信された確認コードを入力します。

1. 「**[!UICONTROL Verify]**」をクリックします。

1. Adobe アカウントからログアウトします。

### フォローアップ手順

新しい所有者が、現在の（現在は以前の）所有者の元のメールアドレスを使用してAdobe アカウントを正常に設定したら、次の手順を実行して所有権を転送します。

1. [account.adobe.com](https://account.adobe.com/) に移動し、[ 一時アカウント ](#change-to-a-temporary-account) のメールアドレスを使用してAdobeへのログインを完了します。

1. アカウント名とアバターの下で、「**[!UICONTROL Change Email]**」をクリックします。

1. ダイアログで、新しい所有者のメールアドレスを入力します。

1. 「**[!UICONTROL Change]**」をクリックします。

   この手順では、新しい所有者のメールアドレスに送信される確認メールを生成します。 メールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しい所有者の E メール アドレスに送信される確認コードを入力します。

1. 「**[!UICONTROL Verify]**」をクリックします。

>[!IMPORTANT]
>
>サポートリクエストを送信して、アカウント所有者のメールアドレスが更新されたことをサポートチームに通知します。 更新を完了するには、[Commerce Marketplace](https://commercemarketplace.adobe.com/) プロファイルのメールアドレスの更新など、さらに手順を実行する必要があります。 リクエストには、以前のアカウント所有者のメールアドレスを含めます。
