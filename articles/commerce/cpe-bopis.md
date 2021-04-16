---
title: 在 Dynamics 365 Commerce 评估环境中配置 BOPIS
description: 本主题说明在预配 Microsoft Dynamics 365 Commerce 评估环境后如何在此环境中配置“线上购买，店内提货”(BOPIS)。
author: rubendel
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 219504da62fd4637ed01f9acbab32f873cef81b0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795947"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="2cdd9-103">在 Dynamics 365 Commerce 评估环境中配置 BOPIS</span><span class="sxs-lookup"><span data-stu-id="2cdd9-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2cdd9-104">本主题说明在预配 Microsoft Dynamics 365 Commerce 评估环境后如何在其中配置“线上购买，店内提货”(BOPIS)。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="2cdd9-105">必备项</span><span class="sxs-lookup"><span data-stu-id="2cdd9-105">Prerequisite</span></span>

<span data-ttu-id="2cdd9-106">请仅在预配和配置了 Commerce 评估环境之后，再完成本主题中的过程。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="2cdd9-107">有关如何预配和配置环境的信息，请参阅[预配 Dynamics 365 Commerce 评估环境](provisioning-guide.md)和[配置 Dynamics 365 Commerce 评估环境](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning)。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="2cdd9-108">端到端预配和配置 Commerce 环境之后，可以使用本主题启用 BOPIS 方案。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="2cdd9-109">配置 POS</span><span class="sxs-lookup"><span data-stu-id="2cdd9-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="2cdd9-110">配置 Modern POS</span><span class="sxs-lookup"><span data-stu-id="2cdd9-110">Configure Modern POS</span></span>

<span data-ttu-id="2cdd9-111">涉及信用卡付款的 BOPIS 方案需要硬件工作站。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="2cdd9-112">硬件工作站内置在适用于 Windows 和 Android 客户端的 Modern POS 内。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="2cdd9-113">如果您使用适用于 iOS 的 Cloud POS 或 Modern POS，销售点 (POS) 客户端必须与共享硬件工作站配对。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="2cdd9-114">本主题说明如何为 Windows 和 Android 客户端配置 BOPIS。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="2cdd9-115">有关如何设置共享硬件工作站的信息，请参阅[配置和安装 Retail 硬件工作站](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation)。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="2cdd9-116">转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> 收银机**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="2cdd9-117">选择收银机 **SANFRAN-5**，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="2cdd9-118">将 **硬件配置文件** 字段的值从 **HW002** 更改为 **HW001**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="2cdd9-119">要同步更改，转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="2cdd9-120">选择配送计划 **1090**，然后在操作窗格上选择 **立即运行**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="2cdd9-121">选择 **是**，然后选择 **确定** 启动数据同步。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="2cdd9-122">安装 Modern POS</span><span class="sxs-lookup"><span data-stu-id="2cdd9-122">Install Modern POS</span></span>

