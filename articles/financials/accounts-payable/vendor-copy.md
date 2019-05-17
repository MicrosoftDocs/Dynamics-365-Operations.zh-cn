---
title: 使用共享的编号规则复制供应商
description: 本主题说明如何使用共享的编号规则将供应商复制到另一个法人但却保持相同的供应商 ID。
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 14e361b38f417ee7017981f564eac1b12c93b9f5
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1508868"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a><span data-ttu-id="95405-103">使用共享的编号规则复制供应商</span><span class="sxs-lookup"><span data-stu-id="95405-103">Copy vendors by using shared number sequences</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95405-104">您可以使用共享的编号规则分配供应商 ID。</span><span class="sxs-lookup"><span data-stu-id="95405-104">You can use shared number sequences to assign vendor IDs.</span></span> <span data-ttu-id="95405-105">利用共享的编号规则，您还可以将供应商从一个法人复制到另一个法人，但却在这两个法人中使用相同的供应商 ID。</span><span class="sxs-lookup"><span data-stu-id="95405-105">Shared number sequences also let you copy vendors from one legal entity to another legal entity but use the same vendor IDs in both legal entities.</span></span>

## <a name="setup"></a><span data-ttu-id="95405-106">设置</span><span class="sxs-lookup"><span data-stu-id="95405-106">Setup</span></span>

<span data-ttu-id="95405-107">使用共享的编号规则分配供应商 ID 时会激活此功能。</span><span class="sxs-lookup"><span data-stu-id="95405-107">The feature is activated when you use a shared number sequence to assign vendor IDs.</span></span> <span data-ttu-id="95405-108">您必须在要将供应商复制到的每个法人中使用相同的编号规则。</span><span class="sxs-lookup"><span data-stu-id="95405-108">You must use the same number sequence in every legal entity that you want to copy a vendor to.</span></span> <span data-ttu-id="95405-109">您可以在**应付帐款参数**页上为每个法人更改供应商编号规则。</span><span class="sxs-lookup"><span data-stu-id="95405-109">You change the vendor number sequence on the **Accounts payable parameters** page for each legal entity.</span></span> <span data-ttu-id="95405-110">选择**应付帐款** \> **设置** \> **应付帐款参数**，然后选择**编号规则**选项卡。</span><span class="sxs-lookup"><span data-stu-id="95405-110">Select **Accounts payable** \> **Setup** \> **Accounts payable parameters**, and then select the **Number sequences** tab.</span></span>

<span data-ttu-id="95405-111">您还可以为每个供应商组设置供应商编号规则。</span><span class="sxs-lookup"><span data-stu-id="95405-111">You can also set up vendor number sequences for each vendor group.</span></span> <span data-ttu-id="95405-112">还必须共享这些编号规则。</span><span class="sxs-lookup"><span data-stu-id="95405-112">These number sequences must also be shared.</span></span> <span data-ttu-id="95405-113">首先使用供应商组的编号规则。</span><span class="sxs-lookup"><span data-stu-id="95405-113">The number sequence for a vendor group is used first.</span></span> <span data-ttu-id="95405-114">如果没有为供应商组指定编号规则，则使用在**应付帐款参数**页上指定的编号规则。</span><span class="sxs-lookup"><span data-stu-id="95405-114">If no number sequence is specified for a vendor group, the number sequence that is specified on the **Accounts payable parameters** page is used.</span></span>

<span data-ttu-id="95405-115">如果您使用手动供应商 ID，也可以在法人之间复制供应商。</span><span class="sxs-lookup"><span data-stu-id="95405-115">You can also copy vendors between legal entities if you use manual vendor IDs.</span></span> <span data-ttu-id="95405-116">但是，如果您尝试将供应商复制到已存在供应商 ID 的法人，则不会启动复制过程。</span><span class="sxs-lookup"><span data-stu-id="95405-116">However, if you try to copy a vendor to a legal entity where the vendor ID already exists, the copy process won't be started.</span></span>

## <a name="copy-a-vendor"></a><span data-ttu-id="95405-117">复制供应商</span><span class="sxs-lookup"><span data-stu-id="95405-117">Copy a vendor</span></span>

