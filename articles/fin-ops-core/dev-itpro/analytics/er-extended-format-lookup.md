---
title: 电子报告 (ER) 扩展格式查找
description: 本主题描述了将所需格式存储在全局存储库中时如何在 ER 格式查询中设置 ER 格式参考。
author: NickSelin
manager: AnnBe
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c72335d7d83934146f827ef0bb568b79a585a7a5
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015126"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a><span data-ttu-id="f6f98-103">允许用户设置 ER 格式参考，以从全局存储库中查询格式</span><span class="sxs-lookup"><span data-stu-id="f6f98-103">Allow users to set up an ER format reference inquiring a format from the Global repository</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f6f98-104">您可以使用[电子报告](general-electronic-reporting.md) (ER) 框架，以根据各个国家/地区的法律要求为出站文档配置[格式](general-electronic-reporting.md#FormatComponentOutbound)。</span><span class="sxs-lookup"><span data-stu-id="f6f98-104">You can use the [Electronic reporting](general-electronic-reporting.md) (ER) framework to configure [formats](general-electronic-reporting.md#FormatComponentOutbound) for outbound documents in accordance to the legal requirements of various countries/regions.</span></span> <span data-ttu-id="f6f98-105">您还可以使用 ER 框架配置用于解析入站文档的[格式](general-electronic-reporting.md#FormatComponentInbound)，并使用这些文档中的信息附加或更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="f6f98-105">You can also use the ER framework to configure [formats](general-electronic-reporting.md#FormatComponentInbound) for parsing inbound documents and use the information from those documents to append or update application data.</span></span> <span data-ttu-id="f6f98-106">其中每种格式都可以在 Dynamics 365 Finance 实例中用于在特定业务流程中处理入站或出站业务文档。</span><span class="sxs-lookup"><span data-stu-id="f6f98-106">Each of these formats can used in your Dynamics 365 Finance instance for handling inbound or outbound business documents as part of a certain business process.</span></span> 

<span data-ttu-id="f6f98-107">通常，您必须指定特定业务流程中必须使用哪种 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="f6f98-107">Usually, you must specify what ER format must be used in a certain business process.</span></span> <span data-ttu-id="f6f98-108">为此，请在配置为业务流程特定参数的一部分的查找字段中选择单一 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="f6f98-108">To do that, select a single ER format in a lookup field that is configured as part of business process-specific parameters.</span></span> <span data-ttu-id="f6f98-109">这些查找字段通常用 ER 框架的适当 API 来实现。</span><span class="sxs-lookup"><span data-stu-id="f6f98-109">These lookup fields are usually implemented by using the appropriate API of the ER framework.</span></span> <span data-ttu-id="f6f98-110">有关更多信息，请参见 [ER 框架 API - 用于显示格式映射查找的代码](er-apis-app73.md#code-to-display-a-format-mapping-lookup)。</span><span class="sxs-lookup"><span data-stu-id="f6f98-110">For more information, see [ER framework API - code to display a format mapping lookup](er-apis-app73.md#code-to-display-a-format-mapping-lookup).</span></span>

<span data-ttu-id="f6f98-111">例如，当您配置[外贸参数](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters)时，您需要设置对各种 ER 格式的引用，这些格式将用于生成 Intrastat 声明和 Intrastat 声明控制报告。</span><span class="sxs-lookup"><span data-stu-id="f6f98-111">For example, when you configure [foreign trade parameters](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters), you need to set up the references to individual ER formats that will be used to generate the Intrastat declaration and the Intrastat declaration control report.</span></span> <span data-ttu-id="f6f98-112">以下屏幕截图显示了 ER 格式查找字段在**外贸参数**页面中的外观。</span><span class="sxs-lookup"><span data-stu-id="f6f98-112">The screenshots below show how the ER formats lookup field looks like in the **Foreign trade parameters** page.</span></span>

<span data-ttu-id="f6f98-113">如果当前的 Finance 实例不包含与 Intrastat 业务流程相关的 ER 格式，则此查找字段将为空。</span><span class="sxs-lookup"><span data-stu-id="f6f98-113">If the current Finance instance contains no Intrastat business process related ER formats, this lookup field will be empty.</span></span>

<span data-ttu-id="f6f98-114">[![外贸参数页面](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)</span><span class="sxs-lookup"><span data-stu-id="f6f98-114">[![Foreign trade parameters page](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)</span></span>

<span data-ttu-id="f6f98-115">如果当前的 Finance 实例包含与 Intrastat 业务流程相关的 ER 格式，则此查找字段将提供 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="f6f98-115">If the current Finance instance contains Intrastat business process related ER formats, this lookup field offers the ER formats.</span></span>

<span data-ttu-id="f6f98-116">[![外贸参数页面](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)</span><span class="sxs-lookup"><span data-stu-id="f6f98-116">[![Foreign trade parameters page](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)</span></span>

<span data-ttu-id="f6f98-117">此查找仅提供已导入到当前 Finance 实例的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="f6f98-117">This lookup offers only the ER formats that have already been imported to the current Finance instance.</span></span> <span data-ttu-id="f6f98-118">要将 ER 解决方案[导入](./tasks/er-import-configuration-lifecycle-services.md)到当前 Finance 实例中，您需要有权运行 ER 框架的适当功能，并且该框架支持包含 ER 格式的 ER 解决方案的[生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)。</span><span class="sxs-lookup"><span data-stu-id="f6f98-118">To [import](./tasks/er-import-configuration-lifecycle-services.md) ER solutions to the current Finance instance, you need to have permissions to run the appropriate function of the ER framework that supports the [lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md) of ER solutions that contain ER formats.</span></span>

<span data-ttu-id="f6f98-119">从 Finance 版本 10.0.9（2020 年 4 月发布）开始，已扩展了用 ER 框架 API 实现的 ER 格式查找用户界面。</span><span class="sxs-lookup"><span data-stu-id="f6f98-119">Starting in the Finance version 10.0.9 (April 2020 release), the user interface of the ER format lookup that is implemented by using the ER framework API, has been extended.</span></span> <span data-ttu-id="f6f98-120">您仍然可以选择**选择格式配置**快速选项卡上的现有 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="f6f98-120">You can still select the existing ER formats, which on the **Select format configuration** FastTab.</span></span> <span data-ttu-id="f6f98-121">除此之外，扩展查找还提供了新的选项来搜索全局存储库 (GR) 以查找特定的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="f6f98-121">In addition to that, the extended lookup offers the new option to search the Global repository (GR) to locate specific ER formats.</span></span> <span data-ttu-id="f6f98-122">GR 的所有 ER 格式均在**从全局知识库导入**快速选项卡上提供。</span><span class="sxs-lookup"><span data-stu-id="f6f98-122">All ER formats of the GR are offered on the **Import from Global repository** FastTab.</span></span>

<span data-ttu-id="f6f98-123">[![外贸参数页面](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)</span><span class="sxs-lookup"><span data-stu-id="f6f98-123">[![Foreign trade parameters page](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)</span></span>

<span data-ttu-id="f6f98-124">类似于**选择格式配置**快速选项卡，**从全局知识库导入**快速选项卡仅显示适用于在此查找字段选择 ER 格式所针对的业务流程的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="f6f98-124">Similar to the **Select format configuration** FastTab, the **Import from Global repository** FastTab shows only the ER formats that are applicable to the business process for which an ER format is selected in this lookup field.</span></span> <span data-ttu-id="f6f98-125">在此示例中，生成 Intrastat 声明。</span><span class="sxs-lookup"><span data-stu-id="f6f98-125">In this example, the generation of Intrastat declaration.</span></span> <span data-ttu-id="f6f98-126">ER 格式适用于用户当前登录的公司，具体取决于公司所在国家/地区的上下文。</span><span class="sxs-lookup"><span data-stu-id="f6f98-126">The ER format is applicable for the company to which the user is currently signed in, depending on the company country context.</span></span>

<span data-ttu-id="f6f98-127">在**从全局知识库导入**快速选项卡上选择 ER 格式时，会从 GR 将选定的 ER 格式[配置](general-electronic-reporting.md#Configuration)导入到当前的 Finance 实例中。</span><span class="sxs-lookup"><span data-stu-id="f6f98-127">When you select an ER format on the **Import from Global repository** FastTab, the selected ER format [configuration](general-electronic-reporting.md#Configuration) is imported from the GR to the current Finance instance.</span></span>

<span data-ttu-id="f6f98-128">[![外贸参数页面](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)</span><span class="sxs-lookup"><span data-stu-id="f6f98-128">[![Foreign trade parameters page](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)</span></span>

<span data-ttu-id="f6f98-129">然后，如果导入成功完成，则对导入的 ER 格式的引用将存储在此查找字段中。</span><span class="sxs-lookup"><span data-stu-id="f6f98-129">Then, if the import completes successfully, the reference to the imported ER format is stored in this lookup field.</span></span> <span data-ttu-id="f6f98-130">请注意，首次访问 GR 时，您需要点击提供的链接以注册用于管理对 GR 存储的访问的 [Regulatory Configuration Service](https://aka.ms/rcs) (RCS)。</span><span class="sxs-lookup"><span data-stu-id="f6f98-130">Note that when you access the GR for the first time, you need to follow the link provided to sign up for the [Regulatory Configuration Service](https://aka.ms/rcs) (RCS) that is used to manage access to the GR storage.</span></span>

<span data-ttu-id="f6f98-131">[![外贸参数页面](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)</span><span class="sxs-lookup"><span data-stu-id="f6f98-131">[![Foreign trade parameters page](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)</span></span>

<span data-ttu-id="f6f98-132">默认情况下，**从全局知识库导入**快速选项卡会显示基于 GR 内容自动创建的临时存储中的 ER 格式列表，以提高性能。</span><span class="sxs-lookup"><span data-stu-id="f6f98-132">By default, the **Import from Global repository** FastTab presents the list of ER formats from the temporary storage that is automatically created based on the GR content for performance improvements.</span></span> <span data-ttu-id="f6f98-133">第一次打开**从全局知识库导入**快速选项卡时会出现这种情况，打开过程可能需要几秒钟。</span><span class="sxs-lookup"><span data-stu-id="f6f98-133">This happens when the **Import from Global repository** FastTab is opened the first time, which may take several seconds.</span></span>

<span data-ttu-id="f6f98-134">如果您在**从全局知识库导入**快速选项卡中没有看到所需的 ER 格式，但是您确定此 ER 格式存储在 GR 中，请选择**同步**选项。</span><span class="sxs-lookup"><span data-stu-id="f6f98-134">If you do not see the required ER format in the **Import from Global repository** FastTab, but you are sure that this ER format is stored in the GR, select the **Synchronize** option.</span></span> <span data-ttu-id="f6f98-135">这将更新临时存储并将其与 GR 的当前内容同步。</span><span class="sxs-lookup"><span data-stu-id="f6f98-135">This will update the temporary storage and synchronize it with the current content of the GR.</span></span>

## <a name="feature-activation"></a><span data-ttu-id="f6f98-136">功能激活</span><span class="sxs-lookup"><span data-stu-id="f6f98-136">Feature activation</span></span>

<span data-ttu-id="f6f98-137">此功能的可用性由**功能管理**中的**允许查询全局知识库的 ER 格式配置的扩展查找**功能控制。</span><span class="sxs-lookup"><span data-stu-id="f6f98-137">The availability of this functionality is controlled by the feature **Extended lookup of ER format configurations allowing to inquire the Global repository** in the **Feature management**.</span></span> <span data-ttu-id="f6f98-138">默认情况下启用了此功能。</span><span class="sxs-lookup"><span data-stu-id="f6f98-138">This feature is enabled by default.</span></span>

<span data-ttu-id="f6f98-139">[![功能管理页面](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)</span><span class="sxs-lookup"><span data-stu-id="f6f98-139">[![Feature management page](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)</span></span>

## <a name="security-considerations"></a><span data-ttu-id="f6f98-140">安全考虑</span><span class="sxs-lookup"><span data-stu-id="f6f98-140">Security considerations</span></span>

<span data-ttu-id="f6f98-141">**维护配置库** (**ERMaintainSolutionRepositories**) 权限控制通过启用的**从全局知识库导入**快速选项卡打开 ER 格式查找的用户是否能够访问 GR。</span><span class="sxs-lookup"><span data-stu-id="f6f98-141">The **Maintain configuration repositories** (**ERMaintainSolutionRepositories**) privilege controls access to the GR for a user opening the ER format lookup with the enabled **Import from Global repository** FastTab.</span></span> <span data-ttu-id="f6f98-142">要允许用户从 ER 格式查找中访问 GR 内容，您需要直接或者通过使用已分配的角色和职责向客户授予 **ERMaintainSolutionRepositories** 权限，以更改安全设置。</span><span class="sxs-lookup"><span data-stu-id="f6f98-142">To allow users to access the GR content from the ER format lookups, you need to change the security settings by granting the **ERMaintainSolutionRepositories** privilege to users either directly or by using already assigned roles and duties.</span></span>

<span data-ttu-id="f6f98-143">以下屏幕截图显示了如何将此权限授予分配有**会计**角色的用户。</span><span class="sxs-lookup"><span data-stu-id="f6f98-143">The following screenshot shows how this privilege can be granted to users who are assigned to the **Accountant** role.</span></span> <span data-ttu-id="f6f98-144">该角色允许用户在**外贸参数**页上的**文件格式映射**和**报告格式映射**字段中配置外贸参数，并设置对 ER 格式的引用。</span><span class="sxs-lookup"><span data-stu-id="f6f98-144">This role makes allows users to configure foreign trade parameters and set up references to the ER formats in the **File format mapping** and **Report format mapping** fields on the **Foreign trade parameters** page.</span></span>

<span data-ttu-id="f6f98-145">[![安全配置页面](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)</span><span class="sxs-lookup"><span data-stu-id="f6f98-145">[![Security configuration page](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="f6f98-146">限制</span><span class="sxs-lookup"><span data-stu-id="f6f98-146">Limitations</span></span>

<span data-ttu-id="f6f98-147">当前仅支持在 ER 格式查找中访问 GR，以选择用于生成出站文档的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="f6f98-147">Access to the GR in the ER format lookup is currently only supported for the selection of ER formats that are used to generate outbound documents.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="f6f98-148">常见问题</span><span class="sxs-lookup"><span data-stu-id="f6f98-148">Frequently asked questions</span></span>

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a><span data-ttu-id="f6f98-149">为什么不能从 ER 格式查找中访问全局知识库？</span><span class="sxs-lookup"><span data-stu-id="f6f98-149">Why can't I access the Global repository from the ER format lookup?</span></span>

<span data-ttu-id="f6f98-150">如果在**功能管理**页上启用了**允许查询全局知识库的 ER 格式配置的扩展查找**功能，但是用户无法在**从全局知识库导入**快速选项卡中看到 ER 格式，并且**同步**选项可见但已禁用，那么请确保已向用户授予**维护配置库** (**ERMaintainSolutionRepositories**) 权限。</span><span class="sxs-lookup"><span data-stu-id="f6f98-150">If you have enabled the **Extended lookup of ER format configurations allowing to inquire the Global repository** feature on the **Feature management** page, but users can't see ER formats on the **Import from Global repository** FastTab and the **Synchronize** option is visible but disabled, make sure that the **Maintain configuration repositories** (**ERMaintainSolutionRepositories**) privilege has been granted to the user.</span></span> <span data-ttu-id="f6f98-151">与系统管理员联系以获取此权限。</span><span class="sxs-lookup"><span data-stu-id="f6f98-151">Contact your system administrator to receive this privilege.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6f98-152">其他资源</span><span class="sxs-lookup"><span data-stu-id="f6f98-152">Additional resources</span></span>

- [<span data-ttu-id="f6f98-153">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="f6f98-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f6f98-154">电子报告 (ER) 框架 API</span><span class="sxs-lookup"><span data-stu-id="f6f98-154">Electronic reporting (ER) framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="f6f98-155">管理电子报告 (ER) 配置生命周期</span><span class="sxs-lookup"><span data-stu-id="f6f98-155">Manage Electronic reporting (ER) configurations lifecycle</span></span>](general-electronic-reporting-manage-configuration-lifecycle.md)
