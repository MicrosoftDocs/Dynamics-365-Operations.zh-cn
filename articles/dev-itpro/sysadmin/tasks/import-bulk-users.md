--- 
title: "批量导入用户"
description: "系统管理员可通过此过程从 Azure Active Directory 导入大量用户。"
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 54af656c040486f7de718ce589973a6ebe005850
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="import-users-in-bulk"></a><span data-ttu-id="3a74f-103">批量导入用户</span><span class="sxs-lookup"><span data-stu-id="3a74f-103">Import users in bulk</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a74f-104">系统管理员可通过此过程从 Azure Active Directory 导入大量用户。</span><span class="sxs-lookup"><span data-stu-id="3a74f-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="3a74f-105">作为批处理作业运行</span><span class="sxs-lookup"><span data-stu-id="3a74f-105">Run as a batch job</span></span>
1. <span data-ttu-id="3a74f-106">转到“系统管理”>“用户”>“用户”。</span><span class="sxs-lookup"><span data-stu-id="3a74f-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="3a74f-107">单击“批量导入”。</span><span class="sxs-lookup"><span data-stu-id="3a74f-107">Click Batch import.</span></span>
3. <span data-ttu-id="3a74f-108">展开“后台运行”部分。</span><span class="sxs-lookup"><span data-stu-id="3a74f-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="3a74f-109">在“批处理”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="3a74f-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="3a74f-110">在“任务描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3a74f-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="3a74f-111">在“批处理组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3a74f-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="3a74f-112">这是可选步骤。</span><span class="sxs-lookup"><span data-stu-id="3a74f-112">This is an optional step.</span></span>  
7. <span data-ttu-id="3a74f-113">在“专用”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="3a74f-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="3a74f-114">这是可选步骤。</span><span class="sxs-lookup"><span data-stu-id="3a74f-114">This is an optional step.</span></span>  
8. <span data-ttu-id="3a74f-115">在“关键作业”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="3a74f-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="3a74f-116">这是可选步骤。</span><span class="sxs-lookup"><span data-stu-id="3a74f-116">This is an optional step.</span></span>  
9. <span data-ttu-id="3a74f-117">在“监视类别”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="3a74f-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="3a74f-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3a74f-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="3a74f-119">在沙盒环境中运行</span><span class="sxs-lookup"><span data-stu-id="3a74f-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="3a74f-120">单击“批量导入”。</span><span class="sxs-lookup"><span data-stu-id="3a74f-120">Click Batch import.</span></span>
2. <span data-ttu-id="3a74f-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3a74f-121">Click OK.</span></span>


