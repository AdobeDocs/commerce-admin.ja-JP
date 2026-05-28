---
title: '[!UICONTROL Catalog] > [!UICONTROL XML Sitemap]'
description: Commerce管理者の[!UICONTROL Catalog] > [!UICONTROL XML Sitemap] ページで設定を確認します。
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: 4d5699dc5c4dc4b2bcf208bb0e660ba61e28c507
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 2%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![ カテゴリーオプション ](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | ストアビュー | サイトマップカテゴリの更新頻度を指定します。 オプション：`Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | ストアビュー | 他のコンテンツに関連して、カテゴリーサイトマップの更新の優先順位を決定する`0.0`から`1.0`までの値。 ゼロ （`0.0`）の優先度が最も低くなっています。 |

{style="table-layout:auto"}

## [!UICONTROL Products Options]

![製品オプション ](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | ストアビュー | サイトマップ製品の更新頻度を指定します。 オプション：`Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | ストアビュー | 他のコンテンツに関する製品サイトマップの更新の優先順位を決定する`0.0`から`1.0`までの値。 ゼロ （`0.0`）の優先度が最も低くなっています。 |
| [!UICONTROL Add Images into Sitemap] | ストアビュー | サイトマップに含める画像の範囲を指定します。 オプション：`None` / `Base Only` / `All` |

{style="table-layout:auto"}

## [!UICONTROL CMS Pages Options]

![CMS ページオプション ](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | ストアビュー | サイトマップ CMS ページの更新頻度を指定します。 オプション：`Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | ストアビュー | CMS ページサイトマップの更新の優先度を他のコンテンツに対して決定する`0.0`から`1.0`の間の値。 ゼロ （`0.0`）の優先度が最も低くなっています。 |

{style="table-layout:auto"}

## [!UICONTROL Store Url Options]

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | ストアビュー | ストア URLが更新される頻度を指定します。 オプション：`Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | ストアビュー | 他のコンテンツに関するストア URLの更新の優先順位を決定する`0.0`から`1.0`までの値。 ゼロ （`0.0`）の優先度が最も低くなっています。 |

{style="table-layout:auto"}

## [!UICONTROL Generation Settings]

![生成設定](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストアビュー | ストアでXML サイトマップを使用できるかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Generation Method] | ストアビュー | XML サイトマップの生成方法を指定します。 `Standard`は従来の同期生成プロセスを使用し、メモリ内のすべてのデータを処理します。一方、`Batch`は非同期メモリ最適化バッチモードを使用して、柔軟性と拡張性を向上させます。 このオプションは、2.4.9 リリース以降で使用できます。 オプション：`Standard` / `Batch` |
| [!UICONTROL Start Time] | ストアビュー | サイトマップが更新される日の時間、分、秒を指定します。 |
| [!UICONTROL Frequency] | ストアビュー | サイトマップの更新頻度を指定します。 オプション：`Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | ストアビュー | サイトマップの更新処理中にエラーが発生した場合に通知を受け取るユーザーのメールアドレス。 複数のアドレスの場合は、それぞれコンマで区切ります。 |
| [!UICONTROL Error Email Sender] | web サイト | エラー通知の送信者として表示されるストア連絡先を識別します。 オプション：`General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | web サイト | エラー通知に使用される電子メールテンプレートを識別します。 既定のテンプレート：`Sitemap generate Warnings` |

{style="table-layout:auto"}

## [!UICONTROL Sitemap File Limits]

![ サイトマップファイルの制限](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | ストアビュー | 単一のサイトマップに含めることができるURLの最大数を指定します。 |
| [!UICONTROL Maximum File Size] | ストアビュー | 生成されたサイトマップの最大サイズをバイト単位で指定します。 |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Submission Settings]

![検索エンジン送信設定](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | ストアビュー | robots.txt ファイルにディレクティブを送信できるようにします。 オプション：`Yes` / `No` |

{style="table-layout:auto"}
