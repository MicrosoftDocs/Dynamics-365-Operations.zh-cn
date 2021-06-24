---
title: Regulatory Configuration Service (RCS) - Lifecycle Services (LCS) 存储弃用
description: 本主题提供有关计划作为 Regulatory Configuration Service (RCS) 全局存储库推出的一部分的 Microsoft Dynamics Lifecycle Services (LCS) 存储弃用的信息。
author: JaneA07
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: abaeb34db1d209fa8e5cc83a98c333f42e91f2d2
ms.sourcegitcommit: 7cda434becd198c1cd405e001289777ae7a24fe1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2021
ms.locfileid: "6127911"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a><span data-ttu-id="27def-103">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 存储弃用</span><span class="sxs-lookup"><span data-stu-id="27def-103">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27def-104">使用 Microsoft Dynamics Lifecycle Services (LCS) 作为电子申报 (ER) 配置的存储库将弃用。</span><span class="sxs-lookup"><span data-stu-id="27def-104">The use of Microsoft Dynamics Lifecycle Services (LCS) as a storage repository for Electronic reporting (ER) configurations is being deprecated.</span></span> <span data-ttu-id="27def-105">此弃用将涉及以下更改：</span><span class="sxs-lookup"><span data-stu-id="27def-105">This deprecation will involve the following changes:</span></span>

- <span data-ttu-id="27def-106">在 Microsoft Dynamics 365 应用程序中使用的 Microsoft 生产的配置将不再发布到 LCS 中的共用资产库。</span><span class="sxs-lookup"><span data-stu-id="27def-106">Microsoft-produced configurations that are used in Microsoft Dynamics 365 applications will no longer be published to the Shared asset library in LCS.</span></span> <span data-ttu-id="27def-107">相反，它们将仅通过 RCS 全局存储库发布。</span><span class="sxs-lookup"><span data-stu-id="27def-107">Instead, they will be published only through the RCS Global repository.</span></span> <span data-ttu-id="27def-108">但是，Dynamics AX 2012 的配置将继续发布到 LCS 中的共用资产库，直到 AX 2012 的支持生命周期结束。</span><span class="sxs-lookup"><span data-stu-id="27def-108">However, configurations for Dynamics AX 2012 will continue to be published to the Shared asset library in LCS until the support lifecycle for AX 2012 ends.</span></span>
- <span data-ttu-id="27def-109">允许您将配置从 Finance and Operations 应用和从 RCS 上传到 LCS 中的项目资产库的功能将停用。</span><span class="sxs-lookup"><span data-stu-id="27def-109">The functionality that lets you upload configurations to the Project asset library in LCS from Finance and Operations apps, and from RCS, will be inactivated.</span></span> <span data-ttu-id="27def-110">但是，您仍然可以使用 LCS 中的浏览器将配置上传到项目资产库。</span><span class="sxs-lookup"><span data-stu-id="27def-110">However, you will still be able to use the browser in LCS to upload configurations to the Project asset library.</span></span> <span data-ttu-id="27def-111">因此，您仍然可以向 LCS 添加配置，以便将它们包含在解决方案包中。</span><span class="sxs-lookup"><span data-stu-id="27def-111">Therefore, you will still be able to add configurations to LCS so that they can be included in solution packages.</span></span>
- <span data-ttu-id="27def-112">在一段时间内，从 LCS 导入配置将继续可用，并在 Finance and Operations 应用和 RCS 中受支持。</span><span class="sxs-lookup"><span data-stu-id="27def-112">Import of configurations from LCS will continue to be available and supported in Finance and Operations apps, and in RCS, for some time.</span></span> <span data-ttu-id="27def-113">但是，该功能最终将弃用。</span><span class="sxs-lookup"><span data-stu-id="27def-113">However, the functionality will eventually be deprecated.</span></span> <span data-ttu-id="27def-114">（确切的弃用日期将在稍后公布。）</span><span class="sxs-lookup"><span data-stu-id="27def-114">(The exact deprecation date will be announced later.)</span></span>

