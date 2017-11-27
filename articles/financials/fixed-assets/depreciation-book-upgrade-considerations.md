---
title: "折旧帐簿升级概览"
description: "在以前的版本中，固定资产有两种评估概念 - 价值模型和折旧帐簿。 在 Microsoft Dynamics 365 for Operations (1611) 中，价值模型功能和折旧帐簿功能已经合并为一个概念，即帐簿。 本主题介绍升级时的考虑事项。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e95fa9dd15dfe5e6b26de61b5dbc1a9a6c0d768d
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="depreciation-book-upgrade-overview"></a><span data-ttu-id="2bccf-105">折旧帐簿升级概览</span><span class="sxs-lookup"><span data-stu-id="2bccf-105">Depreciation book upgrade overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2bccf-106">在以前的版本中，固定资产有两种评估概念 - 价值模型和折旧帐簿。</span><span class="sxs-lookup"><span data-stu-id="2bccf-106">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="2bccf-107">在 Microsoft Dynamics 365 for Operations (1611) 中，价值模型功能和折旧帐簿功能已经合并为一个概念，即帐簿。</span><span class="sxs-lookup"><span data-stu-id="2bccf-107">In Microsoft Dynamics 365 for Operations (1611), the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span> <span data-ttu-id="2bccf-108">本主题介绍升级时的考虑事项。</span><span class="sxs-lookup"><span data-stu-id="2bccf-108">This topic provides some things to consider for the upgrade.</span></span> 

<span data-ttu-id="2bccf-109">升级流程会将您的现有设置和所有现有交易记录移动到新的帐簿结构。</span><span class="sxs-lookup"><span data-stu-id="2bccf-109">The upgrade process will move your existing setup and all existing transactions to the new book structure.</span></span> <span data-ttu-id="2bccf-110">价值模型将依照保留当前状态，作为过帐到总帐的帐簿。</span><span class="sxs-lookup"><span data-stu-id="2bccf-110">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="2bccf-111">折旧帐簿将移至“**过帐到总帐**”设置为“**否**”的帐簿。</span><span class="sxs-lookup"><span data-stu-id="2bccf-111">Depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="2bccf-112">折旧帐簿日记帐名称将移动到过帐层设置为**无**的总帐日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="2bccf-112">Depreciation book journal names will be moved to a general ledger journal name with the posting layer set to **None**.</span></span> <span data-ttu-id="2bccf-113">折旧帐簿交易记录将移到固定资产交易记录。</span><span class="sxs-lookup"><span data-stu-id="2bccf-113">Depreciation book transactions will be moved to Fixed asset transactions.</span></span> 

<span data-ttu-id="2bccf-114">在运行数据升级之前，应了解将折旧帐簿日志行升级到交易记录凭证的两个选项以及凭证系列将要使用的编号规则。</span><span class="sxs-lookup"><span data-stu-id="2bccf-114">Before running the data upgrade, you should understand the two options available for upgrading depreciation book journal lines to transaction vouchers, and the number sequence that will be used for the voucher series.</span></span> 

<span data-ttu-id="2bccf-115">选项 1：**系统定义的编号规则** -这是优化升级性能的默认选项。</span><span class="sxs-lookup"><span data-stu-id="2bccf-115">Option 1:  **System-defined number sequence** - This is the default option to optimize upgrade performance.</span></span> <span data-ttu-id="2bccf-116">升级不使用编号规则框架，而是使用基于设置的方法分配凭证。</span><span class="sxs-lookup"><span data-stu-id="2bccf-116">The upgrade will not use the number sequences framework, but instead will allocate vouchers with a set-based approach.</span></span> <span data-ttu-id="2bccf-117">升级后，将基于升级的交易记录使用适当的**下一个编号集**创建新的编号规则。</span><span class="sxs-lookup"><span data-stu-id="2bccf-117">After the upgrade, the new number sequence will be created with the **Next number set** appropriately based on the upgraded transactions.</span></span> <span data-ttu-id="2bccf-118">默认情况下，编号规则将以 FADBUpgr\#\#\#\#\#\#\#\#\# 格式使用。</span><span class="sxs-lookup"><span data-stu-id="2bccf-118">By default, the number sequence used will be in the FADBUpgr\#\#\#\#\#\#\#\#\# format.</span></span> <span data-ttu-id="2bccf-119">使用此方法时有一些参数可供您调整格式：</span><span class="sxs-lookup"><span data-stu-id="2bccf-119">There are a few parameters available to you to adjust the format when using this approach:</span></span>

