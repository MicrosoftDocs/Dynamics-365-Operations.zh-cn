---
title: 产品生命周期状态和交易
description: 此主题说明在工程产品的生命周期中如何控制每个生命周期状态允许的交易。
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 989cfd3846e4921d24f5dcf809f1735d2cf62dbb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005319"
---
# <a name="product-lifecycle-states-and-transactions"></a><span data-ttu-id="3b83e-103">产品生命周期状态和交易</span><span class="sxs-lookup"><span data-stu-id="3b83e-103">Product lifecycle states and transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b83e-104">当工程产品经历生命周期时，您能够控制每个生命周期状态允许哪些交易这一点很重要。</span><span class="sxs-lookup"><span data-stu-id="3b83e-104">As an engineering product goes through its lifecycle, it's important that you be able to control which transactions are allowed for each lifecycle state.</span></span> <span data-ttu-id="3b83e-105">例如，尚未处于成熟状态的产品不应放入销售订单中。</span><span class="sxs-lookup"><span data-stu-id="3b83e-105">For example, products that aren't yet in a mature state should not be put on a sales order.</span></span> <span data-ttu-id="3b83e-106">或者，如果产品即将达到生命周期结束状态，您可能需要控制该产品的流入。</span><span class="sxs-lookup"><span data-stu-id="3b83e-106">Alternatively, if a product is reaching its end-of-life state, you might want to control the inflow of that product.</span></span>

<span data-ttu-id="3b83e-107">对于工程产品，生命周期状态的更改将连接到产品的工程版本。</span><span class="sxs-lookup"><span data-stu-id="3b83e-107">For an engineering product, changes to the lifecycle state are connected to the product's engineering versions.</span></span> <span data-ttu-id="3b83e-108">因此，产品的生命周期状态也可以连接到其工程版本。</span><span class="sxs-lookup"><span data-stu-id="3b83e-108">Therefore, the product's lifecycle state can also be connected to its engineering versions.</span></span> <span data-ttu-id="3b83e-109">当产品生命周期状态连接到工程版本时，您可以使用生命周期状态来控制工程版本允许哪些交易。</span><span class="sxs-lookup"><span data-stu-id="3b83e-109">When the product lifecycle state is connected to an engineering version, you can use the lifecycle state to control which transactions are allowed for the engineering version.</span></span>

## <a name="create-and-manage-product-lifecycle-states"></a><span data-ttu-id="3b83e-110">创建和管理产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="3b83e-110">Create and manage product lifecycle states</span></span>

<span data-ttu-id="3b83e-111">要使用产品生命周期状态，请转到 **工程更改管理 \> 设置 \> 产品生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="3b83e-111">To work with product lifecycle states, go to **Engineering change management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="3b83e-112">然后按照以下步骤之一操作。</span><span class="sxs-lookup"><span data-stu-id="3b83e-112">Then follow one of these steps.</span></span>

- <span data-ttu-id="3b83e-113">若要创建新生命周期状态，在操作窗格上选择 **新建**，然后按照以下子部分中的说明设置字段。</span><span class="sxs-lookup"><span data-stu-id="3b83e-113">To create a new lifecycle state, select **New** on the Action Pane, and then set the fields as described in the following subsections.</span></span>
- <span data-ttu-id="3b83e-114">若要编辑现有生命周期状态，在列表窗格中选择它，在操作窗格上选择 **编辑**，然后按照以下子部分中的说明设置字段。</span><span class="sxs-lookup"><span data-stu-id="3b83e-114">To edit an existing lifecycle state, select it in the list pane, select **Edit** on the Action Pane, and then set the fields as described in the following subsections.</span></span>
- <span data-ttu-id="3b83e-115">若要删除现有生命周期状态，在列表窗格中选择它，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="3b83e-115">To delete an existing lifecycle state, select it in the list pane, and then select **Delete** on the Action Pane.</span></span>

