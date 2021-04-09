---
title: 使用共享的编号规则复制客户
description: 本主题说明如何使用共享的编号规则将客户复制到另一个法人但却保持相同的客户 ID。
author: mikefalkner
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 9f7d3648514bcdb3ad249c657f34ecc5e1d817d3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827594"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a><span data-ttu-id="891d5-103">使用共享的编号规则复制客户</span><span class="sxs-lookup"><span data-stu-id="891d5-103">Copy customers by using shared number sequences</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="891d5-104">您可以使用共享的编号规则分配客户 ID。</span><span class="sxs-lookup"><span data-stu-id="891d5-104">You can use shared number sequences to assign customer IDs.</span></span> <span data-ttu-id="891d5-105">利用共享的编号规则，您还可以将客户从一个法人复制到另一个法人，但却在这两个法人中使用相同的客户 ID。</span><span class="sxs-lookup"><span data-stu-id="891d5-105">Shared number sequences also let you copy customers from one legal entity to another legal entity but use the same customer IDs in both legal entities.</span></span>

## <a name="setup"></a><span data-ttu-id="891d5-106">设置</span><span class="sxs-lookup"><span data-stu-id="891d5-106">Setup</span></span>

<span data-ttu-id="891d5-107">使用共享的编号规则分配客户 ID 时会激活此功能。</span><span class="sxs-lookup"><span data-stu-id="891d5-107">The feature is activated when you use a shared number sequence to assign customer IDs.</span></span> <span data-ttu-id="891d5-108">您必须在要将客户复制到的每个法人中使用相同的编号规则。</span><span class="sxs-lookup"><span data-stu-id="891d5-108">You must use the same number sequence in every legal entity that you want to copy a customer to.</span></span> <span data-ttu-id="891d5-109">您可以在 **应收帐款参数** 页上为每个法人更改客户编号规则。</span><span class="sxs-lookup"><span data-stu-id="891d5-109">You change the customer number sequence on the **Accounts receivable parameters** page for each legal entity.</span></span> <span data-ttu-id="891d5-110">选择 **应收帐款** \> **参数**，然后选择 **编号规则** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="891d5-110">Select **Accounts receivable** \> **Parameters**, and then select the **Number sequences** tab.</span></span>

<span data-ttu-id="891d5-111">您还可以为每个客户组设置客户编号规则。</span><span class="sxs-lookup"><span data-stu-id="891d5-111">You can also set up customer number sequences for each customer group.</span></span> <span data-ttu-id="891d5-112">还必须共享这些编号规则。</span><span class="sxs-lookup"><span data-stu-id="891d5-112">These number sequences must also be shared.</span></span> <span data-ttu-id="891d5-113">首先使用客户组的编号规则。</span><span class="sxs-lookup"><span data-stu-id="891d5-113">The number sequence for a customer group is used first.</span></span> <span data-ttu-id="891d5-114">如果没有为客户组指定编号规则，则使用在 **应收帐款参数** 页上指定的编号规则。</span><span class="sxs-lookup"><span data-stu-id="891d5-114">If no number sequence is specified for a customer group, the number sequence that is specified on the **Accounts receivable parameters** page is used.</span></span>

<span data-ttu-id="891d5-115">如果您使用手动客户 ID，也可以在法人之间复制客户。</span><span class="sxs-lookup"><span data-stu-id="891d5-115">You can also copy customers between legal entities if you use manual customer IDs.</span></span> <span data-ttu-id="891d5-116">但是，如果您尝试将客户复制到已存在客户 ID 的法人，则不会启动复制过程。</span><span class="sxs-lookup"><span data-stu-id="891d5-116">However, if you try to copy a customer to a legal entity where the customer ID already exists, the copy process won't be started.</span></span>

## <a name="copy-a-customer"></a><span data-ttu-id="891d5-117">复制客户</span><span class="sxs-lookup"><span data-stu-id="891d5-117">Copy a customer</span></span>

