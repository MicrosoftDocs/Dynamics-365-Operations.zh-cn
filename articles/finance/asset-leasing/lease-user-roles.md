---
title: 分配租赁用户角色
description: 本主题描述资产租赁中使用的安全角色。 它还说明了如何将用户分配给这些角色。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b31d0880d4f2cd2b8ad2dffcfe279421f935ed35
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440962"
---
# <a name="assign-lease-user-roles"></a>分配租赁用户角色

[!include [banner](../includes/banner.md)]

本主题描述资产租赁中使用的安全角色。 它还说明了如何将用户分配给这些角色。

三个用户角色区分资产租赁中的访问权限。 一种角色适合于维护租赁，一种角色适合于查看租赁，而另一种角色适合于履行租赁业务员的职责。 每个角色有所有租赁页面的特定权限，并且每个角色都允许用户根据其工作职责查看，创建，编辑或删除租赁。

| 角色           | 说明 |
|----------------|-------------|
| 维护租赁 | 此角色的用户可以添加，编辑，删除和查看租赁。 该角色是为日常用户设计的，这些用户的任务包括创建和发布月度日记帐条目和添加新租赁。 此角色提供所有资产租赁功能的访问权限。 |
| 查看租赁     | 此角色的用户只能查看租赁记录，计划和运行报告。 不能创建新租赁，编辑现有租赁或根据租赁创建日记帐条目。 该角色是为只需要查看租赁，租赁计划以及针对这些租赁发生的交易的用户设计的。 |
| 租赁业务员    | 此角色的用户只能创建新租赁。 不能编辑或删除现有租赁，查看租赁计划或过帐租赁日记帐条目。 该角色是为执行数据输入功能的用户设计的。 |

请按照以下步骤将用户分配给资产租赁中使用的角色。

1. 转到 **系统管理 \> 安全 \> 将用户分配到角色**。
2. 选择 **维护租赁**、**租赁业务员** 或 **查看租赁** 角色，然后选择 **手动分配/排除用户**。
3. 选择要分配给该角色的用户，然后选择 **分配给角色**。
