---
title: "成本元素维度"
description: "作为成本核算中的其中一个核心支柱，成本元素维度用来对成本分类和跟踪成本流向。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0f47c75b6f6f4533501070f78698de82cf70f9bd
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="cost-element-dimensions"></a>成本元素维度

[!INCLUDE [banner](../includes/banner.md)]

作为成本核算中的其中一个核心支柱，成本元素维度用来对成本分类和跟踪成本流向。 

一个成本元素对应于会计科目表的成本相关物料。 基本上它可以是成本流向的公司中的最低级别的任何元素类型。 成本元素的概念范围从会计科目到所有与成本相关的资源。 目前，成本核算支持会计科目。

## <a name="two-types-of-cost-elements"></a>成本元素的两种类型
成本元素有两种类型：主要成本元素和辅助成本元素。 下表描述了两种类型之间的区别：

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>主要成本元素</strong></td>
<td><strong>辅助成本元素</strong></td>
</tr>
<tr class="even">
<td>主要成本元素表示从财务会计到成本核算的成本流动。 成本元素结构对应于总帐中的损益科目结构，其中成本要素可能对应于主科目。 并非所有的主科目都必须表示为成本元素，具体取决于业务要求。 主要成本元素的一些示例包括：
<ul>
<li>所售货物成本 (COG)</li>
<li>间接物料成本</li>
<li>人员成本</li>
<li>能源成本</li>
</ul></td>
<td>辅助成本元素表示内部成本流，因为这些成本仅在成本核算中创建和使用。 它们可用于确保成本来源可以跟踪。 这些成本元素在成本分摊和开销计算中使用。 辅助成本元素的一些示例包括：
<ul>
<li>生产成本</li>
<li>生产、物料和营销开销</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>成本元素维度和成本元素维度成员
成本元素被称为“*成本元素维度*”。 各个维度值被称为“*成本元素维度成员*”。 例如，你将美国会计科目表结构 (COA) 作为法定申报的基础。 此 COA 用作成本元素维度。 科目为主要成本元素，在成本核算中表示为成本元素维度成员。 以下屏幕截图举例说明了作为成本元素维度的主科目及其作为成本元素维度成员的实际主科目。 

[![成本元素维度](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>通过数据连接器导入成本元素维度成员
为了便于设置成本核算中的成本元素维度成员，您可以使用预构建或您自定义构建的数据连接器检索一个或多个源系统中的主要成本元素。

## <a name="implementation-considerations"></a>实施注意事项
由于成本元素表示最低级别的成本详细信息，因此您应当确保在实施成本元素结构时包括管理报告所必需的所有成本元素。 为成本控制找出合适的成本元素数量是一项挑战。 如果有上千个成本元素，则难以控制每一个成本元素。 作为替代方案，您可以将成本元素分组，在聚合级别管理成本控制。




