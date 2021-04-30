---
title: 实施常见问题
description: 本主题列出了有关如何实行 Dynamics 365 Human Resources 实施项目的常见问题。
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1b4b336953ef6bd74da009b3bb44fbcf2eab5a8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892315"
---
# <a name="go-live-faq"></a><span data-ttu-id="bf919-103">实施常见问题</span><span class="sxs-lookup"><span data-stu-id="bf919-103">Go-live FAQ</span></span> 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bf919-104">本主题列出了有关如何实行 Dynamics 365 Human Resources 实施项目的常见问题。</span><span class="sxs-lookup"><span data-stu-id="bf919-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="bf919-105">何时可以配置和请求生产环境？</span><span class="sxs-lookup"><span data-stu-id="bf919-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="bf919-106">通常，在满足以下条件后才部署生产环境：</span><span class="sxs-lookup"><span data-stu-id="bf919-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="bf919-107">所有自定义都是代码完成的。</span><span class="sxs-lookup"><span data-stu-id="bf919-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="bf919-108">用户验收测试 (UAT) 已完成。</span><span class="sxs-lookup"><span data-stu-id="bf919-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="bf919-109">客户已签核解决方案。</span><span class="sxs-lookup"><span data-stu-id="bf919-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="bf919-110">实行没有任何锁定问题。</span><span class="sxs-lookup"><span data-stu-id="bf919-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="bf919-111">当符合条件的客户处于此阶段时，Microsoft FastTrack 团队将与项目团队一起进行实行评估。</span><span class="sxs-lookup"><span data-stu-id="bf919-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="bf919-112">部署生产环境的先决条件是什么？</span><span class="sxs-lookup"><span data-stu-id="bf919-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="bf919-113">有关先决条件的列表，请参阅 [准备实行](hr-admin-go-live-prepare.md)。</span><span class="sxs-lookup"><span data-stu-id="bf919-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="bf919-114">什么是实行评估？</span><span class="sxs-lookup"><span data-stu-id="bf919-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="bf919-115">实行评估是 [Microsoft FastTrack 计划](/dynamics365/fasttrack/)的一部分。</span><span class="sxs-lookup"><span data-stu-id="bf919-115">The go-live assessment is part of the [Microsoft FastTrack program](/dynamics365/fasttrack/).</span></span> <span data-ttu-id="bf919-116">在此审查中，解决方案架构师会评估实施项目是否已准备就绪，可以成功地进行直接转换和实行。</span><span class="sxs-lookup"><span data-stu-id="bf919-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="bf919-117">必须对每个实施项目执行此审查，才能请求在生产环境中实行。</span><span class="sxs-lookup"><span data-stu-id="bf919-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="bf919-118">我们的沙盒环境已在美国中部数据中心中部署。</span><span class="sxs-lookup"><span data-stu-id="bf919-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="bf919-119">我们希望在美国西部数据中心中部署生产环境。</span><span class="sxs-lookup"><span data-stu-id="bf919-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="bf919-120">我可以在生产配置中选择美国西部作为数据中心吗？</span><span class="sxs-lookup"><span data-stu-id="bf919-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="bf919-121">在部署 Human Resources 环境时，LCS 不会限制您选择其他数据中心，但是我们强烈建议您不要选择其他数据中心。</span><span class="sxs-lookup"><span data-stu-id="bf919-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="bf919-122">如果您希望生产环境位于美国西部数据中心，则应首先将沙盒环境重新部署到美国西部数据中心，对其进行测试，然后签核。</span><span class="sxs-lookup"><span data-stu-id="bf919-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="bf919-123">有关选择正确的数据中心的信息，请参阅[网络要求](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements)。</span><span class="sxs-lookup"><span data-stu-id="bf919-123">For information about selecting the correct datacenter, see [Network requirements](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="bf919-124">我对 Human Resources 环境的 Azure 资源具有什么级别的访问权限？</span><span class="sxs-lookup"><span data-stu-id="bf919-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="bf919-125">对 Human Resources 环境的访问受到限制。</span><span class="sxs-lookup"><span data-stu-id="bf919-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="bf919-126">您无法访问虚拟机 (VM) 或 Microsoft Internet Information Services (IIS)。</span><span class="sxs-lookup"><span data-stu-id="bf919-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="bf919-127">您也无法通过 Microsoft SQL Server Management Studio 访问数据库。</span><span class="sxs-lookup"><span data-stu-id="bf919-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="bf919-128">尽管您无法直接访问 Azure 资源或 Dynamics 365 Human Resources 环境，但您可以使用其他功能来访问数据：</span><span class="sxs-lookup"><span data-stu-id="bf919-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="bf919-129">您可以在自己的 Azure 租户中部署 Azure SQL 数据库，并使用提供您自己的数据库 (BYOD) 功能来同步数据。</span><span class="sxs-lookup"><span data-stu-id="bf919-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="bf919-130">有关详细信息，请参阅[提供您自己的数据库 (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md)。</span><span class="sxs-lookup"><span data-stu-id="bf919-130">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span>

