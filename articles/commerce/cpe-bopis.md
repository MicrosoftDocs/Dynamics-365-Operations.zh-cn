---
title: 在 Dynamics 365 Commerce 评估环境中配置 BOPIS
description: 本主题说明在预配 Microsoft Dynamics 365 Commerce 评估环境后如何在此环境中配置“线上购买，店内提货”(BOPIS)。
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ec1c556a70ed92a40d3cb2bf45fb6156b7dbf7fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993467"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a>在 Dynamics 365 Commerce 评估环境中配置 BOPIS

[!include [banner](includes/banner.md)]

本主题说明在预配 Microsoft Dynamics 365 Commerce 评估环境后如何在其中配置“线上购买，店内提货”(BOPIS)。

## <a name="prerequisite"></a>必备项

请仅在预配和配置了 Commerce 评估环境之后，再完成本主题中的过程。 有关如何预配和配置环境的信息，请参阅[预配 Dynamics 365 Commerce 评估环境](provisioning-guide.md)和[配置 Dynamics 365 Commerce 评估环境](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning)。

端到端预配和配置 Commerce 环境之后，可以使用本主题启用 BOPIS 方案。

## <a name="configure-the-pos"></a>配置 POS

### <a name="configure-modern-pos"></a>配置 Modern POS

涉及信用卡付款的 BOPIS 方案需要硬件工作站。 硬件工作站内置在适用于 Windows 和 Android 客户端的 Modern POS 内。 如果您使用适用于 iOS 的 Cloud POS 或 Modern POS，销售点 (POS) 客户端必须与共享硬件工作站配对。 本主题说明如何为 Windows 和 Android 客户端配置 BOPIS。 有关如何设置共享硬件工作站的信息，请参阅[配置和安装 Retail 硬件工作站](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation)。

1. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> 收银机**。
2. 选择收银机 **SANFRAN-5**，然后选择 **编辑**。
3. 将 **硬件配置文件** 字段的值从 **HW002** 更改为 **HW001**，然后选择 **保存**。
4. 要同步更改，转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划**。
5. 选择配送计划 **1090**，然后在操作窗格上选择 **立即运行**。
6. 选择 **是**，然后选择 **确定** 启动数据同步。 

### <a name="install-modern-pos"></a>安装 Modern POS

1. 转至 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> 设备**。
2. 选择设备 **SANFRANCIS-5**。
3. 在操作窗格上，选择 **下载**，然后选择 **配置文件**。
4. 选择 **下载**，然后选择 **Retail Modern POS**。 
5. 当下载 **ModernPOSSetup.exe** 文件完成后，选择 **打开文件**。

    ![打开文件](./dev-itpro/media/PAYMENTS/openfile.png)

6. 选择 **下一步** 逐步完成安装流程。 安装完成后，选择 **关闭**。

### <a name="activate-modern-pos"></a>激活 Modern POS

