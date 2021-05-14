---
title: 审核产品配置模型
description: 该过程的运行要求至少有一个产品配置模型可用。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c945756997b0580ac7ffb19261f9184e53a1c10
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920499"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="32ca6-103">审核产品配置模型</span><span class="sxs-lookup"><span data-stu-id="32ca6-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32ca6-104">该过程的运行要求至少有一个产品配置模型可用。</span><span class="sxs-lookup"><span data-stu-id="32ca6-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="32ca6-105">该过程使用演示数据公司 USMF 的高端扬声器模型。</span><span class="sxs-lookup"><span data-stu-id="32ca6-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="32ca6-106">请注意，此模型已通过审核，但该过程将向您介绍完整流程。</span><span class="sxs-lookup"><span data-stu-id="32ca6-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="32ca6-107">转到 **产品信息管理 \> 产品 \> 产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="32ca6-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="32ca6-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="32ca6-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="32ca6-109">选择该过程的“高端扬声器模型”。</span><span class="sxs-lookup"><span data-stu-id="32ca6-109">Select the High end speaker model for this procedure.</span></span>  
1. <span data-ttu-id="32ca6-110">选择 **版本**。</span><span class="sxs-lookup"><span data-stu-id="32ca6-110">Select **Versions**.</span></span>
1. <span data-ttu-id="32ca6-111">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="32ca6-111">Select **New**.</span></span>
1. <span data-ttu-id="32ca6-112">在 **产品编号** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="32ca6-112">In the **Product number** field, enter or select a value.</span></span>
    * <span data-ttu-id="32ca6-113">该参考产品代表一个产品配置模型版本。</span><span class="sxs-lookup"><span data-stu-id="32ca6-113">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="32ca6-114">仅拥有基于约束的配置技术的基础产品会出现在此列表中。</span><span class="sxs-lookup"><span data-stu-id="32ca6-114">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
1. <span data-ttu-id="32ca6-115">在 **开始日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="32ca6-115">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="32ca6-116">选择产品模型版本何时可用。</span><span class="sxs-lookup"><span data-stu-id="32ca6-116">Select when the product model version will be available.</span></span>  
1. <span data-ttu-id="32ca6-117">在 **结束日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="32ca6-117">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="32ca6-118">选择此产品模型版本将过期的结束日期，或选择“从不”。</span><span class="sxs-lookup"><span data-stu-id="32ca6-118">Select an end date when this product model version will expire, or select Never.</span></span>  
1. <span data-ttu-id="32ca6-119">选择 **审核** 打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="32ca6-119">Select **Approve** to open the drop dialog.</span></span>
1. <span data-ttu-id="32ca6-120">在 **审核人** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="32ca6-120">In the **Approved by** field, enter or select a value.</span></span>
    * <span data-ttu-id="32ca6-121">选择负责审批产品模型用于工序的人员。</span><span class="sxs-lookup"><span data-stu-id="32ca6-121">Select the person who is responsible for approving product models for use in operations.</span></span>  
1. <span data-ttu-id="32ca6-122">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="32ca6-122">Select **OK**.</span></span>
1. <span data-ttu-id="32ca6-123">在 **定价方法** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="32ca6-123">In the **Pricing method** field, select an option.</span></span>
    * <span data-ttu-id="32ca6-124">启用产品模型版本。</span><span class="sxs-lookup"><span data-stu-id="32ca6-124">Activate the product model version.</span></span> <span data-ttu-id="32ca6-125">一次只可能启用一个产品的一个产品模型。</span><span class="sxs-lookup"><span data-stu-id="32ca6-125">It is only possible to have one product active for one product model at a time.</span></span>  
1. <span data-ttu-id="32ca6-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="32ca6-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]