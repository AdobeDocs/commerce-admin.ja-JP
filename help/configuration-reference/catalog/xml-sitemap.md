---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap]'
description: の設定を確認します。 [!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap] コマース管理者のページ。
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 2%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![カテゴリオプション](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | ストア表示 | サイトマップカテゴリの更新頻度を決定します。 オプション： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | ストア表示 | 次の値の間 `0.0` および `1.0` これにより、他のコンテンツと関連したカテゴリサイトマップの更新の優先度が決まります。 ゼロ （`0.0`）が最も優先度が低くなります。 |

{style="table-layout:auto"}

## [!UICONTROL Products Options]

![製品オプション](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | ストア表示 | サイトマップ製品の更新頻度を決定します。 オプション： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | ストア表示 | 次の値の間 `0.0` および `1.0` これにより、他のコンテンツと関連した製品サイトマップの更新の優先度が決まります。 ゼロ （`0.0`）が最も優先度が低くなります。 |
| [!UICONTROL Add Images into Sitemap] | ストア表示 | 画像をサイトマップに含める範囲を決定します。 オプション： `None` / `Base Only` / `All` |

{style="table-layout:auto"}

## [!UICONTROL CMS Pages Options]

![CMS ページオプション](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | ストア表示 | サイトマップ CMS ページの更新頻度を決定します。 オプション： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | ストア表示 | 次の値の間 `0.0` および `1.0` これにより、他のコンテンツと関連した CMS ページサイトマップの更新の優先度が決まります。 ゼロ （`0.0`）が最も優先度が低くなります。 |

{style="table-layout:auto"}

## [!UICONTROL Store Url Options]

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Frequency] | ストア表示 | ストア URL の更新頻度を決定します。 オプション： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | ストア表示 | 次の値の間 `0.0` および `1.0` 他のコンテンツと比較して、ストア URL の更新の優先度を決定します。 ゼロ （`0.0`）が最も優先度が低くなります。 |

{style="table-layout:auto"}

## [!UICONTROL Generation Settings]

![生成設定](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストア表示 | ストアで XML サイトマップを使用できるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Start Time] | ストア表示 | サイトマップを更新する時刻（時、分、秒）を指定します。 |
| [!UICONTROL Frequency] | ストア表示 | サイトマップの更新頻度を決定します。 オプション： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | ストア表示 | サイトマップの更新プロセス中にエラーが発生した場合に通知を受け取る人物のメールアドレス。 複数のアドレスの場合は、それぞれをコンマで区切ります。 |
| [!UICONTROL Error Email Sender] | Web サイト | エラー通知の送信者として表示される店舗連絡先を識別します。 オプション： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | Web サイト | エラー通知に使用するメールテンプレートを識別します。 デフォルトのテンプレート： `Sitemap generate Warnings` |

{style="table-layout:auto"}

## [!UICONTROL Sitemap File Limits]

![サイトマップファイルの制限](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | ストア表示 | 単一のサイトマップに含めることができる URL の最大数を決定します。 |
| [!UICONTROL Maximum File Size] | ストア表示 | 生成されたサイトマップの最大サイズをバイト単位で決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Submission Settings]

![検索エンジン送信設定](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | ストア表示 | robots.txt ファイルに対してディレクティブを送信できるようにします。 オプション： `Yes` / `No` |

{style="table-layout:auto"}
