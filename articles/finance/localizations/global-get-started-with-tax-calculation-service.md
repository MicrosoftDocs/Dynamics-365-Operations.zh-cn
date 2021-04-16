---
title: 开始使用税务计算加载项
description: 本主题说明如何设置税务计算加载项。
author: wangchen
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 835ae33fba31d4bccb218969aa9aa61eaa7a3061
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832585"
---
# <a name="get-started-with-the-tax-calculation-add-in-preview"></a><span data-ttu-id="cf48d-103">开始使用税务计算加载项（预览）</span><span class="sxs-lookup"><span data-stu-id="cf48d-103">Get started with the tax calculation add-in (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="cf48d-104">本主题提供有关如何开始使用税务计算加载项的信息。</span><span class="sxs-lookup"><span data-stu-id="cf48d-104">This topic provides information about how to get started with the tax calculation add-in.</span></span> <span data-ttu-id="cf48d-105">首先，它指导您完成 Microsoft Dynamics Lifecycle Services (LCS)、Regulatory Configuration Service (RCS) 以及 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中的配置步骤。</span><span class="sxs-lookup"><span data-stu-id="cf48d-105">It first guides you through the configuration steps in Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS), and Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cf48d-106">然后，它审查在 Finance 和 Supply Chain Management 交易中使用税务计算加载项的通用流程。</span><span class="sxs-lookup"><span data-stu-id="cf48d-106">It then reviews the common process for using the tax calculation add-in in Finance and Supply Chain Management transactions.</span></span>

<span data-ttu-id="cf48d-107">该设置由四个主要步骤组成：</span><span class="sxs-lookup"><span data-stu-id="cf48d-107">The setup consists of four main steps:</span></span>

1. <span data-ttu-id="cf48d-108">在 LCS 中，安装税务计算加载项。</span><span class="sxs-lookup"><span data-stu-id="cf48d-108">In LCS, install the tax calculation add-in.</span></span>
2. <span data-ttu-id="cf48d-109">在 RCS 中，设置税务计算功能。</span><span class="sxs-lookup"><span data-stu-id="cf48d-109">In RCS, set up the tax calculation feature.</span></span> <span data-ttu-id="cf48d-110">此设置不特定于法人。</span><span class="sxs-lookup"><span data-stu-id="cf48d-110">This setup isn't specific to a legal entity.</span></span> <span data-ttu-id="cf48d-111">它可以在 Finance 和 Supply Chain Management 中跨法人共享。</span><span class="sxs-lookup"><span data-stu-id="cf48d-111">It can be shared across legal entities in Finance and Supply Chain Management.</span></span>
3. <span data-ttu-id="cf48d-112">在 Finance 和 Supply Chain Management 中，按法人设置税务计算加载项参数。</span><span class="sxs-lookup"><span data-stu-id="cf48d-112">In Finance and Supply Chain Management, set up the tax calculation add-in parameters by legal entity.</span></span>
4. <span data-ttu-id="cf48d-113">在 Finance 和 Supply Chain Management 中，创建销售订单等交易，然后使用税务计算加载项以确定和计算税务。</span><span class="sxs-lookup"><span data-stu-id="cf48d-113">In Finance and Supply Chain Management, create transactions such as sales orders, and use the tax calculation add-in to determine and calculate taxes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cf48d-114">先决条件</span><span class="sxs-lookup"><span data-stu-id="cf48d-114">Prerequisites</span></span>

<span data-ttu-id="cf48d-115">在完成本主题中的过程之前，必须具备以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="cf48d-115">Before you can complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="cf48d-116">您有权访问 LCS 帐户，并且已部署具有运行 Dynamics 365 版本 10.0.18 或更高版本的第 2 层（或以上）环境的 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="cf48d-116">You have access to your LCS account, and you've deployed an LCS project with a Tier 2 (or above) environment that runs Dynamics 365 version 10.0.18 or later.</span></span>
- <span data-ttu-id="cf48d-117">您有权访问 RCS 帐户。</span><span class="sxs-lookup"><span data-stu-id="cf48d-117">You have access to your RCS account.</span></span>
- <span data-ttu-id="cf48d-118">您已与 Microsoft 联系，以在部署的 Finance 或 Supply Chain Management 环境中启用发布外部测试版。</span><span class="sxs-lookup"><span data-stu-id="cf48d-118">You've contacted Microsoft to enable the flighting in your deployed Finance or Supply Chain Management environment.</span></span>

