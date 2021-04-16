---
title: 启用预算提案（预览）
description: 本主题说明如何在 Finance Insights 中开启预算提案功能。
author: ShivamPandey-msft
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7e90a1a2f2a8e7808f03ce9a6ee58c027bd48d8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818696"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="07e5a-103">启用预算提案（预览）</span><span class="sxs-lookup"><span data-stu-id="07e5a-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="07e5a-104">本主题说明如何在 Finance Insights 中开启预算提案功能。</span><span class="sxs-lookup"><span data-stu-id="07e5a-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="07e5a-105">按照 Microsoft Dynamics Lifecycle Services (LCS) 中环境页面内的信息连接到该环境的 Azure SQL 主实例。</span><span class="sxs-lookup"><span data-stu-id="07e5a-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="07e5a-106">运行以下 Transact-SQL (T-SQL) 命令为沙盒环境开启外部测试版。</span><span class="sxs-lookup"><span data-stu-id="07e5a-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="07e5a-107">（可能必须先在 LCS 中为 IP 地址开启访问权限，才能远程连接到应用程序对象服务器 \[AOS\]。）</span><span class="sxs-lookup"><span data-stu-id="07e5a-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="07e5a-108">如果您的 Microsoft Dynamics 365 Finance 部署是 Service Fabric 部署，则可跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="07e5a-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="07e5a-109">Finance Insights 团队应该已经为您开启了外部测试版。</span><span class="sxs-lookup"><span data-stu-id="07e5a-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="07e5a-110">如果在 **功能管理** 工作区中未看到此功能，或者在尝试开启时遇到问题，请向 [Finance Insights App Preview 团队](mailto:fiap@microsoft.com)发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="07e5a-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="07e5a-111">打开 **功能管理** 工作区，然后执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="07e5a-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="07e5a-112">选择 **检查更新**。</span><span class="sxs-lookup"><span data-stu-id="07e5a-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="07e5a-113">搜索 **预算提案**，然后启用该功能。</span><span class="sxs-lookup"><span data-stu-id="07e5a-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="07e5a-114">转到 **预算 \> 设置 \> 基本预算 \> 预算提案(预览)**，然后选择 **启用功能**。</span><span class="sxs-lookup"><span data-stu-id="07e5a-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="07e5a-115">隐私声明</span><span class="sxs-lookup"><span data-stu-id="07e5a-115">Privacy notice</span></span>
<span data-ttu-id="07e5a-116">预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="07e5a-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]