-   <span data-ttu-id="2bccf-120">**编号规则代码** – 标识编号规则的代码。</span><span class="sxs-lookup"><span data-stu-id="2bccf-120">**Number sequence code** – The code to identify the number sequence.</span></span> <span data-ttu-id="2bccf-121">此编号规则代码不存在，因为它将通过升级创建。</span><span class="sxs-lookup"><span data-stu-id="2bccf-121">This number sequence code cannot exist since it will be created by the upgrade.</span></span>
    -   <span data-ttu-id="2bccf-122">常量名称：**NumberSequenceDefaultCode**</span><span class="sxs-lookup"><span data-stu-id="2bccf-122">Constant name: **NumberSequenceDefaultCode**</span></span>
    -   <span data-ttu-id="2bccf-123">默认值："FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="2bccf-123">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="2bccf-124">**前缀** - 将用作凭证号前缀的常量字符串。</span><span class="sxs-lookup"><span data-stu-id="2bccf-124">**Prefix** – The constant string value that will be used as a prefix for the voucher numbers.</span></span>
    -   <span data-ttu-id="2bccf-125">常量名称：**NumberSequenceDefaultParameterPrefix**</span><span class="sxs-lookup"><span data-stu-id="2bccf-125">Constant name: **NumberSequenceDefaultParameterPrefix**</span></span>
    -   <span data-ttu-id="2bccf-126">默认值："FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="2bccf-126">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="2bccf-127">**字母数字的长度** – 编号规则的字母数字段的长度。</span><span class="sxs-lookup"><span data-stu-id="2bccf-127">**Alphanumeric length** – The length of the alphanumeric segment of the number sequence.</span></span>
    -   <span data-ttu-id="2bccf-128">常量名称：**NumberSequenceDefaultParameterAlpanumericLength**</span><span class="sxs-lookup"><span data-stu-id="2bccf-128">Constant name: **NumberSequenceDefaultParameterAlpanumericLength **</span></span>
    -   <span data-ttu-id="2bccf-129">默认值：9</span><span class="sxs-lookup"><span data-stu-id="2bccf-129">Default value: 9</span></span>
-   <span data-ttu-id="2bccf-130">**开始编号** - 编号规则要使用的第一个数字。</span><span class="sxs-lookup"><span data-stu-id="2bccf-130">**Start number** - The first number to be used in the number sequence.</span></span>
    -   <span data-ttu-id="2bccf-131">常量名称：**NumberSequenceDefaultParameterStartNumber**</span><span class="sxs-lookup"><span data-stu-id="2bccf-131">Constant name: **NumberSequenceDefaultParameterStartNumber  **</span></span>
    -   <span data-ttu-id="2bccf-132">默认值：1</span><span class="sxs-lookup"><span data-stu-id="2bccf-132">Default value: 1</span></span>

<span data-ttu-id="2bccf-133">选项 2：**现有的用户定义的编号规则** -此选项允许您定义升级时要使用的编号规则。</span><span class="sxs-lookup"><span data-stu-id="2bccf-133">Option 2: **Existing user-defined number sequence** - This option will allow you to define the number sequence to be used for the upgrade.</span></span> <span data-ttu-id="2bccf-134">如果需要高级编号规则配置，则考虑使用此选项。</span><span class="sxs-lookup"><span data-stu-id="2bccf-134">Consider using this option if you need advanced number sequence configuration.</span></span> <span data-ttu-id="2bccf-135">要使用编号规则，必须使用以下信息修改升级类 ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans：</span><span class="sxs-lookup"><span data-stu-id="2bccf-135">To use a number sequence, you must modify the upgrade class ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans with the following information:</span></span>

