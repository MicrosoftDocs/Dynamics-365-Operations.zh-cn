---
title: 工作未锁定
description: 工作未锁定
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924196"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="91005-103">工作未锁定</span><span class="sxs-lookup"><span data-stu-id="91005-103">Work isn't blocked</span></span>

<span data-ttu-id="91005-104">错误代码：WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="91005-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="91005-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="91005-105">Symptoms</span></span>

<span data-ttu-id="91005-106">系统将显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="91005-106">The system shows the following error message:</span></span>

> <span data-ttu-id="91005-107">未锁定 ID 为 %1 的工作。</span><span class="sxs-lookup"><span data-stu-id="91005-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="91005-108">原因</span><span class="sxs-lookup"><span data-stu-id="91005-108">Cause</span></span>

<span data-ttu-id="91005-109">波次上的 **锁定波次** 选项设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="91005-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="91005-110">工作无法解锁，因为其当前未被锁定。</span><span class="sxs-lookup"><span data-stu-id="91005-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="91005-111">解决方法</span><span class="sxs-lookup"><span data-stu-id="91005-111">Resolution</span></span>

 <span data-ttu-id="91005-112">仅 **锁定波次** 选项设置为 *是* 的工作可以解锁。</span><span class="sxs-lookup"><span data-stu-id="91005-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
