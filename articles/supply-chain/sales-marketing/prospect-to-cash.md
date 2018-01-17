---
title: "从目标客户到现金"
description: "本主题提供在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 与 Microsoft Dynamics 365 for Sales 之间从目标客户到现金解决方案的概述。"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f169b0ee20a7ca0c8d05c8bdcf2c04d411722f01
ms.openlocfilehash: ff166f89d13acbc3aefcbdb39f485881c81cb42c
ms.contentlocale: zh-cn
ms.lasthandoff: 12/21/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="6edb5-103">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="6edb5-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6edb5-104">从目标客户到现金解决方案提供跨 Dynamics 365 for Finance and Operations Enterprise Edition 与 Dynamics 365 for Sales 的直接同步。</span><span class="sxs-lookup"><span data-stu-id="6edb5-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="6edb5-105">提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="6edb5-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="6edb5-106">当数据在 Finance and Operations 与 Sales 之间流动时，您可以在 Sales 中执行销售和市场营销活动，并可以使用 Finance and Operations 中的库存管理处理订单履行。</span><span class="sxs-lookup"><span data-stu-id="6edb5-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span>

<span data-ttu-id="6edb5-107">在当前版本中，从目标客户到现金解决方案提供以下类型的直接同步：</span><span class="sxs-lookup"><span data-stu-id="6edb5-107">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="6edb5-108">维护 Sales 中的帐户并将它们直接从 Sales 同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6edb5-108">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="6edb5-109">维护 Finance and Operations 中的产品并将其直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="6edb5-109">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="6edb5-110">维护 Sales 中的联系人并将其直接同步到 Finance and Operations 的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="6edb5-110">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="6edb5-111">将 Sales 中的销售报价单直接同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6edb5-111">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="6edb5-112">将 Finance and Operations 中的销售订单直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="6edb5-112">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="6edb5-113">直接在 Sales 和 Finance and Operations 之间同步销售订单</span><span class="sxs-lookup"><span data-stu-id="6edb5-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="6edb5-114">将 Finance and Operations 中的销售发票直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="6edb5-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

<span data-ttu-id="6edb5-115">在早期版本中，从目标客户到现金解决方案提供以下类型的非直接同步：</span><span class="sxs-lookup"><span data-stu-id="6edb5-115">In earlier versions, the Prospect to cash solution provides the following types of non-direct synchronization:</span></span>

