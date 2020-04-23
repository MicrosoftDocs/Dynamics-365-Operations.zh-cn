---
title: 转包
description: 此主题帮助您在 Dynamics 365 Supply Chain Management 中的制造内构建转包演练。
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1cc1040393d843f39ca8c741a7c51435c7169c00
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211046"
---
# <a name="subcontracting"></a><span data-ttu-id="7973f-103">转包</span><span class="sxs-lookup"><span data-stu-id="7973f-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7973f-104">此主题帮助您在 Microsoft Dynamics 365 Supply Chain Management 中的制造内构建转包演练。</span><span class="sxs-lookup"><span data-stu-id="7973f-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="7973f-105">本主题的第一部分介绍如何设置数据。</span><span class="sxs-lookup"><span data-stu-id="7973f-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="7973f-106">第二部分引导您完成演练中的步骤。</span><span class="sxs-lookup"><span data-stu-id="7973f-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="7973f-107">目标对象</span><span class="sxs-lookup"><span data-stu-id="7973f-107">Target audience</span></span>

<span data-ttu-id="7973f-108">在本主题中，将学习如何在制造中设置转包。</span><span class="sxs-lookup"><span data-stu-id="7973f-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="7973f-109">将使用 HQUS 法人中的现有数据对转包活动流进行基本设置。</span><span class="sxs-lookup"><span data-stu-id="7973f-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="7973f-110">HQUS 法人中的演示数据包括预设的设置参数，用于为演练中的步骤提供支持。</span><span class="sxs-lookup"><span data-stu-id="7973f-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="7973f-111">接管演练针对各种角色面临的关键痛点和挑战，仍然可以由系统管理员完成。</span><span class="sxs-lookup"><span data-stu-id="7973f-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="7973f-112">演示方案</span><span class="sxs-lookup"><span data-stu-id="7973f-112">Demo scenario</span></span>

<span data-ttu-id="7973f-113">HQUS 法人制造高端扬声器。</span><span class="sxs-lookup"><span data-stu-id="7973f-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="7973f-114">在制造过程中，扬声器要经过三道工序。</span><span class="sxs-lookup"><span data-stu-id="7973f-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="7973f-115">**预装配** – 装配扬声器机箱。</span><span class="sxs-lookup"><span data-stu-id="7973f-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="7973f-116">机箱的材料在此工序开始前于材料仓库领料。</span><span class="sxs-lookup"><span data-stu-id="7973f-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="7973f-117">–**涂层** – 装配扬声器机箱之后，必须为其涂层。</span><span class="sxs-lookup"><span data-stu-id="7973f-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="7973f-118">此工序由供应商（即转包商）完成。</span><span class="sxs-lookup"><span data-stu-id="7973f-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="7973f-119">预装配后的扬声器机箱和两种材料一起发给涂层转包商。</span><span class="sxs-lookup"><span data-stu-id="7973f-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="7973f-120">**完工** – 预装配后的扬声器机箱由转包商涂层之后，将发回 HQUS 法人，以便完成扬声器的最终装配。</span><span class="sxs-lookup"><span data-stu-id="7973f-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="7973f-121">下图显示这三道工序及其使用的材料。</span><span class="sxs-lookup"><span data-stu-id="7973f-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![预装配、涂层和完工工序及其使用的材料](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="7973f-123">设置</span><span class="sxs-lookup"><span data-stu-id="7973f-123">Setup</span></span>

<span data-ttu-id="7973f-124">开始此演练之前，必须设置数据。</span><span class="sxs-lookup"><span data-stu-id="7973f-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="7973f-125">设置成品</span><span class="sxs-lookup"><span data-stu-id="7973f-125">Set up the finished product</span></span>

