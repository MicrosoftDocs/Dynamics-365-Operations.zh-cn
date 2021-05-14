---
title: 为配置的产品变型创建产品编号命名法
description: 此步骤显示如何为配置的产品变型设置产品编号命名法，以及如何将其附加到可配置的基础产品。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921003"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="0cd5a-103">为配置的产品变型创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="0cd5a-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0cd5a-104">此步骤显示如何为配置的产品变型设置产品编号命名法，以及如何将其附加到可配置的基础产品。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="0cd5a-105">此过程还演示如何为产品配置模型组件构建配置命名法。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="0cd5a-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0cd5a-107">为基础产品 D0004 分配了新的产品编号命名法。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="0cd5a-108">此任务通常由产品设计师完成。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="0cd5a-109">创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="0cd5a-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="0cd5a-110">转到 **产品信息管理 \> 设置 \> 产品命名法**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="0cd5a-111">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-111">Select **New**.</span></span>
1. <span data-ttu-id="0cd5a-112">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="0cd5a-113">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="0cd5a-114">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-114">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-115">选择 **基础产品编号**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="0cd5a-116">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-116">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-117">选择 **文本常量**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="0cd5a-118">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cd5a-119">在 **文本** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="0cd5a-120">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-120">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-121">选择 **配置**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="0cd5a-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="0cd5a-123">为基础产品分配产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="0cd5a-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="0cd5a-124">转到 **产品信息管理 \> 产品 \> 基础产品**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="0cd5a-125">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0cd5a-126">例如，使用值“D”在 **产品编号** 字段中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="0cd5a-127">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="0cd5a-128">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-128">Select **Edit**.</span></span>
1. <span data-ttu-id="0cd5a-129">在 **使用命名法** 字段中选择 *是*。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="0cd5a-130">在 **产品变型编号命名法** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="0cd5a-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-131">Close the page.</span></span>
1. <span data-ttu-id="0cd5a-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="0cd5a-133">为产品配置模型组件创建命名法</span><span class="sxs-lookup"><span data-stu-id="0cd5a-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="0cd5a-134">转到 **产品信息管理 \> 产品 \> 产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="0cd5a-135">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="0cd5a-136">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="0cd5a-137">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-137">Select **Edit**.</span></span>
1. <span data-ttu-id="0cd5a-138">在 **使用配置命名法** 字段中选择 *是*。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="0cd5a-139">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-139">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-140">选择 **属性值**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="0cd5a-141">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cd5a-142">在 **属性** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="0cd5a-143">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-143">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-144">选择 **文本常量**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="0cd5a-145">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cd5a-146">在 **文本** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="0cd5a-147">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-147">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-148">选择 **属性值**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="0cd5a-149">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cd5a-150">在 **属性** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="0cd5a-151">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-151">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-152">选择 **文本常量**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="0cd5a-153">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cd5a-154">在 **文本** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="0cd5a-155">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-155">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-156">选择 **属性值**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="0cd5a-157">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cd5a-158">在 **属性** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="0cd5a-159">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-159">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-160">选择 **文本常量**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="0cd5a-161">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cd5a-162">在 **文本** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="0cd5a-163">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-163">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-164">选择 **属性值**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="0cd5a-165">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cd5a-166">在 **属性** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="0cd5a-167">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-167">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-168">选择 **文本常量**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="0cd5a-169">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cd5a-170">在 **文本** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="0cd5a-171">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-171">Select **Add**.</span></span>
1. <span data-ttu-id="0cd5a-172">选择 **编号规则值**。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="0cd5a-173">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0cd5a-174">在 **编号规则** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="0cd5a-175">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-175">Close the page.</span></span>
1. <span data-ttu-id="0cd5a-176">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-176">Close the page.</span></span>
1. <span data-ttu-id="0cd5a-177">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0cd5a-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]