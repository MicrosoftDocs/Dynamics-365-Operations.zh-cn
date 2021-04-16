---
title: 波次步骤代码
description: 此主题提供波次步骤代码及其用法的概述。
author: josaw1
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f44d500d58dffb37b27d230b0633336eb87996a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838050"
---
# <a name="wave-step-codes"></a><span data-ttu-id="3c862-103">波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="3c862-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c862-104">波次步骤代码是用户可设置并用于将特定波次方法实例链接到相应模板的代码。</span><span class="sxs-lookup"><span data-stu-id="3c862-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="3c862-105">模板包括用于补货、集装化、标签打印、装载计划和排序的模板。</span><span class="sxs-lookup"><span data-stu-id="3c862-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="3c862-106">如果不使用波次步骤代码，用户必须输入普通文本才能引用来自波次方法实例的特定模板。</span><span class="sxs-lookup"><span data-stu-id="3c862-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="3c862-107">普通文本容易出错，因为用户必须确保其为波次模板中的特定波次步骤方法添加的波次步骤文本与目标模板中的波次步骤文本完全匹配。</span><span class="sxs-lookup"><span data-stu-id="3c862-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="3c862-108">特定波次步骤类型的波次步骤类型在单独页面中设置。</span><span class="sxs-lookup"><span data-stu-id="3c862-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="3c862-109">必须在下拉列表中为波次模板中每个需要波次步骤代码的波次步骤方法实例选择波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="3c862-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="3c862-110">在下拉列表中进行的选择将替换普通文本，因此有助于降低人为错误的风险和影响。</span><span class="sxs-lookup"><span data-stu-id="3c862-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="3c862-111">设置代码用于将波次模板中的波次步骤方法链接到该方法的目标模板。</span><span class="sxs-lookup"><span data-stu-id="3c862-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="3c862-112">波次步骤代码功能的使用是可选的。</span><span class="sxs-lookup"><span data-stu-id="3c862-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="3c862-113">此功能已在组织范围内为所有法人启用。</span><span class="sxs-lookup"><span data-stu-id="3c862-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="3c862-114">设置演示</span><span class="sxs-lookup"><span data-stu-id="3c862-114">Setup demo</span></span> 

<span data-ttu-id="3c862-115">必须为此演示安装演示数据，并且必须使用 **USMF** 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="3c862-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="3c862-116">启用波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="3c862-116">Enable wave step codes</span></span>

<span data-ttu-id="3c862-117">请执行以下步骤开启波次步骤代码功能。</span><span class="sxs-lookup"><span data-stu-id="3c862-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="3c862-118">转到 **功能管理**。</span><span class="sxs-lookup"><span data-stu-id="3c862-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="3c862-119">选择以启用称为 **组织范围波次步骤代码** 的功能。</span><span class="sxs-lookup"><span data-stu-id="3c862-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="3c862-120">将把所有法人中的所有现有波次步骤普通文本升级为新结构。</span><span class="sxs-lookup"><span data-stu-id="3c862-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="3c862-121">对所有法人完成此升级后，此功能便会启用。</span><span class="sxs-lookup"><span data-stu-id="3c862-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="3c862-122">如果无法为一个或多个法人启用此功能，也不会为任何法人启用。</span><span class="sxs-lookup"><span data-stu-id="3c862-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="3c862-123">在启用时，将在数据升级期间进行验证。</span><span class="sxs-lookup"><span data-stu-id="3c862-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="3c862-124">如果升级失败，您会收到一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="3c862-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="3c862-125">以下冲突可能导致升级失败：</span><span class="sxs-lookup"><span data-stu-id="3c862-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="3c862-126">存在重复波次步骤普通文本。</span><span class="sxs-lookup"><span data-stu-id="3c862-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="3c862-127">存在自定义项。</span><span class="sxs-lookup"><span data-stu-id="3c862-127">Customizations exist.</span></span>
- <span data-ttu-id="3c862-128">与波次步骤方法实例关联的波次步骤普通文本与预期模板类型不匹配。</span><span class="sxs-lookup"><span data-stu-id="3c862-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="3c862-129">解决验证期间确定的所有冲突之后，您可以重试启用此功能。</span><span class="sxs-lookup"><span data-stu-id="3c862-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="3c862-130">启用此功能后，**波次步骤代码** 页（**仓库管理 \> 设置 \> 波次 \> 波次步骤代码**）变为可用。</span><span class="sxs-lookup"><span data-stu-id="3c862-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="3c862-131">此页中列出启用组织范围波次步骤代码功能后升级的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="3c862-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="3c862-132">创建新波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="3c862-132">Create new wave step codes</span></span>

