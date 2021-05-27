---
title: 转移单的税务功能支持
description: 本主题说明使用税务计算服务提供转移单的新税务功能支持。
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3a5c2b6fb48d98ba045c77ed034d976f7d89af98
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021361"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="67929-103">转移单的税务功能支持</span><span class="sxs-lookup"><span data-stu-id="67929-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67929-104">本主题提供有关转移单中税务计算和过帐集成的信息。</span><span class="sxs-lookup"><span data-stu-id="67929-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="67929-105">此功能使您可以针对库存转移在转移单中设置税务计算和过帐。</span><span class="sxs-lookup"><span data-stu-id="67929-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="67929-106">根据欧盟 (EU) 增值税 (VAT) 法规，库存转移将考虑集团内部供应和集团内部购置。</span><span class="sxs-lookup"><span data-stu-id="67929-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="67929-107">若要配置和使用此功能，您必须完成三个主要步骤：</span><span class="sxs-lookup"><span data-stu-id="67929-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="67929-108">**RCS 设置：** 在 Regulatory Configuration Service 中，在转移单中为税码确定设置税务功能、税码和税码适用性。</span><span class="sxs-lookup"><span data-stu-id="67929-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="67929-109">**Finance 设置：** 在 Microsoft Dynamics 365 Finance 中，打开 **转移单中的税务** 功能，设置库存的税务服务参数，并设置核心税务参数。</span><span class="sxs-lookup"><span data-stu-id="67929-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="67929-110">**库存设置：** 设置转移单事务的库存配置。</span><span class="sxs-lookup"><span data-stu-id="67929-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="67929-111">为税务和转移单事务设置 RCS</span><span class="sxs-lookup"><span data-stu-id="67929-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="67929-112">请按照以下步骤设置转移单中涉及的税务。</span><span class="sxs-lookup"><span data-stu-id="67929-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="67929-113">在此处显示的示例中，转移单从荷兰转到比利时。</span><span class="sxs-lookup"><span data-stu-id="67929-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="67929-114">在 **税务功能** 页面上的 **版本** 选项卡上，选择草稿功能版本，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="67929-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![选择编辑](../media/tax-feature-support-01.png)

