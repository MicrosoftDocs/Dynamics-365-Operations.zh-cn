---
title: 为本地部署配置 SQL Server Reporting Services
description: 本主题提供有关为本地部署配置 SQL Server Reporting Services (SSRS) 的信息。
author: PeterRFriis
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: cc8bb6c3a993274f70316145f2ec8a6217e6886c
ms.sourcegitcommit: d7c18228256daeefbf6518c3ef82fed4f7dbc161
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571696"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a><span data-ttu-id="28e76-103">为本地部署配置 SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="28e76-103">Configure SQL Server Reporting Services for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28e76-104">使用本主题中的步骤为您的 Microsoft Dynamics 365 Finance + Operations (on-premises) 部署配置 SQL Server Reporting Services (SSRS)。</span><span class="sxs-lookup"><span data-stu-id="28e76-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 Finance + Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="28e76-105">打开 Reporting Services 配置管理器应用程序。</span><span class="sxs-lookup"><span data-stu-id="28e76-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="28e76-106">保留默认的 **服务器名称**（这应是当前计算机的名称）和 **报表服务器实例**，**MSSQLSERVER**。</span><span class="sxs-lookup"><span data-stu-id="28e76-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span>
3. <span data-ttu-id="28e76-107">单击 **连接**。</span><span class="sxs-lookup"><span data-stu-id="28e76-107">Click **Connect**.</span></span>

    <span data-ttu-id="28e76-108">[![报表服务配置连接](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>

4. <span data-ttu-id="28e76-109">单击 **服务帐户** 选项卡并验证设置是否与以下图形匹配。</span><span class="sxs-lookup"><span data-stu-id="28e76-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="28e76-110">[![服务帐户选项卡](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>

5. <span data-ttu-id="28e76-111">单击 **Web 服务 URL** 选项卡并验证设置是否与以下图形匹配。</span><span class="sxs-lookup"><span data-stu-id="28e76-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="28e76-112">[![Web 服务 URL 选项卡](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span>

6. <span data-ttu-id="28e76-113">单击 **数据库** 选项卡并验证 **数据库名称** 和 **凭据设置** 是否与以下图形匹配。</span><span class="sxs-lookup"><span data-stu-id="28e76-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="28e76-114">你需要创建一个新的数据库。</span><span class="sxs-lookup"><span data-stu-id="28e76-114">You will need to create a new database.</span></span> <span data-ttu-id="28e76-115">为此，请单击 **更改数据库**，然后验证新的数据库名称是否为：**DynamicsAxReportServer**。</span><span class="sxs-lookup"><span data-stu-id="28e76-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="28e76-116">[![数据库选项卡](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>

7. <span data-ttu-id="28e76-117">单击 **Web 门户 URL** 选项卡并验证设置是否与以下图形匹配。</span><span class="sxs-lookup"><span data-stu-id="28e76-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="28e76-118">你必须单击 **应用** 以创建和正确配置门户。</span><span class="sxs-lookup"><span data-stu-id="28e76-118">You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="28e76-119">[![Web 门户 URL 选项卡](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>

    <span data-ttu-id="28e76-120">配置门户后，**Web 门户** 选项卡将与以下图形匹配。</span><span class="sxs-lookup"><span data-stu-id="28e76-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>

    <span data-ttu-id="28e76-121">[![Web 门户选项卡](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>

8. <span data-ttu-id="28e76-122">单击报表 URL 以查看 SQL Server Reporting Services Web 门户。</span><span class="sxs-lookup"><span data-stu-id="28e76-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span>
9. <span data-ttu-id="28e76-123">当你在该门户时，创建名为 **Dynamics** 的新文件夹。</span><span class="sxs-lookup"><span data-stu-id="28e76-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="28e76-124">[![Dynamics 文件夹](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>

10. <span data-ttu-id="28e76-125">在 **Reporting Services 配置管理器** 中，单击 **电子邮件设置** 选项卡并验证设置是否与以下图形匹配。</span><span class="sxs-lookup"><span data-stu-id="28e76-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="28e76-126">[![电子邮件设置选项卡](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>

11. <span data-ttu-id="28e76-127">单击 **执行帐户** 选项卡并验证设置是否与以下图形匹配。</span><span class="sxs-lookup"><span data-stu-id="28e76-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="28e76-128">[![执行帐户选项卡](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>

    <span data-ttu-id="28e76-129">不要更改 **加密密钥** 选项卡上的默认设置。</span><span class="sxs-lookup"><span data-stu-id="28e76-129">Don't change the default settings on the **Encryption Keys** tab.</span></span>

    <span data-ttu-id="28e76-130">[![加密密钥选项卡](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>

12. <span data-ttu-id="28e76-131">单击 **订阅设置** 选项卡，并验证设置是否与以下图形匹配。</span><span class="sxs-lookup"><span data-stu-id="28e76-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="28e76-132">[![订阅设置选项卡](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>

    <span data-ttu-id="28e76-133">不要更改 **扩大部署** 选项卡上的默认设置。</span><span class="sxs-lookup"><span data-stu-id="28e76-133">Don't change the default settings on the **Scale-out Deployment** tab.</span></span>

    <span data-ttu-id="28e76-134">[![扩大部署选项卡](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>

    <span data-ttu-id="28e76-135">不要更改 **Power BI 集成** 选项卡上的默认设置。</span><span class="sxs-lookup"><span data-stu-id="28e76-135">Don't change the default settings on the **Power BI Integration** tab.</span></span>

    <span data-ttu-id="28e76-136">[![Power BI 集成选项卡](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span>

13. <span data-ttu-id="28e76-137">单击 **退出** 以关闭 **Reporting Services 配置管理器**。</span><span class="sxs-lookup"><span data-stu-id="28e76-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="28e76-138">[![关闭 Reporting Services 配置管理器](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="28e76-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
