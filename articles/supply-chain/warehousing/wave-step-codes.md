---
title: 波次步骤代码
description: 此主题提供波次步骤代码及其用法的概述。
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992349"
---
# <a name="wave-step-codes"></a><span data-ttu-id="17043-103">波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="17043-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="17043-104">关于波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="17043-104">About wave step codes</span></span>

<span data-ttu-id="17043-105">波次步骤代码是用户可设置并用于将特定波次方法实例链接到相应模板的代码。</span><span class="sxs-lookup"><span data-stu-id="17043-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="17043-106">模板包括用于补货、集装化、标签打印、装载计划和排序的模板。</span><span class="sxs-lookup"><span data-stu-id="17043-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="17043-107">如果不使用波次步骤代码，用户必须输入普通文本才能引用来自波次方法实例的特定模板。</span><span class="sxs-lookup"><span data-stu-id="17043-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="17043-108">普通文本容易出错，因为用户必须确保其为波次模板中的特定波次步骤方法添加的波次步骤文本与目标模板中的波次步骤文本完全匹配。</span><span class="sxs-lookup"><span data-stu-id="17043-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="17043-109">特定波次步骤类型的波次步骤类型在单独页面中设置。</span><span class="sxs-lookup"><span data-stu-id="17043-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="17043-110">必须在下拉列表中为波次模板中每个需要波次步骤代码的波次步骤方法实例选择波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="17043-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="17043-111">在下拉列表中进行的选择将替换普通文本，因此有助于降低人为错误的风险和影响。</span><span class="sxs-lookup"><span data-stu-id="17043-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="17043-112">设置代码用于将波次模板中的波次步骤方法链接到该方法的目标模板。</span><span class="sxs-lookup"><span data-stu-id="17043-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="17043-113">是否使用波次步骤代码功能为可选，并且按法人使用。</span><span class="sxs-lookup"><span data-stu-id="17043-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="17043-114">因此，如果特定法人使用此功能，则将把该法人中的所有现有波次步骤代码升级为新结构。</span><span class="sxs-lookup"><span data-stu-id="17043-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="17043-115">设置演示</span><span class="sxs-lookup"><span data-stu-id="17043-115">Setup demo</span></span> 

<span data-ttu-id="17043-116">必须为此演示安装演示数据，并且必须使用 **USMF** 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="17043-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="17043-117">启用波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="17043-117">Enable wave step codes</span></span>

<span data-ttu-id="17043-118">请执行以下步骤开启波次步骤代码功能。</span><span class="sxs-lookup"><span data-stu-id="17043-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="17043-119">转到**仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="17043-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="17043-120">在**常规**选项卡的**波次处理**快速选项卡上，将**启用波次步骤代码**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="17043-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="17043-121">将把所有现有波次步骤普通文本升级为新结构。</span><span class="sxs-lookup"><span data-stu-id="17043-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="17043-122">为法人完成此升级之后，**波次管理参数**页上的**启用波次步骤代码**选项不再可用。</span><span class="sxs-lookup"><span data-stu-id="17043-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="17043-123">升级期间将进行验证，而如果升级失败，您将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="17043-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="17043-124">以下冲突可能导致升级失败：</span><span class="sxs-lookup"><span data-stu-id="17043-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="17043-125">存在重复波次步骤普通文本。</span><span class="sxs-lookup"><span data-stu-id="17043-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="17043-126">存在自定义项。</span><span class="sxs-lookup"><span data-stu-id="17043-126">Customizations exist.</span></span>
- <span data-ttu-id="17043-127">与波次步骤方法实例关联的波次步骤普通文本与预期模板类型不匹配。</span><span class="sxs-lookup"><span data-stu-id="17043-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="17043-128">解决验证期间确定的所有冲突之后，可以重新运行升级流程。</span><span class="sxs-lookup"><span data-stu-id="17043-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="17043-129">升级成功之后，**波次步骤代码**页（**仓库管理 \> 设置 \> 波次 \> 波次步骤代码**）变为可用。</span><span class="sxs-lookup"><span data-stu-id="17043-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="17043-130">此页中列出开启波次步骤代码功能时升级的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="17043-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="17043-131">创建新波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="17043-131">Create new wave step codes</span></span>

<span data-ttu-id="17043-132">可使用**波次步骤代码**页创建和删除波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="17043-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="17043-133">每个新波次步骤代码及其关联的 ID 必须在所有波次步骤类型中唯一，并且必须是为特定波次步骤类型定义的。</span><span class="sxs-lookup"><span data-stu-id="17043-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="17043-134">应用波次步骤代码</span><span class="sxs-lookup"><span data-stu-id="17043-134">Apply wave step codes</span></span>

<span data-ttu-id="17043-135">定义正确的波次步骤代码之后，可以将其应用于波次处理方法。</span><span class="sxs-lookup"><span data-stu-id="17043-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="17043-136">若要应用波次步骤代码，请转到相应的目标模板。</span><span class="sxs-lookup"><span data-stu-id="17043-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="17043-137">下面是波次步骤代码应该针对的目标模板：</span><span class="sxs-lookup"><span data-stu-id="17043-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="17043-138">**补货模板：** 仓库管理 \> 设置 \> 补货 \> 补货模板</span><span class="sxs-lookup"><span data-stu-id="17043-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="17043-139">**装载计划模板：** 仓库管理 \> 设置 \> 装载 \> 装载计划模板</span><span class="sxs-lookup"><span data-stu-id="17043-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="17043-140">**排序模板：** 仓库管理 \> 设置 \> 装箱 \> 出站排序模板</span><span class="sxs-lookup"><span data-stu-id="17043-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="17043-141">**集装化模板：** 仓库管理 \> 设置 \> 集装箱 \> 集装箱生成模板</span><span class="sxs-lookup"><span data-stu-id="17043-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="17043-142">**标签打印模板：** 仓库管理 \> 设置 \> 文档路线选择 \> 波次标签模板</span><span class="sxs-lookup"><span data-stu-id="17043-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="17043-143">从波次模板中选择的波次处理方法引用此列表中的模板时，将应用这些模板。</span><span class="sxs-lookup"><span data-stu-id="17043-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="17043-144">如果波次模板中的波次处理方法的波次步骤代码与一个模板类型中的波次步骤代码匹配，将应用该模板。</span><span class="sxs-lookup"><span data-stu-id="17043-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="17043-145">示例场景</span><span class="sxs-lookup"><span data-stu-id="17043-145">Sample scenario</span></span>

<span data-ttu-id="17043-146">以下过程可帮助确保为波次模板应用您创建的补货模板。</span><span class="sxs-lookup"><span data-stu-id="17043-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="17043-147">转到**仓库管理 \> 设置 \> 波次 \> 波次步骤代码**，然后为**补货**类型创建波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="17043-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="17043-148">转到**仓库管理 \> 设置 \> 补货 \> 补货模板**，然后创建补货模板。</span><span class="sxs-lookup"><span data-stu-id="17043-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="17043-149">在补货模板中，选择为**补货**类型创建的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="17043-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="17043-150">转到**仓库管理 \> 设置 \> 波次 \> 波次模板**，然后选择要使用的波次模板。</span><span class="sxs-lookup"><span data-stu-id="17043-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="17043-151">在该模板中的**方法**快速选项卡上，选择**捕获**方法。</span><span class="sxs-lookup"><span data-stu-id="17043-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="17043-152">在**波次步骤代码**字段中，选择在补货模板中选择的波次步骤代码。</span><span class="sxs-lookup"><span data-stu-id="17043-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