> [!NOTE]
> <span data-ttu-id="3b83e-116">工程产品使用与标准（非工程）产品相同的产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="3b83e-116">Engineering products use the same product lifecycle states as standard (non-engineering) products.</span></span> <span data-ttu-id="3b83e-117">您还可以通过转到 **产品信息管理 \> 设置 \> 产品生命周期状态**，来打开此主题中介绍的 **产品生命周期状态** 页。</span><span class="sxs-lookup"><span data-stu-id="3b83e-117">You can also open the **Product lifecycle state** page that is described in this topic by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="3b83e-118">有关工程产品和标准产品的产品生命周期状态的详细信息，请参阅[产品生命周期状态概述](../pim/product-lifecycle.md)。</span><span class="sxs-lookup"><span data-stu-id="3b83e-118">For more information about product lifecycle states, for both engineering products and standard products, see [Product lifecycle state overview](../pim/product-lifecycle.md).</span></span>

### <a name="header"></a><span data-ttu-id="3b83e-119">单头</span><span class="sxs-lookup"><span data-stu-id="3b83e-119">Header</span></span>

<span data-ttu-id="3b83e-120">在产品生命周期状态的标头上设置以下字段。</span><span class="sxs-lookup"><span data-stu-id="3b83e-120">Set the following fields on the header of a product lifecycle state.</span></span>

| <span data-ttu-id="3b83e-121">字段</span><span class="sxs-lookup"><span data-stu-id="3b83e-121">Field</span></span> | <span data-ttu-id="3b83e-122">说明</span><span class="sxs-lookup"><span data-stu-id="3b83e-122">Description</span></span> |
|---|---|
| <span data-ttu-id="3b83e-123">州或省/自治区/直辖市</span><span class="sxs-lookup"><span data-stu-id="3b83e-123">State</span></span> | <span data-ttu-id="3b83e-124">为产品生命周期状态输入名称。</span><span class="sxs-lookup"><span data-stu-id="3b83e-124">Enter a name for the product lifecycle state.</span></span> |
| <span data-ttu-id="3b83e-125">说明</span><span class="sxs-lookup"><span data-stu-id="3b83e-125">Description</span></span> | <span data-ttu-id="3b83e-126">输入产品生命周期状态的描述。</span><span class="sxs-lookup"><span data-stu-id="3b83e-126">Enter a description of the product lifecycle state.</span></span> |

### <a name="general-fasttab"></a><span data-ttu-id="3b83e-127">常规快速选项卡</span><span class="sxs-lookup"><span data-stu-id="3b83e-127">General FastTab</span></span>

<span data-ttu-id="3b83e-128">在 **常规** 快速选项卡上设置以下字段。</span><span class="sxs-lookup"><span data-stu-id="3b83e-128">Set the following fields on the **General** FastTab.</span></span>

