--- 
title: "计算各个法人的固定资产折旧"
description: "此过程显示如何设置和运行多个法人的折旧过程。"
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: zh-cn
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>计算各个法人的固定资产折旧

[!include [task guide banner](../../includes/task-guide-banner.md)]

固定资产折旧可以一步跨多个法人运行。 此过程显示如何设置和运行多个法人的过程。 它使用会计师角色。  

此记录使用 USMF 公司演示。


步骤 (16) 子任务：设置跨公司折旧运行日记帐。 

1. 首先，必须设置用于在每个法人中运行的跨公司折扣的日记帐。 转到固定资产>设置>固定资产参数。 
2. 展开“固定资产方案”部分。 
3. 创建具有要用于法人中的每个过帐层的日记帐名称的记录。 如果帐簿不过帐到总帐，则不应选则具有关联日记帐的过帐层。 单击“添加”。 
4. 在“过帐层”字段中，输入或选择一个值。 
5. 在“日记帐名称”字段中，输入或选择一个值。 
6. 在每个法人中的固定资产参数页面上重复日记帐设置。 

子任务：计算折旧

1. 使用“创建折旧方案”页开始在法人中运行折旧。 转到“固定资产”>“日记帐条目”>“创建折旧方案”。 
2. 在“过帐层”字段中，输入或选择一个值。 
3. 日记帐名称默认来自固定资产参数。 当前法人的日记帐名称可以在此处更改。 
4. 在“结束日期”字段中输入日期。 
5. 选择要包括在折旧运行中的法人。 仅具有在固定资产参数页面为固定资产方案设置的日记帐的法人才会在列表中显示。 
6. 启用后，“过帐日记帐”选项将在折旧日记帐创建时自动过帐它们。 如果未选择，将创建日记帐，但不会过帐，因此，您可以在过帐前查看详细信息。 在“过帐日记帐”字段中选择“是”。 
7. 筛选字段包括为此折旧运行选择的法人的所有固定资产、组和帐簿。 
8. “批处理”选项默认情况下启用。 启用此选项后，折旧日记帐创建和过帐将在后台运行。 
9. 单击“创建日记帐”。 
10. 您必须查看在各自的法人创建的折旧日记帐。 转到固定资产>流水输入项>固定资产流水。

