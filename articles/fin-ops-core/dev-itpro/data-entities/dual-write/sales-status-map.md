---
title: 设置销售订单状态列的映射
description: 本主题说明如何为双写入设置销售订单状态列。
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: cc70501d231390ea15104d508a36300a1b2cd44c
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744291"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="8d664-103">设置销售订单状态列的映射</span><span class="sxs-lookup"><span data-stu-id="8d664-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8d664-104">指示销售订单状态的列在 Microsoft Dynamics 365 Supply Chain Management 和 Dynamics 365 Sales 中具有不同的枚举值。</span><span class="sxs-lookup"><span data-stu-id="8d664-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="8d664-105">采用双写入映射这些列需要进行其他设置。</span><span class="sxs-lookup"><span data-stu-id="8d664-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="8d664-106">Supply Chain Management 中的列</span><span class="sxs-lookup"><span data-stu-id="8d664-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="8d664-107">在 Supply Chain Management 中，两个列反映销售订单的状态。</span><span class="sxs-lookup"><span data-stu-id="8d664-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="8d664-108">您必须映射的列是 **状态** 和 **文档状态**。</span><span class="sxs-lookup"><span data-stu-id="8d664-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="8d664-109">**状态** 枚举指定订单的整体状态。</span><span class="sxs-lookup"><span data-stu-id="8d664-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="8d664-110">此状态显示在订单标题上。</span><span class="sxs-lookup"><span data-stu-id="8d664-110">This status is shown on the order header.</span></span>

<span data-ttu-id="8d664-111">**状态** 枚举具有以下值：</span><span class="sxs-lookup"><span data-stu-id="8d664-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="8d664-112">未结订单</span><span class="sxs-lookup"><span data-stu-id="8d664-112">Open Order</span></span>
- <span data-ttu-id="8d664-113">已交货</span><span class="sxs-lookup"><span data-stu-id="8d664-113">Delivered</span></span>
- <span data-ttu-id="8d664-114">已开单</span><span class="sxs-lookup"><span data-stu-id="8d664-114">Invoiced</span></span>
- <span data-ttu-id="8d664-115">已取消</span><span class="sxs-lookup"><span data-stu-id="8d664-115">Cancelled</span></span>

<span data-ttu-id="8d664-116">**文档状态** 枚举指定为订单生成的最新文档。</span><span class="sxs-lookup"><span data-stu-id="8d664-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="8d664-117">例如，如果订单已确认，此文档为销售订单确认。</span><span class="sxs-lookup"><span data-stu-id="8d664-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="8d664-118">如果销售订单已部分开票，然后确认其余行，文档状态仍为 **发票**，因为发票是在流程后期生成的。</span><span class="sxs-lookup"><span data-stu-id="8d664-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="8d664-119">**文档状态** 枚举具有以下值：</span><span class="sxs-lookup"><span data-stu-id="8d664-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="8d664-120">确认单</span><span class="sxs-lookup"><span data-stu-id="8d664-120">Confirmation</span></span>
- <span data-ttu-id="8d664-121">领料单</span><span class="sxs-lookup"><span data-stu-id="8d664-121">Picking List</span></span>
- <span data-ttu-id="8d664-122">装箱单</span><span class="sxs-lookup"><span data-stu-id="8d664-122">Packing Slip</span></span>
- <span data-ttu-id="8d664-123">账单</span><span class="sxs-lookup"><span data-stu-id="8d664-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="8d664-124">Sales 中的列</span><span class="sxs-lookup"><span data-stu-id="8d664-124">columns in Sales</span></span>

<span data-ttu-id="8d664-125">在 Sales 中，两个列指示订单的状态。</span><span class="sxs-lookup"><span data-stu-id="8d664-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="8d664-126">您必须映射的列是 **状态** 和 **处理状态**。</span><span class="sxs-lookup"><span data-stu-id="8d664-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="8d664-127">**状态** 枚举指定订单的整体状态。</span><span class="sxs-lookup"><span data-stu-id="8d664-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="8d664-128">它具有以下值：</span><span class="sxs-lookup"><span data-stu-id="8d664-128">It has the following values:</span></span>

