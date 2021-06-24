---
title: 启用预算提案（预览）
description: 本主题说明如何在 Finance Insights 中开启预算提案功能。
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222526"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="2325c-103">启用预算提案（预览）</span><span class="sxs-lookup"><span data-stu-id="2325c-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="2325c-104">本主题说明如何在 Finance Insights 中开启预算提案功能。</span><span class="sxs-lookup"><span data-stu-id="2325c-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="2325c-105">按照 Microsoft Dynamics Lifecycle Services (LCS) 中环境页面内的信息连接到该环境的 Azure SQL 主实例。</span><span class="sxs-lookup"><span data-stu-id="2325c-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="2325c-106">运行以下 Transact-SQL (T-SQL) 命令为沙盒环境开启外部测试版。</span><span class="sxs-lookup"><span data-stu-id="2325c-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="2325c-107">（可能必须先在 LCS 中为 IP 地址开启访问权限，才能远程连接到应用程序对象服务器 \[AOS\]。）</span><span class="sxs-lookup"><span data-stu-id="2325c-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="2325c-108">如果您使用的是 10.0.20 或更高版本，或者如果您使用的是 Service Fabric 部署，请跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="2325c-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="2325c-109">Finance Insights 团队应该已经为您开启了外部测试版。</span><span class="sxs-lookup"><span data-stu-id="2325c-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="2325c-110">如果在 **功能管理** 工作区中看不到此功能，或者如果在尝试打开该功能时遇到问题，请联系 <fiap@microsoft.com>。</span><span class="sxs-lookup"><span data-stu-id="2325c-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="2325c-111">打开 **功能管理** 工作区，然后执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="2325c-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="2325c-112">选择 **检查更新**。</span><span class="sxs-lookup"><span data-stu-id="2325c-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="2325c-113">搜索 **预算提案**，然后启用该功能。</span><span class="sxs-lookup"><span data-stu-id="2325c-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="2325c-114">转到 **预算 \> 设置 \> 基本预算 \> 预算提案(预览)**，然后选择 **启用功能**。</span><span class="sxs-lookup"><span data-stu-id="2325c-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
