---
title: 将 Dynamics 365 Supply Chain Management（资产管理）与 Dynamics 365 Guides 集成
description: 本主题说明如何将 Microsoft Dynamics 365 Supply Chain Management 中的资产管理模块与 Dynamics 365 Guides 集成，以便在日常服务和维护工作流中利用混合现实指南。
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: e3e9e74397faec12f6eecff1f562fd9d731ac5e2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230144"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="4af7e-103">将 Dynamics 365 Supply Chain Management（资产管理）与 Dynamics 365 Guides 集成</span><span class="sxs-lookup"><span data-stu-id="4af7e-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="4af7e-104">您可以将 Microsoft Dynamics 365 Supply Chain Management 中的 **资产管理模块** 与 Dynamics 365 Guides 集成，以便在日常服务和维护工作流中利用混合现实指南。</span><span class="sxs-lookup"><span data-stu-id="4af7e-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="4af7e-105">如果指南与资产管理工作订单相关联，则在 Supply Chain Management (Dynamics 365) 移动应用中打开工作订单的维护清单的工作人员会发现指南可用。</span><span class="sxs-lookup"><span data-stu-id="4af7e-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="4af7e-106">然后，工作人员可以在 Dynamics 365 Guides HoloLens 应用中查找并打开该指南。</span><span class="sxs-lookup"><span data-stu-id="4af7e-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4af7e-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="4af7e-107">Prerequisites</span></span>

