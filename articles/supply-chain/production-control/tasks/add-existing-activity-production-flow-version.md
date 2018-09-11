--- 
title: "将现有活动添加到生产流版本"
description: "创建生产流的新版本时，可以选择将为较低版本创建的活动添加到新版本。"
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a74fb34db71ba4b539c1b6ede361329aaeb94920
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>将现有活动添加到生产流版本

[!include [task guide banner](../../includes/task-guide-banner.md)]

创建生产流的新版本时，可以选择将为较低版本创建的活动添加到新版本。 此过程显示如何在不复制活动的情况下，为现有生产流创建新版本。 在下一步中，将现有活动添加到新版本。 

此任务需要已创建了版本和活动的生产流。


## <a name="create-a-new-production-flow-version"></a>创建新的生产流版本
1. 转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
4. 单击“编辑”。
5. 在列表中，标记所选的行。
6. 在“到期日期”字段中，输入日期和时间。
    * 请注意，创建新生产流版本之前，务必检查有效版本的到期日期和时间。 将使用有效开始日期创建新版本，用于连接到所选版本的到期日期。  
7. 单击“添加”。
8. 在“复制自版本”字段中选择“否”。
    * 如果复制的版本的大多数活动将替换为新活动，则选择“否”将从空版本开始。 将未更改的活动手动添加到活动窗体中“添加现有功能”内。  
9. 在“重复看板规则”字段中选择“否”。
    * 如果活动未复制到新版本，则不能在创建新版本时复制看板规则。   相反，您以后将在看板规则窗体中使用创建替换看板功能，以便将原来的生产流版本的看板规则替换为使用新版本的活动的看板规则。  
10. 单击“确定”。
11. 在列表中，找到并选择所需记录。

## <a name="add-an-existing-activity"></a>添加现有活动
1. 单击“活动”。
2. 单击“添加现有”打开下拉对话框。
    * 找到并选择要添加到新生产流版本的现有活动。  请注意，此列表为此生产流的所有以前版本显示为此生产流已创建的所有活动。  
3. 在“活动”字段中，输入或选择一个值。
4. 单击“确定”。


