---
title: Commerce アカウントの転送
description: Commerce アカウントを別のオーナーまたは電子メールアドレスに転送する方法について説明します。
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: e33c207c5c9ba9ca6e82688e28c985cb9b3b7c71
workflow-type: tm+mt
source-wordcount: '1196'
ht-degree: 0%

---

# Commerce アカウントの転送

ビジネスの責任が変更される場合、新しいオーナーまたは別のメールアドレスにCommerce アカウントを転送する必要が生じる場合があります。 この転送には、アカウントに関連付けられているプライマリユーザーメールに変更が必要です。

以下では、Commerce（MAGEID）アカウントを転送する手順について説明します。 Cloud アカウント（Cloud プロジェクトまたはNew Relic）の所有権に関する変更は含まれていません。 クラウドプロジェクトへのアクセスについて詳しくは、「[Commerce on Cloud Infrastructure ガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=ja)」の「_ユーザーアクセスの管理_」を参照してください。

>[!IMPORTANT]
>
>新しいアカウント所有者が共有アクセスを使用して拡張機能を購入した場合、アカウント転送プロセスが開始されるとすぐに、これらの拡張機能へのアクセスが失われます。 アカウントの転送をリクエストする前に、新しい所有者が[&#x200B; マーケットプレイスアカウント &#x200B;](https://commercemarketplace.adobe.com/sales/order/history/)から購入の注文IDを取得し、[&#x200B; マーケットプレイスチーム &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)からこれらの拡張機能の払い戻しをリクエストしていることを確認してください。 拡張機能の購入を別のアカウントに転送することはできません。

## 転送タイプの特定

Commerce アカウントの転送の種類は、現在の所有者と新しい所有者が利用できるCommerce アカウントの資格情報によって異なります。 次のシナリオでは、これらの資格情報に基づいた様々な転送タイプについて説明します。

| 転送タイプ | 現在の所有者 | 新しい所有者 |
| ------------- | ------------- | --------- |
| [新しいAdobe IDとメールの変更](#new-adobe-id-and-email-change) | **_がAdobe ログインアカウントに接続されていない_** MAGEIDがあります | MAGEIDがなく、Adobe ログインアカウントに接続されていません。 |
| [電子メールの変更](#email-change) | Adobe ログインアカウントで&#x200B;**_接続_**&#x200B;されたMAGEIDを持っています。 | Adobe ログインアカウントがありますが、**_にはAdobe ログインアカウントに接続されたMAGEID_**&#x200B;がありません。 |
| [Adobe ID アカウントの切り替え](#adobe-id-account-switch) | Adobe ログインアカウントに&#x200B;**_接続_**&#x200B;されたMAGEIDを持っています。 | Has a MAGEID and is connected to an Adobe login account. |

{style="table-layout:auto"}

>[!NOTE]
>
>As Adobe Commerce continues to integrate with other Adobe solutions, a Commerce account (MAGEID) now requires an association with an Adobe login. This Adobe ID uses the same email address connected to your Commerce account.

## New Adobe ID and email change

>[!IMPORTANT]
>
>[転送タイプ &#x200B;](#identify-your-transfer-type)を確認し、この一連の手順の前提条件を満たしていることを確認してください。

この種類の転送には、既存のCommerce アカウントにリンクされたAdobe IDを持ち、そのアカウントを新しい所有者のメールアドレスに変更する必要があります。

1. [Commerce アカウントのログイン &#x200B;](https://account.magento.com/customer/account/login/) ページに移動します。

1. **[!UICONTROL Sign in with Adobe ID]**&#x200B;をクリックします。

1. **[!UICONTROL Create an account]**&#x200B;をクリックします。

1. 現在の所有者の電子メールアドレスとパスワードを入力します。

1. **[!UICONTROL Continue]**&#x200B;をクリックします。

   この手順では、Adobe IDを作成し、現在のCommerce アカウント（MAGEID）にリンクします。 With this account link, the _[!UICONTROL Email]_&#x200B;field is blocked from any changes. 関連付けられたメールアドレスの設定は、Adobe ID アカウントから管理されます。

1. [account.adobe.com](https://account.adobe.com/)に移動します。

1. **[!UICONTROL Change Email]**&#x200B;をクリックします。

1. Enter the new owner&#39;s email address.

   新しいメールアドレスが既にシステム内の別のアカウントにリンクされている場合、転送に直接使用することはできません。 代わりに、[一時的な電子メールアドレス &#x200B;](#change-to-a-temporary-account)を使用して変更を容易にする必要があります。

1. **[!UICONTROL Change]**&#x200B;をクリックします。

   This step generates a verification email sent to the new email address. このメールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. Enter the confirmation code sent to the new email address.

1. **[!UICONTROL Verify]**&#x200B;をクリックします。

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## 電子メールの変更

>[!IMPORTANT]
>
>[転送タイプ &#x200B;](#identify-your-transfer-type)を確認し、この一連の手順の前提条件を満たしていることを確認してください。

この転送タイプでは、現在のアカウントオーナーは他のAdobe製品にアクセスできなくなります。

1. [account.adobe.com](https://account.adobe.com/)に移動し、Adobe ログインを完了します。

1. アカウント名とアバターの下で、**[!UICONTROL Change Email]**&#x200B;をクリックします。

1. ダイアログで、新しい所有者のメールアドレスを入力します。

   新しいメールアドレスが既にシステム内の別のアカウントにリンクされている場合、転送に直接使用することはできません。 代わりに、[一時的な電子メールアドレス &#x200B;](#change-to-a-temporary-account)を使用して変更を容易にする必要があります。

1. **[!UICONTROL Change]**&#x200B;をクリックします。

   この手順では、新しいメールアドレスに送信された確認メールを生成します。 このメールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. Enter the confirmation code sent to the new email address.

1. **[!UICONTROL Verify]**&#x200B;をクリックします。

## Adobe ID account switch

>[!IMPORTANT]
>
>[転送タイプ &#x200B;](#identify-your-transfer-type)を確認し、この一連の手順の前提条件を満たしていることを確認してください。

This transfer type uses a temporary email address to switch account ownership when both the current owner and new owner have existing Adobe IDs, and you want to retain both accounts. To complete the ownership transfer, you must use a temporary email address that is not associated with an Adobe ID.

### 一時アカウントに変更

現在の所有者は、Adobe IDを別の一時的なメールアドレスに関連付けるために、これらの手順を完了します。

1. [account.adobe.com](https://account.adobe.com/)に移動し、Adobe ログインを完了します。

1. アカウント名とアバターの下で、**[!UICONTROL Change Email]**&#x200B;をクリックします。

1. ダイアログで、Adobe IDで使用されていない有効な一時メールアドレスを入力します。

>[!NOTE]
>
>確認コードでメールを取得するには、メールアドレスにアクセスできる必要があります。
>
>アカウントメールにアクセスできない場合は、IT部門に会社のメールシステムでアカウントメールアドレスのメール転送を設定するように依頼します。 メール転送を設定できない場合は、新しいアカウントオーナーにAdobe IDが設定されていることを確認し、アカウント転送を開始するために必要なすべての詳細を[&#x200B; サポートリクエスト &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)送信します。

1. **[!UICONTROL Change]**&#x200B;をクリックします。

   この手順では、一時的なメールアドレスに送信された確認メールを生成します。 このメールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 一時的なメールアドレスに送信された確認コードを入力します。

1. **[!UICONTROL Verify]**&#x200B;をクリックします。

1. Adobe アカウントからログアウトします。

### 新しい所有者ステップ

現在の所有者が一時的なメールアドレスへの転送を完了した後、新しい所有者は、現在の所有者の元のメールアドレスを指すようにアカウント設定を変更するには、次の手順を完了する必要があります。

1. [account.adobe.com](https://account.adobe.com/)に移動し、Adobe ログインを完了します。

1. アカウント名とアバターの下で、**[!UICONTROL Change Email]**&#x200B;をクリックします。

1. ダイアログで、現在の所有者の元のメールアドレスを入力します。

1. **[!UICONTROL Change]**&#x200B;をクリックします。

   この手順では、現在の所有者の元のメールアドレスに送信された確認メールを生成します。 このメールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 現在の所有者の元のメールアドレスに送信された確認コードを入力します。

1. **[!UICONTROL Verify]**&#x200B;をクリックします。

1. Adobe アカウントからログアウトします。

### Follow up steps

After the new owner successfully configures their Adobe account with the original email address of the current owner, complete these steps to transfer ownership.

1. Navigate to [account.adobe.com](https://account.adobe.com/), and complete the Adobe login using the email address for the [temporary account](#change-to-a-temporary-account).

1. Under the account name and avatar, click **[!UICONTROL Change Email]**.

1. ダイアログで、新しい所有者のメールアドレスを入力します。

1. **[!UICONTROL Change]**&#x200B;をクリックします。

   この手順では、新しい所有者のメールアドレスに送信された確認メールを生成します。 このメールには、メールアドレスの変更を完了するために必要な確認コードが含まれています。

1. 新しい所有者のメールアドレスに送信された確認コードを入力します。

1. **[!UICONTROL Verify]**&#x200B;をクリックします。

## 最後のステップ

新しい所有者が1番目または3番目のユースケースの手順を完了したら、新しい所有者は[&#x200B; サポートリクエストを送信して](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case) メールアドレスの更新をサポートチームに通知する必要があります。 その後、サポートチームは、[Commerce Marketplace](https://commercemarketplace.adobe.com/) プロファイルの電子メールアドレスの更新など、追加の作業を完了します。 リクエストに以前のアカウント所有者のメールアドレスを含めます。