<span data-ttu-id="95405-118">要复制供应商，请选择**所有供应商**列表页面上的**新建**，打开**所有供应商 - 新记录**页面。</span><span class="sxs-lookup"><span data-stu-id="95405-118">To copy a vendor, select **New** on the **All vendors** list page to open the **All vendors, new record** page.</span></span> <span data-ttu-id="95405-119">请注意，系统不会立即分配新的供应商 ID。</span><span class="sxs-lookup"><span data-stu-id="95405-119">Notice that the new vendor ID isn't assigned immediately.</span></span> <span data-ttu-id="95405-120">此行为与先前版本的 Microsoft Dynamics 365 for Finance and Operations 中的行为不同。</span><span class="sxs-lookup"><span data-stu-id="95405-120">This behavior differs from the behavior in previous versions of Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="95405-121">由于您尚未选择供应商组，因此系统无法确定要使用的正确编号规则。</span><span class="sxs-lookup"><span data-stu-id="95405-121">Because you haven't yet selected the vendor group, the system can't determine the correct number sequence to use.</span></span> <span data-ttu-id="95405-122">此外，系统无法确定您是要尝试创建新供应商还是复制供应商。</span><span class="sxs-lookup"><span data-stu-id="95405-122">Additionally, it can't determine whether you're trying to create a new vendor or copy a vendor.</span></span> <span data-ttu-id="95405-123">因此，在页面底部选择**保存**之前，不会分配供应商 ID。</span><span class="sxs-lookup"><span data-stu-id="95405-123">Therefore, the vendor ID isn't assigned until you select **Save** at the bottom of the page.</span></span>

<span data-ttu-id="95405-124">如果您要创建新供应商，则可以像往常一样继续填写所有字段。</span><span class="sxs-lookup"><span data-stu-id="95405-124">If you're creating a new vendor, you can continue to fill in all the fields as you usually do.</span></span> <span data-ttu-id="95405-125">在完成并选择**保存**时，您将会发现系统自动分配了供应商 ID。</span><span class="sxs-lookup"><span data-stu-id="95405-125">When you've finished, and you select **Save**, you will see that the vendor ID was assigned automatically.</span></span> <span data-ttu-id="95405-126">或者，您将发现对手动编号规则使用了手动供应商 ID。</span><span class="sxs-lookup"><span data-stu-id="95405-126">Alternatively, for manual number sequences, you will see that your manual vendor ID was used.</span></span>

<span data-ttu-id="95405-127">要复制供应商，请在**名称**字段中输入一个或多个字符以表示要查找的供应商。</span><span class="sxs-lookup"><span data-stu-id="95405-127">To copy a vendor, in the **Name** field, enter one or more characters that represent the vendor that you're looking for.</span></span> <span data-ttu-id="95405-128">搜索对话框会显示可能表示您正在寻找的供应商的当事方列表。</span><span class="sxs-lookup"><span data-stu-id="95405-128">A search dialog box shows a list of parties that might represent the vendor that you're looking for.</span></span> <span data-ttu-id="95405-129">当您选择其中一个当事方时，对话框右侧会显示附加信息：</span><span class="sxs-lookup"><span data-stu-id="95405-129">When you select one of the parties, additional information appears on the right side of the dialog box:</span></span>

- <span data-ttu-id="95405-130">**常规**选项卡显示当事方的电话号码和地址。</span><span class="sxs-lookup"><span data-stu-id="95405-130">The **General** tab shows the party's phone number and address.</span></span>
- <span data-ttu-id="95405-131">**角色**选项卡显示所选当事方可能具有的角色，以及该当事方具有每种角色所在的法人。</span><span class="sxs-lookup"><span data-stu-id="95405-131">The **Roles** tab shows the roles that the selected party can have and the legal entity where it has each role.</span></span>
- <span data-ttu-id="95405-132">**税务登记 ID** 选项卡显示分配给当事方的税务登记 ID。</span><span class="sxs-lookup"><span data-stu-id="95405-132">**Tax registration ID** tab shows the tax registration IDs that are assigned to the party.</span></span>

<span data-ttu-id="95405-133">只有在当事方具有供应商角色时，并且仅当该当事方在非当前法人中具有该角色时，您才能复制该当事方。</span><span class="sxs-lookup"><span data-stu-id="95405-133">You can copy a party only if it has a vendor role, and if it has that role in a legal entity that isn't the current legal entity.</span></span> <span data-ttu-id="95405-134">在您查找满足这些标准的当事方时，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="95405-134">When you find a party that meets these criteria, follow these steps.</span></span>