2. <span data-ttu-id="67929-116">在 **税务功能设置** 页面上的 **税码** 选项卡上，选择 **添加** 以创建新税码。</span><span class="sxs-lookup"><span data-stu-id="67929-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="67929-117">对于此示例，创建了三个税码：**NL-Exempt**、**BE-RC-21** 和 **BE-RC+21**。</span><span class="sxs-lookup"><span data-stu-id="67929-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="67929-118">当从荷兰仓库中装运转移单时，将应用荷兰增值税免税代码 (**NL-Exempt**)。</span><span class="sxs-lookup"><span data-stu-id="67929-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="67929-119">创建税码 **NL-Exempt**。</span><span class="sxs-lookup"><span data-stu-id="67929-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="67929-120">选择 **添加**，在 **税码** 字段中输入 **NL-Exempt**。</span><span class="sxs-lookup"><span data-stu-id="67929-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="67929-121">在 **税种组分** 字段中选择 **按净额**。</span><span class="sxs-lookup"><span data-stu-id="67929-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="67929-122">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="67929-122">Select **Save**.</span></span>
        4. <span data-ttu-id="67929-123">在 **比率** 表中选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="67929-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="67929-124">在 **常规** 部分中，将 **是免税** 切换到 **是**。</span><span class="sxs-lookup"><span data-stu-id="67929-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![NL-Exempt 税码](../media/tax-feature-support-02.png)

    - <span data-ttu-id="67929-126">当在比利时仓库收到转移单时，通过使用 **BE-RC-21** 和 **BE-RC+21** 税码应用冲销费用机制。</span><span class="sxs-lookup"><span data-stu-id="67929-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="67929-127">创建税码 **BE-RC-21**。</span><span class="sxs-lookup"><span data-stu-id="67929-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="67929-128">选择 **添加**，在 **税码** 字段中输入 **BE-RC-21**。</span><span class="sxs-lookup"><span data-stu-id="67929-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="67929-129">在 **税种组分** 字段中选择 **按净额**。</span><span class="sxs-lookup"><span data-stu-id="67929-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="67929-130">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="67929-130">Select **Save**.</span></span>
        4. <span data-ttu-id="67929-131">在 **比率** 表中选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="67929-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="67929-132">在 **税率** 字段中输入 **-21**。</span><span class="sxs-lookup"><span data-stu-id="67929-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="67929-133">在 **常规** 部分中，将 **是冲销费用** 切换到 **是**。</span><span class="sxs-lookup"><span data-stu-id="67929-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="67929-134">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="67929-134">Select **Save**.</span></span>

        ![冲销费用的 BE-RC-21 税码](../media/tax-feature-support-03.png)
        
        <span data-ttu-id="67929-136">创建税码 **BE-RC+21**。</span><span class="sxs-lookup"><span data-stu-id="67929-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="67929-137">选择 **添加**，在 **税码** 字段中输入 **BE-RC-21**。</span><span class="sxs-lookup"><span data-stu-id="67929-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="67929-138">在 **税种组分** 字段中选择 **按净额**。</span><span class="sxs-lookup"><span data-stu-id="67929-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="67929-139">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="67929-139">Select **Save**.</span></span>
        4. <span data-ttu-id="67929-140">在 **比率** 表中选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="67929-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="67929-141">在 **税率** 字段中输入 **21**。</span><span class="sxs-lookup"><span data-stu-id="67929-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="67929-142">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="67929-142">Select **Save**.</span></span>

        ![冲销费用的 BE-RC+21 税码](../media/tax-feature-support-04.png)

3. <span data-ttu-id="67929-144">定义税码的适用性。</span><span class="sxs-lookup"><span data-stu-id="67929-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="67929-145">选择 **管理列**，然后选择应该用于生成适用性表的列。</span><span class="sxs-lookup"><span data-stu-id="67929-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="67929-146">请务必将 **业务流程** 和 **税务方向** 列添加到表。</span><span class="sxs-lookup"><span data-stu-id="67929-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="67929-147">这两个列对于转移单中的税务功能至关重要。</span><span class="sxs-lookup"><span data-stu-id="67929-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="67929-148">添加适用性规则。</span><span class="sxs-lookup"><span data-stu-id="67929-148">Add applicability rules.</span></span> <span data-ttu-id="67929-149">不要将 **税码**、**税组** 和 **物料税组** 留空。</span><span class="sxs-lookup"><span data-stu-id="67929-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="67929-150">为转移单装运添加新规则。</span><span class="sxs-lookup"><span data-stu-id="67929-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="67929-151">在 **适用性规则** 表中选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="67929-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="67929-152">在 **业务流程** 字段中，选择 **库存** 以使该规则适用于转移单。</span><span class="sxs-lookup"><span data-stu-id="67929-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="67929-153">在 **从国家/地区装运** 字段中，输入 **NLD**。</span><span class="sxs-lookup"><span data-stu-id="67929-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="67929-154">在 **运达国家/地区** 字段中，输入 **BEL**。</span><span class="sxs-lookup"><span data-stu-id="67929-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="67929-155">在 **税务方向** 字段中，选择 **输出** 以使该规则适用于转移单装运。</span><span class="sxs-lookup"><span data-stu-id="67929-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="67929-156">在 **税码** 字段中，选择 **NL-Exempt**。</span><span class="sxs-lookup"><span data-stu-id="67929-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="67929-157">在 **税组** 字段和 **物料税组** 中，输入在 Finance 系统中定义的相关销售税组和物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="67929-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="67929-158">为转移单收货添加另一个规则。</span><span class="sxs-lookup"><span data-stu-id="67929-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="67929-159">在 **适用性规则** 表中选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="67929-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="67929-160">在 **业务流程** 字段中，选择 **库存** 以使该规则适用于转移单。</span><span class="sxs-lookup"><span data-stu-id="67929-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="67929-161">在 **从国家/地区装运** 字段中，输入 **NLD**。</span><span class="sxs-lookup"><span data-stu-id="67929-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="67929-162">在 **运达国家/地区** 字段中，输入 **BEL**。</span><span class="sxs-lookup"><span data-stu-id="67929-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="67929-163">在 **税务方向** 字段中，选择 **输入** 以使该规则适用于转移单收货。</span><span class="sxs-lookup"><span data-stu-id="67929-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="67929-164">在 **税码** 字段中，选择 **BE-RC+21** 和 **BE-RC-21**。</span><span class="sxs-lookup"><span data-stu-id="67929-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="67929-165">在 **税组** 字段和 **物料税组** 中，输入在 Finance 系统中定义的相关销售税组和物料销售税组。</span><span class="sxs-lookup"><span data-stu-id="67929-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![适用性规则](../media/image5.png)

