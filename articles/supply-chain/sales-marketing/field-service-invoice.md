---
title: 将 Field Service 中的协议发票同步为 Supply Chain Management 中的普通发票
description: 本主题讨论用于将 Dynamics 365 Field Service 中的协议发票同步到 Dynamics 365 Supply Chain Management 中的普通发票的模板和基础任务。
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: f1790366cebf317472bc1ef9a5ecd2a19fe755d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980823"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="35390-103">将 Field Service 中的协议发票同步为 Supply Chain Management 中的普通发票</span><span class="sxs-lookup"><span data-stu-id="35390-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="35390-104">本主题讨论用于将 Dynamics 365 Field Service 中的协议发票同步到 Dynamics 365 Supply Chain Management 中的普通发票的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="35390-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="35390-105">模板和任务</span><span class="sxs-lookup"><span data-stu-id="35390-105">Templates and tasks</span></span>

<span data-ttu-id="35390-106">以下模板和基础任务用于运行从 Field Service 中的协议发票到 Supply Chain Management 中的普通发票的同步。</span><span class="sxs-lookup"><span data-stu-id="35390-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="35390-107">**数据集成中的模板名称**</span><span class="sxs-lookup"><span data-stu-id="35390-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="35390-108">协议发票（Field Service 到 Supply Chain Management）</span><span class="sxs-lookup"><span data-stu-id="35390-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="35390-109">**数据集成项目中的任务名称**</span><span class="sxs-lookup"><span data-stu-id="35390-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="35390-110">发票抬头</span><span class="sxs-lookup"><span data-stu-id="35390-110">Invoice headers</span></span>
- <span data-ttu-id="35390-111">发票行</span><span class="sxs-lookup"><span data-stu-id="35390-111">Invoice lines</span></span>

<span data-ttu-id="35390-112">在发生协议发票同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="35390-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="35390-113">科目（Sales 到 Supply Chain Management）- 直接</span><span class="sxs-lookup"><span data-stu-id="35390-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="35390-114">实体集</span><span class="sxs-lookup"><span data-stu-id="35390-114">Entity set</span></span>

| <span data-ttu-id="35390-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="35390-115">Field Service</span></span>  | <span data-ttu-id="35390-116">供应链管理</span><span class="sxs-lookup"><span data-stu-id="35390-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="35390-117">发票</span><span class="sxs-lookup"><span data-stu-id="35390-117">invoices</span></span>       | <span data-ttu-id="35390-118">Dataverse 客户普通发票抬头</span><span class="sxs-lookup"><span data-stu-id="35390-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="35390-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="35390-119">invoicedetails</span></span> | <span data-ttu-id="35390-120">Dataverse 客户普通发票行</span><span class="sxs-lookup"><span data-stu-id="35390-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="35390-121">实体流</span><span class="sxs-lookup"><span data-stu-id="35390-121">Entity flow</span></span>

<span data-ttu-id="35390-122">可通过 Microsoft Dataverse 数据集成项目将 Field Service 中从协议创建的发票同步到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="35390-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="35390-123">对这些发票的更新将同步到 Supply Chain Management 中的普通发票，前提是这些普通发票的会计状态为 **进行中**。</span><span class="sxs-lookup"><span data-stu-id="35390-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="35390-124">在 Supply Chain Management 中过帐了普通发票并且会计状态更新为 **已完成** 之后，将不再可以从 Field Service 同步更新。</span><span class="sxs-lookup"><span data-stu-id="35390-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="35390-125">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="35390-125">Field Service CRM solution</span></span>

