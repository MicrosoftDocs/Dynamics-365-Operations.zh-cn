---
title: 配置 Dynamics 365 Commerce 评估环境
description: 本主题说明如何在预配后配置 Microsoft Dynamics 365 Commerce 评估环境。
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 87933c57ee5f626b224b1edc92da13906e3edc2613f61c5b4a917d8cc5d1dcd3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742432"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>配置 Dynamics 365 Commerce 评估环境

[!include [banner](includes/banner.md)]

本主题说明如何在预配后配置 Microsoft Dynamics 365 Commerce 评估环境。

请仅在预配了 Commerce 评估环境之后，再完成本主题中的过程。 有关如何预配 Commerce 评估环境的信息，请参阅[预配 Commerce 评估环境](provisioning-guide.md)。

端到端预配 Commerce 评估环境后，必须先完成其他预配后配置步骤，然后才能开始评估环境。 要完成这些步骤，您必须使用 Microsoft Dynamics Lifecycle Services (LCS) 和 Dynamics 365 Commerce。

## <a name="before-you-start"></a>开始之前

1. 登录 [LCS 门户](https://lcs.dynamics.com)。
1. 转到您的项目。
1. 在顶级菜单上，选择 **云托管的环境**。
1. 在列表中选择您的环境。
1. 在右侧的环境信息中，选择 **登录到环境**。 您将被送到 Commerce headquarters。
1. 确保选择了右上角的 **USRT** 法人。

在 Commerce headquarters 进行预配后活动期间，请确保 **USRT** 法人始终处于选中状态。

## <a name="configure-the-point-of-sale"></a>配置销售点

### <a name="associate-a-worker-with-your-identity"></a>将工作人员与您的标识关联

要将工作人员与您的标识关联，请在 Commerce headquarters 中执行以下步骤。

1. 使用左侧菜单转到 **模块 \> Retail 和 Commerce \> 员工 \> 工作人员**。
1. 在列表中，找到并选择以下记录：**000713 - Andrew Collette**。
1. 在“操作窗格”上，选择 **Commerce**。
1. 选择 **关联现有标识**。
1. 在（**使用电子邮件搜索** 右侧的）**电子邮件** 字段中，输入您的电子邮件地址。
1. 选择 **搜索**。
1. 选择包含您的姓名的记录。
1. 选择 **确定**。
1. 选择 **保存**。

### <a name="activate-cloud-pos"></a>激活 Cloud POS

要激活 Cloud POS，请在 LCS 中执行以下步骤。

1. 在顶级菜单上，选择 **云托管的环境**。
1. 在列表中选择您的环境。
1. 在右侧的环境信息中，选择 **登录到云销售点**。
1. 选择 **下一步** 打开 **开始之前** 对话框。
1. 保留 **服务器 URL** 字段不变。 选择 **下一步**。
1. 使用您的 Microsoft Azure Active Directory (Azure AD) 帐户登录。
1. 在 **商店名称** 下，选择 **旧金山**，然后选择 **下一步**。
1. 在 **收银机和设备** 下，选择 **SANFRAN-1**。
1. 选择 **激活**。 您已注销并进入 POS 登录页面。
1. 现在可使用操作员 ID **000713** 和密码 **123** 登录到云 POS 体验。

## <a name="set-up-your-site-in-commerce"></a>在 Commerce 中设置站点

要开始在 Commerce 中设置评估站点，请按照下列步骤操作。

1. 使用您在预配期间初始化电子商务时记下的 URL 登录站点构建器（请参阅[初始化电子商务](provisioning-guide.md#initialize-e-commerce)）。
1. 选择 **Fabrikam** 站点打开站点设置对话框。
1. 选择初始化电子商务时输入的域。
1. 选择 **Fabrikam 扩展的在线商店** 作为默认渠道。 （请务必选择 **扩展的** 在线商店。）
1. 选择 **en-us** 作为默认语言。
1. 保留 **路径** 的值不变。
1. 选择 **确定**。 将出现站点上的页面的列表。

## <a name="enable-jobs"></a>启用作业

要在 Commerce 中启用作业，请执行以下步骤。

1. 登录到环境（总部）。
1. 使用左侧菜单转到 **Retail 和 Commerce \> 查询和报表 \> 批处理作业**。

    必须为以下每个作业完成此过程的其余步骤：

    * 处理零售订单电子邮件通知
    * 产品可用性
    * P-0001
    * 同步订单作业

1. 使用快速筛选器按名称搜索作业。
1. 如果作业的状态为 **正在执行**，请执行以下步骤：

    1. 选择记录。
    1. 在操作窗格上，在 **批处理作业** 选项卡上，选择 **更改状态**。
    1. 选择 **取消**，然后选择 **确定**。

（可选）您还可以将以下作业的重复执行间隔设置为一 (1) 分钟：

* 处理零售订单电子邮件通知作业
* P-0001 作业
* 同步订单作业

### <a name="run-full-data-synchronization"></a>运行完全数据同步

要在 Commerce 中运行完整的数据同步，请在 Commerce headquarters 中按照下列步骤操作。

1. 使用左侧菜单转到 **模块 \> Retail 和 Commerce \> 总部设置 \> 商业调度程序 \> 渠道数据库**。
1. 选择名为 **scXXXXXXXXX** 的渠道。
1. 在操作窗格中，选择 **完全数据同步**。
1. 输入 **9999** 作为配送计划。
1. 选择 **确定**。
1. 选择 **确定**。

### <a name="test-credit-card-information-to-do-test-purchases"></a>测试信用卡信息以执行测试性购买

若要在站点中执行测试交易，可使用以下测试信用卡信息：

- **卡号：** 4111-1111-1111-1111
- **到期日期：** 10/20
- **卡验证值 (CVV) 代码：** 737

> [!IMPORTANT]
> 在任何情况下，都不要尝试在测试站点上使用实际的信用卡信息。

## <a name="next-steps"></a>后续步骤

在预配和配置步骤完成之后，您就可以开始使用评估环境了。 使用 Commerce 站点构建器 URL 可以转到创作体验。 使用 Commerce 站点 URL 可以转到零售客户站点体验。

要为 Commerce 评估环境配置可选功能，请参阅[为 Commerce 评估环境配置可选功能](cpe-optional-features.md)。

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 评估环境概览](cpe-overview.md)

[预配 Dynamics 365 Commerce 评估环境](provisioning-guide.md)

[为 Dynamics 365 Commerce 评估环境配置可选功能](cpe-optional-features.md)

[在 Dynamics 365 Commerce 评估环境中配置 BOPIS](cpe-bopis.md)

[Dynamics 365 Commerce 评估环境常见问题](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure 门户](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]