1. <span data-ttu-id="95405-135">**复制供应商**选项将会出现。</span><span class="sxs-lookup"><span data-stu-id="95405-135">A **Copy vendor** option appears.</span></span> <span data-ttu-id="95405-136">默认情况下，此选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="95405-136">By default, this option is set to **No**.</span></span> <span data-ttu-id="95405-137">要将供应商复制到当前法人，请将此选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="95405-137">To copy the vendor to the current legal entity, set the option to **Yes**.</span></span> 
2. <span data-ttu-id="95405-138">**法人**字段将会出现。</span><span class="sxs-lookup"><span data-stu-id="95405-138">A **Legal entity** field appears.</span></span> <span data-ttu-id="95405-139">选择要从其中复制供应商的法人。</span><span class="sxs-lookup"><span data-stu-id="95405-139">Select the legal entity to copy the vendor from.</span></span> <span data-ttu-id="95405-140">如果供应商只存在于一个法人中，则默认情况下此字段会设置为该法人。</span><span class="sxs-lookup"><span data-stu-id="95405-140">If the vendor exists in only one legal entity, the field is set to that legal entity by default.</span></span>
3. <span data-ttu-id="95405-141">选择**选择**。</span><span class="sxs-lookup"><span data-stu-id="95405-141">Select **Select**.</span></span> <span data-ttu-id="95405-142">此时会创建新供应商。</span><span class="sxs-lookup"><span data-stu-id="95405-142">The new vendor is created.</span></span>

## <a name="validation"></a><span data-ttu-id="95405-143">验证</span><span class="sxs-lookup"><span data-stu-id="95405-143">Validation</span></span>

<span data-ttu-id="95405-144">复制供应商时，系统会尝试保存新供应商信息。</span><span class="sxs-lookup"><span data-stu-id="95405-144">When you copy a vendor, the system tries to save the new vendor information.</span></span> <span data-ttu-id="95405-145">系统会运行验证以验证复制的数据是否完好。</span><span class="sxs-lookup"><span data-stu-id="95405-145">Validations are run to verify that the data that was copied is good.</span></span> <span data-ttu-id="95405-146">对于每项失败的验证，您都会收到一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="95405-146">You receive an error message for every validation that fails.</span></span> <span data-ttu-id="95405-147">错误消息说明了必须更新哪些信息。</span><span class="sxs-lookup"><span data-stu-id="95405-147">The error messages explain what information must be updated.</span></span> <span data-ttu-id="95405-148">在修复所有验证错误之前，无法保存供应商的副本。</span><span class="sxs-lookup"><span data-stu-id="95405-148">The copy of the vendor can't be saved until you fix all the validation errors.</span></span>

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a><span data-ttu-id="95405-149">使用免税编号搜索功能复制供应商</span><span class="sxs-lookup"><span data-stu-id="95405-149">Copy a vendor by using the Tax exempt number search feature</span></span>

<span data-ttu-id="95405-150">您还可以使用**所有供应商**页面操作窗格上**供应商**选项卡内**登记**组中的免税编号搜索功能来复制供应商。 </span><span class="sxs-lookup"><span data-stu-id="95405-150">You can also copy vendors by using the Tax exempt number search feature that is in the **Registration** group on the **Vendor** tab on the Action Pane of the **All vendors** page.</span></span> <span data-ttu-id="95405-151">出现的**免税编号搜索**对话框会显示免税编号、供应商 ID、供应商名称以及使用免税 ID 的法人。</span><span class="sxs-lookup"><span data-stu-id="95405-151">The **Tax exempt number search** dialog box that appears shows tax exempt numbers, the vendor ID, the vendor name, and the legal entity where the tax exempt ID is used.</span></span> <span data-ttu-id="95405-152">只有当供应商在非当前法人中时，您才能复制供应商。</span><span class="sxs-lookup"><span data-stu-id="95405-152">You can copy a vendor only if it's in a legal entity that isn't the current legal entity.</span></span> <span data-ttu-id="95405-153">在选择满足此标准的供应商后，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="95405-153">After you select a vendor that meets this criterion, follow these steps.</span></span>

1. <span data-ttu-id="95405-154">**复制供应商**选项将会出现。</span><span class="sxs-lookup"><span data-stu-id="95405-154">A **Copy vendor** option appears.</span></span> <span data-ttu-id="95405-155">默认情况下，此选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="95405-155">By default, this option is set to **No**.</span></span> <span data-ttu-id="95405-156">要将供应商复制到当前法人，请将此选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="95405-156">To copy the vendor to the current legal entity, set the option to **Yes**.</span></span>
2. <span data-ttu-id="95405-157">选择**选择**。</span><span class="sxs-lookup"><span data-stu-id="95405-157">Select **Select**.</span></span> <span data-ttu-id="95405-158">此时会创建新供应商。</span><span class="sxs-lookup"><span data-stu-id="95405-158">The new vendor is created.</span></span>