## <a name="set-up-the-tax-calculation-add-in-in-lcs"></a><span data-ttu-id="cf48d-119">在 LCS 中，设置税务计算加载项</span><span class="sxs-lookup"><span data-stu-id="cf48d-119">Set up the tax calculation add-in in LCS</span></span>

1. <span data-ttu-id="cf48d-120">登录到 [LCS](https://lcs.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="cf48d-120">Sign in to [LCS](https://lcs.dynamics.com)</span></span>
2. <span data-ttu-id="cf48d-121">完成 Microsoft Power Platform 集成的设置。</span><span class="sxs-lookup"><span data-stu-id="cf48d-121">Complete the setup for Microsoft Power Platform integration.</span></span> <span data-ttu-id="cf48d-122">有关详细信息，请参阅[加载项概览](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="cf48d-122">For more information, see [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
3. <span data-ttu-id="cf48d-123">选择已部署的非生产环境之一，然后选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-123">Select one of your deployed non-production environments, and then select **Install a new add-in**.</span></span>
4. <span data-ttu-id="cf48d-124">选择 **税务计算(预览)**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-124">Select **Tax calculation (preview)**.</span></span>
5. <span data-ttu-id="cf48d-125">阅读并同意条款和条件，然后选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-125">Read and agree to the terms and conditions, and then select **Install**.</span></span>

## <a name="set-up-the-tax-calculation-add-in-in-rcs"></a><span data-ttu-id="cf48d-126">在 RCS 中，设置税务计算加载项</span><span class="sxs-lookup"><span data-stu-id="cf48d-126">Set up the tax calculation add-in in RCS</span></span>

<span data-ttu-id="cf48d-127">此部分中的步骤与特定法人无关。</span><span class="sxs-lookup"><span data-stu-id="cf48d-127">The steps in this section aren't related to a specific legal entity.</span></span> <span data-ttu-id="cf48d-128">您只能完成一次此过程，并且可以在 RCS 中的任何法人中完成该过程。</span><span class="sxs-lookup"><span data-stu-id="cf48d-128">You must complete this procedure only one time, and you can complete it in any legal entity in RCS.</span></span>

1. <span data-ttu-id="cf48d-129">登录 [RCS](https://marketing.configure.global.dynamics.com/)。</span><span class="sxs-lookup"><span data-stu-id="cf48d-129">Sign in to [RCS](https://marketing.configure.global.dynamics.com/).</span></span>
2. <span data-ttu-id="cf48d-130">在 Finance 中，在 **电子报告** 工作区中，添加新配置提供者。</span><span class="sxs-lookup"><span data-stu-id="cf48d-130">In Finance, in the **Electronic reporting** workspace, add a new configuration provider.</span></span> <span data-ttu-id="cf48d-131">使用您的公司名称作为提供者的名称。</span><span class="sxs-lookup"><span data-stu-id="cf48d-131">Use your company name as the name of the provider.</span></span> <span data-ttu-id="cf48d-132">有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="cf48d-132">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="cf48d-133">选择刚创建的配置提供者，然后选择 **设置有效**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-133">Select the configuration provider that you just created, and then select **Set active**.</span></span>
4. <span data-ttu-id="cf48d-134">选择 **Microsoft** 配置提供者，然后选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-134">Select the **Microsoft** configuration provider, and then select **Repositories**.</span></span>
5. <span data-ttu-id="cf48d-135">在 **类型** 字段中，选择 **全局**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-135">In the **Type** field, select **Global**.</span></span>
6. <span data-ttu-id="cf48d-136">选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-136">Select **Open**.</span></span>
7. <span data-ttu-id="cf48d-137">转到 **税务数据模型**，展开文件树，然后选择 **税务配置 - 欧洲**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-137">Go to **Tax Data Model**, expand the file tree, and then select **Tax Configuration - Europe**.</span></span>
8. <span data-ttu-id="cf48d-138">选择最新版本，然后选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-138">Select the latest version, and then select **Import**.</span></span>
9. <span data-ttu-id="cf48d-139">返回到 **全球化功能(预览)** 工作区，选择 **功能**，选择 **税务计算** 磁贴，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-139">Return to the **Globalization features (Preview)** workspace, select **Features**, select the **Tax calculation** tile, and then select **Add**.</span></span>
10. <span data-ttu-id="cf48d-140">选择以下功能类型之一：</span><span class="sxs-lookup"><span data-stu-id="cf48d-140">Select one of the following feature types:</span></span>

    - <span data-ttu-id="cf48d-141">**新功能** – 创建具有空白内容的功能设置。</span><span class="sxs-lookup"><span data-stu-id="cf48d-141">**New feature** – Create a feature setup that has blank content.</span></span>
    - <span data-ttu-id="cf48d-142">**基于现有功能** – 从现有功能创建功能，然后从现有功能设置复制内容。</span><span class="sxs-lookup"><span data-stu-id="cf48d-142">**Based on existing feature** – Create a feature from an existing feature, and copy the content from the existing feature setup.</span></span>

11. <span data-ttu-id="cf48d-143">输入功能的名称和描述，然后选择 **创建功能**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-143">Enter a name and description for the feature, and then select **Create feature**.</span></span>

    <span data-ttu-id="cf48d-144">创建功能后，将自动创建该功能的草稿版本。</span><span class="sxs-lookup"><span data-stu-id="cf48d-144">After the feature is created, a draft version of it is automatically created.</span></span>

12. <span data-ttu-id="cf48d-145">选择功能的草稿版本，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-145">Select the draft version of the feature, and then select **Edit**.</span></span> <span data-ttu-id="cf48d-146">填写 **税务计算设置** 页面。</span><span class="sxs-lookup"><span data-stu-id="cf48d-146">The **Tax calculation setup** page is filled in.</span></span>
13. <span data-ttu-id="cf48d-147">选择 **配置版本**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-147">Select **Configuration version**.</span></span> <span data-ttu-id="cf48d-148">您应该看到在步骤 8 中导入的配置版本。</span><span class="sxs-lookup"><span data-stu-id="cf48d-148">You should see the configuration version that you imported in step 8.</span></span>

    <span data-ttu-id="cf48d-149">Microsoft 为税务计算加载项提供默认的税务配置。</span><span class="sxs-lookup"><span data-stu-id="cf48d-149">Microsoft provides a default tax configuration for the tax calculation add-in.</span></span> <span data-ttu-id="cf48d-150">此配置涵盖了税务计算行为的大多数要求。</span><span class="sxs-lookup"><span data-stu-id="cf48d-150">This configuration covers most of the requirements for tax calculation behaviors.</span></span> <span data-ttu-id="cf48d-151">它将根据市场反馈进行更新。</span><span class="sxs-lookup"><span data-stu-id="cf48d-151">It will be updated based on market feedbacks.</span></span> <span data-ttu-id="cf48d-152">如果必须扩展配置以满足特定要求，请参阅[如何在税务服务中生成扩展](https://go.microsoft.com/fwlink/?linkid=2138483)，以获取有关如何生成和选择自己的税务配置的信息。</span><span class="sxs-lookup"><span data-stu-id="cf48d-152">If you must extend the configuration to meet specific requirements, see [How to build extension in tax service](https://go.microsoft.com/fwlink/?linkid=2138483) for information about how to generate and select your own tax configuration.</span></span>

    <span data-ttu-id="cf48d-153">在选择 **配置版本** 后，将显示其他几个选项卡：</span><span class="sxs-lookup"><span data-stu-id="cf48d-153">After you select **Configuration version**, several additional tabs appear:</span></span>

    - <span data-ttu-id="cf48d-154">**税码** – 此选项卡对于税务计算服务是必填的。</span><span class="sxs-lookup"><span data-stu-id="cf48d-154">**Tax codes** – This tab is mandatory for the tax calculation service.</span></span> <span data-ttu-id="cf48d-155">它用于维护税码的主数据。</span><span class="sxs-lookup"><span data-stu-id="cf48d-155">It's used to maintain master data for tax codes.</span></span> <span data-ttu-id="cf48d-156">当您在法人中启用税务功能设置的当前版本时，在此选项卡上创建的所有税码会自动同步到 Finance。</span><span class="sxs-lookup"><span data-stu-id="cf48d-156">All tax codes that are created on this tab are automatically synced to Finance when you enable the current version of the tax feature setup in the legal entity.</span></span>
    - <span data-ttu-id="cf48d-157">**税码适用性** – 此选项卡对于税务计算加载项是必填的。</span><span class="sxs-lookup"><span data-stu-id="cf48d-157">**Tax codes applicability** – This tab is mandatory for the tax calculation add-in.</span></span> <span data-ttu-id="cf48d-158">它用于定义确定税码、税组和物料税组的矩阵。</span><span class="sxs-lookup"><span data-stu-id="cf48d-158">It's used to define a matrix that determines the tax code, tax group, and item tax group.</span></span> <span data-ttu-id="cf48d-159">确定的税码用于计算税额。</span><span class="sxs-lookup"><span data-stu-id="cf48d-159">The tax code that is determined is used to calculate the tax amount.</span></span> <span data-ttu-id="cf48d-160">**税码**、**税组** 和 **物料税组** 字段的值将返回到 Finance。</span><span class="sxs-lookup"><span data-stu-id="cf48d-160">The values of the **Tax code**, **Tax group**, and **Item tax group** fields are returned to Finance.</span></span>
    - <span data-ttu-id="cf48d-161">**客户税务登记编号适用性** – 此选项卡对于税务计算加载项是可选的。</span><span class="sxs-lookup"><span data-stu-id="cf48d-161">**Customer tax registration number applicability** – This tab is optional for the tax calculation add-in.</span></span> <span data-ttu-id="cf48d-162">如果针对一位客户有多个税务登记编号，税务计算加载项可以自动确定正确的税务登记编号。</span><span class="sxs-lookup"><span data-stu-id="cf48d-162">If you have multiple tax registration numbers for one customer, the tax calculation add-in can automatically determine the correct tax registration number.</span></span> <span data-ttu-id="cf48d-163">在此选项卡上的矩阵中，定义加载项用于进行确定的规则。</span><span class="sxs-lookup"><span data-stu-id="cf48d-163">In the matrix on this tab, you define the rules that the add-in uses to make the determination.</span></span> <span data-ttu-id="cf48d-164">否则，Finance 和 Supply Chain Management 将继续在销售交易的应纳税单据上使用默认的税务登记编号。</span><span class="sxs-lookup"><span data-stu-id="cf48d-164">Otherwise, Finance and Supply Chain Management will continue to use the default tax registration number on taxable documents for sales transactions.</span></span>
    - <span data-ttu-id="cf48d-165">**供应商税务登记编号适用性** – 此选项卡对于税务计算加载项是可选的。</span><span class="sxs-lookup"><span data-stu-id="cf48d-165">**Vendor tax registration number applicability** – This tab is optional for the tax calculation add-in.</span></span> <span data-ttu-id="cf48d-166">如果针对一位供应商有多个税务登记编号，税务计算加载项可以自动确定正确的税务登记编号。</span><span class="sxs-lookup"><span data-stu-id="cf48d-166">If you have multiple tax registration numbers for one vendor, the tax calculation add-in can automatically determine the correct tax registration number.</span></span> <span data-ttu-id="cf48d-167">在此选项卡上的矩阵中，定义加载项用于进行确定的规则。</span><span class="sxs-lookup"><span data-stu-id="cf48d-167">In the matrix on this tab, you define the rules that the add-in uses to make the determination.</span></span> <span data-ttu-id="cf48d-168">否则，Finance 和 Supply Chain Management 将继续在采购交易的应纳税单据上使用默认的税务登记编号。</span><span class="sxs-lookup"><span data-stu-id="cf48d-168">Otherwise, Finance and Supply Chain Management will continue to use the default tax registration number on taxable documents for purchase transactions.</span></span>
    - <span data-ttu-id="cf48d-169">**清单代码适用性** – 此选项卡对于税务计算加载项是可选的。</span><span class="sxs-lookup"><span data-stu-id="cf48d-169">**List code applicability** – This tab is optional for the tax calculation add-in.</span></span> <span data-ttu-id="cf48d-170">它可以通过更灵活、可配置的规则帮助自动确定 **清单代码** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="cf48d-170">It can help automatically determine the value of the **List code** field through more flexible and configurable rules.</span></span> <span data-ttu-id="cf48d-171">在此选项卡上的矩阵中，您可以定义加载项用于进行确定的规则。</span><span class="sxs-lookup"><span data-stu-id="cf48d-171">In the matrix on this tab, you can define the rules that the add-in uses to make the determination.</span></span> <span data-ttu-id="cf48d-172">否则，Finance 和 Supply Chain Management 将继续在应纳税单据上使用默认代码。</span><span class="sxs-lookup"><span data-stu-id="cf48d-172">Otherwise, Finance and Supply Chain Management will continue to use the default code on taxable documents.</span></span>

14. <span data-ttu-id="cf48d-173">在 **税码** 选项卡上，选择 **添加**，然后输入税码和描述。</span><span class="sxs-lookup"><span data-stu-id="cf48d-173">On the **Tax codes** tab, select **Add**, and enter the tax code and a description.</span></span>
15. <span data-ttu-id="cf48d-174">选择 **税种组分**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-174">Select **Tax component**.</span></span> <span data-ttu-id="cf48d-175">税种组分是在所选税务配置的以前版本中定义的一组税务计算方法。</span><span class="sxs-lookup"><span data-stu-id="cf48d-175">The tax component is a group of tax calculation methods that was defined in the previous version of the selected tax configuration.</span></span> <span data-ttu-id="cf48d-176">以下税种组分可用：</span><span class="sxs-lookup"><span data-stu-id="cf48d-176">The following tax components are available:</span></span>

    - <span data-ttu-id="cf48d-177">按净额</span><span class="sxs-lookup"><span data-stu-id="cf48d-177">By net amount</span></span>
    - <span data-ttu-id="cf48d-178">按总额</span><span class="sxs-lookup"><span data-stu-id="cf48d-178">By gross amount</span></span>
    - <span data-ttu-id="cf48d-179">按数量</span><span class="sxs-lookup"><span data-stu-id="cf48d-179">By quantity</span></span>
    - <span data-ttu-id="cf48d-180">按利润</span><span class="sxs-lookup"><span data-stu-id="cf48d-180">By margin</span></span>
    - <span data-ttu-id="cf48d-181">税上税</span><span class="sxs-lookup"><span data-stu-id="cf48d-181">Tax on tax</span></span>

16. <span data-ttu-id="cf48d-182">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-182">Select **Save**.</span></span> <span data-ttu-id="cf48d-183">根据您选择的税种组分，更多字段变为可用。</span><span class="sxs-lookup"><span data-stu-id="cf48d-183">More fields become available, based on the tax component that you selected.</span></span>
17. <span data-ttu-id="cf48d-184">使用以下选项以标识税码的性质：</span><span class="sxs-lookup"><span data-stu-id="cf48d-184">Use the following options to identify the nature of the tax code:</span></span>

    - <span data-ttu-id="cf48d-185">是免税</span><span class="sxs-lookup"><span data-stu-id="cf48d-185">Is Exempt</span></span>
    - <span data-ttu-id="cf48d-186">是销项税</span><span class="sxs-lookup"><span data-stu-id="cf48d-186">Is Use tax</span></span>
    - <span data-ttu-id="cf48d-187">是冲销费用</span><span class="sxs-lookup"><span data-stu-id="cf48d-187">Is Reverse Charge</span></span>
    - <span data-ttu-id="cf48d-188">不包括在基数金额计算中</span><span class="sxs-lookup"><span data-stu-id="cf48d-188">Exclude in Base Amount Calculation</span></span>

    <span data-ttu-id="cf48d-189">对于销项税方案，设置一个具有正税率的税码，然后将其标记为 **是销项税**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-189">For a use tax scenario, set up a single tax code that has a positive tax rate, and mark it as **Is Use tax**.</span></span>

    <span data-ttu-id="cf48d-190">对于冲销费用方案，设置两个税码，一个具有正税率，另一个具有负税率，但税率值相同。</span><span class="sxs-lookup"><span data-stu-id="cf48d-190">For a reverse charge scenario, set up two tax codes, one of which has a positive tax rate, and the other of which has a negative tax rate but the same rate value.</span></span> <span data-ttu-id="cf48d-191">将负税码标记为 **是冲销费用**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-191">Mark the negative tax code as **Is reverse charge**.</span></span> <span data-ttu-id="cf48d-192">有关 Finance 中冲销费用解决方案的详细信息，请参阅[增值税/GST 方案的冲销费用机制](emea-reverse-charge.md)。</span><span class="sxs-lookup"><span data-stu-id="cf48d-192">For more information about the reverse charge solution in Finance, see [Reverse charge mechanism for VAT/GST scheme](emea-reverse-charge.md).</span></span>
    
    <span data-ttu-id="cf48d-193">对于不应包括在价内交易的税务基数金额计算中的某些税务类型（例如某些国家/地区中的关税），请选中 **不包括在基数金额计算中** 复选框。</span><span class="sxs-lookup"><span data-stu-id="cf48d-193">For some tax types which should be excluded in the tax base amount calculation for price inclusive transactions, like custom duty in some countries, select the **Exclude in Base Amount Calculation** check box.</span></span>

    <span data-ttu-id="cf48d-194">保持此税码的税率和税额限制。</span><span class="sxs-lookup"><span data-stu-id="cf48d-194">Maintain tax rates and the tax amount limits for this tax code.</span></span>

18. <span data-ttu-id="cf48d-195">重复步骤 14 到步骤 17，以添加所需的所有其他税码。</span><span class="sxs-lookup"><span data-stu-id="cf48d-195">Repeat steps 14 through 17 to add all other tax codes that are required.</span></span>
19. <span data-ttu-id="cf48d-196">在 **税码适用性** 选项卡上，选择确定正确税码所需的列，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-196">On the **Tax codes applicability** tab, select the columns that are required to determine the correct tax code, and then select **Add**.</span></span>
20. <span data-ttu-id="cf48d-197">输入或选择每列的值。</span><span class="sxs-lookup"><span data-stu-id="cf48d-197">Enter or select values for each column.</span></span> <span data-ttu-id="cf48d-198">**税码**、**税组** 和 **物料税组** 字段将是此矩阵的输出。</span><span class="sxs-lookup"><span data-stu-id="cf48d-198">The **Tax code**, **Tax group**, and **Item tax group** fields will be the output of this matrix.</span></span>
21. <span data-ttu-id="cf48d-199">重复步骤 19 到步骤 20，以设置客户税务登记编号、供应商税务登记编号和清单代码的适用性。</span><span class="sxs-lookup"><span data-stu-id="cf48d-199">Repeat steps 19 through 20 to set up the applicability of customer tax registration numbers, vendor tax registration numbers, and list codes.</span></span>
22. <span data-ttu-id="cf48d-200">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="cf48d-200">Select **Save**, and then close the page.</span></span>
23. <span data-ttu-id="cf48d-201">选择 **更改状态** \> **完成**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-201">Select **Change status** \> **Complete**.</span></span> <span data-ttu-id="cf48d-202">在状态更改为 **完成** 后，无法再编辑该版本。</span><span class="sxs-lookup"><span data-stu-id="cf48d-202">After the status is changed to **Complete**, the version can no longer be edited.</span></span>
24. <span data-ttu-id="cf48d-203">选择 **更改状态** \> **发布**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-203">Select **Change status** \> **Publish**.</span></span> <span data-ttu-id="cf48d-204">此版本的税务功能设置将推送到全局存储库，并将对 Finance 中的每个法人可见。</span><span class="sxs-lookup"><span data-stu-id="cf48d-204">This version of the tax feature setup will be pushed to the global repository and will be visible to each legal entity in Finance.</span></span>

## <a name="dynamics-365-setup"></a><span data-ttu-id="cf48d-205">Dynamics 365 设置</span><span class="sxs-lookup"><span data-stu-id="cf48d-205">Dynamics 365 setup</span></span>

<span data-ttu-id="cf48d-206">如上一部分所述，在 RCS 中完成设置后，您将具有税务功能的已发布版本。</span><span class="sxs-lookup"><span data-stu-id="cf48d-206">After you complete the setup in RCS, as described in the previous section, you will have a published version of the tax feature.</span></span> <span data-ttu-id="cf48d-207">请按照以下步骤在 Finance 中设置税务计算加载项。</span><span class="sxs-lookup"><span data-stu-id="cf48d-207">Follow these steps to set up the tax calculation add-in in Finance.</span></span>

<span data-ttu-id="cf48d-208">本部分中的设置由法人完成。</span><span class="sxs-lookup"><span data-stu-id="cf48d-208">The setup in this section is done by legal entity.</span></span> <span data-ttu-id="cf48d-209">您必须为要在 Finance 中启用税务计算加载项的每个法人配置它。</span><span class="sxs-lookup"><span data-stu-id="cf48d-209">You must configure it for each legal entity that you want to enable the tax calculation add-in for in Finance.</span></span>

1. <span data-ttu-id="cf48d-210">在 Finance 中，转到 **税务** \> **设置** \> **税务配置** \> **税务计算加载项设置(预览)**。</span><span class="sxs-lookup"><span data-stu-id="cf48d-210">In Finance, go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax calcluation add-in setup (Preview)**.</span></span>
2. <span data-ttu-id="cf48d-211">在 **常规** 选项卡上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="cf48d-211">On the **General** tab, set the following fields:</span></span>

    - <span data-ttu-id="cf48d-212">**启用税务计算加载项** – 选中此复选框以为法人启用税务计算加载项。</span><span class="sxs-lookup"><span data-stu-id="cf48d-212">**Enable tax calculation add-in** – Select this check box to enable the tax calculation add-in for the legal entity.</span></span> <span data-ttu-id="cf48d-213">如果未为当前法人启用税务计算加载项，法人将继续使用现有税务引擎来确定和计算税务。</span><span class="sxs-lookup"><span data-stu-id="cf48d-213">If the tax calculation add-in isn't enabled for the current legal entity, the legal entity will continue to use the existing tax engine to determine and calculate tax.</span></span>
    - <span data-ttu-id="cf48d-214">**功能设置** – 选择法人的已发布税务功能设置和版本。</span><span class="sxs-lookup"><span data-stu-id="cf48d-214">**Feature setup** – Select a published tax feature setup and version for the legal entity.</span></span> <span data-ttu-id="cf48d-215">有关如何设置和完成已发布税务功能的详细信息，请参阅本主题的上一部分。</span><span class="sxs-lookup"><span data-stu-id="cf48d-215">For more information about how to set up and complete a published tax feature, see the previous section of this topic.</span></span>
    - <span data-ttu-id="cf48d-216">**业务流程** – 选择要为税务计算加载项启用的业务流程。</span><span class="sxs-lookup"><span data-stu-id="cf48d-216">**Business Process** – Select the business processes to enable for the tax calculation add-in.</span></span>
    - <span data-ttu-id="cf48d-217">**启用税码调整** – 将此选项设置为 **是** 以在销售税页面上启用税码调整。</span><span class="sxs-lookup"><span data-stu-id="cf48d-217">**Enable tax code adjustment** – Set this option to **Yes** to enable tax code adjustments on the sales tax page.</span></span>

3. <span data-ttu-id="cf48d-218">在 **计算** 选项卡上，定义法人的预期舍入规则。</span><span class="sxs-lookup"><span data-stu-id="cf48d-218">On the **Calculation** tab, define the expected rounding rule for the legal entity.</span></span>
4. <span data-ttu-id="cf48d-219">在 **错误处理** 选项卡上，为法人定义预期的错误处理方法。</span><span class="sxs-lookup"><span data-stu-id="cf48d-219">On the **Error handling** tab, define the expected error handling method for the legal entity.</span></span> <span data-ttu-id="cf48d-220">在税务计算加载项中，每个结果代码有三个可用的选项：</span><span class="sxs-lookup"><span data-stu-id="cf48d-220">Three options are available for each result code from the tax calculation add-in:</span></span>

    - <span data-ttu-id="cf48d-221">无</span><span class="sxs-lookup"><span data-stu-id="cf48d-221">No</span></span>
    - <span data-ttu-id="cf48d-222">警告</span><span class="sxs-lookup"><span data-stu-id="cf48d-222">Warning</span></span>
    - <span data-ttu-id="cf48d-223">错误​</span><span class="sxs-lookup"><span data-stu-id="cf48d-223">Error</span></span>

5. <span data-ttu-id="cf48d-224">保存税务计算加载项设置。</span><span class="sxs-lookup"><span data-stu-id="cf48d-224">Save the tax calculation add-in setup.</span></span>
6. <span data-ttu-id="cf48d-225">针对每个其他法人，重复步骤 1 到步骤 5。</span><span class="sxs-lookup"><span data-stu-id="cf48d-225">Repeat steps 1 through 5 for each additional legal entity.</span></span>

## <a name="transaction-processing"></a><span data-ttu-id="cf48d-226">交易处理</span><span class="sxs-lookup"><span data-stu-id="cf48d-226">Transaction processing</span></span>

<span data-ttu-id="cf48d-227">完成所有设置过程后，您可以使用税务计算加载项在 Finance 中确定和计算税务。</span><span class="sxs-lookup"><span data-stu-id="cf48d-227">After you've completed all the setup procedures, you can use the tax calculation add-in to determine and calculate tax in Finance.</span></span> <span data-ttu-id="cf48d-228">处理交易的步骤保持不变。</span><span class="sxs-lookup"><span data-stu-id="cf48d-228">The steps to process transactions remain the same.</span></span> <span data-ttu-id="cf48d-229">以下交易在 Finance 版本 10.0.18 中受支持：</span><span class="sxs-lookup"><span data-stu-id="cf48d-229">The following transactions are supported in Finance version 10.0.18:</span></span>

- <span data-ttu-id="cf48d-230">销售流程</span><span class="sxs-lookup"><span data-stu-id="cf48d-230">Sales process</span></span>

    - <span data-ttu-id="cf48d-231">销售报价</span><span class="sxs-lookup"><span data-stu-id="cf48d-231">Sales quotation</span></span>
    - <span data-ttu-id="cf48d-232">销售订单</span><span class="sxs-lookup"><span data-stu-id="cf48d-232">Sales order</span></span>
    - <span data-ttu-id="cf48d-233">确认单</span><span class="sxs-lookup"><span data-stu-id="cf48d-233">Confirmation</span></span>
    - <span data-ttu-id="cf48d-234">领料单</span><span class="sxs-lookup"><span data-stu-id="cf48d-234">Picking list</span></span>
    - <span data-ttu-id="cf48d-235">装箱单</span><span class="sxs-lookup"><span data-stu-id="cf48d-235">Packing slip</span></span>
    - <span data-ttu-id="cf48d-236">销售账单</span><span class="sxs-lookup"><span data-stu-id="cf48d-236">Sales invoice</span></span>
    - <span data-ttu-id="cf48d-237">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="cf48d-237">Credit note</span></span>
    - <span data-ttu-id="cf48d-238">退货单</span><span class="sxs-lookup"><span data-stu-id="cf48d-238">Return order</span></span>
    - <span data-ttu-id="cf48d-239">标题费用</span><span class="sxs-lookup"><span data-stu-id="cf48d-239">Header charge</span></span>
    - <span data-ttu-id="cf48d-240">行费用</span><span class="sxs-lookup"><span data-stu-id="cf48d-240">Line charge</span></span>

- <span data-ttu-id="cf48d-241">采购流程</span><span class="sxs-lookup"><span data-stu-id="cf48d-241">Purchase process</span></span>

    - <span data-ttu-id="cf48d-242">采购订单</span><span class="sxs-lookup"><span data-stu-id="cf48d-242">Purchase order</span></span>
    - <span data-ttu-id="cf48d-243">确认单</span><span class="sxs-lookup"><span data-stu-id="cf48d-243">Confirmation</span></span>
    - <span data-ttu-id="cf48d-244">收货清单</span><span class="sxs-lookup"><span data-stu-id="cf48d-244">Receipts list</span></span>
    - <span data-ttu-id="cf48d-245">产品收据</span><span class="sxs-lookup"><span data-stu-id="cf48d-245">Product receipt</span></span>
    - <span data-ttu-id="cf48d-246">采购账单</span><span class="sxs-lookup"><span data-stu-id="cf48d-246">Purchase invoice</span></span>
    - <span data-ttu-id="cf48d-247">标题费用</span><span class="sxs-lookup"><span data-stu-id="cf48d-247">Header charge</span></span>
    - <span data-ttu-id="cf48d-248">行费用</span><span class="sxs-lookup"><span data-stu-id="cf48d-248">Line charge</span></span>
    - <span data-ttu-id="cf48d-249">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="cf48d-249">Credit note</span></span>
    - <span data-ttu-id="cf48d-250">退货单</span><span class="sxs-lookup"><span data-stu-id="cf48d-250">Return order</span></span>
    - <span data-ttu-id="cf48d-251">采购申请</span><span class="sxs-lookup"><span data-stu-id="cf48d-251">Purchase requisition</span></span>
    - <span data-ttu-id="cf48d-252">采购申请行费用</span><span class="sxs-lookup"><span data-stu-id="cf48d-252">Purchase requisition line charge</span></span>
    - <span data-ttu-id="cf48d-253">询价</span><span class="sxs-lookup"><span data-stu-id="cf48d-253">Request for quotation</span></span>
    - <span data-ttu-id="cf48d-254">询价标题费用</span><span class="sxs-lookup"><span data-stu-id="cf48d-254">Request for quotation header charge</span></span>
    - <span data-ttu-id="cf48d-255">询价行费用</span><span class="sxs-lookup"><span data-stu-id="cf48d-255">Request for quotation line charge</span></span>

- <span data-ttu-id="cf48d-256">库存流程</span><span class="sxs-lookup"><span data-stu-id="cf48d-256">Inventory process</span></span>

    - <span data-ttu-id="cf48d-257">转移单 – 装运</span><span class="sxs-lookup"><span data-stu-id="cf48d-257">Transfer order – ship</span></span>
    - <span data-ttu-id="cf48d-258">转移单 - 接收</span><span class="sxs-lookup"><span data-stu-id="cf48d-258">Transfer order - receive</span></span>
