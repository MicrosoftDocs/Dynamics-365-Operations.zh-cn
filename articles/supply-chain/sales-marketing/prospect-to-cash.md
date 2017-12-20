---
title: "从目标客户到现金"
description: "本主题提供在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 与 Microsoft Dynamics 365 for Sales 之间从目标客户到现金解决方案的概述。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
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
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: zh-cn
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="26070-103">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="26070-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="26070-104">从目标客户到现金解决方案提供跨 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 与 Microsoft Dynamics 365 for Sales 的直接同步。</span><span class="sxs-lookup"><span data-stu-id="26070-104">The Prospect to cash solution provides direct synchronization across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, and Microsoft Dynamics 365 for Sales.</span></span> <span data-ttu-id="26070-105">提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。</span><span class="sxs-lookup"><span data-stu-id="26070-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="26070-106">当数据在 Finance and Operations 与 Sales 之间流动时，您可以在 Sales 中执行销售和市场营销活动，并可以使用 Finance and Operations 中的库存管理处理订单履行。</span><span class="sxs-lookup"><span data-stu-id="26070-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span>

<span data-ttu-id="26070-107">在当前版本中，从目标客户到现金解决方案提供以下类型的直接同步：</span><span class="sxs-lookup"><span data-stu-id="26070-107">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="26070-108">维护 Sales 中的帐户并将它们直接从 Sales 同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="26070-108">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="26070-109">维护 Finance and Operations 中的产品并将它们直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="26070-109">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="26070-110">在 Sales 中维护联系人并将它们直接同步到 Finance and Operations 的联系人或客户</span><span class="sxs-lookup"><span data-stu-id="26070-110">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="26070-111">将 Sales 中的销售报价单直接同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="26070-111">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="26070-112">将 Finance and Operations 中的销售订单直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="26070-112">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="26070-113">将 Sales 与 Finance and Operations 的销售订单直接同步</span><span class="sxs-lookup"><span data-stu-id="26070-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="26070-114">将 Finance and Operations 中的销售发票直接同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="26070-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

<span data-ttu-id="26070-115">在早期版本中，从目标客户到现金解决方案提供以下类型的非直接同步：</span><span class="sxs-lookup"><span data-stu-id="26070-115">In earlier versions, the Prospect to cash solution provides the following types of non-direct synchronization:</span></span>