<span data-ttu-id="891d5-118">要复制客户，请选择 **所有客户** 列表页面上的 **新建** 以打开 **创建客户** 对话框。</span><span class="sxs-lookup"><span data-stu-id="891d5-118">To copy a customer, select **New** on the **All customers** list page to open the **Create customer** dialog box.</span></span> <span data-ttu-id="891d5-119">请注意，系统未立即分配新的客户 ID。</span><span class="sxs-lookup"><span data-stu-id="891d5-119">Notice that the new customer ID isn't assigned immediately.</span></span> <span data-ttu-id="891d5-120">此行为与先前版本中的行为不同。</span><span class="sxs-lookup"><span data-stu-id="891d5-120">This behavior differs from the behavior in previous versions.</span></span> <span data-ttu-id="891d5-121">由于您尚未选择客户组，因此系统无法确定要使用的正确编号规则。</span><span class="sxs-lookup"><span data-stu-id="891d5-121">Because you haven't yet selected the customer group, the system can't determine the correct number sequence to use.</span></span> <span data-ttu-id="891d5-122">此外，系统无法确定您是要尝试创建新客户还是复制客户。</span><span class="sxs-lookup"><span data-stu-id="891d5-122">Additionally, it can't determine whether you're trying to create a new customer or copy a customer.</span></span> <span data-ttu-id="891d5-123">因此，在对话框底部选择 **保存** 之前，不会分配客户 ID。</span><span class="sxs-lookup"><span data-stu-id="891d5-123">Therefore, the customer ID isn't assigned until you select **Save** at the bottom of the dialog box.</span></span>

<span data-ttu-id="891d5-124">如果您要创建新客户，则可以像往常一样继续填写所有字段。</span><span class="sxs-lookup"><span data-stu-id="891d5-124">If you're creating a new customer, you can continue to fill in all the fields as you usually do.</span></span> <span data-ttu-id="891d5-125">在完成并选择 **保存** 时，您将会发现系统自动分配了客户 ID。</span><span class="sxs-lookup"><span data-stu-id="891d5-125">When you've finished, and you select **Save**, you will see that the customer ID was assigned automatically.</span></span> <span data-ttu-id="891d5-126">或者，您将发现对手动编号规则使用了手动客户 ID。</span><span class="sxs-lookup"><span data-stu-id="891d5-126">Alternatively, for manual number sequences, you will see that your manual customer ID was used.</span></span>

<span data-ttu-id="891d5-127">要复制客户，请在 **名称** 字段中输入一个或多个能代表所查找客户的字符。</span><span class="sxs-lookup"><span data-stu-id="891d5-127">To copy a customer, in the **Name** field, enter one or more characters that represent the customer that you're looking for.</span></span> <span data-ttu-id="891d5-128">搜索对话框会显示可能代表所寻找客户的当事方列表。</span><span class="sxs-lookup"><span data-stu-id="891d5-128">A search dialog box shows a list of parties that might represent the customer that you're looking for.</span></span> <span data-ttu-id="891d5-129">当您选择其中一个当事方时，对话框右侧会显示附加信息：</span><span class="sxs-lookup"><span data-stu-id="891d5-129">When you select one of the parties, additional information appears on the right side of the dialog box:</span></span>

- <span data-ttu-id="891d5-130">**常规** 选项卡显示当事方的电话号码和地址。</span><span class="sxs-lookup"><span data-stu-id="891d5-130">The **General** tab shows the party's phone number and address.</span></span>
- <span data-ttu-id="891d5-131">**角色** 选项卡显示所选当事方可能具有的角色，以及该当事方具有每种角色所在的法人。</span><span class="sxs-lookup"><span data-stu-id="891d5-131">The **Roles** tab shows the roles that the selected party can have and the legal entity where it has each role.</span></span>
- <span data-ttu-id="891d5-132">**税务登记 ID** 选项卡显示分配给当事方的税务登记 ID。</span><span class="sxs-lookup"><span data-stu-id="891d5-132">**Tax registration ID** tab shows the tax registration IDs that are assigned to the party.</span></span>

<span data-ttu-id="891d5-133">只有在当事方具有客户角色时，并且仅当该当事方在非当前法人中具有该角色时，您才能复制该当事方。</span><span class="sxs-lookup"><span data-stu-id="891d5-133">You can copy a party only if it has a customer role, and if it has that role in a legal entity that isn't the current legal entity.</span></span> <span data-ttu-id="891d5-134">在您查找满足这些标准的当事方时，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="891d5-134">When you find a party that meets these criteria, follow these steps.</span></span>

