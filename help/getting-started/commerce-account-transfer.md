---
title: Adobe Commerce アカウントの転送
description: Adobe Commerce アカウントを新しいオーナーまたは電子メールアドレスに転送する方法、適切な転送タイプを選択する方法、電子メールの変更を確認する方法、およびサポートに連絡する方法について説明します。
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
TQID: https://experienceleague.adobe.com/CIyzus4f8WcBH-jW9R1nCL-gkl065DLTHbjNn0K6e7E
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e01cba363eb149286479718e660f8cdf6526e826
workflow-type: tm+mt
source-wordcount: 1553
ht-degree: 0%

---

# Adobe Commerce アカウントの転送

ビジネスの責任が変更される場合、新しいオーナーまたは別のメールアドレスにAdobe Commerce アカウントを転送する必要が生じる場合があります。 この転送には、アカウントに関連付けられているプライマリユーザーメールに変更が必要です。

次に、Adobe Commerce アカウント（MAGEID）を転送する手順を示します。 クラウドインフラストラクチャプロジェクトの所有権または[!DNL New Relic]の所有権に関するAdobe Commerceへの変更は含まれていません。 クラウドプロジェクトへのアクセスについて詳しくは、「_Commerce on Cloud Infrastructure ガイド_」の「[&#x200B; ユーザーアクセスの管理](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/project/user-access)」を参照してください。

>[!IMPORTANT]
>
>新しいアカウント所有者が共有アクセスを使用して拡張機能を購入した場合、アカウントの転送が開始されるとすぐに、これらの拡張機能へのアクセスが失われます。
>
>アカウントの転送をリクエストする前に、新しい所有者が[購入者 [!DNL Commerce Marketplace]  アカウント &#x200B;](https://commercemarketplace.adobe.com/sales/order/history/)から購入の注文IDを取得し、[[!DNL Commerce Marketplace]  チーム &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)から返金をリクエストしていることを確認してください。 拡張機能の購入を別のアカウントに転送することはできません。

## 転送タイプの特定

適切なAdobe Commerce アカウント転送プロセスは、現在の所有者と新しい所有者のアカウントステータス、および現在の所有者のメールアドレスに引き続きアクセスできるかどうかによって異なります。 たとえば、現在の所有者が退職した場合でも、そのアドレスに送信されたメールにアクセスする必要がある場合があります。

次のシナリオでは、これらの条件に基づいて使用可能な転送オプションについて説明します。

| 転送タイプ | 現在の所有者 | 新しい所有者 |
| ------------- | ------------- | --------- |
| [新しいAdobe IDとメールの変更](#new-adobe-id-and-email-change) | Adobe IDに接続されていないMAGEIDがある | MAGEIDを持たず、Adobe IDを持っていません。 |
| [電子メールの変更のみ](#email-change) | Adobe IDに接続されているMAGEIDがあります。 | にはAdobe IDがありますが、アカウントにMAGEIDが接続されていません。 |
| [Adobe ID アカウントの切り替え](#adobe-id-account-switch) | Adobe IDに接続されているMAGEIDがあります。 | MAGEIDがあり、Adobe IDに接続されています。 |

{style="table-layout:auto"}

>[!NOTE]
>
>Adobe Commerceが他のAdobe ソリューションとの統合を継続する場合、Adobe Commerce アカウント（MAGEID）にはAdobe IDとの関連付けが必要になります。 Adobe IDでは、[Adobe Commerce アカウント &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)に接続された同じ電子メールアドレスを使用します。

## Adobe IDのメール変更を確認する

[account.adobe.com](https://account.adobe.com/)で、同じ検証ワークフローを使用する転送パスがいくつかあります。 ターゲットの電子メールアドレスを入力して「**[!UICONTROL Change]**」をクリックしたら、次の手順を実行します。

1. 入力したアドレスに送信された確認メールを開き、確認コードを見つけます。

1. 確認コードを入力してください。

1. **[!UICONTROL Verify]**&#x200B;をクリックします。

## 新しいAdobe IDとメールの変更

>[!IMPORTANT]
>
>[転送タイプ &#x200B;](#identify-your-transfer-type)を確認し、このパスが状況に一致することを確認します。
>
>- 現在のオーナーは同社に在籍しています。
>- 現在のオーナーには、Adobe IDがないか、[Adobe Commerce アカウント （MAGEID） &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)に接続されていないAdobe IDがあります。
>- 新しいオーナーはAdobe IDを持っておらず、Adobe Commerce アカウントも持っていません。

現在の所有者がAdobe IDにリンクされていないMAGEIDを持っている場合は、このパスを使用します。 現在の所有者は、まずAdobe IDを作成してリンクし、その後、そのAdobe ID メールアドレスを新しい所有者のメールアドレスに変更します。

1. [Adobe Commerce アカウントのログイン &#x200B;](https://account.magento.com/customer/account/login/) ページに移動します。

1. **[!UICONTROL Sign in with Adobe ID]**&#x200B;をクリックします。

1. **[!UICONTROL Create an account]**&#x200B;をクリックします。

1. 現在の所有者のメールアドレスとパスワードを入力します。

1. **[!UICONTROL Continue]**&#x200B;をクリックします。

   この手順では、Adobe IDを作成し、現在のAdobe Commerce アカウント（MAGEID）にリンクします。 このアカウントリンクを使用すると、_[!UICONTROL Email]_&#x200B;フィールドは変更によってブロックされます。 関連付けられたメールアドレスの設定は、Adobe ID アカウントから管理されます。

1. [account.adobe.com](https://account.adobe.com/)に移動します。

1. **[!UICONTROL Change Email]**&#x200B;をクリックします。

1. 新しい所有者のメールアドレスを入力します。

   新しいメールアドレスが既にシステム内の別のアカウントにリンクされている場合、転送に直接使用することはできません。 代わりに、[Adobe ID アカウント スイッチ &#x200B;](#adobe-id-account-switch) パスに従い、[一時メール アドレス &#x200B;](#change-to-a-temporary-account)を使用してください。

1. [電子メール検証手順](#verify-an-adobe-id-email-change)を完了します。

新しい所有者が電子メールアドレスを確認したら、[最後の手順](#final-steps)に進み、Adobe Commerce サポートが[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) プロファイルなどのアカウントレコードを更新できるようにします。

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on){transcript=true}

## メール変更時のみ {#email-change}

>[!IMPORTANT]
>
>[転送タイプ &#x200B;](#identify-your-transfer-type)を確認し、このパスが状況に一致することを確認します。
>
>- 現在のオーナーは同社に在籍しています。
>- 現在のオーナーは、[Adobe Commerce アカウント （MAGEID） &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)に接続されたAdobe IDを持っています。
>- 新しいオーナーには、Adobe Commerce アカウントに接続されていないAdobe IDがあります。

開始する前に、この転送タイプでは、現在のアカウントオーナーがそのAdobe IDに関連付けられている他のAdobe製品にアクセスできなくなります。

1. [account.adobe.com](https://account.adobe.com/)に移動し、Adobe ログインを完了します。

1. アカウント名とアバターの下で、**[!UICONTROL Change Email]**&#x200B;をクリックします。

1. ダイアログで、新しい所有者のメールアドレスを入力します。

   新しいメールアドレスが既にシステム内の別のアカウントにリンクされている場合、転送に直接使用することはできません。 代わりに、[Adobe ID アカウント スイッチ &#x200B;](#adobe-id-account-switch) パスに従い、[一時メール アドレス &#x200B;](#change-to-a-temporary-account)を使用してください。

1. [電子メール検証手順](#verify-an-adobe-id-email-change)を完了します。

新しい所有者が電子メールアドレスを確認したら、[最後の手順](#final-steps)に進み、Adobe Commerce サポートが[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) プロファイルなどのアカウントレコードを更新できるようにします。

## Adobe ID アカウントスイッチ

>[!IMPORTANT]
>
>[転送タイプ &#x200B;](#identify-your-transfer-type)を確認し、このパスが状況に一致することを確認します。
>
>- 現在の所有者は会社に在籍していませんが、現在の所有者の会社の電子メールアドレスに送信された電子メールに引き続きアクセス可能であるか、IT チームが承認済みの連絡先に電子メールを転送できます。
>- 現在のオーナーは、[Adobe Commerce アカウント （MAGEID） &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)に接続されたAdobe IDを持っています。
>- 新しいオーナーには、Adobe Commerce アカウントに接続されたAdobe IDがあります。

この転送タイプでは、現在の所有者と新しい所有者の両方が既存のAdobe IDを持っていて、両方のAdobe IDを保持したい場合に、一時的なメールアドレスを使用してアカウントの所有権を切り替えます。 所有権の移転を完了するには、Adobe IDに関連付けられていない一時的なメールアドレスを使用する必要があります。

### 一時アカウントに変更

現在の所有者のAdobe IDを一時的なメールアドレスに関連付けるには、次の手順を実行します。 確認コードを取得するには、そのメールアドレスにアクセスできる必要があります。

>[!NOTE]
>
>現在の所有者の電子メールにアクセスできない場合は、IT チームに対して、会社の電子メールシステムでアカウントの電子メールアドレスの電子メール転送を設定するように依頼します。 メール転送を設定できない場合は、新しいアカウントオーナーにAdobe IDが設定されていることを確認し、アカウント転送を開始するために必要なすべての詳細を[&#x200B; サポートリクエスト &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)送信します。

1. [account.adobe.com](https://account.adobe.com/)に移動し、Adobe ログインを完了します。

1. アカウント名とアバターの下で、**[!UICONTROL Change Email]**&#x200B;をクリックします。

1. ダイアログで、Adobe IDで使用されていない有効な一時メールアドレスを入力します。

1. [電子メール検証手順](#verify-an-adobe-id-email-change)を完了します。

1. Adobe アカウントからログアウトします。

### 新しい所有者ステップ

現在の所有者が一時的なメールアドレスへの転送を完了した後、新しい所有者は、Adobe IDのメールアドレスを現在の所有者の元のメールアドレスに変更するには、次の手順を実行する必要があります。

1. [account.adobe.com](https://account.adobe.com/)に移動し、Adobe ログインを完了します。

1. アカウント名とアバターの下で、**[!UICONTROL Change Email]**&#x200B;をクリックします。

1. ダイアログで、現在の所有者の元のメールアドレスを入力します。

1. [電子メール検証手順](#verify-an-adobe-id-email-change)を完了します。

1. Adobe アカウントからログアウトします。

### フォローアップの手順

新しい所有者が現在の所有者の元のメールアドレスでAdobe IDを正常に設定したら、次の手順を実行して、そのメールアドレスを新しい所有者に割り当てます。

1. [account.adobe.com](https://account.adobe.com/)に移動し、[一時アカウント &#x200B;](#change-to-a-temporary-account)の電子メールアドレスを使用してAdobe ログインを完了します。

1. アカウント名とアバターの下で、**[!UICONTROL Change Email]**&#x200B;をクリックします。

1. ダイアログで、新しい所有者のメールアドレスを入力します。

1. [電子メール検証手順](#verify-an-adobe-id-email-change)を完了します。

新しい所有者が電子メールアドレスを確認したら、[最後の手順](#final-steps)に進み、Adobe Commerce サポートが[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) プロファイルなどのアカウントレコードを更新できるようにします。

## 最後のステップ

[新規Adobe IDとメールの変更](#new-adobe-id-and-email-change)、[&#x200B; メールの変更のみ](#email-change)、または[Adobe ID アカウントの切り替え](#adobe-id-account-switch) プロセスを完了した後、これらの手順を実行します。

1. 新しい所有者として、[&#x200B; サポートリクエストを送信](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case)。

   次の詳細を含めます。

   - 前のアカウント所有者のメールアドレス
   - 新しい所有者のメールアドレス
   - Adobe Commerce アカウントの転送を完了し、Adobe IDのメールアドレスを更新したことに関するメモ

1. Adobe Commerce サポートがアップデートを確認するまでお待ちください。

   サポートでは、[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) プロファイルの電子メールアドレスなど、関連するレコードも更新されます。

サポートがリクエストを完了した後、新しいオーナーはAdobe IDを使用してAdobe Commerce アカウントにログインできます。 MAGEIDは、アカウントの使用権限IDのままです。
