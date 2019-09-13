---
title: 配置人工和支出的标准成本
description: 本主题介绍如何为项目的人工和费用设置标准价。
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867718"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>配置人工和支出的标准成本

[!include [task guide banner](../../includes/task-guide-banner.md)]

本主题介绍如何为项目的人工和费用设置标准价。 此任务使用 USSI 数据集。

1. 在导航窗格中，转到**模块 > 项目管理与核算 > 设置 > 价格 > 成本价(工时)**。
2. 选择**新建**。
3. 在**生效日期**字段中，输入日期。
4. 在**成本价**字段中，输入一个数字。 可为项目类别设置标准成本价，也可以按照工作人员编号、项目编号、类别、日期以及它们的任何组合来设置成本价。 应用的成本价是最能提供详细信息的成本价。  
5. 选择**保存**。
6. 在导航窗格中，转到**模块 > 项目管理与核算 > 设置 > 价格 > 销售价(工时)**。
7. 选择**新建**。
8. 在**生效日期**字段中，输入日期。
9. 在**有效**字段中，选择一个选项。
10. 在**定价**字段中输入数字。 可以根据工时交易记录或按项目类别设置标准销售价。 也可以按工作人员编号、项目编号、类别、交易记录日期或其中任一组合设置销售价。 实际销售价是工作人员在“工时”日记帐中输入交易记录时应用的价格，它是具有最高详细级别的销售价。 例如，如果同时设置了一般销售价和工作人员特定的销售价，将使用工作人员特定的销售价。  
11. 选择**保存**。
12. 关闭该页面。
13. 在导航窗格中，转到**模块 > 项目管理与核算 > 设置 > 价格 > 成本价(支出)**。
14. 选择**新建**。
15. 在**生效日期**字段中，输入日期。
16. 在**成本价**字段中，输入一个数字。 可以填写多个字段，但是要保存记录，至少必须填写该字段。  
17. 选择**保存**。
18. 在导航窗格中，转到**模块 > 项目管理与核算 > 设置 > 价格 > 销售价(支出)**。
19. 选择**新建**。
20. 在**生效日期**字段中，输入日期。
21. 在**有效**字段中，选择一个选项。
22. 在**定价**字段中输入数字。 工作人员在费用日记帐凭证中输入交易记录时使用的实际销售价是最详细的销售价。 例如，如果同时设置了日记帐和工作人员特定的销售价，将使用工作人员特定的销售价。  
23. 选择**保存**。