- <span data-ttu-id="8d664-129">在职</span><span class="sxs-lookup"><span data-stu-id="8d664-129">Active</span></span>
- <span data-ttu-id="8d664-130">提交日期</span><span class="sxs-lookup"><span data-stu-id="8d664-130">Submitted</span></span>
- <span data-ttu-id="8d664-131">已履行</span><span class="sxs-lookup"><span data-stu-id="8d664-131">Fulfilled</span></span>
- <span data-ttu-id="8d664-132">已开单</span><span class="sxs-lookup"><span data-stu-id="8d664-132">Invoiced</span></span>
- <span data-ttu-id="8d664-133">已取消</span><span class="sxs-lookup"><span data-stu-id="8d664-133">Cancelled</span></span>

<span data-ttu-id="8d664-134">引入了 **处理状态** 枚举，以便可以通过 Supply Chain Management 更准确地映射状态。</span><span class="sxs-lookup"><span data-stu-id="8d664-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="8d664-135">下表显示了 Supply Chain Management 中 **处理状态** 的映射。</span><span class="sxs-lookup"><span data-stu-id="8d664-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="8d664-136">处理状态</span><span class="sxs-lookup"><span data-stu-id="8d664-136">Processing Status</span></span>   | <span data-ttu-id="8d664-137">Supply Chain Management 中的状态</span><span class="sxs-lookup"><span data-stu-id="8d664-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="8d664-138">Supply Chain Management 中的文档状态</span><span class="sxs-lookup"><span data-stu-id="8d664-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="8d664-139">在职</span><span class="sxs-lookup"><span data-stu-id="8d664-139">Active</span></span>              | <span data-ttu-id="8d664-140">未结订单</span><span class="sxs-lookup"><span data-stu-id="8d664-140">Open Order</span></span>                        | <span data-ttu-id="8d664-141">None</span><span class="sxs-lookup"><span data-stu-id="8d664-141">None</span></span>                                       |
| <span data-ttu-id="8d664-142">已确认</span><span class="sxs-lookup"><span data-stu-id="8d664-142">Confirmed</span></span>           | <span data-ttu-id="8d664-143">未结订单</span><span class="sxs-lookup"><span data-stu-id="8d664-143">Open Order</span></span>                        | <span data-ttu-id="8d664-144">确认单</span><span class="sxs-lookup"><span data-stu-id="8d664-144">Confirmation</span></span>                               |
| <span data-ttu-id="8d664-145">已领料</span><span class="sxs-lookup"><span data-stu-id="8d664-145">Picked</span></span>              | <span data-ttu-id="8d664-146">未结订单</span><span class="sxs-lookup"><span data-stu-id="8d664-146">Open Order</span></span>                        | <span data-ttu-id="8d664-147">领料单</span><span class="sxs-lookup"><span data-stu-id="8d664-147">Picking List</span></span>                               |
| <span data-ttu-id="8d664-148">已部分交货</span><span class="sxs-lookup"><span data-stu-id="8d664-148">Partially Delivered</span></span> | <span data-ttu-id="8d664-149">未结订单</span><span class="sxs-lookup"><span data-stu-id="8d664-149">Open Order</span></span>                        | <span data-ttu-id="8d664-150">装箱单</span><span class="sxs-lookup"><span data-stu-id="8d664-150">Packing Slip</span></span>                               |
| <span data-ttu-id="8d664-151">已交货</span><span class="sxs-lookup"><span data-stu-id="8d664-151">Delivered</span></span>           | <span data-ttu-id="8d664-152">已交货</span><span class="sxs-lookup"><span data-stu-id="8d664-152">Delivered</span></span>                         | <span data-ttu-id="8d664-153">装箱单</span><span class="sxs-lookup"><span data-stu-id="8d664-153">Packing Slip</span></span>                               |
| <span data-ttu-id="8d664-154">已部分开票</span><span class="sxs-lookup"><span data-stu-id="8d664-154">Partially Invoiced</span></span>  | <span data-ttu-id="8d664-155">已交货</span><span class="sxs-lookup"><span data-stu-id="8d664-155">Delivered</span></span>                         | <span data-ttu-id="8d664-156">账单</span><span class="sxs-lookup"><span data-stu-id="8d664-156">Invoice</span></span>                                    |
| <span data-ttu-id="8d664-157">已开单</span><span class="sxs-lookup"><span data-stu-id="8d664-157">Invoiced</span></span>            | <span data-ttu-id="8d664-158">已开单</span><span class="sxs-lookup"><span data-stu-id="8d664-158">Invoiced</span></span>                          | <span data-ttu-id="8d664-159">账单</span><span class="sxs-lookup"><span data-stu-id="8d664-159">Invoice</span></span>                                    |
| <span data-ttu-id="8d664-160">已取消</span><span class="sxs-lookup"><span data-stu-id="8d664-160">Cancelled</span></span>           | <span data-ttu-id="8d664-161">已取消</span><span class="sxs-lookup"><span data-stu-id="8d664-161">Cancelled</span></span>                         | <span data-ttu-id="8d664-162">不适用</span><span class="sxs-lookup"><span data-stu-id="8d664-162">Not applicable</span></span>                             |

