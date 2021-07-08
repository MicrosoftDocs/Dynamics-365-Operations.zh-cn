---
title: 主计划的参数不存在
description: 当您尝试确认计划订单时，将收到一条错误消息，表明主计划不存在任何参数。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294022"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="dfa89-103">主计划的参数不存在</span><span class="sxs-lookup"><span data-stu-id="dfa89-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="dfa89-104">错误代码：SYS25368</span><span class="sxs-lookup"><span data-stu-id="dfa89-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="dfa89-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="dfa89-105">Symptoms</span></span>

<span data-ttu-id="dfa89-106">当您尝试确认计划订单时，将收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="dfa89-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="dfa89-107">主计划 %1 的参数不存在。</span><span class="sxs-lookup"><span data-stu-id="dfa89-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="dfa89-108">原因</span><span class="sxs-lookup"><span data-stu-id="dfa89-108">Cause</span></span>

<span data-ttu-id="dfa89-109">由于配置问题，系统找不到指定计划的设置。</span><span class="sxs-lookup"><span data-stu-id="dfa89-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="dfa89-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="dfa89-110">Resolution</span></span>

- <span data-ttu-id="dfa89-111">转到 **主计划 \> 设置 \> 计划 \> 主计划**，并确保存在具有指定名称的计划。</span><span class="sxs-lookup"><span data-stu-id="dfa89-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