1. <span data-ttu-id="2cdd9-123">转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> 设备**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="2cdd9-124">选择设备 **SANFRANCIS-5**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="2cdd9-125">在操作窗格上，选择 **下载**，然后选择 **配置文件**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="2cdd9-126">选择 **下载**，然后选择 **Retail Modern POS**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="2cdd9-127">当下载 **ModernPOSSetup.exe** 文件完成后，选择 **打开文件**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![打开文件](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="2cdd9-129">选择 **下一步** 逐步完成安装流程。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="2cdd9-130">安装完成后，选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="2cdd9-131">激活 Modern POS</span><span class="sxs-lookup"><span data-stu-id="2cdd9-131">Activate Modern POS</span></span>

1. <span data-ttu-id="2cdd9-132">在 Windows 桌面上，选择 **开始** 按钮，然后输入 **Retail Modern POS**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="2cdd9-133">选择 **Retail Modern POS** 应用程序启动激活。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="2cdd9-134">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-134">Select **Next**.</span></span> <span data-ttu-id="2cdd9-135">**服务器 URL**、**设备 ID** 和 **收银机编号** 字段应使用在上一过程中下载的配置文件中的信息进行预设。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="2cdd9-136">选择 **激活**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-136">Select **Activate**.</span></span>
5. <span data-ttu-id="2cdd9-137">身份验证对话框将出现。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-137">An authentication dialog box appears.</span></span> <span data-ttu-id="2cdd9-138">选择使用以前与工作人员 **000713 - Andrew Collette** 关联的电子邮件地址的帐户。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2cdd9-139">如果您尚未将工作人员与您的标识相关联，激活将不会成功。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="2cdd9-140">在这种情况下，请按照[配置 Dynamics 365 Commerce 评估环境](cpe-post-provisioning.md#associate-a-worker-with-your-identity)主题中“将工作人员与您的标识关联”一节的步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="2cdd9-141">当提示您让您的组织管理设备时，请选择 **仅此应用**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="2cdd9-142">激活完成后，选择 **开始**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="2cdd9-143">在 Modern POS 中启用 BOPIS</span><span class="sxs-lookup"><span data-stu-id="2cdd9-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="2cdd9-144">将 **000713** 作为操作员 ID、将 **123** 作为密码登录 Modern POS。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="2cdd9-145">在播放介绍性演练视频时，请选中对话框左下角的两个复选框，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="2cdd9-146">如果未提示您结束班次，请滚动到 **欢迎** 页面的右侧，选择 **结束班次**，然后重新登录到 POS。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="2cdd9-147">登录后，在系统提示时，选择 **执行非银箱操作**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="2cdd9-148">在 **欢迎** 页上，向右滚动，然后选择 **选择硬件工作站** 操作。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="2cdd9-149">选择 **管理**，将 **使用硬件工作站** 选项设置为 **打开**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="2cdd9-150">注销 POS，然后重新登录。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="2cdd9-151">登录后，选择 **开始新班次**，然后选择 **银箱**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="2cdd9-152">完成 BOPIS 方案</span><span class="sxs-lookup"><span data-stu-id="2cdd9-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="2cdd9-153">为店内提货创建店面订单</span><span class="sxs-lookup"><span data-stu-id="2cdd9-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="2cdd9-154">转到在环境配置期间您在[初始化电子商务](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce)步骤中指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="2cdd9-155">选择一个商品，然后选择 **添加到购物车**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="2cdd9-156">在购物袋页面上，为您刚才添加的订单行选择 **提货**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="2cdd9-157">在 **选择商店** 对话框中，输入 **旧金山**，然后选择 **搜索** 按钮。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="2cdd9-158">在结果列表中，找到“旧金山”商店，然后选择 **在此提货**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="2cdd9-159">在购物袋页面上，选择 **以访客身份结帐**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="2cdd9-160">要继续结帐，您必须接受 Cookie 通知。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="2cdd9-161">此通知在结帐页面的顶部显示为横幅。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="2cdd9-162">对于信用卡付款方式，请输入以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="2cdd9-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="2cdd9-163">**持卡人姓名：** 输入姓名。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="2cdd9-164">**卡号：** 输入 **4111-1111-1111-1111**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="2cdd9-165">**到期日期：** 输入 **10/20**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="2cdd9-166">**卡验证值 (CVV) 代码：** 输入 **737**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2cdd9-167">在任何情况下，都不要尝试在测试站点上使用实际的信用卡信息。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="2cdd9-168">输入帐单地址的详细信息继续结帐，然后选择 **保存并继续**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="2cdd9-169">准备下订单时，选择 **结帐**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="2cdd9-170">将在线订单同步到后台</span><span class="sxs-lookup"><span data-stu-id="2cdd9-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="2cdd9-171">有关如何同步在线订单的信息，请参阅[过帐在线销售和付款](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments)。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="2cdd9-172">在商店提货</span><span class="sxs-lookup"><span data-stu-id="2cdd9-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="2cdd9-173">登录到 POS。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="2cdd9-174">在 **欢迎** 屏幕，选择 **订单履行**</span><span class="sxs-lookup"><span data-stu-id="2cdd9-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="2cdd9-175">在要提货的商品列表中，从在线下单的订单中选择该行。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="2cdd9-176">选择订单行后，选择 **提货**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="2cdd9-177">行项已添加到交易屏幕，结欠余额将显示 **$0.00**。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="2cdd9-178">选择结欠金额 **$0.00**，或选择任何一个付款方式来完成交易。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2cdd9-179">故障排除</span><span class="sxs-lookup"><span data-stu-id="2cdd9-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="2cdd9-180">在 POS 中检索到的在线订单的结欠余额不是零</span><span class="sxs-lookup"><span data-stu-id="2cdd9-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="2cdd9-181">检索到订单为店内提货时，如果结欠余额不是 0（零），请确保正在使用 Modern POS，并且硬件工作站处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="2cdd9-182">如果使用的是适用于 iOS 的 Cloud POS 或 Modern POS，请确保共享硬件工作站处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="2cdd9-183">需要某种形式的活动硬件工作站来检索在线进行的付款。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="2cdd9-184">付款捕获的一般问题</span><span class="sxs-lookup"><span data-stu-id="2cdd9-184">General issues with payment capture</span></span>

<span data-ttu-id="2cdd9-185">对于所有一般性问题，作为第一步，始终应该查阅 Modern POS 或 Internet 信息服务 (IIS) 硬件工作站事件日志。</span><span class="sxs-lookup"><span data-stu-id="2cdd9-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="2cdd9-186">您可以在 Windows 事件日志的以下节点下找到这些日志：</span><span class="sxs-lookup"><span data-stu-id="2cdd9-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="2cdd9-187">应用程序和服务日志 \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="2cdd9-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="2cdd9-188">应用程序和服务日志 \> Microsoft \> Dynamics \> Commerce-Hardware Station</span><span class="sxs-lookup"><span data-stu-id="2cdd9-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2cdd9-189">其他资源</span><span class="sxs-lookup"><span data-stu-id="2cdd9-189">Additional resources</span></span>

[<span data-ttu-id="2cdd9-190">Dynamics 365 Commerce 评估环境概览</span><span class="sxs-lookup"><span data-stu-id="2cdd9-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="2cdd9-191">预配 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="2cdd9-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="2cdd9-192">为 Dynamics 365 Commerce 评估环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="2cdd9-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="2cdd9-193">Dynamics 365 Commerce 评估环境常见问题</span><span class="sxs-lookup"><span data-stu-id="2cdd9-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="2cdd9-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="2cdd9-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="2cdd9-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="2cdd9-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="2cdd9-196">Microsoft Azure 门户</span><span class="sxs-lookup"><span data-stu-id="2cdd9-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="2cdd9-197">Dynamics 365 Commerce 网站</span><span class="sxs-lookup"><span data-stu-id="2cdd9-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="2cdd9-198">Adyen 付款连接器</span><span class="sxs-lookup"><span data-stu-id="2cdd9-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="2cdd9-199">使用 Adyen 连接器保存在线付款工具</span><span class="sxs-lookup"><span data-stu-id="2cdd9-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="2cdd9-200">全渠道付款概览</span><span class="sxs-lookup"><span data-stu-id="2cdd9-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)


[!INCLUDE[footer-include](../includes/footer-banner.md)]