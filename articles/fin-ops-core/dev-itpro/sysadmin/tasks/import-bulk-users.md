---
title: 从 Azure Active Directory 导入用户
description: 系统管理员可通过此过程从 Azure Active Directory 手动导入所选用户或导入大量用户。
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9f03ae7197790c1aac6ebf3cb94ff7963b1291e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745781"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="2ace6-103">从 Azure Active Directory 导入用户</span><span class="sxs-lookup"><span data-stu-id="2ace6-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="2ace6-104">导入所选用户</span><span class="sxs-lookup"><span data-stu-id="2ace6-104">Import select users</span></span>

<span data-ttu-id="2ace6-105">系统管理员可通过此过程从 Azure Active Directory (Azure AD) 导入所选用户。</span><span class="sxs-lookup"><span data-stu-id="2ace6-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="2ace6-106">将使用当前会话公司作为默认公司导入用户。</span><span class="sxs-lookup"><span data-stu-id="2ace6-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="2ace6-107">导入用户之前，请更改当前公司（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="2ace6-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="2ace6-108">转到 **系统管理 > 用户 > 用户**。</span><span class="sxs-lookup"><span data-stu-id="2ace6-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="2ace6-109">单击 **导入用户**。</span><span class="sxs-lookup"><span data-stu-id="2ace6-109">Click **Import users**.</span></span>
4. <span data-ttu-id="2ace6-110">选择应导入的用户，然后选择 **导入用户**。</span><span class="sxs-lookup"><span data-stu-id="2ace6-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="2ace6-111">导入完成后，将需要为用户分配角色。</span><span class="sxs-lookup"><span data-stu-id="2ace6-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="2ace6-112">批量导入用户</span><span class="sxs-lookup"><span data-stu-id="2ace6-112">Import users in bulk</span></span>

<span data-ttu-id="2ace6-113">系统管理员可通过此过程从 Azure Active Directory 导入大量用户。</span><span class="sxs-lookup"><span data-stu-id="2ace6-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="2ace6-114">请注意，使用“批量导入”选项时不能选择用户。</span><span class="sxs-lookup"><span data-stu-id="2ace6-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="2ace6-115">将导入作为批处理作业运行</span><span class="sxs-lookup"><span data-stu-id="2ace6-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="2ace6-116">将使用当前会话公司作为默认公司导入用户。</span><span class="sxs-lookup"><span data-stu-id="2ace6-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="2ace6-117">导入用户之前，请更改当前公司（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="2ace6-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="2ace6-118">转到 **系统管理 > 用户 > 用户**。</span><span class="sxs-lookup"><span data-stu-id="2ace6-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="2ace6-119">单击 **批量导入**。</span><span class="sxs-lookup"><span data-stu-id="2ace6-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="2ace6-120">展开 **后台运行** 部分。</span><span class="sxs-lookup"><span data-stu-id="2ace6-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="2ace6-121">在 **批处理** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="2ace6-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="2ace6-122">在 **批处理组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2ace6-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="2ace6-123">这是可选步骤。</span><span class="sxs-lookup"><span data-stu-id="2ace6-123">This is an optional step.</span></span>  
7. <span data-ttu-id="2ace6-124">在 **专用** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="2ace6-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="2ace6-125">这是可选步骤。</span><span class="sxs-lookup"><span data-stu-id="2ace6-125">This is an optional step.</span></span>  
8. <span data-ttu-id="2ace6-126">在 **关键作业** 字段中，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="2ace6-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="2ace6-127">这是可选步骤。</span><span class="sxs-lookup"><span data-stu-id="2ace6-127">This is an optional step.</span></span>  
9. <span data-ttu-id="2ace6-128">在 **监视类别** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="2ace6-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="2ace6-129">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="2ace6-129">Click **OK**.</span></span>

<span data-ttu-id="2ace6-130">导入完成后，将需要为用户分配角色。</span><span class="sxs-lookup"><span data-stu-id="2ace6-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="2ace6-131">在沙盒环境中运行</span><span class="sxs-lookup"><span data-stu-id="2ace6-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="2ace6-132">选择 **批量导入**。</span><span class="sxs-lookup"><span data-stu-id="2ace6-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="2ace6-133">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="2ace6-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]