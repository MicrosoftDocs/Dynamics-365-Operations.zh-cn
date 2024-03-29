---
title: 创建 POS 权限组
description: 本文介绍如何创建 POS 权限组。
author: josaw1
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailPosPermissionGroup, HcmJob
ms.openlocfilehash: 0aa394e5dc6685954c31cdddae7cdc042b80af29
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277952"
---
# <a name="create-pos-permission-groups"></a>创建 POS 权限组

[!include [banner](../includes/banner.md)]

本文介绍如何创建 POS 权限组。 创建此任务的演示数据公司是 USRT。 此任务旨在面向商业运营经理角色。

1. 在导航窗格中，转到 **模块 > Retail 和 Commerce > 员工 > 权限组**。
2. 选择 **新建**。
3. 在 **POS 权限组 ID** 字段中，输入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 选择 **查看时钟条目** 字段中的 **是**。 您现在可以启用或禁用您的 POS 权限组的各种权限。 对于某些权限，您可以设置一个值，以用于评估 POS 用户是否可以执行该操作。 此任务指南会启用某些可能提供给出纳员的权限。  
6. 选择 **允许创建订单** 字段中的 **是**。
7. 选择 **允许编辑订单** 字段中的 **是**。
8. 选择 **允许检索订单** 字段中的 **是**。
9. 选择 **允许密码更改** 字段中的 **是**。
10. 选择 **允许直接结束** 字段中的 **是**。
11. 选择 **保存**。 在您的更改保存之后，您需要运行“人员分配计划”，以将这些更改发布到商业渠道。 
12. 在导航窗格中，转到 **导航窗格 > 模块 > 人力资源 > 作业 > 作业**。
13. 接下来，我们会将 POS 权限组分配到某一作业。 在列表中，找到并选择所需记录。
14. 选择 **编辑**。
15. 展开 **工作分类** 部分。
16. 在“POS 权限组 ID”字段中，输入或选择一个值。 除非工作人员 POS 权限已在其职位级别进行覆写，此作业所对应职位的所有工作人员都将使用此 POS 权限组的设置。  
17. 选择 **保存**。 在您的更改保存之后，您需要运行“人员分配计划”，以将这些更改发布到渠道。  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
