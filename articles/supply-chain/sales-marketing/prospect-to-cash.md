---
title: "从目标客户到现金"
description: "本主题提供在 Dynamics 365 for Finance and Operations Enterprise Edition 与 Dynamics 365 for Sales 之间从目标客户到现金解决方案的概述。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="20bb5-103">从目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="20bb5-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="20bb5-104">从目标客户到现金解决方案使用[数据集成](/common-data-service/entity-reference/dynamics-365-integration) 通过 Common Data Service 跨 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 和 Dynamics 365 for Sales 实例同步数据。</span><span class="sxs-lookup"><span data-stu-id="20bb5-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="20bb5-105">提供数据集成功能的从目标客户到现金模板启用 Finance and Operations 与 Sales 之间的帐户、联系人、产品、销售报价、销售订单和销售发票数据流。</span><span class="sxs-lookup"><span data-stu-id="20bb5-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="20bb5-106">当数据在 Finance and Operations 与 Sales 之间流动时，您可以在 Sales 中执行销售和市场营销活动以及使用 Finance and Operations 中的库存管理处理订单履行。</span><span class="sxs-lookup"><span data-stu-id="20bb5-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="20bb5-107">此解决方案提供在以下区域的集成：</span><span class="sxs-lookup"><span data-stu-id="20bb5-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="20bb5-108">维护 Sales 中的帐户并将它们同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20bb5-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="20bb5-109">维护 Sales 中的联系人并将它们同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20bb5-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="20bb5-110">维护 Finance and Operations 中的产品并将它们同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="20bb5-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="20bb5-111">在 Sales 中创建销售报价并将它们同步到 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20bb5-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="20bb5-112">在 Finance and Operations 中创建销售订单并将它们同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="20bb5-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="20bb5-113">在 Finance and Operations 中创建发票并将它们同步到 Sales</span><span class="sxs-lookup"><span data-stu-id="20bb5-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="20bb5-114">Dynamics 365 for Finance and Operations Enterprise Edition 的系统要求</span><span class="sxs-lookup"><span data-stu-id="20bb5-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="20bb5-115">若要使用从目标客户到现金解决方案，必须进行以下安装：</span><span class="sxs-lookup"><span data-stu-id="20bb5-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="20bb5-116">具有平台更新 8（使用平台 7.0.4565.16212 的应用 7.2.11792.56024）的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）</span><span class="sxs-lookup"><span data-stu-id="20bb5-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="20bb5-117">Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）的两个修补程序。</span><span class="sxs-lookup"><span data-stu-id="20bb5-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="20bb5-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - 此修补程序可以通过数据集成功能将销售订单行从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="20bb5-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="20bb5-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - 此修补程序可以通过数据集成功能将销售订单从 Finance and Operations 同步到 Sales。</span><span class="sxs-lookup"><span data-stu-id="20bb5-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="20bb5-120">**注意**：您只需安装 KB4036524，该安装包括来自 KB4036461 的更改。</span><span class="sxs-lookup"><span data-stu-id="20bb5-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="20bb5-121">Dynamics 365 for Sales 的系统要求</span><span class="sxs-lookup"><span data-stu-id="20bb5-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="20bb5-122">若要使用从目标客户到现金解决方案，必须进行以下安装：</span><span class="sxs-lookup"><span data-stu-id="20bb5-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="20bb5-123">Dynamics 365 for Sales 版本 1612 (8.2.1.207) (DB 8.2.1.207) 联机或更高版本。</span><span class="sxs-lookup"><span data-stu-id="20bb5-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="20bb5-124">Dynamics 365 for Sales 版本 1.14.0.0 (v14) 或更高版本的从目标客户到现金解决方案。</span><span class="sxs-lookup"><span data-stu-id="20bb5-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="20bb5-125">安装用于 Sales 的从目标客户到现金解决方案</span><span class="sxs-lookup"><span data-stu-id="20bb5-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="20bb5-126">在 CustomerSource 上下载[用于 Dynamics 365 for Sales 的从目标客户到现金解决方案包 zip 文件](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash)。</span><span class="sxs-lookup"><span data-stu-id="20bb5-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="20bb5-127">确保 zip 文件未锁定，否则当您安装解决方案包时会收到错误消息“找不到导入包”。</span><span class="sxs-lookup"><span data-stu-id="20bb5-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="20bb5-128">要解锁文件，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="20bb5-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="20bb5-129">右键单击 zip 文件。</span><span class="sxs-lookup"><span data-stu-id="20bb5-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="20bb5-130">选择**属性**，然后选择**解锁**。</span><span class="sxs-lookup"><span data-stu-id="20bb5-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="20bb5-131">解压缩和运行 PackageDeployer.exe。</span><span class="sxs-lookup"><span data-stu-id="20bb5-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="20bb5-132">在 Sales 实例中安装从目标客户到现金解决方案。</span><span class="sxs-lookup"><span data-stu-id="20bb5-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="20bb5-133">选择 **Office 365** 部署类型。</span><span class="sxs-lookup"><span data-stu-id="20bb5-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="20bb5-134">选择**显示高级**。</span><span class="sxs-lookup"><span data-stu-id="20bb5-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="20bb5-135">对于快速安装，请选择**区域**。</span><span class="sxs-lookup"><span data-stu-id="20bb5-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="20bb5-136">如果您选择**不知道**，系统将搜索所有区域并且需要更长的安装时间。</span><span class="sxs-lookup"><span data-stu-id="20bb5-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="20bb5-137">输入具有安装用户权限的管理员用户的**用户名**和**密码**。</span><span class="sxs-lookup"><span data-stu-id="20bb5-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