- [<span data-ttu-id="26070-116">维护 Sales 中的帐户并将它们同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="26070-116">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
- [<span data-ttu-id="26070-117">维护 Sales 中的联系人并将它们同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="26070-117">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
- [<span data-ttu-id="26070-118">维护 Finance and Operations 中的产品并将它们同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="26070-118">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
- [<span data-ttu-id="26070-119">在 Sales 中创建销售报价并将它们同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="26070-119">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
- [<span data-ttu-id="26070-120">在 Finance and Operations 中创建销售订单并将它们同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="26070-120">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
- [<span data-ttu-id="26070-121">在 Finance and Operations 中创建发票并将它们同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="26070-121">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="26070-122">Finance and Operations 的系统要求</span><span class="sxs-lookup"><span data-stu-id="26070-122">System requirements for Finance and Operations</span></span>

<span data-ttu-id="26070-123">若要使用从目标客户到现金解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="26070-123">To use the Prospect to cash solution, you must install the following components:</span></span>

### <a name="july-2017"></a><span data-ttu-id="26070-124">2017 年 7 月</span><span class="sxs-lookup"><span data-stu-id="26070-124">July 2017</span></span> 

- <span data-ttu-id="26070-125">具有平台更新 8（使用平台版本 7.0.4565.16212 的应用程序版本 7.2.11792.56024）的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）</span><span class="sxs-lookup"><span data-stu-id="26070-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212)</span></span>
- <span data-ttu-id="26070-126">以下 Finance and Operations 修补程序：</span><span class="sxs-lookup"><span data-stu-id="26070-126">The following hotfixes for Finance and Operations:</span></span>

    - <span data-ttu-id="26070-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – 此修补程序可以通过数据集成功能将销售订单从 Sales 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="26070-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="26070-128">它还提供多个其他增强。</span><span class="sxs-lookup"><span data-stu-id="26070-128">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="26070-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – 此修补程序可以通过数据集成功能将销售订单行从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="26070-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="26070-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – 此修补程序可以通过数据集成功能将销售订单从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="26070-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="26070-131">您只需安装 KB4045570，该安装包括来自其他 Microsoft 知识库 (KB) 文章的更改。</span><span class="sxs-lookup"><span data-stu-id="26070-131">You only have to install KB4045570, because the installation includes the changes from the other Microsoft Knowledge Base (KB) articles.</span></span>

### <a name="november-2016-version-1611"></a><span data-ttu-id="26070-132">2016 年 11 月（版本 1611）</span><span class="sxs-lookup"><span data-stu-id="26070-132">November 2016 (Version 1611)</span></span>

- <span data-ttu-id="26070-133">具有平台更新 8 或更高版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2016 年 11 月）</span><span class="sxs-lookup"><span data-stu-id="26070-133">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (November 2016) with platform update 8 or higher</span></span>

- <span data-ttu-id="26070-134">以下 Finance and Operations 修补程序：</span><span class="sxs-lookup"><span data-stu-id="26070-134">The following hotfixes for Finance and Operations:</span></span>

    - <span data-ttu-id="26070-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - 使用数据集成器将销售订单从 Microsoft Dynamics 365 for Finance and Operations 同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="26070-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Microsoft Dynamics 365 for Finance and Operations to Sales</span></span> 
    - <span data-ttu-id="26070-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - 使用数据集成器将销售订单标头和行从 Microsoft Dynamics 365 for Finance and Operations 同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="26070-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Microsoft Dynamics 365 for Finance and Operations to Sales</span></span>
    - <span data-ttu-id="26070-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - 需要支持通过数据实体进行从目标客户到现金的集成</span><span class="sxs-lookup"><span data-stu-id="26070-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="26070-138">安装修补程序后，您必须从 SalesPopulateProspectToCash 触发以下批处理作业。</span><span class="sxs-lookup"><span data-stu-id="26070-138">After installing the hotfixes you have to trigger the following batch job from the form SalesPopulateProspectToCash.</span></span> <span data-ttu-id="26070-139">因为只需要一次，因此此窗体会隐藏。</span><span class="sxs-lookup"><span data-stu-id="26070-139">This form is hidden as you only need it once.</span></span> <span data-ttu-id="26070-140">若要访问此窗体，请在登录到环境后将以下信息添加到您的浏览器地址：&mi=action:SalesPopulateProspectToCash E.g.</span><span class="sxs-lookup"><span data-stu-id="26070-140">To access it add the following to your browser address, when logged in to the environment: &mi=action:SalesPopulateProspectToCash E.g.</span></span> <span data-ttu-id="26070-141">https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash 在打开的窗体中单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="26070-141">https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash In the form that opens click OK.</span></span>
    <span data-ttu-id="26070-142">这将在“SalesLine”、“SalesQuotationLine”和“CustInvoiceTrans”表中使用唯一值填充新的“LineCreationSequnceNumber”字段，并刷新产品列表。</span><span class="sxs-lookup"><span data-stu-id="26070-142">This will populate a new “LineCreationSequnceNumber” field in “SalesLine”, “SalesQuotationLine” and “CustInvoiceTrans” tables with unique values and refresh the product list.</span></span> <span data-ttu-id="26070-143">若要让 P2C 集成在 7.1 上运行则需要此设置</span><span class="sxs-lookup"><span data-stu-id="26070-143">This is needed for the P2C integration to work on 7.1</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="26070-144">Sales 的系统要求</span><span class="sxs-lookup"><span data-stu-id="26070-144">System requirements for Sales</span></span>

<span data-ttu-id="26070-145">若要使用从目标客户到现金解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="26070-145">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="26070-146">Microsoft Dynamics 365 for Sales 版本 1612 (8.2.1.207) (DB 8.2.1.207) 联机</span><span class="sxs-lookup"><span data-stu-id="26070-146">Microsoft Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="26070-147">Microsoft Dynamics 365 for Sales 版本 1.15.0.0 (v15) 的从目标客户到现金解决方案</span><span class="sxs-lookup"><span data-stu-id="26070-147">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

   > [!NOTE]
   >
   > <span data-ttu-id="26070-148">具有版本 1.0.0.0 和 1.0.0.1 的模板在 Microsoft Dynamics 365 for Sales 版本 1.14.1.0 的从目标客户到现金解决方案上受支持</span><span class="sxs-lookup"><span data-stu-id="26070-148">Templates with version 1.0.0.0 and 1.0.0.1 are supported on Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.1.0</span></span>
   >
   > <span data-ttu-id="26070-149">具有版本 2.0.0.0 和 2.1.0.0 的模板在 Microsoft Dynamics 365 for Sales 版本 1.15.0.0 的从目标客户到现金解决方案上受支持</span><span class="sxs-lookup"><span data-stu-id="26070-149">Templates with version 2.0.0.0 and 2.1.0.0 are upported on Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.15.0.0</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="26070-150">安装用于 Sales 的从目标客户到现金解决方案</span><span class="sxs-lookup"><span data-stu-id="26070-150">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="26070-151">从 CustomerSource 下载[用于 Dynamics 365 for Sales 的从目标客户到现金解决方案包 zip 文件](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash)。</span><span class="sxs-lookup"><span data-stu-id="26070-151">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="26070-152">确保 zip 文件是否未锁定。</span><span class="sxs-lookup"><span data-stu-id="26070-152">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="26070-153">否则，在尝试安装解决方案包时，您将收到以下错误消息：“找不到导入包”。</span><span class="sxs-lookup"><span data-stu-id="26070-153">Otherwise, when you try to install the solution package, you receive the following error message: "No import packages were found."</span></span> <span data-ttu-id="26070-154">若要解锁 zip 文件，右键单击文件，然后选择**属性**。</span><span class="sxs-lookup"><span data-stu-id="26070-154">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="26070-155">然后选择**解锁**。</span><span class="sxs-lookup"><span data-stu-id="26070-155">Then select **Unblock**.</span></span>
3. <span data-ttu-id="26070-156">解压缩和运行 **PackageDeployer.exe**。</span><span class="sxs-lookup"><span data-stu-id="26070-156">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="26070-157">在 Sales 实例中安装从目标客户到现金解决方案：</span><span class="sxs-lookup"><span data-stu-id="26070-157">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="26070-158">选择 **Office 365** 作为部署类型。</span><span class="sxs-lookup"><span data-stu-id="26070-158">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="26070-159">选择**显示高级**。</span><span class="sxs-lookup"><span data-stu-id="26070-159">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="26070-160">对于快速安装，请选择一个区域。</span><span class="sxs-lookup"><span data-stu-id="26070-160">For a quick installation, select a region.</span></span> <span data-ttu-id="26070-161">如果您选择**不知道**，系统将搜索所有区域并且安装需要更长时间。</span><span class="sxs-lookup"><span data-stu-id="26070-161">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="26070-162">输入具有安装权限的管理员用户的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="26070-162">Enter the user name and password of an admin user who has installation rights.</span></span>