| <span data-ttu-id="3b83e-129">字段</span><span class="sxs-lookup"><span data-stu-id="3b83e-129">Field</span></span> | <span data-ttu-id="3b83e-130">说明</span><span class="sxs-lookup"><span data-stu-id="3b83e-130">Description</span></span> |
|---|---|
| <span data-ttu-id="3b83e-131">发布给法人时的默认值</span><span class="sxs-lookup"><span data-stu-id="3b83e-131">Default when released to a legal entity</span></span> | <span data-ttu-id="3b83e-132">对于标准产品，如果默认情况下此生命周期状态应在所有产品首次发布时应用到所有产品，则将此选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="3b83e-132">For standard products, set this option to *Yes* if this lifecycle state should be applied to all products by default when they are first released.</span></span> <span data-ttu-id="3b83e-133">如果此生命周期状态将在以后手动应用则设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="3b83e-133">Set it to *No* if this lifecycle state will be manually applied later.</span></span><p><span data-ttu-id="3b83e-134">此设置不适用于工程产品。</span><span class="sxs-lookup"><span data-stu-id="3b83e-134">This setting isn't applicable to engineering products.</span></span> <span data-ttu-id="3b83e-135">工程产品版本在工程公司中创建后其生命周期状态在它的工程更改类别中指定。</span><span class="sxs-lookup"><span data-stu-id="3b83e-135">The lifecycle state of an engineering product version after it's created in the engineering company is specified in its engineering change category.</span></span> <span data-ttu-id="3b83e-136">当产品发布到运营公司时，将复制产品的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="3b83e-136">When the product is released to an operational company, the lifecycle state of the product is copied.</span></span> <span data-ttu-id="3b83e-137">换言之，当工程产品发布到运营公司时，它的生命周期状态与在工程公司中时的状态相同。</span><span class="sxs-lookup"><span data-stu-id="3b83e-137">In other words, when an engineering product is released to an operational company, it has the same lifecycle state that it had in the engineering company.</span></span> <span data-ttu-id="3b83e-138">生命周期状态可以在运营公司中覆盖。</span><span class="sxs-lookup"><span data-stu-id="3b83e-138">The lifecycle state can be overwritten in the operational company.</span></span></p> |
| <span data-ttu-id="3b83e-139">对于计划有效</span><span class="sxs-lookup"><span data-stu-id="3b83e-139">Is active for planning</span></span> | <span data-ttu-id="3b83e-140">将此选项设置为 *是* 将在主计划和物料清单 (BOM) 级别的计算中包括处于此生命周期状态的产品。</span><span class="sxs-lookup"><span data-stu-id="3b83e-140">Set this option to *Yes* to include products that are in this lifecycle state in calculations at the master planning and bill of materials (BOM) levels.</span></span> <span data-ttu-id="3b83e-141">将其设置为 *否* 将从计算中排除处于此生命周期状态的产品。</span><span class="sxs-lookup"><span data-stu-id="3b83e-141">Set it to *No* to exclude products that are in this lifecycle state from the calculations.</span></span> |

### <a name="enabled-business-processes-fasttab"></a><span data-ttu-id="3b83e-142">“已启用业务流程”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="3b83e-142">Enabled business processes FastTab</span></span>

<span data-ttu-id="3b83e-143">使用 **已启用业务流程** 快速选项卡可以控制当前生命周期状态下的产品可以使用哪些可用业务流程。</span><span class="sxs-lookup"><span data-stu-id="3b83e-143">Use the **Enabled business processes** FastTab to control which of the available business processes can be used with products in the current lifecycle state.</span></span> <span data-ttu-id="3b83e-144">此快速选项卡上列出的流程可以通过以下方式自动找到：</span><span class="sxs-lookup"><span data-stu-id="3b83e-144">The processes that are listed on this FastTab are automatically found in the following way:</span></span>

- <span data-ttu-id="3b83e-145">首次保存新的生命周期状态时，页面将加载当前可用的业务流程。</span><span class="sxs-lookup"><span data-stu-id="3b83e-145">The first time that you save a new lifecycle state, the page loads the business processes that are currently available.</span></span>
- <span data-ttu-id="3b83e-146">如果您将新的业务流程添加到系统，您可以通过在操作窗格上选择 **检查更新**，来为现有生命周期状态更新 **已启用业务流程** 快速选项卡上的列表。</span><span class="sxs-lookup"><span data-stu-id="3b83e-146">If you add new business processes to your system, you can update the list on the **Enabled business processes** FastTab for an existing lifecycle state by selecting **Check for updates** on the Action Pane.</span></span>

<span data-ttu-id="3b83e-147">以下字段可用于 **已启用业务流程** 快速选项卡上列出的每个流程。</span><span class="sxs-lookup"><span data-stu-id="3b83e-147">The following fields are available for each process that is listed on the **Enabled business processes** FastTab.</span></span>

