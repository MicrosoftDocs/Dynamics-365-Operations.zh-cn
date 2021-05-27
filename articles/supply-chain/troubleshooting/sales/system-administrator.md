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
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="32578-103">系统管理员由于未被授权无法清除订单保留</span><span class="sxs-lookup"><span data-stu-id="32578-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="32578-104">知识库编号：4614642</span><span class="sxs-lookup"><span data-stu-id="32578-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="32578-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="32578-105">Symptoms</span></span>

<span data-ttu-id="32578-106">系统管理员无法清除销售订单保留，除非他们具有在订单保留代码中分配的特定角色。</span><span class="sxs-lookup"><span data-stu-id="32578-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="32578-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="32578-107">Resolution</span></span>

<span data-ttu-id="32578-108">对某些操作（如清除销售订单保留）的访问由设置业务策略驱动。</span><span class="sxs-lookup"><span data-stu-id="32578-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="32578-109">通常不允许系统管理员执行此类操作。</span><span class="sxs-lookup"><span data-stu-id="32578-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="32578-110">更多情况下，执行特定任务的访问权限由业务策略管理，组织中只有特定人员被批准执行该任务。</span><span class="sxs-lookup"><span data-stu-id="32578-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="32578-111">示例包括工作流审核产生的审核和工作流配置产生的特定任务。</span><span class="sxs-lookup"><span data-stu-id="32578-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="32578-112">虽然没有工作流与订单保留关联，但原理相似。</span><span class="sxs-lookup"><span data-stu-id="32578-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="32578-113">一个相关角色指定组织中有权清除订单保留的特定人员组。</span><span class="sxs-lookup"><span data-stu-id="32578-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="32578-114">此权限不一定授予所有管理员，因为该方法违反了定义的业务策略。</span><span class="sxs-lookup"><span data-stu-id="32578-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
