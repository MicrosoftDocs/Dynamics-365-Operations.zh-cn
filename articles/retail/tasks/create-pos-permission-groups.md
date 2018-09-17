--- 
title: "创建 POS 权限组"
description: "此程序将会显示如何创建 POS 权限组。"
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: bcda7c3a5c2cc97fbc6e4945e4d5f0ec42a7a478
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---
# <a name="create-pos-permission-groups"></a>创建 POS 权限组

[!include[task guide banner](../includes/task-guide-banner.md)]

此程序将会显示如何创建 POS 权限组。 创建此任务的演示数据公司是 USRT。 此任务旨在面向零售运营经理。

1. 转至“权限组”。
2. 单击“新建”。
3. 在“POS 权限组 ID”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。
5. 选择“查看时钟条目”字段中的“是”。
    * 您现在可以启用或禁用您的 POS 权限组的各种权限。 对于某些权限，您可以设置一个值，以用于评估 POS 用户是否可以执行该操作。  此任务指南会启用某些可能提供给出纳员的权限。  
6. 选择“允许创建订单”字段中的“是”。
7. 选择“允许编辑订单”字段中的“是”。
8. 选择“允许检索订单”字段中的“是”。
9. 选择“允许密码更改”字段中的“是”。
10. 选择“允许直接结束”字段中的“是”。
11. 单击“保存”。
    * 在您的更改保存之后，您需要运行“人员分配计划”，以将这些更改应用到零售渠道。  
12. 关闭该页面。
13. 转至“作业”。
    * 接下来，我们会将 POS 权限组分配到某一作业。  
14. 在列表中，找到并选择所需记录。
15. 在列表中，单击所选行中的链接。
16. 单击“编辑”。
17. 展开“工作分类”部分。
18. 在“POS 权限组 ID”字段中，输入或选择一个值。
    * 除非工作人员 POS 权限已在其职位级别进行覆写，此作业所对应职位的所有工作人员都将使用此 POS 权限组的设置。  
19. 单击“保存”。
    * 在您的更改保存之后，您需要运行“人员分配计划”，以将这些更改应用到零售渠道。  