| <span data-ttu-id="3b83e-148">字段</span><span class="sxs-lookup"><span data-stu-id="3b83e-148">Field</span></span> | <span data-ttu-id="3b83e-149">说明</span><span class="sxs-lookup"><span data-stu-id="3b83e-149">Description</span></span> |
|---|---|
| <span data-ttu-id="3b83e-150">加工</span><span class="sxs-lookup"><span data-stu-id="3b83e-150">Process</span></span> | <span data-ttu-id="3b83e-151">此只读字段显示现有业务流程的名称。</span><span class="sxs-lookup"><span data-stu-id="3b83e-151">This read-only field shows the name of an existing business process.</span></span> |
| <span data-ttu-id="3b83e-152">处理区域</span><span class="sxs-lookup"><span data-stu-id="3b83e-152">Process area</span></span> | <span data-ttu-id="3b83e-153">此只读字段显示现有流程区域的名称。</span><span class="sxs-lookup"><span data-stu-id="3b83e-153">This read-only field shows the name of an existing process area.</span></span> |
| <span data-ttu-id="3b83e-154">策略</span><span class="sxs-lookup"><span data-stu-id="3b83e-154">Policy</span></span> | <span data-ttu-id="3b83e-155">选择以下值之一来控制是否以及如何允许处于此生命周期状态的产品使用当前流程：</span><span class="sxs-lookup"><span data-stu-id="3b83e-155">Select one of the following values to control whether and how the current process will be permitted for products that are in this lifecycle state:</span></span><ul><li><span data-ttu-id="3b83e-156">**已启用** – 允许业务流程。</span><span class="sxs-lookup"><span data-stu-id="3b83e-156">**Enabled** – The business process is allowed.</span></span></li><li><span data-ttu-id="3b83e-157">**已阻止** – 不允许流程。</span><span class="sxs-lookup"><span data-stu-id="3b83e-157">**Blocked** – The process isn't allowed.</span></span> <span data-ttu-id="3b83e-158">如果用户尝试对处于此生命周期状态的产品使用该流程，系统将阻止尝试并显示错误。</span><span class="sxs-lookup"><span data-stu-id="3b83e-158">If a user tries to use the process on a product that is in this lifecycle state, the system will block the attempt and show an error instead.</span></span> <span data-ttu-id="3b83e-159">例如，您可以阻止购买生命周期结束的产品。</span><span class="sxs-lookup"><span data-stu-id="3b83e-159">For example, you might block end-of-life products from being purchased.</span></span></li><li><span data-ttu-id="3b83e-160">**已启用，但有警告** – 允许流程，但会显示警告。</span><span class="sxs-lookup"><span data-stu-id="3b83e-160">**Enabled with warning** – The process is allowed, but a warning will be shown.</span></span> <span data-ttu-id="3b83e-161">例如，您可能希望将原型产品放入研发部门创建的生产订单中。</span><span class="sxs-lookup"><span data-stu-id="3b83e-161">For example, you might want a prototype product to be put on a production order that is created by the Research and Development department.</span></span> <span data-ttu-id="3b83e-162">但是，其他部门应该意识到他们还不应该生产该产品。</span><span class="sxs-lookup"><span data-stu-id="3b83e-162">However, other departments should be aware that they should not produce the product yet.</span></span></li></ul> |

<span data-ttu-id="3b83e-163">如果您要作为自定义添加更多生命周期状态规则，可以通过在上部窗格中选择 **刷新流程** 来在用户界面 (UI) 中查看这些规则。</span><span class="sxs-lookup"><span data-stu-id="3b83e-163">If you're adding more lifecycle state rules as a customization, you can view those rules in the user interface (UI) by selecting **Refresh processes** in the upper pane.</span></span> <span data-ttu-id="3b83e-164">**刷新流程** 按钮仅对管理员可用。</span><span class="sxs-lookup"><span data-stu-id="3b83e-164">The **Refresh processes** button is available only to administrators.</span></span>