## <a name="deprecation-notice"></a><span data-ttu-id="27def-115">弃用通知</span><span class="sxs-lookup"><span data-stu-id="27def-115">Deprecation notice</span></span>

<span data-ttu-id="27def-116">将在 [Dynamics 365 Finance 中的删除或弃用功能 - LCS 弃用通知](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)中传达使用 LCS 作为存储的弃用。</span><span class="sxs-lookup"><span data-stu-id="27def-116">Deprecation of the use of LCS as storage was communicated in [Removed or deprecated features in Dynamics 365 Finance - LCS Deprecation notice](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="27def-117">计划弃用日期为 2022 年 4 月 1 日。</span><span class="sxs-lookup"><span data-stu-id="27def-117">The planned deprecation date is April 1, 2022.</span></span>

## <a name="key-features"></a><span data-ttu-id="27def-118">主要功能</span><span class="sxs-lookup"><span data-stu-id="27def-118">Key features</span></span>

- <span data-ttu-id="27def-119">您可以使用 RCS 创建和编辑配置。</span><span class="sxs-lookup"><span data-stu-id="27def-119">You can use RCS to create and edit configurations.</span></span> <span data-ttu-id="27def-120">然后，可以将这些配置直接从设计器推送到连接的应用程序。</span><span class="sxs-lookup"><span data-stu-id="27def-120">You can then push those configurations directly from the designer to a connected application.</span></span> <span data-ttu-id="27def-121">因此，您可以快速更改和测试您的配置。</span><span class="sxs-lookup"><span data-stu-id="27def-121">Therefore, you can quickly change and test your configurations.</span></span>
- <span data-ttu-id="27def-122">全局存储库是所有 ER 配置的集中存储。</span><span class="sxs-lookup"><span data-stu-id="27def-122">The Global repository is the centralized storage for all ER configurations.</span></span>

## <a name="guidance-for-one-time-and-ongoing-actions"></a><span data-ttu-id="27def-123">一次性和持续操作的指南</span><span class="sxs-lookup"><span data-stu-id="27def-123">Guidance for one-time and ongoing actions</span></span>

<span data-ttu-id="27def-124">本部分介绍了必须一次性完成的一组步骤。</span><span class="sxs-lookup"><span data-stu-id="27def-124">This section describes a set of steps that must be completed one time.</span></span> <span data-ttu-id="27def-125">它还介绍了必须持续完成的步骤。</span><span class="sxs-lookup"><span data-stu-id="27def-125">It also describes steps that must be completed on an ongoing basis afterward.</span></span>

### <a name="one-time-action"></a><span data-ttu-id="27def-126">一次性操作</span><span class="sxs-lookup"><span data-stu-id="27def-126">One-time action</span></span>

<span data-ttu-id="27def-127">将所有必需的配置从 LCS 导入到 RCS，然后将其从 RCS 发布到全局存储库。</span><span class="sxs-lookup"><span data-stu-id="27def-127">Import all required configurations from LCS to RCS, and then publish them from RCS to the Global repository.</span></span> <span data-ttu-id="27def-128">如果您使用特定于项目的资产库在 LCS 中存储派生的配置，则必须在 LCS 仍可访问时完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="27def-128">If you're using project-specific asset libraries to store derived configurations in LCS, the following steps must be completed while LCS is still accessible.</span></span>

1. <span data-ttu-id="27def-129">如果 RCS 实例尚不可用，请提供一个。</span><span class="sxs-lookup"><span data-stu-id="27def-129">If an RCS instance isn't already available, provision one.</span></span> <span data-ttu-id="27def-130">有关详细信息，请参阅 [RCS 概述](rcs-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="27def-130">For more information, see [RCS overview](rcs-overview.md).</span></span>
2. <span data-ttu-id="27def-131">在预配的 RCS 实例中，对于资产库中包含派生的 ER 配置的每个 LCS 项目，注册相应的 LCS 存储库。</span><span class="sxs-lookup"><span data-stu-id="27def-131">In the provisioned RCS instance, for every LCS project in the Asset library that includes derived ER configurations, register the appropriate LCS repository.</span></span>
3. <span data-ttu-id="27def-132">将 ER 配置从 LCS 存储库导入到 RCS。</span><span class="sxs-lookup"><span data-stu-id="27def-132">Import the ER configurations from the LCS repositories to RCS.</span></span> <span data-ttu-id="27def-133">有关详细信息，请参阅[从 LCS 导入配置](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md)。</span><span class="sxs-lookup"><span data-stu-id="27def-133">For more information, see [Import configurations from LCS](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md).</span></span>
4. <span data-ttu-id="27def-134">如果未自动提供全局存储库，请在 RCS 中注册它。</span><span class="sxs-lookup"><span data-stu-id="27def-134">If the Global repository isn't automatically provided, register it in RCS.</span></span>
5. <span data-ttu-id="27def-135">将所有派生的配置从当前的 RCS 实例上传到全局存储库。</span><span class="sxs-lookup"><span data-stu-id="27def-135">Upload all derived configurations from the current RCS instance to the Global repository.</span></span> <span data-ttu-id="27def-136">使用 **允许用户通过一次操作将所有配置上传到 GR 的配置包** 功能来帮助上传。</span><span class="sxs-lookup"><span data-stu-id="27def-136">Use the **Configuration packages that allows the user to upload all configurations to GR in one operation** feature to help with the upload.</span></span> <span data-ttu-id="27def-137">有关详细信息，请参阅 [RCS 全局存储库上传](rcs-global-repo-upload.md)。</span><span class="sxs-lookup"><span data-stu-id="27def-137">For more information, see [RCS global repo upload](rcs-global-repo-upload.md).</span></span>

### <a name="going-forward"></a><span data-ttu-id="27def-138">持续操作</span><span class="sxs-lookup"><span data-stu-id="27def-138">Going forward</span></span>

<span data-ttu-id="27def-139">使用 RCS 中的视觉设计器创建所有新配置。</span><span class="sxs-lookup"><span data-stu-id="27def-139">Use the visual designers in RCS to create all new configurations.</span></span> <span data-ttu-id="27def-140">然后，将配置上传到全局存储库以进行存储。</span><span class="sxs-lookup"><span data-stu-id="27def-140">Then upload the configurations to the Global repository for storage.</span></span> <span data-ttu-id="27def-141">有关详细信息，请参阅[在 RCS 中创建 ER 配置并上传到全局存储库](rcs-global-repo-upload.md)。</span><span class="sxs-lookup"><span data-stu-id="27def-141">For more information, see [Create ER configuration in RCS and upload to Global repo](rcs-global-repo-upload.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="27def-142">常见问题</span><span class="sxs-lookup"><span data-stu-id="27def-142">Frequently asked questions</span></span>

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a><span data-ttu-id="27def-143">此更改是否意味着 LCS 不能用作配置的中央存储？</span><span class="sxs-lookup"><span data-stu-id="27def-143">Does this change mean that LCS can't be used as central storage for configurations?</span></span>

<span data-ttu-id="27def-144">是。</span><span class="sxs-lookup"><span data-stu-id="27def-144">Yes.</span></span> <span data-ttu-id="27def-145">允许您将配置从 Finance and Operations 应用上传到 LCS 中的项目资产库的功能将弃用。</span><span class="sxs-lookup"><span data-stu-id="27def-145">The functionality that lets you upload configurations to the Project asset library in LCS from Finance and Operations apps will be deprecated.</span></span> <span data-ttu-id="27def-146">但是，您仍然可以根据需要使用 LCS 中的浏览器将配置上传到项目资产库。</span><span class="sxs-lookup"><span data-stu-id="27def-146">However, you can still use the browser in LCS to upload configurations to the Project asset library as you require.</span></span>

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a><span data-ttu-id="27def-147">我认为 RCS 是用于导入全局模板文件的替代存储库。</span><span class="sxs-lookup"><span data-stu-id="27def-147">I thought that RCS was a replacement repository for importing global template files.</span></span> <span data-ttu-id="27def-148">我没有想过使用它来存储配置。</span><span class="sxs-lookup"><span data-stu-id="27def-148">I didn't think that it's used to store configurations.</span></span> <span data-ttu-id="27def-149">哪个是对的？</span><span class="sxs-lookup"><span data-stu-id="27def-149">Which is correct?</span></span>

<span data-ttu-id="27def-150">RCS 是用于创建和编辑 ER 配置的设计服务。</span><span class="sxs-lookup"><span data-stu-id="27def-150">RCS is a design service for creating and editing ER configurations.</span></span> <span data-ttu-id="27def-151">RCS 有自己的存储库，称为全局存储库。</span><span class="sxs-lookup"><span data-stu-id="27def-151">RCS has its own repository that is known as the Global repository.</span></span> <span data-ttu-id="27def-152">此存储库用于存储在 RCS 中创建的配置。</span><span class="sxs-lookup"><span data-stu-id="27def-152">This repository is used to store configurations that are created in RCS.</span></span> <span data-ttu-id="27def-153">在使用 LCS 作为存储弃用后，全局存储库将是 Microsoft 配置的单一来源。</span><span class="sxs-lookup"><span data-stu-id="27def-153">After the use of LCS as storage is deprecated, the Global repository will be the single source for Microsoft configurations.</span></span> <span data-ttu-id="27def-154">您必须完成一次性操作，将所需的所有配置从 LCS 导入到 RCS，然后将其从 RCS 发布到全局存储库。</span><span class="sxs-lookup"><span data-stu-id="27def-154">You must complete a one-time action to import all the configurations that you require from LCS to RCS and then publish them from RCS to the Global repository.</span></span>

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a><span data-ttu-id="27def-155">如果没有 LCS，建议使用什么方法存储配置，以便可以轻松管理和传输“测试”和“生产”配置？</span><span class="sxs-lookup"><span data-stu-id="27def-155">Without LCS, what is the suggested way to store configurations so that "test" and "production" configurations can easily be managed and transferred?</span></span>

<span data-ttu-id="27def-156">RCS 使用 *连接的应用程序* 概念。</span><span class="sxs-lookup"><span data-stu-id="27def-156">RCS uses the concept of a *connected application*.</span></span> <span data-ttu-id="27def-157">连接的应用程序在 RCS 和 Finance and Operations 应用的任何实例之间建立一个连接。</span><span class="sxs-lookup"><span data-stu-id="27def-157">A connected application forms a connection between RCS and any instance of Finance and Operations apps.</span></span> <span data-ttu-id="27def-158">因为 RCS 可用于编辑配置，因此可使用连接的应用程序将配置直接从设计人员推送到 Finance and Operations 应用环境。</span><span class="sxs-lookup"><span data-stu-id="27def-158">Because RCS can be used to edit configurations, the connected application can be used to push the configurations directly from the designer to Finance and Operations apps environments.</span></span> <span data-ttu-id="27def-159">因此，您可以快速更改和测试您的配置，而不必经过 LCS 项目级存储。</span><span class="sxs-lookup"><span data-stu-id="27def-159">Therefore, you can quickly change and test your configurations instead of having to go through LCS project-level storage.</span></span>

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a><span data-ttu-id="27def-160">是否有显示设置和管理的任何示例？</span><span class="sxs-lookup"><span data-stu-id="27def-160">Are there any examples that show the setup and management?</span></span>

<span data-ttu-id="27def-161">没有示例，但您可以完成本主题前面的步骤，以将您的配置迁移到 RCS 全局存储库。</span><span class="sxs-lookup"><span data-stu-id="27def-161">There are no examples, but you can complete the steps earlier in this topic to migrate your configurations to the RCS Global repository.</span></span>
