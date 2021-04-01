---
title: 标识假设并确定试验指标
description: 本主题描述了如何在 Dynamics 365 Commerce 中标识您在电子商务网站上运行的试验的假设和成功指标。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 91614cda804cae4574fce4c9cfb31c63d876f19b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238622"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="34396-103">标识假设并确定试验的成功指标</span><span class="sxs-lookup"><span data-stu-id="34396-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="34396-104">试验生命周期的第一阶段包括标识试验假设并确定要跟踪以评估成功与否的指标。</span><span class="sxs-lookup"><span data-stu-id="34396-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="34396-105">下图显示了在 Dynamics 365 Commerce 中的电子商务网站上[设置和运行试验](experimentation-overview.md)所涉及的所有步骤。</span><span class="sxs-lookup"><span data-stu-id="34396-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="34396-106">其他步骤在单独的主题中介绍。</span><span class="sxs-lookup"><span data-stu-id="34396-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="34396-107">[![试验用户旅程 - 标识](./media/experimentation_identify.svg)](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="34396-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="34396-108">假设是您可以预测试验结果的语句。</span><span class="sxs-lookup"><span data-stu-id="34396-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="34396-109">定义一个假设有许多因素，例如，有关用户行为的研究和您已收集的网站数据。</span><span class="sxs-lookup"><span data-stu-id="34396-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="34396-110">通过假设，您将定义要通过试验验证的假定或理论。</span><span class="sxs-lookup"><span data-stu-id="34396-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="34396-111">试验假设的一个示例可能是“*在夏季，我主页上的白色 T 恤图片比海军毛衣的点击率更高，因为人们希望在夏天穿轻便浅色的衣服。*”</span><span class="sxs-lookup"><span data-stu-id="34396-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="34396-112">在这种情况下，您将创建包括白色 T 恤和海军毛衣的变体，并同时发布它们。</span><span class="sxs-lookup"><span data-stu-id="34396-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="34396-113">若要验证假设，试验的成功与否应与用户的操作直接相关；例如，如果网站用户单击链接或按钮。</span><span class="sxs-lookup"><span data-stu-id="34396-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks on a link or button.</span></span> <span data-ttu-id="34396-114">这些操作必须与将报告给跟踪试验的第三方服务的事件相对应。</span><span class="sxs-lookup"><span data-stu-id="34396-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="34396-115">随着时间的推移，将采取该操作的用户百分比作为一个指标，您可以使用该指标生成报告和进行分析。</span><span class="sxs-lookup"><span data-stu-id="34396-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="34396-116">若要查看所有可用的事件和属性，请参阅 [Commerce 组件的诊断和疑难解答事件](dev-itpro/retail-component-events-diagnostics-troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="34396-116">To review all of the available events and attributes, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>

## <a name="previous-step"></a><span data-ttu-id="34396-117">上一步</span><span class="sxs-lookup"><span data-stu-id="34396-117">Previous step</span></span>
[<span data-ttu-id="34396-118">Dynamics 365 Commerce 中的试验</span><span class="sxs-lookup"><span data-stu-id="34396-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="34396-119">后续步骤</span><span class="sxs-lookup"><span data-stu-id="34396-119">Next step</span></span>
[<span data-ttu-id="34396-120">设计试验</span><span class="sxs-lookup"><span data-stu-id="34396-120">Set up an experiment</span></span>](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]