- <span data-ttu-id="bf919-131">您可以使用 Dataverse 集成以将选定的实体同步到 Dataverse 数据库。</span><span class="sxs-lookup"><span data-stu-id="bf919-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="bf919-132">有关详细信息，请参阅 [Dataverse 表](hr-developer-entities.md)。</span><span class="sxs-lookup"><span data-stu-id="bf919-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="bf919-133">生产数据库多久备份一次？</span><span class="sxs-lookup"><span data-stu-id="bf919-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="bf919-134">通过以下频率的自动备份保护数据库：</span><span class="sxs-lookup"><span data-stu-id="bf919-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="bf919-135">备份类型</span><span class="sxs-lookup"><span data-stu-id="bf919-135">Type of backup</span></span> | <span data-ttu-id="bf919-136">频率</span><span class="sxs-lookup"><span data-stu-id="bf919-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="bf919-137">完整数据库备份</span><span class="sxs-lookup"><span data-stu-id="bf919-137">Full database backup</span></span> | <span data-ttu-id="bf919-138">每周</span><span class="sxs-lookup"><span data-stu-id="bf919-138">Weekly</span></span> |
| <span data-ttu-id="bf919-139">差异数据库备份</span><span class="sxs-lookup"><span data-stu-id="bf919-139">Differential database backup</span></span> | <span data-ttu-id="bf919-140">每 12-24 小时</span><span class="sxs-lookup"><span data-stu-id="bf919-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="bf919-141">交易日志备份</span><span class="sxs-lookup"><span data-stu-id="bf919-141">Transaction log backup</span></span> | <span data-ttu-id="bf919-142">每 5 至 10 分钟</span><span class="sxs-lookup"><span data-stu-id="bf919-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="bf919-143">Microsoft 保留足够的备份，以允许过去 14 天内的时间点还原 (PITR)。</span><span class="sxs-lookup"><span data-stu-id="bf919-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="bf919-144">有关详细信息，请参阅 [了解自动 SQL 数据库备份](/azure/azure-sql/database/automated-backups-overview?tabs=single-database)。</span><span class="sxs-lookup"><span data-stu-id="bf919-144">For more information, see [Learn about automatic SQL Database backups](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="bf919-145">我可以请求生产数据库备份的副本吗？</span><span class="sxs-lookup"><span data-stu-id="bf919-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="bf919-146">编号</span><span class="sxs-lookup"><span data-stu-id="bf919-146">No.</span></span> <span data-ttu-id="bf919-147">但是，您可以提交数据库刷新服务请求，以将生产环境复制到沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="bf919-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="bf919-148">您可以在自己的 Azure 租户中部署 Azure SQL 数据库，并使用 BYOD 功能来同步生产环境中的数据。</span><span class="sxs-lookup"><span data-stu-id="bf919-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="bf919-149">有关详细信息，请参阅[提供您自己的数据库 (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md)。</span><span class="sxs-lookup"><span data-stu-id="bf919-149">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="bf919-150">如何将沙盒环境移动到生产环境以供实行？</span><span class="sxs-lookup"><span data-stu-id="bf919-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="bf919-151">由于无法使用复制功能将环境从沙盒移动到生产环境，因此必须使用数据包将数据移动到生产环境中。</span><span class="sxs-lookup"><span data-stu-id="bf919-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="bf919-152">我们建议在整个项目中维护在您的沙箱中配置的实体的清除列表。</span><span class="sxs-lookup"><span data-stu-id="bf919-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="bf919-153">然后，测试实行所需的所有数据包的直接转换和迁移流程。</span><span class="sxs-lookup"><span data-stu-id="bf919-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="bf919-154">在准备实行时，必须手动将所有数据包移动到生产环境中。</span><span class="sxs-lookup"><span data-stu-id="bf919-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="bf919-155">如果生产环境出现故障，该怎么办？</span><span class="sxs-lookup"><span data-stu-id="bf919-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="bf919-156">若要报告生产中断，请按照 [报告生产中断](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md)中介绍的流程操作。</span><span class="sxs-lookup"><span data-stu-id="bf919-156">To report a Production outage, follow the process described in [Report a production outage](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="bf919-157">请参阅</span><span class="sxs-lookup"><span data-stu-id="bf919-157">See also</span></span>

 [<span data-ttu-id="bf919-158">准备实施</span><span class="sxs-lookup"><span data-stu-id="bf919-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]