4. <span data-ttu-id="67929-167">完成并发布新的税务功能版本。</span><span class="sxs-lookup"><span data-stu-id="67929-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="67929-168">[![更改新版本的状态](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="67929-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="67929-169">为转移单事务设置 Finance</span><span class="sxs-lookup"><span data-stu-id="67929-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="67929-170">请执行以下步骤以启用和设置转移单的税务。</span><span class="sxs-lookup"><span data-stu-id="67929-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="67929-171">在 Finance 中，转到 **工作区** \> **功能管理**。</span><span class="sxs-lookup"><span data-stu-id="67929-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="67929-172">在列表中，找到并选择 **转移单中的税务** 功能，然后选择 **立即启用** 以打开它。</span><span class="sxs-lookup"><span data-stu-id="67929-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="67929-173">**转移单中的税务** 功能完全依赖于税务服务。</span><span class="sxs-lookup"><span data-stu-id="67929-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="67929-174">因此，仅在安装税务服务后才能打开它。</span><span class="sxs-lookup"><span data-stu-id="67929-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![转移单中的税务功能](../media/image7.png)

3. <span data-ttu-id="67929-176">启用税务服务，然后选择 **库存** 业务流程。</span><span class="sxs-lookup"><span data-stu-id="67929-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="67929-177">您必须在希望提供税务服务和转移单中的税务的功能的 Finance 中为每个法人完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="67929-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="67929-178">转到 **税务** \> **设置** \> **税务配置** \> **税务服务设置**。</span><span class="sxs-lookup"><span data-stu-id="67929-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="67929-179">在 **业务流程** 字段中，选择 **库存**。</span><span class="sxs-lookup"><span data-stu-id="67929-179">In the **Business process** field, select **Inventory**.</span></span>

    ![设置“业务流程”字段](../media/image8.png)

4. <span data-ttu-id="67929-181">验证已设置冲销费用机制。</span><span class="sxs-lookup"><span data-stu-id="67929-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="67929-182">转到 **总帐** \> **设置** \> **参数**，然后在 **冲销费用** 选项卡上，验证 **启用冲销费用** 选项已设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="67929-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![启用冲销费用选项](../media/image9.png)

