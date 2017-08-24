--- 
title: "在物料对于工作单元不可用时准备处理看板作业"
description: "此过程的重点是在某些物料不可用于工作单元时准备流程看板作业，因此对于从仓库领料很有必要。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4899c1d0baebb451e665853767e64f660ca25ca6
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>在物料对于工作单元不可用时准备处理看板作业

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程的重点是在某些物料不可用于工作单元时准备流程看板作业，因此对于从仓库领料很有必要。 “在物料可用时准备流程看板作业”这一过程是创建此过程的先决条件。 此过程是专为机器操作员设计的。 创建此程序的演示数据公司是 USMF。

1. 转到“生产控制”>“看板”>“处理作业的看板面板”。
2. 在“工作单元”字段中，单击下拉按钮打开查找。
3. 在列表中，单击所选行中的链接。
    * 选择 1250 号工作单元。  
4. 在列表中，找到并选择所需记录。
    * 选择看板 000356。  
5. 在列表中，找到并选择所需记录。
    * 在列表中，取消选择行 4。 或者如果您未完成“在物料可用时准备流程看板作业”这一任务，请选择行 4。  
6. 切换“领料单”部分的展开项。
    * 供应状态中的“无条目”图标指示工作单元缺少物料 P0002 的 48 ea。  

## <a name="transfer-materials-to-work-cell"></a>转移物料到工作单元
1. 切换“转移作业”部分的展开项。
2. 使用“快速筛选”来筛选带有值“P0002”的“物料编号”字段。
3. 在列表中，找到并选择所需记录。
4. 单击“开始”。
    * 正在转换中。  
5. 单击“完成”。
    * 物料 P0002 现在可用于看板作业的领料单。 这意味着我们可以为看板准备所有所需的物料。  
6. 单击“准备”。
    * 请注意，作业状态的图标指示作业现在可供处理。  


