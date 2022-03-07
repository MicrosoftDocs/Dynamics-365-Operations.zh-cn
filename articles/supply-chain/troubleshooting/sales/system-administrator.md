---
title: 系统管理员由于未被授权无法清除订单保留
description: 系统管理员由于未被授权无法清除订单保留。
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026320"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>系统管理员由于未被授权无法清除订单保留

知识库编号：4614642

## <a name="symptoms"></a>故障特征

系统管理员无法清除销售订单保留，除非他们具有在订单保留代码中分配的特定角色。

## <a name="resolution"></a>解决方法

对某些操作（如清除销售订单保留）的访问由设置业务策略驱动。 通常不允许系统管理员执行此类操作。 

更多情况下，执行特定任务的访问权限由业务策略管理，组织中只有特定人员被批准执行该任务。 示例包括工作流审核产生的审核和工作流配置产生的特定任务。

虽然没有工作流与订单保留关联，但原理相似。 一个相关角色指定组织中有权清除订单保留的特定人员组。 此权限不一定授予所有管理员，因为该方法违反了定义的业务策略。
