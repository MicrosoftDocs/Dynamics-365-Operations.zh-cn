---
title: 调用流程自动化流来创建质检订单
description: 本主题以质检订单为例，提供有关使用 Power Automate 自动化业务流程的资源。
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115165"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="29061-103">调用流程自动化流来创建质检订单</span><span class="sxs-lookup"><span data-stu-id="29061-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="29061-104">组织对自动化标准业务流程，为员工提供更便捷的交互以及利用各种数据信号和系统来自动驱动业务流程的需求日益增长。</span><span class="sxs-lookup"><span data-stu-id="29061-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="29061-105">借助机器人流程自动化 (RPA) 和 Microsoft Power Automate，企业可以使用无代码体验来自动化重复流程，从而提高效率和准确性。</span><span class="sxs-lookup"><span data-stu-id="29061-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="29061-106">Supply Chain Management 的可下载自动化解决方案模板以质量订单为例展示了如何使用 Power Automate 来自动化业务流程。</span><span class="sxs-lookup"><span data-stu-id="29061-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="29061-107">您可以在[此处](https://aka.ms/D365SCMQualityOrderRPASolution)下载自动化解决方案模板。</span><span class="sxs-lookup"><span data-stu-id="29061-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="29061-108">有关此功能及其功能的概述，请参见以下视频：[在 Dynamics 365 Supply Chain Management 中利用 RPA 创建质检订单](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="29061-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="29061-109">![RPA 的自动化选项](media/rpa-automation-options.png "RPA 的自动化选项")</span><span class="sxs-lookup"><span data-stu-id="29061-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="29061-110">Power Automate 解决方案模板包括一个云自动化流和一个桌面自动化流，它们可以在 Supply Chain Management 中自动创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="29061-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="29061-111">自动化可以为响应很多事件和信号启动，包括用户输入或机器信号（包括物联网 (IoT)）。</span><span class="sxs-lookup"><span data-stu-id="29061-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="29061-112">此解决方案模板中包含了 *Q-Order* Power 应用程序示例。</span><span class="sxs-lookup"><span data-stu-id="29061-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="29061-113">它允许用户扫描物料的 QR 码，输入数量并使用相机附加图片。</span><span class="sxs-lookup"><span data-stu-id="29061-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="29061-114">包含了解决方案参数来针对生产设施中的特定用例配置自动化。</span><span class="sxs-lookup"><span data-stu-id="29061-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="29061-115">![创建质检订单](media/rpa-create-quality-roder.png "创建质检订单")</span><span class="sxs-lookup"><span data-stu-id="29061-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="29061-116">有关如何下载、安装和使用示例解决方案来自动创建质检订单的完整的分步指南，请参阅[使用 Power Automate Desktop 通过机器人流程自动化在 Dynamics 365 Supply Chain Management 上自动创建质检订单](/power-automate/desktop-flows/dynamics365-scm-rpa)。</span><span class="sxs-lookup"><span data-stu-id="29061-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