<span data-ttu-id="3c862-133">可使用 **波次步骤代码** 页创建和删除波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="3c862-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="3c862-134">每个新波次步骤代码及其关联的 ID 必须在所有波次步骤类型中唯一，并且必须是为特定波次步骤类型定义的。</span><span class="sxs-lookup"><span data-stu-id="3c862-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="3c862-135">应用波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="3c862-135">Apply wave step codes</span></span>

<span data-ttu-id="3c862-136">定义正确的波次步骤代码之后，可以将其应用于波次处理方法。</span><span class="sxs-lookup"><span data-stu-id="3c862-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="3c862-137">若要应用波次步骤代码，请转到相应的目标模板。</span><span class="sxs-lookup"><span data-stu-id="3c862-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="3c862-138">下面是波次步骤代码应该针对的目标模板：</span><span class="sxs-lookup"><span data-stu-id="3c862-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="3c862-139">**补货模板：** 仓库管理 \> 设置 \> 补货 \> 补货模板</span><span class="sxs-lookup"><span data-stu-id="3c862-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="3c862-140">**装载计划模板：** 仓库管理 \> 设置 \> 装载 \> 装载计划模板</span><span class="sxs-lookup"><span data-stu-id="3c862-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="3c862-141">**排序模板：** 仓库管理 \> 设置 \> 装箱 \> 出站排序模板</span><span class="sxs-lookup"><span data-stu-id="3c862-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="3c862-142">**集装化模板：** 仓库管理 \> 设置 \> 集装箱 \> 集装箱生成模板</span><span class="sxs-lookup"><span data-stu-id="3c862-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="3c862-143">**标签打印模板：** 仓库管理 \> 设置 \> 文档路线选择 \> 波次标签模板</span><span class="sxs-lookup"><span data-stu-id="3c862-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="3c862-144">从波次模板中选择的波次处理方法引用此列表中的模板时，将应用这些模板。</span><span class="sxs-lookup"><span data-stu-id="3c862-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="3c862-145">如果波次模板中的波次处理方法的波次步骤代码与一个模板类型中的波次步骤代码匹配，将应用该模板。</span><span class="sxs-lookup"><span data-stu-id="3c862-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="3c862-146">示例场景</span><span class="sxs-lookup"><span data-stu-id="3c862-146">Sample scenario</span></span>

<span data-ttu-id="3c862-147">以下过程可帮助确保为波次模板应用您创建的补货模板。</span><span class="sxs-lookup"><span data-stu-id="3c862-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="3c862-148">转到 **仓库管理 \> 设置 \> 波次 \> 波次步骤代码**，然后为 **补货** 类型创建波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="3c862-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="3c862-149">转到 **仓库管理 \> 设置 \> 补货 \> 补货模板**，然后创建补货模板。</span><span class="sxs-lookup"><span data-stu-id="3c862-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="3c862-150">在补货模板中，选择为 **补货** 类型创建的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="3c862-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="3c862-151">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**，然后选择要使用的波次模板。</span><span class="sxs-lookup"><span data-stu-id="3c862-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="3c862-152">在该模板中的 **方法** 快速选项卡上，选择 **捕获** 方法。</span><span class="sxs-lookup"><span data-stu-id="3c862-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="3c862-153">在 **波次步骤代码** 字段中，选择在补货模板中选择的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="3c862-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="3c862-154">请对每个法人执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="3c862-154">You perform these steps for each legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]