<span data-ttu-id="35390-126">已向 **发票** 表添加了 **具有带协议来源的行** 列。</span><span class="sxs-lookup"><span data-stu-id="35390-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="35390-127">此列帮助确保仅同步从协议创建的发票。</span><span class="sxs-lookup"><span data-stu-id="35390-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="35390-128">如果发票中至少包含一个源自协议的发票行，则该值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="35390-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="35390-129">已向 **发票行** 表添加了 **具有协议来源** 列。</span><span class="sxs-lookup"><span data-stu-id="35390-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="35390-130">此列帮助确保仅同步从协议创建的发票行。</span><span class="sxs-lookup"><span data-stu-id="35390-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="35390-131">如果发票行源自协议，则该值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="35390-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="35390-132">**发票日期** 是 Supply Chain Management 中的必填字段。</span><span class="sxs-lookup"><span data-stu-id="35390-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="35390-133">因此，执行同步之前，Field Service 中的这一列必须有值。</span><span class="sxs-lookup"><span data-stu-id="35390-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="35390-134">为了满足此要求，添加了以下逻辑：</span><span class="sxs-lookup"><span data-stu-id="35390-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="35390-135">如果 **发票** 表的 **发票日期** 列为空（即无值），将把该字段设置为添加源自协议的发票时的当前日期。</span><span class="sxs-lookup"><span data-stu-id="35390-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="35390-136">用户可更改 **发票日期** 列。</span><span class="sxs-lookup"><span data-stu-id="35390-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="35390-137">但是，用户尝试保存源自协议的发票时，如果发票的 **发票日期** 列为空，将出现业务流程错误。</span><span class="sxs-lookup"><span data-stu-id="35390-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="35390-138">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="35390-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="35390-139">在 Supply Chain Management 中</span><span class="sxs-lookup"><span data-stu-id="35390-139">In Supply Chain Management</span></span>

<span data-ttu-id="35390-140">必须针对集成设置发票来源，以便区分 Supply Chain Management 中创建自 Field Service 中的协议发票的普通发票。</span><span class="sxs-lookup"><span data-stu-id="35390-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="35390-141">如果发票的发票来源的类型为 **协议发票集成**，则 **销售发票** 抬头中将显示 **外部发票编号** 字段。</span><span class="sxs-lookup"><span data-stu-id="35390-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="35390-142">除了在发票抬头中显示，还可以使用 **外部发票编号** 信息在将发票从 Supply Chain Management 同步到 Field Service 期间帮助确保过滤掉创建自 Field Service 协议发票的发票。</span><span class="sxs-lookup"><span data-stu-id="35390-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="35390-143">转至 **应收帐款** \> **设置** \> **发票来源代码**。</span><span class="sxs-lookup"><span data-stu-id="35390-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="35390-144">选择 **新建** 创建新的发票来源。</span><span class="sxs-lookup"><span data-stu-id="35390-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="35390-145">在 **发票来源** 字段中，输入发票来源的名称，如 **FS**。</span><span class="sxs-lookup"><span data-stu-id="35390-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="35390-146">在 **描述** 字段中，输入描述，如 **Field Service 协议发票**。</span><span class="sxs-lookup"><span data-stu-id="35390-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="35390-147">选中 **来源类型分配** 复选框。</span><span class="sxs-lookup"><span data-stu-id="35390-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="35390-148">将 **发票来源类型** 字段设置为 **协议发票集成**。</span><span class="sxs-lookup"><span data-stu-id="35390-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="35390-149">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="35390-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="35390-150">在数据集成项目中</span><span class="sxs-lookup"><span data-stu-id="35390-150">In the Data Integration project</span></span>

<span data-ttu-id="35390-151">任务：**发票行**</span><span class="sxs-lookup"><span data-stu-id="35390-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="35390-152">确保 Supply Chain Management 的 **主科目显示值** 字段的默认值更新为匹配所需值。</span><span class="sxs-lookup"><span data-stu-id="35390-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="35390-153">默认模板值为 **401100**。</span><span class="sxs-lookup"><span data-stu-id="35390-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="35390-154">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="35390-154">Template mapping in Data integration</span></span>

<span data-ttu-id="35390-155">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="35390-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="35390-156">协议发票（Field Service 到 Supply Chain Management）：发票头</span><span class="sxs-lookup"><span data-stu-id="35390-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="35390-157">[![数据集成中的模板映射](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="35390-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="35390-158">协议发票（Field Service 到 Supply Chain Management）：发票行</span><span class="sxs-lookup"><span data-stu-id="35390-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="35390-159">[![数据集成中的模板映射](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="35390-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
