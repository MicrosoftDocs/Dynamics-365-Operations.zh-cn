---
title: 设置自动过帐到默认描述
description: 本主题说明如何设置用于介绍自动过帐到总帐的会计条目的默认文本。 您可以使用自由格式的文本或通过选择固定变量设置默认描述文本。
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3963b4ed63021dd3c84a0d87b768486dcb0f386d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837073"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="90ef4-104">设置自动过帐到默认描述</span><span class="sxs-lookup"><span data-stu-id="90ef4-104">Set up default descriptions for automatic posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90ef4-105">本主题说明如何设置用于介绍自动过帐到总帐的会计条目的默认文本。</span><span class="sxs-lookup"><span data-stu-id="90ef4-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="90ef4-106">您可以使用自由格式的文本或通过选择固定变量设置默认描述文本。</span><span class="sxs-lookup"><span data-stu-id="90ef4-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="90ef4-107">对于一些国家或地区的某些交易记录类型，您还可以选择在 Microsoft Dynamics AX 数据库中包括与这些交易记录类型相关的字段的文本。</span><span class="sxs-lookup"><span data-stu-id="90ef4-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="90ef4-108">有关交易记录类型以及国家和地区的列表，请参阅本主题后面的[可选：向默认描述添加其他文本](#optional-add-other-text-to-default-descriptions)一节。</span><span class="sxs-lookup"><span data-stu-id="90ef4-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="90ef4-109">设置默认描述</span><span class="sxs-lookup"><span data-stu-id="90ef4-109">Set up default descriptions</span></span>

1. <span data-ttu-id="90ef4-110">转至 **组织管理** \> **设置** \> **默认描述**。</span><span class="sxs-lookup"><span data-stu-id="90ef4-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="90ef4-111">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="90ef4-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="90ef4-112">在 **描述** 字段中，选择要为其创建默认描述的交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="90ef4-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="90ef4-113">在 **语言** 字段中，选择此描述适用的语言。</span><span class="sxs-lookup"><span data-stu-id="90ef4-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="90ef4-114">在 **文本** 字段中，输入默认描述。</span><span class="sxs-lookup"><span data-stu-id="90ef4-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="90ef4-115">您可以在该字段中键入文本，也可以使用以下一个或多个自由文本变量：</span><span class="sxs-lookup"><span data-stu-id="90ef4-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="90ef4-116">**%1** – 添加交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="90ef4-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="90ef4-117">**%2** – 添加对应于正在过帐到总帐的文档类型的标识符。</span><span class="sxs-lookup"><span data-stu-id="90ef4-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="90ef4-118">例如，对于与发票相关的交易记录类型，变量 **%2** 添加发票编号。</span><span class="sxs-lookup"><span data-stu-id="90ef4-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="90ef4-119">**%3** – 添加与正在过帐到总帐的文档类型相关的标识符。</span><span class="sxs-lookup"><span data-stu-id="90ef4-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="90ef4-120">例如，对于与发票相关的交易记录类型，变量 **%3** 添加客户帐号。</span><span class="sxs-lookup"><span data-stu-id="90ef4-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="90ef4-121">可选：向默认描述添加其他文本</span><span class="sxs-lookup"><span data-stu-id="90ef4-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="90ef4-122">对于一些国家或地区的某些交易记录类型，默认描述可以在您的数据中包括来自与这些交易记录类型相关的字段的文本。</span><span class="sxs-lookup"><span data-stu-id="90ef4-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="90ef4-123">以下列表显示了此选项适用的交易记录类型以及国家和地区。</span><span class="sxs-lookup"><span data-stu-id="90ef4-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="90ef4-124">**交易记录类型**</span><span class="sxs-lookup"><span data-stu-id="90ef4-124">**Transaction types**</span></span>