- [<span data-ttu-id="6edb5-116">维护 Sales 中的帐户并将它们同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6edb5-116">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
- [<span data-ttu-id="6edb5-117">维护 Sales 中的联系人并将其同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6edb5-117">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
- [<span data-ttu-id="6edb5-118">维护 Finance and Operations 中的产品并将其同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="6edb5-118">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
- [<span data-ttu-id="6edb5-119">在 Sales 中创建销售报价并将其同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6edb5-119">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
- [<span data-ttu-id="6edb5-120">在 Finance and Operations 中创建销售订单并将其同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="6edb5-120">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
- [<span data-ttu-id="6edb5-121">在 Finance and Operations 中创建发票并将它们同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="6edb5-121">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="6edb5-122">Finance and Operations 的系统要求</span><span class="sxs-lookup"><span data-stu-id="6edb5-122">System requirements for Finance and Operations</span></span>

<span data-ttu-id="6edb5-123">若要使用从目标客户到现金解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="6edb5-123">To use the Prospect to cash solution, you must install the following components:</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="6edb5-124">Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）</span><span class="sxs-lookup"><span data-stu-id="6edb5-124">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="6edb5-125">具有平台更新 8（使用平台版本 7.0.4565.16212 的应用程序版本 7.2.11792.56024）的 Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）</span><span class="sxs-lookup"><span data-stu-id="6edb5-125">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212)</span></span>
- <span data-ttu-id="6edb5-126">必须包含以下修补程序：</span><span class="sxs-lookup"><span data-stu-id="6edb5-126">The following hotfixes are required:</span></span>

    - <span data-ttu-id="6edb5-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – 此修补程序可以通过数据集成功能将销售订单从 Sales 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="6edb5-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="6edb5-128">它还提供多个其他增强。</span><span class="sxs-lookup"><span data-stu-id="6edb5-128">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="6edb5-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – 此修补程序可以通过数据集成功能将销售订单行从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="6edb5-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="6edb5-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – 此修补程序可以通过数据集成功能将销售订单从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="6edb5-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6edb5-131">您只需安装 KB4045570，因为该安装包括来自其他修补程序的更改。</span><span class="sxs-lookup"><span data-stu-id="6edb5-131">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="6edb5-132">Dynamics 365 for Finance and Operations 版本 1611（2016 年 11 月）</span><span class="sxs-lookup"><span data-stu-id="6edb5-132">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span> 

- <span data-ttu-id="6edb5-133">具有平台更新 8 或更高版本的 Dynamics 365 for Finance and Operations 版本 1611（2016 年 11 月）</span><span class="sxs-lookup"><span data-stu-id="6edb5-133">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="6edb5-134">必须包含以下修补程序：</span><span class="sxs-lookup"><span data-stu-id="6edb5-134">The following hotfixes are required:</span></span>

    - <span data-ttu-id="6edb5-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - 使用数据集成器将销售订单从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="6edb5-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="6edb5-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - 使用数据集成器将销售订单头和行从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="6edb5-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="6edb5-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - 需要支持通过数据实体进行从目标客户到现金的集成。</span><span class="sxs-lookup"><span data-stu-id="6edb5-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6edb5-138">安装修补程序后，您必须从 **SalesPopulateProspectToCash** 窗体触发以下批处理作业。</span><span class="sxs-lookup"><span data-stu-id="6edb5-138">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="6edb5-139">因为只需要一次，因此此窗体会隐藏。</span><span class="sxs-lookup"><span data-stu-id="6edb5-139">This form is hidden because you only need it once.</span></span> <span data-ttu-id="6edb5-140">要访问窗体，请登录到环境并将以下内容添加到浏览器地址中的 URL：&mi=action:SalesPopulateProspectToCash，例如 https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash。</span><span class="sxs-lookup"><span data-stu-id="6edb5-140">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash.</span></span> <span data-ttu-id="6edb5-141">打开窗体后，单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6edb5-141">When the form opens, click OK.</span></span> <span data-ttu-id="6edb5-142">这将在 **SalesLine**、**SalesQuotationLine** 和 **CustInvoiceTrans** 表中使用唯一值填充新的 **LineCreationSequnceNumber** 字段，并刷新产品列表。</span><span class="sxs-lookup"><span data-stu-id="6edb5-142">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="6edb5-143">这是执行从目标客户到现金的集成所必需的。</span><span class="sxs-lookup"><span data-stu-id="6edb5-143">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="6edb5-144">Sales 的系统要求</span><span class="sxs-lookup"><span data-stu-id="6edb5-144">System requirements for Sales</span></span>

<span data-ttu-id="6edb5-145">若要使用从目标客户到现金解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="6edb5-145">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="6edb5-146">Dynamics 365 for Sales 版本 1612 (8.2.1.207) (DB 8.2.1.207) 联机</span><span class="sxs-lookup"><span data-stu-id="6edb5-146">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="6edb5-147">Dynamics 365 for Sales 版本 1.15.0.0 (v15) 的从目标客户到现金解决方案</span><span class="sxs-lookup"><span data-stu-id="6edb5-147">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

   > [!NOTE]
   >
   > <span data-ttu-id="6edb5-148">具有版本 1.0.0.0 和 1.0.0.1 的模板在 Dynamics 365 for Sales 版本 1.14.1.0 的从目标客户到现金解决方案上受支持</span><span class="sxs-lookup"><span data-stu-id="6edb5-148">Templates with version 1.0.0.0 and 1.0.0.1 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.14.1.0</span></span>
   >
   > <span data-ttu-id="6edb5-149">具有版本 2.0.0.0 和 2.1.0.0 的模板在 Dynamics 365 for Sales 版本 1.15.0.0 的从目标客户到现金解决方案上受支持</span><span class="sxs-lookup"><span data-stu-id="6edb5-149">Templates with version 2.0.0.0 and 2.1.0.0 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="6edb5-150">安装用于 Sales 的从目标客户到现金解决方案</span><span class="sxs-lookup"><span data-stu-id="6edb5-150">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="6edb5-151">从 CustomerSource 下载[用于 Dynamics 365 for Sales 的从目标客户到现金解决方案包 zip 文件](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash)。</span><span class="sxs-lookup"><span data-stu-id="6edb5-151">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="6edb5-152">确保 zip 文件是否未锁定。</span><span class="sxs-lookup"><span data-stu-id="6edb5-152">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="6edb5-153">否则，在尝试安装解决方案包时，您可能会收到以下错误消息：“找不到导入包”。</span><span class="sxs-lookup"><span data-stu-id="6edb5-153">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="6edb5-154">若要解锁 zip 文件，右键单击文件，然后选择**属性**。</span><span class="sxs-lookup"><span data-stu-id="6edb5-154">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="6edb5-155">选择**解锁**。</span><span class="sxs-lookup"><span data-stu-id="6edb5-155">Select **Unblock**.</span></span>
3. <span data-ttu-id="6edb5-156">解压缩和运行 **PackageDeployer.exe**。</span><span class="sxs-lookup"><span data-stu-id="6edb5-156">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="6edb5-157">在 Sales 实例中安装从目标客户到现金解决方案：</span><span class="sxs-lookup"><span data-stu-id="6edb5-157">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="6edb5-158">选择 **Office 365** 作为部署类型。</span><span class="sxs-lookup"><span data-stu-id="6edb5-158">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="6edb5-159">选择**显示高级**。</span><span class="sxs-lookup"><span data-stu-id="6edb5-159">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="6edb5-160">对于快速安装，请选择一个区域。</span><span class="sxs-lookup"><span data-stu-id="6edb5-160">For a quick installation, select a region.</span></span> <span data-ttu-id="6edb5-161">如果您选择**不知道**，系统将搜索所有区域并且安装需要更长时间。</span><span class="sxs-lookup"><span data-stu-id="6edb5-161">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="6edb5-162">输入具有安装权限的管理员用户的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="6edb5-162">Enter the user name and password of an admin user who has installation rights.</span></span>