5. <span data-ttu-id="67929-184">验证已根据税务服务指南在 Finance 中设置了相关的税码、税组、物料税组和增值税登记编号。</span><span class="sxs-lookup"><span data-stu-id="67929-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="67929-185">设置一个临时中转科目。</span><span class="sxs-lookup"><span data-stu-id="67929-185">Set up an interim transit account.</span></span> <span data-ttu-id="67929-186">仅在应用到转移单的税务不适用于免税或冲销费用机制时，才需要此步骤。</span><span class="sxs-lookup"><span data-stu-id="67929-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="67929-187">转到 **税务** \> **设置** \> **销售税** \> **分类帐过帐组**。</span><span class="sxs-lookup"><span data-stu-id="67929-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="67929-188">在 **临时中转** 字段中，选择分类帐科目。</span><span class="sxs-lookup"><span data-stu-id="67929-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![选择临时中转科目](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="67929-190">为转移单事务设置基本库存</span><span class="sxs-lookup"><span data-stu-id="67929-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="67929-191">请按照以下步骤设置基本库存以启用转移单事务。</span><span class="sxs-lookup"><span data-stu-id="67929-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="67929-192">为不同国家或地区的仓库创建发货和运达站点，并为每个站点添加主要地址。</span><span class="sxs-lookup"><span data-stu-id="67929-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="67929-193">转到 **仓库管理** \> **设置** \> **仓库** \> **站点**。</span><span class="sxs-lookup"><span data-stu-id="67929-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="67929-194">选择 **新建** 以创建您稍后将分配给仓库的站点。</span><span class="sxs-lookup"><span data-stu-id="67929-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="67929-195">针对必须创建的所有其他站点重复步骤 2。</span><span class="sxs-lookup"><span data-stu-id="67929-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="67929-196">您创建的站点之一应命名为 **中转**。</span><span class="sxs-lookup"><span data-stu-id="67929-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="67929-197">在此过程的后续步骤中，您将此站点分配给中转仓库，以便可以在转移单的“装运”和“收货”事务中过帐与税务相关的库存凭证。</span><span class="sxs-lookup"><span data-stu-id="67929-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="67929-198">中转站点的地址与税务计算无关。</span><span class="sxs-lookup"><span data-stu-id="67929-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="67929-199">因此，您可以将其留为空白。</span><span class="sxs-lookup"><span data-stu-id="67929-199">Therefore, you can leave it blank.</span></span>

    ![设置站点](../media/image11.png)

2. <span data-ttu-id="67929-201">创建发货、中转和运达仓库。</span><span class="sxs-lookup"><span data-stu-id="67929-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="67929-202">在仓库中维护的任何地址信息将在税务计算过程中覆盖站点地址。</span><span class="sxs-lookup"><span data-stu-id="67929-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="67929-203">转到 **仓库管理** \> **设置** \> **仓库** \> **仓库**。</span><span class="sxs-lookup"><span data-stu-id="67929-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="67929-204">选择 **新建** 以创建仓库，并将其分配给相应的站点。</span><span class="sxs-lookup"><span data-stu-id="67929-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="67929-205">重复步骤 2，以根据需要为每个站点创建仓库。</span><span class="sxs-lookup"><span data-stu-id="67929-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![设置仓库](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="67929-207">对于发货仓库，必须在转移单事务的 **中转仓库** 字段中选择中转仓库。</span><span class="sxs-lookup"><span data-stu-id="67929-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![选择中转仓库](../media/image13.png)

3. <span data-ttu-id="67929-209">验证为转移单事务设置了库存过帐配置。</span><span class="sxs-lookup"><span data-stu-id="67929-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="67929-210">转到 **库存管理** \> **设置** \> **过帐** \> **过帐**。</span><span class="sxs-lookup"><span data-stu-id="67929-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="67929-211">在 **库存** 选项卡上，验证为 **库存发货** 和 **库存收货** 过帐设置了分类帐科目。</span><span class="sxs-lookup"><span data-stu-id="67929-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![设置库存发货和库存收货过帐](../media/image14.png)

    3. <span data-ttu-id="67929-213">验证为 **内部单位应付帐款** 过帐设置了分类帐科目。</span><span class="sxs-lookup"><span data-stu-id="67929-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![设置内部单位应付帐款过帐](../media/image15.png)

    4. <span data-ttu-id="67929-215">验证为 **内部单位应收帐款** 过帐设置了分类帐科目。</span><span class="sxs-lookup"><span data-stu-id="67929-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![设置内部单位应收帐款过帐](../media/image16.png)