<span data-ttu-id="7973f-126">此过程引导您设置已发布产品 D8100，即“涂层机箱”。</span><span class="sxs-lookup"><span data-stu-id="7973f-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="7973f-127">选择**产品信息管理 \> 产品 \> 已发布产品**打开**已发布产品详细信息**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="7973f-128">在快速筛选器字段中，输入 **D8100** 查找现有的已发布产品。</span><span class="sxs-lookup"><span data-stu-id="7973f-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![在“已发布产品详细信息”页中筛选已发布产品 D8100](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="7973f-130">在操作窗格上的**设计**选项卡中，选择**工艺路线**打开**工艺路线**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="7973f-131">**工艺路线**页显示已发放产品 D8100 的八个工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="7973f-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="7973f-132">这八个工艺路线版本拆分为站点 1 和 站点 5 中的四个工艺路线。</span><span class="sxs-lookup"><span data-stu-id="7973f-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="7973f-133">工艺路线 000400 用于计算成本，工艺路线 00041 在涂层工序为内部工序时使用，工艺路线 00042 在涂层工序为外部工序时使用。</span><span class="sxs-lookup"><span data-stu-id="7973f-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![“工艺路线”页上的八个工艺路线版本](./media/subcontract03_route-page.png)

4. <span data-ttu-id="7973f-135">在上窗格的**版本**网格中，为站点 **5** 选择工艺路线版本 **00042**。</span><span class="sxs-lookup"><span data-stu-id="7973f-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="7973f-136">在下窗格的**概览**选项卡中的网格内，选择工序 **20** (**Cbnt CtSc**)。</span><span class="sxs-lookup"><span data-stu-id="7973f-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![已为站点 5 的工艺路线版本 00042 选择了工序 20](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="7973f-138">选择**常规**选项卡。</span><span class="sxs-lookup"><span data-stu-id="7973f-138">Select the **General** tab.</span></span>

    <span data-ttu-id="7973f-139">请注意，**工艺路线类型**字段设置为**供应商**。</span><span class="sxs-lookup"><span data-stu-id="7973f-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="7973f-140">该值指示工序 20 (Cbnt CtSc) 是转包工序。</span><span class="sxs-lookup"><span data-stu-id="7973f-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![“常规”选项卡上的“工艺路线类型”字段设置为“供应商”](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="7973f-142">选择**资源要求**选项卡。</span><span class="sxs-lookup"><span data-stu-id="7973f-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="7973f-143">计划生产期间，将使用产能查找适合的资源。</span><span class="sxs-lookup"><span data-stu-id="7973f-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="7973f-144">请注意，对于工序 20 (Cbnt CtSc)，需要有两种产能（即**涂层**和**涂层机箱**）的资源。</span><span class="sxs-lookup"><span data-stu-id="7973f-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![“资源要求”选项卡上的“涂层”和“涂层机箱”产能](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="7973f-146">选择**适用的资源**打开**适用的资源**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="7973f-147">将找到三种符合该工序的资源要求的资源。</span><span class="sxs-lookup"><span data-stu-id="7973f-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="7973f-148">请注意，资源 8851 和 8852 的类型为**供应商**。</span><span class="sxs-lookup"><span data-stu-id="7973f-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![“适用的资源”对话框中有三种适合的资源。](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="7973f-150">选择**确定**关闭**适合的资源**对话框并返回到**工艺路线**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="7973f-151">关闭**工艺路线**页返回到**已发布产品详细信息**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![“已发布产品详细信息”页](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="7973f-153">在操作窗格上的**设计**选项卡中，选择**物料清单版本**打开**物料清单版本**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="7973f-154">**物料清单版本**页显示已发布产品 D8100 的四个物料清单 (BOM) 版本。</span><span class="sxs-lookup"><span data-stu-id="7973f-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="7973f-155">物料清单 000040 用于涂层和规划，BOM 000041 在涂层工序在内部进行时使用，物料清单 000042 和 000043 在涂层工序转包时使用。</span><span class="sxs-lookup"><span data-stu-id="7973f-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="7973f-156">请注意，物料 S8050 的物料类型为**服务**产品。</span><span class="sxs-lookup"><span data-stu-id="7973f-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="7973f-157">此物料代表转包的工作。</span><span class="sxs-lookup"><span data-stu-id="7973f-157">This item represents the subcontracted work.</span></span>

    ![“物料清单版本”页上的四个物料清单版本](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="7973f-159">在**物料清单行**快速选项卡上，选择**编辑**打开**编辑物料清单行**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="7973f-160">创建生产订单并针对已发布产品 D8100 进行估计折后价，将为物料 S8050 自动生成一个采购订单。</span><span class="sxs-lookup"><span data-stu-id="7973f-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="7973f-161">此采购订单将链接到生产订单。</span><span class="sxs-lookup"><span data-stu-id="7973f-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="7973f-162">要自动生成采购订单，必须将**行类型**字段设置为**供应商**，并且必须为转包商选择供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="7973f-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="7973f-163">在此示例中，供应商帐户为 US-801。</span><span class="sxs-lookup"><span data-stu-id="7973f-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="7973f-164">请注意，物料清单行通过工序编号（此示例中为 20）连接到涂层工序。</span><span class="sxs-lookup"><span data-stu-id="7973f-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![“编辑物料清单行”对话框](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="7973f-166">为仓库工作人员创建密码</span><span class="sxs-lookup"><span data-stu-id="7973f-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="7973f-167">必须为使用手持设备的仓库工作人员定义密码。</span><span class="sxs-lookup"><span data-stu-id="7973f-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="7973f-168">选择**仓库管理 \> 设置 \> 工作人员**打开**工作用户**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="7973f-169">在**用户**快速选项卡上，选择用户 **51** 的行。</span><span class="sxs-lookup"><span data-stu-id="7973f-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![“工作用户”页](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="7973f-171">选择**重置密码**。</span><span class="sxs-lookup"><span data-stu-id="7973f-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="7973f-172">在**密码**和**确认密码**字段中，输入 **1**。</span><span class="sxs-lookup"><span data-stu-id="7973f-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="7973f-173">选择**设置密码**。</span><span class="sxs-lookup"><span data-stu-id="7973f-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="7973f-174">分步演练</span><span class="sxs-lookup"><span data-stu-id="7973f-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="7973f-175">**方案和背景**</span><span class="sxs-lookup"><span data-stu-id="7973f-175">**Scenario and background**</span></span>

<span data-ttu-id="7973f-176">为产品 D8100（即“涂层机箱”）创建 10 件的生产订单。</span><span class="sxs-lookup"><span data-stu-id="7973f-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="7973f-177">为机箱涂层是由供应商 US-801（即 Perfect Coating Solutions）完成的转包工序。</span><span class="sxs-lookup"><span data-stu-id="7973f-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="7973f-178">此生产订单中包含三道工序。</span><span class="sxs-lookup"><span data-stu-id="7973f-178">The production order consists of three operations.</span></span> <span data-ttu-id="7973f-179">在第一道工序中，机箱以内部工序的形式进行预装配。</span><span class="sxs-lookup"><span data-stu-id="7973f-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="7973f-180">将下达预装配的材料以便在原材料仓库中领料。</span><span class="sxs-lookup"><span data-stu-id="7973f-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="7973f-181">预装配完成之后，将把预装配的机箱和涂层工序所需的两种材料一起发给 Perfect Coating Solutions。</span><span class="sxs-lookup"><span data-stu-id="7973f-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="7973f-182">收到供应商发回的涂层机箱之后，需要先进行内部最终装配工序才能将其报告为成品。</span><span class="sxs-lookup"><span data-stu-id="7973f-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="7973f-183">选择**生产控制 \> 生产订单 \> 所有生产订单**打开**所有生产订单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="7973f-184">在操作窗格上，选择**新建生产订单**打开**创建生产订单**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![“创建生产订单”对话框](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="7973f-186">在**物料编号**字段中，选择 **D8100**。</span><span class="sxs-lookup"><span data-stu-id="7973f-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="7973f-187">选择物料编号之后，将显示库存维度的字段。</span><span class="sxs-lookup"><span data-stu-id="7973f-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="7973f-188">在**颜色**字段中，选择**铬**。</span><span class="sxs-lookup"><span data-stu-id="7973f-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="7973f-189">将显示一个消息框，询问是否应插入物料清单和工艺路线的当前版本。</span><span class="sxs-lookup"><span data-stu-id="7973f-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![消息框](./media/subcontract13_message-box.png)

5. <span data-ttu-id="7973f-191">选择**是**。</span><span class="sxs-lookup"><span data-stu-id="7973f-191">Select **Yes**.</span></span> 

    <span data-ttu-id="7973f-192">在**创建生产订单**对话框的**物料清单编号**和**工艺路线编号**字段中，将自动为产品 D8100 分别选择物料清单和工艺路线的当前版本。</span><span class="sxs-lookup"><span data-stu-id="7973f-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="7973f-193">在此示例中，将选择物料清单 **000040** 和工艺路线 **000040**。</span><span class="sxs-lookup"><span data-stu-id="7973f-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="7973f-194">对于物料清单和工艺路线，将为成本计算和规划使用版本 000040。</span><span class="sxs-lookup"><span data-stu-id="7973f-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="7973f-195">在**站点**字段中，选择 **5**。</span><span class="sxs-lookup"><span data-stu-id="7973f-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="7973f-196">在**仓库**字段中，选择 **51**。</span><span class="sxs-lookup"><span data-stu-id="7973f-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="7973f-197">在**物料清单编号**和**工艺路线编号**字段中，将已自动选择的值更改为 **000042**。</span><span class="sxs-lookup"><span data-stu-id="7973f-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7973f-198">对于物料清单和工艺路线，将使用版本 000042 把机箱涂层转包给供应商 US-801。</span><span class="sxs-lookup"><span data-stu-id="7973f-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![“创建生产订单”对话框中已设置值](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="7973f-200">选择**创建**以创建生产订单并返回到**所有生产订单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![“所有生产订单”页中的新生产订单](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="7973f-202">在操作窗格上的**生产订单**选项卡中，选择**估计**打开**估计**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![“估计”对话框](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="7973f-204">选择**确定**确认估计并返回到**所有生产订单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7973f-205">估计生产订单之后，将为供应商 US-801 生成服务物料 S8050 的采购订单。</span><span class="sxs-lookup"><span data-stu-id="7973f-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="7973f-206">在操作窗格上的**生产订单**选项卡中，选择**物料清单**打开**物料清单**页，可在此处查看生产订单的物料清单行。</span><span class="sxs-lookup"><span data-stu-id="7973f-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="7973f-207">请注意，对于服务项 S8050，将引用估计生产订单时生成的采购订单。</span><span class="sxs-lookup"><span data-stu-id="7973f-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![“物料清单”页上的生产订单物料行](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="7973f-209">关闭**物料清单**页返回到**所有生产订单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="7973f-210">在操作窗格上的**计划**选项卡中，选择**计划作业**打开**作业计划**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="7973f-211">指定以下值：</span><span class="sxs-lookup"><span data-stu-id="7973f-211">Specify the following values:</span></span>

    - <span data-ttu-id="7973f-212">在**计划的方向**字段中，选择**从明天开始**。</span><span class="sxs-lookup"><span data-stu-id="7973f-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="7973f-213">将**有限产能**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="7973f-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![“作业计划”对话框](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="7973f-215">选择**确定**关闭**作业计划**对话框并返回到**所有生产订单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="7973f-216">在操作窗格上的**计划** 选项卡中，选择**甘特图**打开**甘特图 - 资源视图**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="7973f-217">此甘特图提供如何为资源计划生产作业的视觉概览。</span><span class="sxs-lookup"><span data-stu-id="7973f-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="7973f-218">请注意，外部涂层工序包含三个作业：处理作业、运输作业和排队时间作业。</span><span class="sxs-lookup"><span data-stu-id="7973f-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![“甘特图 - 资源视图”页中的甘特图](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="7973f-220">关闭**甘特图 - 资源视图**页返回到**所有生产订单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="7973f-221">在操作窗格上的**生产订单**选项卡中，选择**发放**打开**发放**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![“发放”对话框](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="7973f-223">单击**确定**以关闭**发放**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="7973f-224">选择**生产控制 \> 定期任务 \> 发放到仓库 \> 自动发放物料清单和配方行**以打开**自动发放物料清单和配方行**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![“自动发放物料清单和配方行”对话框](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="7973f-226">选择**确定**以运行“自动发放物料清单和配方行”作业。</span><span class="sxs-lookup"><span data-stu-id="7973f-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="7973f-227">此作业将原材料的领料工作发放给仓库。</span><span class="sxs-lookup"><span data-stu-id="7973f-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="7973f-228">选择**生产控制 \> 生产订单 \> 所有生产订单**打开**所有生产订单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="7973f-229">可使用快速筛选器字段选择已在处理的生产订单。</span><span class="sxs-lookup"><span data-stu-id="7973f-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="7973f-230">在操作窗格上的**仓库**选项卡中，选择**工作详细信息**打开**工作**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="7973f-231">请注意，此页显示两组原材料领料工作。</span><span class="sxs-lookup"><span data-stu-id="7973f-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="7973f-232">第一组工作针对材料 M8100 和 M8101。</span><span class="sxs-lookup"><span data-stu-id="7973f-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="7973f-233">这些材料供工序 10 使用。</span><span class="sxs-lookup"><span data-stu-id="7973f-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="7973f-234">第二组工作针对材料 M8202 和 M8250。</span><span class="sxs-lookup"><span data-stu-id="7973f-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="7973f-235">这些物料供工序 20（这是转包工序）使用。</span><span class="sxs-lookup"><span data-stu-id="7973f-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![“工作”页中的两组原材料领料工作](./media/subcontract22_work-page.png)

26. <span data-ttu-id="7973f-237">启动仓库应用程序处理工序 10 的仓库工作。</span><span class="sxs-lookup"><span data-stu-id="7973f-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="7973f-238">选择**生产控制 \> 生产订单 \> 所有生产订单**打开**所有生产订单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="7973f-239">可使用快速筛选器字段选择已在处理的生产订单。</span><span class="sxs-lookup"><span data-stu-id="7973f-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="7973f-240">在操作窗格上的**生产订单**选项卡中，选择**开始**打开**开始**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="7973f-241">在**常规**选项卡上，指定以下值：</span><span class="sxs-lookup"><span data-stu-id="7973f-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="7973f-242">在**开始工序编号**</span><span class="sxs-lookup"><span data-stu-id="7973f-242">In the **From Oper. No.**</span></span> <span data-ttu-id="7973f-243">字段中，选择 **10**。</span><span class="sxs-lookup"><span data-stu-id="7973f-243">field, select **10**.</span></span>
    - <span data-ttu-id="7973f-244">在**截止工序编号**</span><span class="sxs-lookup"><span data-stu-id="7973f-244">In the **To Oper. No.**</span></span> <span data-ttu-id="7973f-245">字段中，选择 **10**。</span><span class="sxs-lookup"><span data-stu-id="7973f-245">field, select **10**.</span></span>

    ![“常规”选项卡中设置的值](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="7973f-247">选择**确定**关闭**开始**对话框并返回到**所有生产订单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="7973f-248">请注意，生产订单的状态现在是**已开始**。</span><span class="sxs-lookup"><span data-stu-id="7973f-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="7973f-249">工序 10 的材料供领料单日记帐自动过帐使用。</span><span class="sxs-lookup"><span data-stu-id="7973f-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="7973f-250">工序 10 所用时间由工艺卡日记帐自动过帐计算。</span><span class="sxs-lookup"><span data-stu-id="7973f-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="7973f-251">启动仓库应用程序处理工序 20 的仓库工作。</span><span class="sxs-lookup"><span data-stu-id="7973f-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="7973f-252">在操作窗格上的**生产订单**选项卡中，选择**开始**打开**开始**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="7973f-253">在**常规**选项卡上，指定以下值：</span><span class="sxs-lookup"><span data-stu-id="7973f-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="7973f-254">在**开始工序编号**</span><span class="sxs-lookup"><span data-stu-id="7973f-254">In the **From Oper. No.**</span></span> <span data-ttu-id="7973f-255">字段中，选择 **20**。</span><span class="sxs-lookup"><span data-stu-id="7973f-255">field, select **20**.</span></span>
    - <span data-ttu-id="7973f-256">在**截止工序编号**</span><span class="sxs-lookup"><span data-stu-id="7973f-256">In the **To Oper. No.**</span></span> <span data-ttu-id="7973f-257">字段中，选择 **20**。</span><span class="sxs-lookup"><span data-stu-id="7973f-257">field, select **20**.</span></span>
    - <span data-ttu-id="7973f-258">在**数量**字段中，输入 **10**。</span><span class="sxs-lookup"><span data-stu-id="7973f-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="7973f-259">将**立即将领料单过帐**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="7973f-259">Set the **Post picking list now** option to **No**.</span></span>

    ![“常规”选项卡中设置的值](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="7973f-261">选择**确定**关闭**开始**对话框并返回到**所有生产订单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="7973f-262">将为用于涂层工序和服务项的材料创建领料单。</span><span class="sxs-lookup"><span data-stu-id="7973f-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="7973f-263">服务项提供转包工序的成本。</span><span class="sxs-lookup"><span data-stu-id="7973f-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="7973f-264">在操作窗格上的**视图** 选项卡中，选择**领料单**打开**领料单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="7973f-265">选择未过帐的领料单，然后选择日记帐编号以显示日记帐行。</span><span class="sxs-lookup"><span data-stu-id="7973f-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![“领料单”页中的日记帐行](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="7973f-267">在操作窗格上，选择**打印** \> **领料单报告**以打开**领料单报告**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="7973f-268">将**使用交货通知板式**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="7973f-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![“领料单报告”对话框](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="7973f-270">选择**确定**以生成**领料单**报告。</span><span class="sxs-lookup"><span data-stu-id="7973f-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="7973f-271">在此示例中，将从生产领料单日记帐打印供应商交货通知。</span><span class="sxs-lookup"><span data-stu-id="7973f-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="7973f-272">交货通知指定发给将进行涂层工序的供应商的材料。</span><span class="sxs-lookup"><span data-stu-id="7973f-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![领料单报表](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="7973f-274">关闭**领料单**报告以返回到**领料单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="7973f-275">在操作窗格上，选择**过帐**以打开**过帐日记帐**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![“过帐日记帐”对话框](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="7973f-277">单击**确定**以关闭**过帐日记帐**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="7973f-278">打开采购订单。</span><span class="sxs-lookup"><span data-stu-id="7973f-278">Open the purchase order.</span></span>

    ![“采购订单”页](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="7973f-280">在操作窗格上的**采购**选项卡上，选择**确认**。</span><span class="sxs-lookup"><span data-stu-id="7973f-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="7973f-281">单击**过帐**以打开**过帐日记帐**对话框。</span><span class="sxs-lookup"><span data-stu-id="7973f-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="7973f-282">选择**确定**关闭**过帐日记帐**对话框并返回到**采购订单**页。</span><span class="sxs-lookup"><span data-stu-id="7973f-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="7973f-283">将单价从 **33** 更改为 **40**。</span><span class="sxs-lookup"><span data-stu-id="7973f-283">Change the unit price from **33** to **40**.</span></span>

    ![“采购订单”页中已更改的单价](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="7973f-285">再次确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="7973f-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="7973f-286">产品收据。</span><span class="sxs-lookup"><span data-stu-id="7973f-286">Product receipt.</span></span>

    ![“过帐的产品收据”对话框](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="7973f-288">采购发票。</span><span class="sxs-lookup"><span data-stu-id="7973f-288">Purchase invoice.</span></span>
52. <span data-ttu-id="7973f-289">更新匹配状态。</span><span class="sxs-lookup"><span data-stu-id="7973f-289">Update the match status.</span></span>

    ![“供应商发票”页](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="7973f-291">完工入库。</span><span class="sxs-lookup"><span data-stu-id="7973f-291">Report as finished.</span></span>

    ![“完工入库”对话框](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="7973f-293">结束。</span><span class="sxs-lookup"><span data-stu-id="7973f-293">End.</span></span>

    ![“结束”对话框](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="7973f-295">成本比较。</span><span class="sxs-lookup"><span data-stu-id="7973f-295">Cost comparison.</span></span>

    ![“成本比较”图](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="7973f-297">数据缺少设置。</span><span class="sxs-lookup"><span data-stu-id="7973f-297">Missing setup in data.</span></span>
