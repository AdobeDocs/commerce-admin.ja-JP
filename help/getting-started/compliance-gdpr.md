---
title: GDPRへの準拠
description: 一般データ保護規則（GDPR）とは、欧州連合（EU）と欧州経済地域のすべての個人のデータ保護とプライバシーを規制する法律です。
exl-id: 88a732f3-f376-4ff5-890c-0535de8eae51
feature: Compliance
TQID: https://experienceleague.adobe.com/KoEiKz5hg35mPMhjHnCpcvzLhq-BymF9aJOn0y3Vcis
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
subfeature_v2: id: bcbf87e7-9b75-4596-bffe-0f376b4c73a7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 518
ht-degree: 0%

---

# GDPRへの準拠

>[!NOTE]
>
>この情報は、Adobe CommerceとMagento Open Sourceのマーチャントおよび開発者が、一般データ保護規則（GDPR）の影響を理解するのに役立つ一連のトピックの1つです。 この情報は情報提供のみを目的としており、法的アドバイスとして解釈されるべきではありません。 自社が法的義務を遵守する必要があるかどうか、どのように遵守すべきかを判断するには、弁護士に相談してください。

一般データ保護規則（GDPR）とは、欧州連合（EU）および欧州経済地域のすべての個人のデータ保護とプライバシーを規制する法律です。 この法律は、EU域外への個人データの輸出にも適用されます。 GDPRは2016年4月に採択され、2018年5月25日に施行されました。 EUに拠点を置いていないが、グローバルなコマースを展開する企業は、この規制に準拠する必要があります。 GDPAでは、**個人データ**&#x200B;を次のように定義しています。

>識別可能な自然人（「データ主体」）に関する情報；識別可能な自然人とは、直接又は間接的に、特に名前、識別番号、位置情報、オンライン識別子などの識別子を参照して、又はその自然人の物理的、生理学的、遺伝的、精神的、経済的、文化的、社会的同一性に固有の1つ以上の要因を参照して識別できる人をいう。

個人データを処理するすべての組織は、以下を開示する必要があります。

- 収集されるデータの種類
- データ収集の目的
- データの収集に使用されるメソッド
- データを保持する期間
- データが他のユーザーと共有されているかどうか

## GDPRとCCPA

お客様のビジネスがGDPRと[ カリフォルニア州消費者プライバシー法（CCPA） ](../getting-started/compliance-ccpa.md)の両方に準拠する必要がある場合は、GDPR コンプライアンスプログラムの一部をCCPAに使用できます。 これらの規制にはいくつかの類似点がありますが、次のような違いがあります。

- 個人情報の定義は、各規制によって異なります。
- GDPRでは、消費者が個人データを特定の目的のために使用する前に、オプトインすることを義務付けており、CCPAは消費者にオプトアウトする権利を提供します。
- CCPAには、データインベントリとマッピングの要件が追加されています。
- この規制には、プライバシーポリシーの要件が異なります。

GDPRを遵守している企業は、CCPAにもとづいて追加の義務を負っている可能性があります。 詳しくは、[CCPA ファクトシート ](https://oag.ca.gov/system/files/attachments/press_releases/CCPA%20Fact%20Sheet%20%2800000002%29.pdf){:target="_blank"}を参照してください。

## ベストプラクティス

- すべてのストアの現在の[ プライバシーポリシー](../getting-started/privacy-policy.md)を確認して、適用される法的要件（GDPRおよびCCPAを含むが、これらに限定されない）に準拠していることを確認します。

- [Googleの設定](../merchandising-promotions/google-tools.md#google-privacy-settings)を更新し、個人情報の使用に関する法的義務に準拠していることを確認します。

- 透明性を維持し、徹底した文書化を行います。

- Adobeを利用して、該当する法的義務を遵守する方法については、[web サイト ](https://business.adobe.com/privacy/general-data-protection-regulation.html){:target="_blank"}をご覧ください。

- データフロー図とデータベースエンティティのマッピングについては、[個人情報参照](https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m2.html){: target="_blank"}を参照してください。
