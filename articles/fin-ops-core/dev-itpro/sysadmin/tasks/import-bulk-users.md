---
title: 从 Azure Active Directory 导入用户
description: 系统管理员可通过此过程从 Azure Active Directory 手动导入所选用户或导入大量用户。
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b6666310309817ff30ccb3902721880b829ee0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679806"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="3b721-103">从 Azure Active Directory 导入用户</span><span class="sxs-lookup"><span data-stu-id="3b721-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="3b721-104">导入所选用户</span><span class="sxs-lookup"><span data-stu-id="3b721-104">Import select users</span></span>

<span data-ttu-id="3b721-105">系统管理员可通过此过程从 Azure Active Directory (Azure AD) 导入所选用户。</span><span class="sxs-lookup"><span data-stu-id="3b721-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="3b721-106">将使用当前会话公司作为默认公司导入用户。</span><span class="sxs-lookup"><span data-stu-id="3b721-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="3b721-107">导入用户之前，请更改当前公司（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="3b721-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="3b721-108">转到 **系统管理 > 用户 > 用户**。</span><span class="sxs-lookup"><span data-stu-id="3b721-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="3b721-109">单击 **导入用户**。</span><span class="sxs-lookup"><span data-stu-id="3b721-109">Click **Import users**.</span></span>
4. <span data-ttu-id="3b721-110">选择应导入的用户，然后选择 **导入用户**。</span><span class="sxs-lookup"><span data-stu-id="3b721-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="3b721-111">导入完成后，将需要为用户分配角色。</span><span class="sxs-lookup"><span data-stu-id="3b721-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="3b721-112">批量导入用户</span><span class="sxs-lookup"><span data-stu-id="3b721-112">Import users in bulk</span></span>

<span data-ttu-id="3b721-113">系统管理员可通过此过程从 Azure Active Directory 导入大量用户。</span><span class="sxs-lookup"><span data-stu-id="3b721-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="3b721-114">请注意，使用“批量导入”选项时不能选择用户。</span><span class="sxs-lookup"><span data-stu-id="3b721-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="3b721-115">将导入作为批处理作业运行</span><span class="sxs-lookup"><span data-stu-id="3b721-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="3b721-116">将使用当前会话公司作为默认公司导入用户。</span><span class="sxs-lookup"><span data-stu-id="3b721-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="3b721-117">导入用户之前，请更改当前公司（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="3b721-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="3b721-118">转到 **系统管理 > 用户 > 用户**。</span><span class="sxs-lookup"><span data-stu-id="3b721-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="3b721-119">单击 **批量导入**。</span><span class="sxs-lookup"><span data-stu-id="3b721-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="3b721-120">展开 **后台运行** 部分。</span><span class="sxs-lookup"><span data-stu-id="3b721-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="3b721-121">在 **批处理** 字段中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="3b721-121">Select \*\*Yes in the **Batch processing** field.</span></span>
6. <span data-ttu-id="3b721-122">在 **批处理组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3b721-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="3b721-123">这是可选步骤。</span><span class="sxs-lookup"><span data-stu-id="3b721-123">This is an optional step.</span></span>  
7. <span data-ttu-id="3b721-124">在 **专用** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="3b721-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="3b721-125">这是可选步骤。</span><span class="sxs-lookup"><span data-stu-id="3b721-125">This is an optional step.</span></span>  
8. <span data-ttu-id="3b721-126">在 **关键作业** 字段中，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="3b721-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="3b721-127">这是可选步骤。</span><span class="sxs-lookup"><span data-stu-id="3b721-127">bThis is an optional step.</span></span>  
9. <span data-ttu-id="3b721-128">在**监视类别**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="3b721-128">In the \*\*Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="3b721-129">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3b721-129">Click **OK**.</span></span>

<span data-ttu-id="3b721-130">导入完成后，将需要为用户分配角色。</span><span class="sxs-lookup"><span data-stu-id="3b721-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="3b721-131">在沙盒环境中运行</span><span class="sxs-lookup"><span data-stu-id="3b721-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="3b721-132">选择 **批量导入**。</span><span class="sxs-lookup"><span data-stu-id="3b721-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="3b721-133">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3b721-133">Select **OK**.</span></span>
