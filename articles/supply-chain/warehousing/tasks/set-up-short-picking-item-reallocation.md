--- 
title: "设置领料短缺的物料重新分配"
description: "此过程显示如何启用仓库工作人员，以便在为其指示的库位的库存不足时，快速找到备用库位。"
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: fedd815cddfea4e00ed61ec6e176b633468c8fb2
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-short-picking-item-reallocation"></a>设置领料短缺的物料重新分配

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何启用仓库工作人员，以便在为其指示的库位的库存不足时，快速找到备用库位。 可以使用自动重新分配流程，该流程使用库位指令检索货物，前提是这些货物在另一个库位可用。 此外，如果使用手动重新分配，则移动设备上将显示库位列表和可用数量，供仓库工作人员选择使用哪个库位的库存。 您可以在演示数据公司 USMF 中使用此过程。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="set-up-work-exceptions"></a>设置工作异常
1. 转到“仓库管理”>“设置”>“工作”>“工作异常”。
2. 单击“新建”。
    * 可以使用不同物料重新分配策略定义多个工作异常，以便让仓库工作人员可以根据处理的装运需求选择一个。  
3. 在”工作异常代码“字段中，键入一个值。
    * 为工作异常分配标题以指示其用途。 例如，“手动领料短缺”。  
4. 在“描述”字段中，键入一个值。
5. 在“异常类型”字段中，选择“领料短缺”。
6. 选中“调整库存”复选框。
    * 此选项意味着领料短缺库位自动将库存调整为 0。  
7. 在“默认调整类型代码”字段中，输入或选择一个值。
    * 例如，在 USMF 中，可以选择“删除 Res Adj Out”。  
8. 在“物料重新分配”字段中，选择“手动”。
    * 如果选择“手动”或“自动和手动”，需要启用仓库工作人员才能使用手动重新分配。  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>设置工作人员以使用物料手动重新分配
1. 关闭该页面。
2. 转到“仓库管理”>“设置”>“工作人员”。
3. 单击“编辑”。
4. 在列表中，选择工作人员 24。
5. 展开“工作”部分。
6. 在“允许手动重新分配物料”字段中选择“是”。


