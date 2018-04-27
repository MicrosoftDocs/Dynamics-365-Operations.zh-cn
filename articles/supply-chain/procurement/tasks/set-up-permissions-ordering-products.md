--- 
title: "代表他人设置产品订购权限"
description: "此过程演示如何为工作人员授予代表其他工作人员起草采购申请的权限。"
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e003f953c05facd5516e2bfa6d1c83ba6381c15
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>代表他人设置产品订购权限

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

此过程演示如何为工作人员授予代表其他工作人员起草采购申请的权限。 换句话说，采购申请“准备人”可以为其他“申请人”创建申请。 此过程还演示如何为工作人员授予在不同法人或营运单位中订购物料和服务的权限。 这些任务通常由采购经理执行。 您可以在此过程中使用 USMF 演示数据公司的数据，也可以使用您自己的数据。


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>授予代表其他工作人员输入采购申请的权限
1. 转到“采购”>“设置”>“政策”>“采购申请权限”。
    * 确保“当前视图”字段设置为“按准备人”。  左窗格中的列表显示已授予为代表其他人起草申请的权限的人员。  
2. 选择要为其授予（准备人）权限的人员。
3. 单击“添加”。
4. 找到并选择要添加为申请人的人员。
    * 申请人是可被准备人代表创建申请的人员。  
    * 如果准备人应该可以代表所选工作人员创建采购申请，请在“授权”字段中选择“特定”。 如果准备人还需要可以代表向工作人员报告的所有工作人员创建采购申请，请选择“报告”。  
5. 在”生效日期“字段，输入日期。
6. 在“截止日期”字段，输入日期。

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>查看有权为所选工作人员创建采购申请的准备人
1. 在“当前视图”字段中，选择“按申请人”。
    * 此视图显示已授予为代表所选工作人员创建采购业务申请权限的准备人列表。  
2. 使用快速筛选器查找您刚才添加为申请人的工作人员。
3. 选择该申请人。
    * “准备人”列表显示有权代表左窗格中选择的申请人订购物料的人员。   您可以在此处添加更多准备人。   此视图还可用于为申请人授予在非该人的主法人或运营单位的法人和营运单位中创建申请的权限。  


