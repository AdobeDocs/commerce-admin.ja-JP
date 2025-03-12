---
title: '[!UICONTROL General] &gt; [!UICONTROL General]'
description: Commerce Admin の [!UICONTROL General] &gt; [!UICONTROL General] ページで設定を確認します。
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

これらの設定フィールドとオプションについて詳しくは、[ 国オプション ](../../getting-started/store-details.md#country-options) を参照してください。

![ 一般 > 国オプション ](./assets/general-country-options.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default Country] | ストア表示 | ストアが所在する国。 |
| [!UICONTROL Allow Countries] | Web サイト | 注文を受け付ける国。 |
| [!UICONTROL Zip/Postal Code is Optional for] | グローバル | 配送先住所に郵便番号が必要ない国。 |
| [!UICONTROL European Union Countries] | グローバル | 欧州連合のメンバーである国。 |
| [!UICONTROL Top Destinations] | ストア表示 | 販売のターゲットとする主な国。 |

{style="table-layout:auto"}

## [!UICONTROL State Options]

これらの設定フィールドとオプションについて詳しくは、[ 状態オプション ](../../getting-started/store-details.md#state-options) を参照してください。

![ 一般/状態オプション ](./assets/general-state-options.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL State is required for] | グローバル | 住所に地域または都道府県を含める必要がある国（ビジネスを行う国）。 |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | グローバル | 国を指定する必要がない場合は、は「_地域/都道府県_ フィールドを顧客の郵送先住所に含めるかどうかを決定します。<br /> <br />**`Yes`**– 国によって要求されていない場合でも、顧客の住所に _地域/都道府県_ フィールドを含めます。<br />**`No`** – 国で必要ない場合、お客様の住所から「地域/都道府県」フィールドを省略します。 |

{style="table-layout:auto"}

## [!UICONTROL Locale Options]

これらの設定フィールドとオプションについて詳しくは、[ ロケールオプション ](../../getting-started/store-details.md#locale-options) を参照してください。

![ 一般/ロケールオプション ](./assets/general-locale-options.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Timezone] | Web サイト | Web サイトが提供する主要市場のタイムゾーン。 通常、タイムゾーンはビジネスの物理的な場所で使用されているものと同じです。 |
| [!UICONTROL Locale] | ストア表示 | ストアビューが提供する、市場で使用される言語、通貨、測定システム。 |
| [!UICONTROL Weight Unit] | ストア表示 | 通常、ロケールからの出荷に使用される測定単位。 オプション：`lbs` / `kgs` |
| [!UICONTROL First Day of Week] | ストア表示 | 店舗ビューが提供する市場の週の最初の日と見なされる日。 |
| [!UICONTROL Weekend Days] | ストア表示 | 市場の週末に落ちる日は、ストアビューによって提供されました。 |

{style="table-layout:auto"}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![ 一般 > Web サイトの制限 ](./assets/general-website-restrictions.png)<!-- zoom -->

これらの設定の変更について詳しくは、『 [ マーチャンダイジングおよびプロモーションガイド _の ](../../merchandising-promotions/event-configure.md#access-restrictions) アクセス制限_ を参照してください。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | Web サイト | Web サイトが制限モードで動作しているかどうかを判断します。<br /> <br />**`Yes`**- Web サイトへのアクセスは、以下のフィールドに設定されている方法で制限されます。<br />**`No`** – 制限は無効で、次の設定は無効です。 |
| [!UICONTROL Restriction Mode] | Web サイト | Web サイトに適用されるアクセス制限の種類を決定します。<br /> <br />**`Website Closed`**- ストアフロントへのすべてのアクセスが制限され、ストアフロント URL は一時的にランディングページにリダイレクトされます。 この設定は、サイトのメンテナンス時や起動前に役立ちます。<br />**`Private Sales: Login Only`** – 登録されたお客様のみがログインしてストアフロントにアクセスできます。 すべてのストアフロント URL は、指定したランディングページまたはログインフォームに一時的にリダイレクトされます。 ユーザーはこのモードでアカウントを作成できません。<br />**`Private Sales: Login and Register`**- ユーザーがストアフロントにアクセスするにはログインする必要があります。 すべてのストアフロント URL は、ユーザーがログインするまで、一時的にログインフォームにリダイレクトされます。 ユーザーは、サイトがこのモードの間にアカウントを登録できます。 |
| [!UICONTROL Startup Page] | ストア表示 | Web サイトがプライベート販売モードの場合、この設定によって、顧客がログインするまで表示されるページが決まります。<br />  <br />**`To login form`**- ユーザーは、ログインするまで、ログインフォームにリダイレクトされます。<br />**`To landing page`** - ユーザーは、ログインするまで、以下に指定された静的ページにリダイレクトされます。<br /> <br />**_重要！_**お客様がログインしてサイト全体にアクセスできるように、指定したランディングページからのログインページへのリンクを必ず含めてください。 |
| [!UICONTROL Landing Page] | ストア表示 | Web サイトが Private Sales モードの場合に表示される最初のページを指定します。 |
| [!UICONTROL HTTP Response] | Web サイト | Web サイトが閉じられ、ボット、クローラーまたはスパイダーによって接続が試行されたときに送信される HTTP 応答を決定します。<br /> <br />**`503 Service unavailable`**- ページは使用できませんが、スパイダーはインデックスを更新しないでください。<br />**`200 OK`** - ランディングページは正しく、サイト上の唯一のページとしてスパイダーによって扱われる必要があります。 |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Web サイト | _ログイン_ フォームおよび _パスワードを忘れた場合_ フォームのフィールドが、以前の入力内容から自動的に入力されるかどうかを決定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Store Information]

![ 一般/ストア情報 ](./assets/general-store-information.png)<!-- zoom -->

これらの設定の変更の詳細については、「[ はじめる前に _」の_ ストア情報 ](../../getting-started/store-details.md) を参照してください。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Store Name] | ストア表示 | ストア表示に関連付けられているストアの名前。 |
| [!UICONTROL Store Phone Number] | ストア表示 | （ストア表示に関連付けられた）ストアのプライマリ電話番号がビジネス用に開かれています。 例：月～金、9～5、土 9～正午（PST） |
| 国 | Web サイト | Web サイトを運営するビジネスの国。 |
| [!UICONTROL Region/State] | Web サイト | Web サイトを運営するビジネスの地域または状態。 |
| [!UICONTROL ZIP/Postal Code] | Web サイト | Web サイトを運営するビジネスの郵便番号。 |
| [!UICONTROL City] | Web サイト | Web サイトを運営するビジネスの市区町村の場所。 |
| [!UICONTROL Street Address] | Web サイト | Web サイトを運営するビジネスの通りや郵送先住所。 |
| [!UICONTROL Street Address Line 2|]Web サイト | 必要に応じて、会社の住所の 2 行目。 |
| [!UICONTROL VAT Number] | Web サイト | Commerce インストールを所有する事業の付加価値税番号（該当する場合）。 |
| [!UICONTROL Validate VAT Number] |  | 付加価値税 ID 番号を検証します。 |

{style="table-layout:auto"}

## [!UICONTROL Single-Store Mode]

![ 一般/シングルストアモード ](./assets/general-single-store-mode.png)<!-- zoom -->

これらの設定の変更方法の詳細については、「[ はじめる前に _の ](../../getting-started/websites-stores-views.md#single-store-mode) シングル ストア モード_ を参照してください。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | グローバル | シングルストアインストールで有効にすると、設定の範囲ボックスと関連するフィールドラベルが非表示になります。オプション : `Yes` / `No` <br/>**_注意：_**複数の表示を持つストアの場合、シングルストアモードは無視されます。<br/> 単一ストアモードを有効にすると、すべてのカタログおよび製品ストア固有のデータが、デフォルトのストア表示からすべてのストア表示範囲にコピーされます。 ストアに storereview が 1 つしかない場合にのみ、カタログおよび製品データがコピーされます。 ストアに、無効な storereview と有効な storereview が 1 つある場合、カタログと製品のデータはコピーされません。<br/> シングルストアモードを有効にすると、コンテンツ固有のデータに対する storreview 固有の設定が無視されます。 代わりに、グローバルレベルの範囲で定義された構成設定を使用して、管理 UI とストアフロントの間の一貫性を確保します。 |

{style="table-layout:auto"}

## [!UICONTROL Data Services]

![ 一般/データサービス ](./assets/general-data-services.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Commerce Events Enabled] | グローバル | 医療関係のお客様が [ データサービス HIPAA](https://experienceleague.adobe.com/en/docs/commerce/data-connection/hipaa-readiness) 拡張機能をインストールしている場合、この設定はデフォルトでオフになっています。 その結果、ライブ検索および製品レコメンデーションで使用されるストアフロントイベントデータが取得されなくなりました。 これは、ストアフロントのイベントデータがクライアントサイドで生成されるからです。 [ ライブ検索 ](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) および [Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview) サービスで使用するストアフロントイベントデータを引き続きキャプチャして送信するには、**Commerce イベント有効** を `Yes` に設定します。 |

{style="table-layout:auto"}
