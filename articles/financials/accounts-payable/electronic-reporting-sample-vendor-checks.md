---
title: "电子申报示例供应商支票"
description: "此主题提供有关如何使用电子申报示例支票格式的一般信息。"
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c9abea228cdaae84ca2b9aada9f36bbe79c1dc6b
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a>电子申报示例支票格式

您可以使用电子申报 (ER) 来确定供应商支票格式。 市场上提供许多银行和支票提供商特定的支票格式。 ER 工具库中的付款支票模型已经包含示例支票格式。 这些示例支票标记为**支票在中间（美国）**和**支票在上面，存根在下面（美国）**。

## <a name="what-check-formats-are-currently-supported"></a>目前支持哪些支票格式？

应始终转至 Microsoft Dynamics Lifecycle Services (LCS) 中的共享资产库，并查看资产类型为 **GER 配置**的可用文件的当前列表。 下一部分“必须执行哪些设置？”包括一个主题的链接，该主题说明如何创建 LCS 存储库以检查可用配置和导入所选配置。

Microsoft Dynamics 365 for Finance and Operations Enterprise 版本包括一个示例格式，其中支票位于顶部，后面是两个汇款部分。 它还包括一个示例格式，其中支票在中间，后面是两个汇款部分。 这些示例格式对应于 Deluxe 公司支票格式。

## <a name="what-do-i-have-to-set-up"></a>我必须设置什么？

- 在您可以使用 ER 打印支票前，必须导入至少一个有效的支票配置到您的 ER 配置。 有关说明，请参阅[从 Lifecycle Services 下载电子申报配置](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)。
- 为银行帐户配置现金和银行管理支票时，选择**一般电子导出格式**复选框，然后选择相应的支票格式作为导出格式配置。
- 您还必须指定汇款上要打印的清单行的数量。 计算此数量时务必包括标头行。 对于这两种示例支票格式，建议的清单行数量为 17。 但是，该数量将根据您的支票库存和打印机驱动程序而有所不同。
- 我们建议您打印一份测试支票以验证支票版式。 若要测试打印支票，请选择**打印测试**选项。 当 Microsoft Excel 的高级打印机属性中的**边距**设置为**无**时，示例支票格式的效果最佳。 生成测试支票后，启用编辑 Excel 输出并配置页面布局，以便所有边距设置为 **0**（零）。 比较支票的测试副本与您的支票库存，并调整设置，直到您对对齐方式满意。
- 为在付款日记帐中配置的银行帐户生成付款时，将使用指定的格式打印支票。

有关详细信息，请参阅 [修改电子申报格式](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md)。