1. <span data-ttu-id="891d5-135">**复制客户** 选项将会出现。</span><span class="sxs-lookup"><span data-stu-id="891d5-135">A **Copy customer** option appears.</span></span> <span data-ttu-id="891d5-136">默认情况下，此选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="891d5-136">By default, this option is set to **No**.</span></span> <span data-ttu-id="891d5-137">要将客户复制到当前法人，请将此选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="891d5-137">To copy the customer to the current legal entity, set the option to **Yes**.</span></span> 
2. <span data-ttu-id="891d5-138">**法人** 字段将会出现。</span><span class="sxs-lookup"><span data-stu-id="891d5-138">A **Legal entity** field appears.</span></span> <span data-ttu-id="891d5-139">选择要从其中复制客户的法人。</span><span class="sxs-lookup"><span data-stu-id="891d5-139">Select the legal entity to copy the customer from.</span></span> <span data-ttu-id="891d5-140">如果客户只存在于一个法人中，则默认情况下此字段会设置为该法人。</span><span class="sxs-lookup"><span data-stu-id="891d5-140">If the customer exists in only one legal entity, the field is set to that legal entity by default.</span></span>
3. <span data-ttu-id="891d5-141">选择 **选择**。</span><span class="sxs-lookup"><span data-stu-id="891d5-141">Select **Select**.</span></span> <span data-ttu-id="891d5-142">此时会创建新客户。</span><span class="sxs-lookup"><span data-stu-id="891d5-142">The new customer is created.</span></span>

## <a name="validation"></a><span data-ttu-id="891d5-143">验证</span><span class="sxs-lookup"><span data-stu-id="891d5-143">Validation</span></span>

<span data-ttu-id="891d5-144">复制客户时，系统会尝试保存新客户信息。</span><span class="sxs-lookup"><span data-stu-id="891d5-144">When you copy a customer, the system tries to save the new customer information.</span></span> <span data-ttu-id="891d5-145">系统会运行验证以验证复制的数据是否完好。</span><span class="sxs-lookup"><span data-stu-id="891d5-145">Validations are run to verify that the data that was copied is good.</span></span> <span data-ttu-id="891d5-146">对于每项失败的验证，您都会收到一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="891d5-146">You receive an error message for every validation that fails.</span></span> <span data-ttu-id="891d5-147">错误消息说明了必须更新哪些信息。</span><span class="sxs-lookup"><span data-stu-id="891d5-147">The error messages explain what information must be updated.</span></span> <span data-ttu-id="891d5-148">在修复所有验证错误之前，无法保存客户的副本。</span><span class="sxs-lookup"><span data-stu-id="891d5-148">The copy of the customer can't be saved until you fix all the validation errors.</span></span>

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a><span data-ttu-id="891d5-149">使用免税编号搜索功能复制客户</span><span class="sxs-lookup"><span data-stu-id="891d5-149">Copy a customer by using tax exempt number search feature</span></span>

<span data-ttu-id="891d5-150">您还可以使用 **所有客户** 页面操作窗格上 **客户** 选项卡内 **登记** 组中的免税编号搜索功能来复制客户。</span><span class="sxs-lookup"><span data-stu-id="891d5-150">You can also copy customers by using the Tax exempt number search feature that is in the **Registration** group on the **Customer** tab on the Action Pane of the **All customers** page.</span></span> <span data-ttu-id="891d5-151">出现的 **免税编号搜索** 对话框会显示免税编号、客户 ID、客户名称以及使用免税 ID 的法人。</span><span class="sxs-lookup"><span data-stu-id="891d5-151">The **Tax exempt number search** dialog box that appears shows tax exempt numbers, the customer ID, the customer name, and the legal entity where the tax exempt ID is used.</span></span> <span data-ttu-id="891d5-152">只有当客户在非当前法人中时，您才能复制客户。</span><span class="sxs-lookup"><span data-stu-id="891d5-152">You can copy a customer only if it's in a legal entity that isn't the current legal entity.</span></span> <span data-ttu-id="891d5-153">在选择满足此标准的客户后，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="891d5-153">After you select a customer that meets this criterion, follow these steps.</span></span>

1. <span data-ttu-id="891d5-154">**复制客户** 选项将会出现。</span><span class="sxs-lookup"><span data-stu-id="891d5-154">A **Copy customer** option appears.</span></span> <span data-ttu-id="891d5-155">默认情况下，此选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="891d5-155">By default, this option is set to **No**.</span></span> <span data-ttu-id="891d5-156">要将客户复制到当前法人，请将此选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="891d5-156">To copy the customer to the current legal entity, set the option to **Yes**.</span></span> 
2. <span data-ttu-id="891d5-157">选择 **选择**。</span><span class="sxs-lookup"><span data-stu-id="891d5-157">Select **Select**.</span></span> <span data-ttu-id="891d5-158">此时会创建新客户。</span><span class="sxs-lookup"><span data-stu-id="891d5-158">The new customer is created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]