<span data-ttu-id="8d664-163">下表显示了 Sales 与 Supply Chain Management 之间的 **处理状态** 的映射。</span><span class="sxs-lookup"><span data-stu-id="8d664-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="8d664-164">处理状态</span><span class="sxs-lookup"><span data-stu-id="8d664-164">Processing Status</span></span>   | <span data-ttu-id="8d664-165">Sales 中的状态</span><span class="sxs-lookup"><span data-stu-id="8d664-165">Status in Sales</span></span> | <span data-ttu-id="8d664-166">Supply Chain Management 中的状态</span><span class="sxs-lookup"><span data-stu-id="8d664-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="8d664-167">在职</span><span class="sxs-lookup"><span data-stu-id="8d664-167">Active</span></span>              | <span data-ttu-id="8d664-168">在职</span><span class="sxs-lookup"><span data-stu-id="8d664-168">Active</span></span>          | <span data-ttu-id="8d664-169">未结订单</span><span class="sxs-lookup"><span data-stu-id="8d664-169">Open Order</span></span>                        |
| <span data-ttu-id="8d664-170">已确认</span><span class="sxs-lookup"><span data-stu-id="8d664-170">Confirmed</span></span>           | <span data-ttu-id="8d664-171">提交日期</span><span class="sxs-lookup"><span data-stu-id="8d664-171">Submitted</span></span>       | <span data-ttu-id="8d664-172">未结订单</span><span class="sxs-lookup"><span data-stu-id="8d664-172">Open Order</span></span>                        |
| <span data-ttu-id="8d664-173">已领料</span><span class="sxs-lookup"><span data-stu-id="8d664-173">Picked</span></span>              | <span data-ttu-id="8d664-174">提交日期</span><span class="sxs-lookup"><span data-stu-id="8d664-174">Submitted</span></span>       | <span data-ttu-id="8d664-175">未结订单</span><span class="sxs-lookup"><span data-stu-id="8d664-175">Open Order</span></span>                        |
| <span data-ttu-id="8d664-176">已部分交货</span><span class="sxs-lookup"><span data-stu-id="8d664-176">Partially Delivered</span></span> | <span data-ttu-id="8d664-177">在职</span><span class="sxs-lookup"><span data-stu-id="8d664-177">Active</span></span>          | <span data-ttu-id="8d664-178">未结订单</span><span class="sxs-lookup"><span data-stu-id="8d664-178">Open Order</span></span>                        |
| <span data-ttu-id="8d664-179">已部分开票</span><span class="sxs-lookup"><span data-stu-id="8d664-179">Partially Invoiced</span></span>  | <span data-ttu-id="8d664-180">在职</span><span class="sxs-lookup"><span data-stu-id="8d664-180">Active</span></span>          | <span data-ttu-id="8d664-181">未结订单</span><span class="sxs-lookup"><span data-stu-id="8d664-181">Open Order</span></span>                        |
| <span data-ttu-id="8d664-182">已部分开票</span><span class="sxs-lookup"><span data-stu-id="8d664-182">Partially Invoiced</span></span>  | <span data-ttu-id="8d664-183">已履行</span><span class="sxs-lookup"><span data-stu-id="8d664-183">Fulfilled</span></span>       | <span data-ttu-id="8d664-184">已交货</span><span class="sxs-lookup"><span data-stu-id="8d664-184">Delivered</span></span>                         |
| <span data-ttu-id="8d664-185">已开单</span><span class="sxs-lookup"><span data-stu-id="8d664-185">Invoiced</span></span>            | <span data-ttu-id="8d664-186">已开单</span><span class="sxs-lookup"><span data-stu-id="8d664-186">Invoiced</span></span>        | <span data-ttu-id="8d664-187">已开单</span><span class="sxs-lookup"><span data-stu-id="8d664-187">Invoiced</span></span>                          |
| <span data-ttu-id="8d664-188">已取消</span><span class="sxs-lookup"><span data-stu-id="8d664-188">Cancelled</span></span>           | <span data-ttu-id="8d664-189">已取消</span><span class="sxs-lookup"><span data-stu-id="8d664-189">Cancelled</span></span>       | <span data-ttu-id="8d664-190">已取消</span><span class="sxs-lookup"><span data-stu-id="8d664-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="8d664-191">设置</span><span class="sxs-lookup"><span data-stu-id="8d664-191">Setup</span></span>