<span data-ttu-id="4af7e-108">在将指南附加到资产管理工作订单之前，您必须满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="4af7e-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="4af7e-109">[设置 Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) 10.0.9 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="4af7e-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="4af7e-110">[为 Supply Chain Management 应用打开双重写入](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md)。</span><span class="sxs-lookup"><span data-stu-id="4af7e-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="4af7e-111">针对 **MRGuidesFeature** 功能[打开发布外部测试版](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features)。</span><span class="sxs-lookup"><span data-stu-id="4af7e-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="4af7e-112">（对于生产环境，您必须首先提交支持票证，才能将您的租户添加到外部测试组。）</span><span class="sxs-lookup"><span data-stu-id="4af7e-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="4af7e-113">在 **许可证配置** 页面上，[打开以下配置密钥](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference)：</span><span class="sxs-lookup"><span data-stu-id="4af7e-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="4af7e-114">资产管理 \> 资产管理混合现实</span><span class="sxs-lookup"><span data-stu-id="4af7e-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="4af7e-115">混合现实 \> 混合现实指南</span><span class="sxs-lookup"><span data-stu-id="4af7e-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="4af7e-116">[设置 Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) 200.0.0.96 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="4af7e-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="4af7e-117">将 Dynamics 365 Guides 与资产管理配合使用</span><span class="sxs-lookup"><span data-stu-id="4af7e-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="4af7e-118">要关联指南，请使用资产管理中的维护清单行。</span><span class="sxs-lookup"><span data-stu-id="4af7e-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="4af7e-119">您可以通过维护清单模板、维护作业类型或工作订单创建关联，因为这三项全都包含维护清单行。</span><span class="sxs-lookup"><span data-stu-id="4af7e-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="4af7e-120">您可以使用模板来节省时间，因为模板可以与使用它的所有维护作业类型相关联。</span><span class="sxs-lookup"><span data-stu-id="4af7e-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="4af7e-121">例如，与维护作业类型相关联的指南会自动与指定该作业类型的所有工作订单相关联。</span><span class="sxs-lookup"><span data-stu-id="4af7e-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="4af7e-122">另一方面，工作订单仅存在直接与该工作订单相关联的指南。</span><span class="sxs-lookup"><span data-stu-id="4af7e-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="4af7e-123">将指南与维护清单模板关联</span><span class="sxs-lookup"><span data-stu-id="4af7e-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="4af7e-124">要将指南与维护清单模板关联，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4af7e-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="4af7e-125">使用 Dynamics 365 Guides PC 和 HoloLens 应用创建指南。</span><span class="sxs-lookup"><span data-stu-id="4af7e-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="4af7e-126">有关如何创建指南的信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="4af7e-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="4af7e-127">使用 PC 应用创建指南</span><span class="sxs-lookup"><span data-stu-id="4af7e-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="4af7e-128">使用 HoloLens 应用放置全息影像</span><span class="sxs-lookup"><span data-stu-id="4af7e-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="4af7e-129">在 Supply Chain Management 中，[创建维护清单模板](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template)。</span><span class="sxs-lookup"><span data-stu-id="4af7e-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="4af7e-130">将您创建的指南与新维护清单模板中的维护清单行相关联：</span><span class="sxs-lookup"><span data-stu-id="4af7e-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="4af7e-131">在 **维护清单行** 快速选项卡上，选择要与指南关联的行。</span><span class="sxs-lookup"><span data-stu-id="4af7e-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="4af7e-132">在 **关联的指南** 快速选项卡上，选择 **添加指南**。</span><span class="sxs-lookup"><span data-stu-id="4af7e-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="4af7e-133">![将指南与维护清单行关联](media/am-guides-integration-add-guide.png "将指南与维护清单行关联")</span><span class="sxs-lookup"><span data-stu-id="4af7e-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="4af7e-134">在 **名称** 字段中，选择指南，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="4af7e-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="4af7e-135">![在“名称”字段中选择指南](media/am-guides-integration-select-guide.png "在“名称”字段中选择指南")</span><span class="sxs-lookup"><span data-stu-id="4af7e-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="4af7e-136">将维护清单模板与作业类型关联：</span><span class="sxs-lookup"><span data-stu-id="4af7e-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="4af7e-137">[创建维护作业类型](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type)，或选择现有的维护作业类型。</span><span class="sxs-lookup"><span data-stu-id="4af7e-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="4af7e-138">在操作窗格上，选择 **维护作业类型默认值**。</span><span class="sxs-lookup"><span data-stu-id="4af7e-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="4af7e-139">![维护作业类型默认值按钮](media/am-guides-integration-job-defaults.png "维护作业类型默认值按钮")</span><span class="sxs-lookup"><span data-stu-id="4af7e-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="4af7e-140">创建一个行，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="4af7e-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="4af7e-141">![创建行](media/am-guides-integration-add-line.png "创建行")</span><span class="sxs-lookup"><span data-stu-id="4af7e-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="4af7e-142">在操作窗格上，选择 **维护清单**。</span><span class="sxs-lookup"><span data-stu-id="4af7e-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="4af7e-143">![维护清单按钮](media/am-guides-integration-maintenance-checklist.png "维护清单按钮")</span><span class="sxs-lookup"><span data-stu-id="4af7e-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="4af7e-144">在 **维护清单行** 快速选项卡上，添加一个行，然后将 **类型** 字段的值更改为 **模板**。</span><span class="sxs-lookup"><span data-stu-id="4af7e-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="4af7e-145">![更改类型值](media/am-guides-integration-checklist-lines.png "更改类型值")</span><span class="sxs-lookup"><span data-stu-id="4af7e-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="4af7e-146">在 **行详细信息** 快速选项卡上的 **模板** 字段中，选择与指南关联的模板，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="4af7e-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="4af7e-147">![选择模板](media/am-guides-integration-checklist-line-details.png "选择模板")</span><span class="sxs-lookup"><span data-stu-id="4af7e-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="4af7e-148">[创建工作订单](work-orders/manually-created-workorders.md#create-work-order)，然后选择使用与指南相关联的维护清单模板的维护作业类型。</span><span class="sxs-lookup"><span data-stu-id="4af7e-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="4af7e-149">指南会自动与工作订单关联。</span><span class="sxs-lookup"><span data-stu-id="4af7e-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="4af7e-150">![选择维护作业类型](media/am-guides-integration-create-work-order.png "选择维护作业类型")</span><span class="sxs-lookup"><span data-stu-id="4af7e-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="4af7e-151">查看与工作订单和工作人员相关联的指南：</span><span class="sxs-lookup"><span data-stu-id="4af7e-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="4af7e-152">打开[资产管理移动工作区](asset-management-mobile-workspace.md)以访问工作订单。</span><span class="sxs-lookup"><span data-stu-id="4af7e-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="4af7e-153">针对此工作订单，[打开维护清单](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job)。</span><span class="sxs-lookup"><span data-stu-id="4af7e-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="4af7e-154">选择清单行以查看关联的指南。</span><span class="sxs-lookup"><span data-stu-id="4af7e-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="4af7e-155">![与清单行关联的指南](media/am-guides-integration-show-guide.png "与清单行关联的指南")</span><span class="sxs-lookup"><span data-stu-id="4af7e-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="4af7e-156">在 HoloLens 上打开指南。</span><span class="sxs-lookup"><span data-stu-id="4af7e-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="4af7e-157">![在 HoloLens 上打开指南](media/am-guides-integration-hololens-select.png "在 HoloLens 上打开指南")</span><span class="sxs-lookup"><span data-stu-id="4af7e-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="4af7e-158">您也可以直接在工作订单或工作类型的维护清单中关联指南。</span><span class="sxs-lookup"><span data-stu-id="4af7e-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4af7e-159">存在一个已知问题，即，当您将维护清单模板与默认的维护作业类型相关联时，链接到该模板的指南不会出现在 **维护作业类型默认值** 页面的 **关联的指南** 快速选项卡上。</span><span class="sxs-lookup"><span data-stu-id="4af7e-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="4af7e-160">但是，在将该作业类型应用于 **关联的指南** 快速选项卡上的工作订单后，将会显示该指南。</span><span class="sxs-lookup"><span data-stu-id="4af7e-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="4af7e-161">请参阅</span><span class="sxs-lookup"><span data-stu-id="4af7e-161">See also</span></span>

- [<span data-ttu-id="4af7e-162">双写入概览</span><span class="sxs-lookup"><span data-stu-id="4af7e-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="4af7e-163">资产管理概览</span><span class="sxs-lookup"><span data-stu-id="4af7e-163">Asset management overview</span></span>](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]