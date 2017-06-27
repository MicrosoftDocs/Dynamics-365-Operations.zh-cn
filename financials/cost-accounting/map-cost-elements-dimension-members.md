---
title: "将成本元素维度成员映射到一组常用维度成员"
description: "通过将不同的成本元素维度成员映射到一组通用的成本元素维度成员，您可以将数据合并为通用格式进行分析。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3cbcc5e7090f1a32b0c35fdb06427b5c225e857b
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>将成本元素维度成员映射到一组常用维度成员

[!include[banner](../includes/banner.md)]


通过将不同的成本元素维度成员映射到一组通用的成本元素维度成员，您可以将数据合并为通用格式进行分析。

如果您是一家全球性公司且遵守法定会计要求，您可能要使用多个会计科目表。 当您从不同的会计科目表导入成本元素维度成员时，您最后可能会将科目混合。 但是，这些科目实际上可能具有相同的本质，因此您想使用通用格式对它们进行分析并分摊成本。

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>将成本元素维度成员映射到通用格式
以下示例说明了您作为成本控制员可以如何在成本核算中创建新的成本元素维度，并且将来自美国会计科目表结构和法国会计科目表结构的成本元素维度成员映射到一组通用的成本元素维度成员。 然后，您可以使用这组通用的成本元素维度成员在成本核算分类帐中对来自两个法人的成本数据进行分析。

| 来源：美国会计科目表                                          | 来源：法国会计科目表                                          | 新的成本元素维度成员通用组                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| 导入来自美国会计科目表的成本元素维度成员 | 导入来自法国会计科目表的成本元素维度成员 | 将美国和法国成本元素维度成员映射到通用组 |
| 5001：销售                                                           | 5001：销售和广告                                               | 5000：销售和广告                                             |
| 5030：广告                                                     | 6390：存货采购\*                                                    | 7000：清洁费用                                                 |
| 7001：清洁费用                                               | 7001：差旅费用                                                      | 7001：差旅费用                                                   |

\*存货采购法国成本元素维度成员未映射。

## <a name="currency-conversion"></a>币种转换
您使用的不同会计科目表可以被设置为使用不同币种。 在这种情况下，请确保指定币种转换，以便按照使用成本元素维度成员所在的成本核算分类帐中的定义，使用正确的币种处理成本数据。 在前一示例中，如果在成本核算分类帐中使用美元 (USD)，您必须创建从 USD 到欧元 (EUR) 的币种转换，以便为映射的成本元素维度成员处理交易记录。

## <a name="update-mappings-at-any-time"></a>在任何时间更新映射
您可以在任何时间更新成本元素维度的映射定义。 由于映射不是按日期生效，因此将在您下一次处理成本交易记录或运行成本计算时应用更改。