<span data-ttu-id="8d664-192">要为销售订单状态列设置映射，必须启用 **IsSOPIntegrationEnabled** 和 **isIntegrationUser** 属性。</span><span class="sxs-lookup"><span data-stu-id="8d664-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="8d664-193">要启用 **IsSOPIntegrationEnabled** 属性，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="8d664-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="8d664-194">在浏览器中，转到 `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`。</span><span class="sxs-lookup"><span data-stu-id="8d664-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="8d664-195">将 **\<test-name\>** 替换为您公司的 Sales 链接。</span><span class="sxs-lookup"><span data-stu-id="8d664-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="8d664-196">在打开的页面上，找到 **organizationid**，记下值。</span><span class="sxs-lookup"><span data-stu-id="8d664-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![查找 organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="8d664-198">在 Sales 中，打开浏览器控制台，运行以下脚本。</span><span class="sxs-lookup"><span data-stu-id="8d664-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="8d664-199">使用步骤 2中的 **organizationid** 值。</span><span class="sxs-lookup"><span data-stu-id="8d664-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![浏览器控制台中的 JavaScript 代码](media/sales-map-script.png)

4. <span data-ttu-id="8d664-201">确认 **IsSOPIntegrationEnabled** 已设置为 **true**。</span><span class="sxs-lookup"><span data-stu-id="8d664-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="8d664-202">使用步骤 1 中的 URL 检查此值。</span><span class="sxs-lookup"><span data-stu-id="8d664-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled 设置为 true](media/sales-map-integration-enabled.png)

<span data-ttu-id="8d664-204">要启用 **isIntegrationUser** 属性，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="8d664-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="8d664-205">在 Sales 中，转到 **设置 \> 自定义 \> 自定义系统**，选择 **用户表**，然后打开 **窗体 \> 用户**。</span><span class="sxs-lookup"><span data-stu-id="8d664-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![打开用户窗体](media/sales-map-user.png)

2. <span data-ttu-id="8d664-207">在字段资源管理器中，找到 **集成用户模式**，然后双击它将它添加到窗体中。</span><span class="sxs-lookup"><span data-stu-id="8d664-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="8d664-208">保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="8d664-208">Save your change.</span></span>

    ![将“集成用户模式”列添加到窗体](media/sales-map-field-explorer.png)

3. <span data-ttu-id="8d664-210">在 Sales 中，转到 **设置 \> 安全 \> 用户**，将视图从 **已启用用户** 更改为 **应用程序用户**。</span><span class="sxs-lookup"><span data-stu-id="8d664-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![将视图从“已启用用户”更改为“应用程序用户”](media/sales-map-enabled-users.png)

4. <span data-ttu-id="8d664-212">选择 **DualWrite IntegrationUser** 的两个条目。</span><span class="sxs-lookup"><span data-stu-id="8d664-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![应用程序用户列表](media/sales-map-user-mode.png)

5. <span data-ttu-id="8d664-214">将 **集成用户模式** 列的值更改为 **是**。</span><span class="sxs-lookup"><span data-stu-id="8d664-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![更改“集成用户模式”列的值](media/sales-map-user-mode-yes.png)

<span data-ttu-id="8d664-216">现在，您的销售订单已映射。</span><span class="sxs-lookup"><span data-stu-id="8d664-216">Your sales orders are now mapped.</span></span>