-   <span data-ttu-id="2bccf-136">**编号规则代码** – 编号规则的代码。</span><span class="sxs-lookup"><span data-stu-id="2bccf-136">**Number sequence code** – The code of the number sequence.</span></span>
    -   <span data-ttu-id="2bccf-137">常量名称：**NumberSequenceExistingCode**</span><span class="sxs-lookup"><span data-stu-id="2bccf-137">Constant name: **NumberSequenceExistingCode **</span></span>
    -   <span data-ttu-id="2bccf-138">默认值：无默认值，必须更新到编号规则代码。</span><span class="sxs-lookup"><span data-stu-id="2bccf-138">Default value: No default, this must be updated to the number sequence code.</span></span>
-   <span data-ttu-id="2bccf-139">**共享编号规则** – 标识编号规则的作用域的布尔值。</span><span class="sxs-lookup"><span data-stu-id="2bccf-139">**Shared number sequence** – A boolean value to identify the scope of the number sequence.</span></span> <span data-ttu-id="2bccf-140">对所有公司的共享编号规则使用“true”，对特定公司的作用域使用“false”。</span><span class="sxs-lookup"><span data-stu-id="2bccf-140">Use "true" for shared number sequences across all companies, and "false" for a company-specific scope.</span></span> <span data-ttu-id="2bccf-141">使用“false”时，含有折旧帐簿交易记录的每一个公司都必须存在具有指定名称的编号规则。</span><span class="sxs-lookup"><span data-stu-id="2bccf-141">When using "false", the number sequence with the specified name must exist in every company that contains depreciation book transactions.</span></span> <span data-ttu-id="2bccf-142">含有折旧帐簿交易记录的每一个分区都存在共享编号规则。</span><span class="sxs-lookup"><span data-stu-id="2bccf-142">Shared number sequences exist in every partition that contains depreciation book transactions.</span></span>
    -   <span data-ttu-id="2bccf-143">常量名称：**NumberSequenceExistingIsShared**</span><span class="sxs-lookup"><span data-stu-id="2bccf-143">Constant name: **NumberSequenceExistingIsShared **</span></span>
    -   <span data-ttu-id="2bccf-144">默认值：true</span><span class="sxs-lookup"><span data-stu-id="2bccf-144">Default value: true</span></span>

<span data-ttu-id="2bccf-145">参数位于 ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans 类的开头。</span><span class="sxs-lookup"><span data-stu-id="2bccf-145">The parameters are located at the beginning of the ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class.</span></span> 

<span data-ttu-id="2bccf-146">*// 指定凭证分配的首选方法* 
*// true，如果您要使用现有的编号规则代码* 
*// false，如果您要使用系统定义的编号规则（默认）* const boolean NumberSequenceUseExistingCode = false;</span><span class="sxs-lookup"><span data-stu-id="2bccf-146">*// Specify a preferable approach of vouchers allocation* 
*// true, if you want to use an existing number sequence code* 
*// false, if you intend to use the system-defined number sequence (default)* const boolean NumberSequenceUseExistingCode = false;</span></span>  

<span data-ttu-id="2bccf-147">*// 如果使用系统定义的编号规则方法，则指定编号规则的参数。*
*// 将使用这些参数创建新的编号规则。*</span><span class="sxs-lookup"><span data-stu-id="2bccf-147">*// If using the system-defined number sequence approach, specify the parameters for the number sequence.*
*// A new number sequence will be created with these parameters.*</span></span> <span data-ttu-id="2bccf-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span><span class="sxs-lookup"><span data-stu-id="2bccf-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span></span>   

