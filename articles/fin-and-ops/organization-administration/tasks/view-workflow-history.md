---
title: 查看工作流历史记录
description: 使用这些步骤可以查看提交给工作流系统进行处理和审核的单据的状态。
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a40fe377322e2d64b751f6cace3eda20736cd321
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560444"
---
# <a name="view-workflow-history"></a>查看工作流历史记录

[!include [task guide banner](../../includes/task-guide-banner.md)]

使用这些步骤可以查看提交给工作流系统进行处理和审核的单据的状态。 创建此程序的演示数据公司是 USMF。

1. 转到“常用 > 查询 > 工作流 > 工作流历史记录”。
    * 使用此窗体可以查看提交给工作流系统进行处理和审核的单据的状态。  
    * “实例 ID”是正在处理或已经处理单据的工作流实例的标识代码。  
    * “状态”是单据的工作流状态。  
    * “工作流 ID”是正在处理或已经处理单据的工作流的标识代码。  
    * “单据”是单据的标识代码。  
    * “单据类型”是提交以处理的单据的类型。  
    * “工作流”是正在处理或已经处理单据的工作流的名称。  
    * “版本”是正在处理或已经处理单据的工作流的版本号。  
    * “创建日期和时间”是是提交单据的日期和时间。  
    * “占用时间”是自单据提交后经过的时间。  
    * “可通过”恢复“按钮恢复所选单据的工作流。  
    * 可通过”撤消“按钮撤消所选单据，以便不处理该单据。   
2. 在列表中，单击所选行中的链接。
    * 确保已展开“工作项”部分。    在此部分中，可以查看与所选单据关联的工作项。 例如，可能必须完成某项任务，或者可能必须审核单据。  
    * “重新分配”按钮将打开一个对话框，从中可向其他用户重新分配工作项。  
    * 确保已展开“跟踪详细信息”部分。    在此部分中，可以查看所选单据的工作流历史记录。  