<span data-ttu-id="90ef4-125">您可以向与以下单据类型相关的交易记录类型的默认描述中添加其他文本：</span><span class="sxs-lookup"><span data-stu-id="90ef4-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="90ef4-126">客户发票</span><span class="sxs-lookup"><span data-stu-id="90ef4-126">Customer invoices</span></span>
- <span data-ttu-id="90ef4-127">客户贷方通知单</span><span class="sxs-lookup"><span data-stu-id="90ef4-127">Customer credit notes</span></span>
- <span data-ttu-id="90ef4-128">客户现金支付</span><span class="sxs-lookup"><span data-stu-id="90ef4-128">Customer cash payments</span></span>
- <span data-ttu-id="90ef4-129">供应商付款</span><span class="sxs-lookup"><span data-stu-id="90ef4-129">Vendor payments</span></span>
- <span data-ttu-id="90ef4-130">销售订单</span><span class="sxs-lookup"><span data-stu-id="90ef4-130">Sales orders</span></span>
- <span data-ttu-id="90ef4-131">采购订单</span><span class="sxs-lookup"><span data-stu-id="90ef4-131">Purchase orders</span></span>
- <span data-ttu-id="90ef4-132">库存日记帐</span><span class="sxs-lookup"><span data-stu-id="90ef4-132">Inventory journals</span></span>
- <span data-ttu-id="90ef4-133">主计划 (MRP)</span><span class="sxs-lookup"><span data-stu-id="90ef4-133">Master planning (MRP)</span></span>
- <span data-ttu-id="90ef4-134">固定资产</span><span class="sxs-lookup"><span data-stu-id="90ef4-134">Fixed assets</span></span>

<span data-ttu-id="90ef4-135">**国家和地区**</span><span class="sxs-lookup"><span data-stu-id="90ef4-135">**Countries and regions**</span></span>

<span data-ttu-id="90ef4-136">此选项仅在以下国家和地区可用：</span><span class="sxs-lookup"><span data-stu-id="90ef4-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="90ef4-137">巴西</span><span class="sxs-lookup"><span data-stu-id="90ef4-137">Brazil</span></span>
- <span data-ttu-id="90ef4-138">中国</span><span class="sxs-lookup"><span data-stu-id="90ef4-138">China</span></span>
- <span data-ttu-id="90ef4-139">捷克共和国</span><span class="sxs-lookup"><span data-stu-id="90ef4-139">Czech Republic</span></span>
- <span data-ttu-id="90ef4-140">东欧</span><span class="sxs-lookup"><span data-stu-id="90ef4-140">Eastern Europe</span></span>
- <span data-ttu-id="90ef4-141">匈牙利</span><span class="sxs-lookup"><span data-stu-id="90ef4-141">Hungary</span></span>
- <span data-ttu-id="90ef4-142">印度</span><span class="sxs-lookup"><span data-stu-id="90ef4-142">India</span></span>
- <span data-ttu-id="90ef4-143">日本</span><span class="sxs-lookup"><span data-stu-id="90ef4-143">Japan</span></span>
- <span data-ttu-id="90ef4-144">立陶宛</span><span class="sxs-lookup"><span data-stu-id="90ef4-144">Lithuania</span></span>
- <span data-ttu-id="90ef4-145">拉脱维亚</span><span class="sxs-lookup"><span data-stu-id="90ef4-145">Latvia</span></span>
- <span data-ttu-id="90ef4-146">波兰</span><span class="sxs-lookup"><span data-stu-id="90ef4-146">Poland</span></span>
- <span data-ttu-id="90ef4-147">俄罗斯</span><span class="sxs-lookup"><span data-stu-id="90ef4-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="90ef4-148">向默认描述添加其他文本</span><span class="sxs-lookup"><span data-stu-id="90ef4-148">Add text to default descriptions</span></span>

<span data-ttu-id="90ef4-149">完成本主题前面的[设置默认描述](#set-up-default-descriptions)一节中的步骤后，执行以下步骤，以向默认描述添加其他文本。</span><span class="sxs-lookup"><span data-stu-id="90ef4-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="90ef4-150">在 **参数** 快速选项卡上，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="90ef4-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="90ef4-151">在 **引用表** 字段中，选择要从其中将参数数据添加到描述的数据库表。</span><span class="sxs-lookup"><span data-stu-id="90ef4-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="90ef4-152">在 **引用字段** 字段中，选择要从其中将参数数据添加到描述的字段。</span><span class="sxs-lookup"><span data-stu-id="90ef4-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="90ef4-153">重复执行第 1 步到第 3 步，以添加更多参数。</span><span class="sxs-lookup"><span data-stu-id="90ef4-153">Repeat steps 1 through 3 to add more parameters.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]