<span data-ttu-id="2bccf-149">*// 如果使用现有编号规则方法，则指定现有的编号规则代码。* 
*// 将对现有的编号规则逐行进行凭证分配。*</span><span class="sxs-lookup"><span data-stu-id="2bccf-149">*// If using the existing number sequence approach, specify the existing number sequence code.* 
*// Voucher allocation will go row-by-row for existing number sequences.*</span></span> <span data-ttu-id="2bccf-150">const str NumberSequenceExistingCode = ''; *// 指定现有编号规则代码的作用域* 
*// true，如果指定的编号规则为共享* 
*// false，如果指定的编号规则为针对特定公司* 
*// 如果未找到具有指定作用域的编号规则代码，将使用默认的系统定义的编号规则。*</span><span class="sxs-lookup"><span data-stu-id="2bccf-150">const str NumberSequenceExistingCode = ''; *// Specify the scope of the existing number sequence code* 
*// true, if the specified number sequence is shared* 
*// false, if the specified number sequence is per-company* 
*// The default system-defined number sequence will be used if a number sequence code with the specified scope is not found.*</span></span> <span data-ttu-id="2bccf-151">const boolean NumberSequenceExistingIsShared = true;</span><span class="sxs-lookup"><span data-stu-id="2bccf-151">const boolean NumberSequenceExistingIsShared = true;</span></span> 

<span data-ttu-id="2bccf-152">修改常量后重新构建含有类的项目。</span><span class="sxs-lookup"><span data-stu-id="2bccf-152">Rebuild the project that contains the class after the constants have been modified.</span></span> 

<span data-ttu-id="2bccf-153">使用系统定义的编号规则方法（选项 1）时，升级将使用基于设置的处理以分配升级脚本参数中指定的凭证号。</span><span class="sxs-lookup"><span data-stu-id="2bccf-153">When using the system-generated number sequence approach (option 1), the upgrade will use set-based processing to allocate the voucher numbers as specified in the upgrade script parameters.</span></span> <span data-ttu-id="2bccf-154">它还将在分配后使用指定参数创建新的编号规则。</span><span class="sxs-lookup"><span data-stu-id="2bccf-154">It will also create a new number sequence with specified parameters after the allocation.</span></span> 

<span data-ttu-id="2bccf-155">使用用户定义的现有编号规则方法（选项 2）时，数据升级检查具有折旧帐簿交易记录的每个分区和公司的数据库中是否存在具有指定作用域的编号规则。</span><span class="sxs-lookup"><span data-stu-id="2bccf-155">When using the user-defined existing number sequence approach (option 2), the data upgrade checks whether the number sequence with the specified scope exists in the database for each partition and company with depreciation book transactions.</span></span> <span data-ttu-id="2bccf-156">如果存在，升级将通过逐行处理分配编号规则通过编号规则框架指定的凭证号。</span><span class="sxs-lookup"><span data-stu-id="2bccf-156">If it does exist, the upgrade will use row-by-row processing to allocate the voucher numbers as specified by the number sequence using the number sequence framework.</span></span> <span data-ttu-id="2bccf-157">如果不存在具有指定作用域的编号规则，升级将使用默认的系统定义的编号规则方法分配凭证号，并将在分配后使用指定的默认参数创建新的编号规则。</span><span class="sxs-lookup"><span data-stu-id="2bccf-157">If the number sequence does not exist with the specified scope, the upgrade will use the default system-defined number sequence approach to allocate the voucher numbers, and will create a new number sequence with specified default parameters after the allocation.</span></span>

<span data-ttu-id="2bccf-158">无论使用任何一种方法，数据升级脚本都会使用为以前的折旧帐簿日记帐名称创建的新总帐日记帐名称上的“**凭证系列**”字段的编号规则。</span><span class="sxs-lookup"><span data-stu-id="2bccf-158">With either approach, the data upgrade script will also use the number sequence for the **Voucher series** field on the new general ledger journal names created for the former depreciation book journal names.</span></span>