1. 在 Windows 桌面上，选择 **开始** 按钮，然后输入 **Retail Modern POS**。
2. 选择 **Retail Modern POS** 应用程序启动激活。
3. 选择 **下一步**。 **服务器 URL**、**设备 ID** 和 **收银机编号** 字段应使用在上一过程中下载的配置文件中的信息进行预设。
4. 选择 **激活**。
5. 身份验证对话框将出现。 选择使用以前与工作人员 **000713 - Andrew Collette** 关联的电子邮件地址的帐户。

    > [!NOTE]
    > 如果您尚未将工作人员与您的标识相关联，激活将不会成功。 在这种情况下，请按照[配置 Dynamics 365 Commerce 评估环境](cpe-post-provisioning.md#associate-a-worker-with-your-identity)主题中“将工作人员与您的标识关联”一节的步骤进行操作。
    
6. 当提示您让您的组织管理设备时，请选择 **仅此应用**。
7. 激活完成后，选择 **开始**。

### <a name="enable-bopis-in-modern-pos"></a>在 Modern POS 中启用 BOPIS

1. 将 **000713** 作为操作员 ID、将 **123** 作为密码登录 Modern POS。
2. 在播放介绍性演练视频时，请选中对话框左下角的两个复选框，然后关闭对话框。
3. 如果未提示您结束班次，请滚动到 **欢迎** 页面的右侧，选择 **结束班次**，然后重新登录到 POS。
4. 登录后，在系统提示时，选择 **执行非银箱操作**。
5. 在 **欢迎** 页上，向右滚动，然后选择 **选择硬件工作站** 操作。
6. 选择 **管理**，将 **使用硬件工作站** 选项设置为 **打开**，然后选择 **确定**。
7. 注销 POS，然后重新登录。
8. 登录后，选择 **开始新班次**，然后选择 **银箱**。

## <a name="complete-a-bopis-scenario"></a>完成 BOPIS 方案

### <a name="create-a-storefront-order-for-in-store-pickup"></a>为店内提货创建店面订单

1. 转到在环境配置期间您在[初始化电子商务](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce)步骤中指定的 URL。
2. 选择一个商品，然后选择 **添加到购物车**。
3. 在购物袋页面上，为您刚才添加的订单行选择 **提货**。
4. 在 **选择商店** 对话框中，输入 **旧金山**，然后选择 **搜索** 按钮。
5. 在结果列表中，找到“旧金山”商店，然后选择 **在此提货**。
6. 在购物袋页面上，选择 **以访客身份结帐**。 

    > [!NOTE]
    > 要继续结帐，您必须接受 Cookie 通知。 此通知在结帐页面的顶部显示为横幅。

7. 对于信用卡付款方式，请输入以下详细信息：

    - **持卡人姓名：** 输入姓名。
    - **卡号：** 输入 **4111-1111-1111-1111**。
    - **到期日期：** 输入 **10/20**。
    - **卡验证值 (CVV) 代码：** 输入 **737**。

    > [!IMPORTANT]
    > 在任何情况下，都不要尝试在测试站点上使用实际的信用卡信息。

8. 输入帐单地址的详细信息继续结帐，然后选择 **保存并继续**。
9. 准备下订单时，选择 **结帐**。

### <a name="synchronize-online-orders-to-the-back-office"></a>将在线订单同步到后台

有关如何同步在线订单的信息，请参阅[过帐在线销售和付款](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments)。

### <a name="pick-up-an-order-in-the-store"></a>在商店提货

1. 登录到 POS。
2. 在 **欢迎** 屏幕，选择 **订单履行**
3. 在要提货的商品列表中，从在线下单的订单中选择该行。
4. 选择订单行后，选择 **提货**。

    行项已添加到交易屏幕，结欠余额将显示 **$0.00**。

5. 选择结欠金额 **$0.00**，或选择任何一个付款方式来完成交易。

## <a name="troubleshooting"></a>故障排除

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>在 POS 中检索到的在线订单的结欠余额不是零

检索到订单为店内提货时，如果结欠余额不是 0（零），请确保正在使用 Modern POS，并且硬件工作站处于活动状态。 如果使用的是适用于 iOS 的 Cloud POS 或 Modern POS，请确保共享硬件工作站处于活动状态。 需要某种形式的活动硬件工作站来检索在线进行的付款。

### <a name="general-issues-with-payment-capture"></a>付款捕获的一般问题

对于所有一般性问题，作为第一步，始终应该查阅 Modern POS 或 Internet 信息服务 (IIS) 硬件工作站事件日志。 您可以在 Windows 事件日志的以下节点下找到这些日志：

- 应用程序和服务日志 \> Microsoft \> Dynamics \> Commerce-ModernPOS
- 应用程序和服务日志 \> Microsoft \> Dynamics \> Commerce-Hardware Station

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 评估环境概览](cpe-overview.md)

[预配 Dynamics 365 Commerce 评估环境](provisioning-guide.md)

[为 Dynamics 365 Commerce 评估环境配置可选功能](cpe-optional-features.md)

[Dynamics 365 Commerce 评估环境常见问题](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure 门户](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)

[Adyen 付款连接器](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[使用 Adyen 连接器保存在线付款工具](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[全渠道付款概览](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)
