---
title: 使用 Dynamics 365 Sales 在 B2B 电子商务网站上管理业务合作伙伴用户
description: 本文介绍如何使用 Microsoft Dynamics 365 Sales 管理 Dynamics 365 Commerce 企业到企业 (B2B) 网站的业务合作伙伴审批。
author: ShalabhjainMSFT
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: d178e619fca7915286181aa803376cd564f60a26
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278643"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>使用 Dynamics 365 Sales 在 B2B 电子商务网站上管理业务合作伙伴用户

[!include [banner](../../includes/banner.md)]

本文介绍如何使用 Microsoft Dynamics 365 Sales 管理 Dynamics 365 Commerce 企业到企业 (B2B) 网站的业务合作伙伴审批。 已投资 Dynamics 365 Sales 解决方案的组织可以将潜在顾客和商机概念用于 B2B 电子商务业务合作伙伴审批流程。

有关 B2B 业务合作伙伴审批流程的背景信息，请参阅[在 B2B 电子商务网站上管理业务合作伙伴用户](manage-b2b-users.md)。

潜在的业务合作伙伴可以通过 B2B 网站上的链接提交加入请求，来启动 B2B 电子商务网站的加入流程。 提交请求并在 Commerce headquarters 中运行相关作业（如 **P-0001** 和 **同步订单和渠道请求**）后，加入请求保存在 Commerce headquarters 中的 **所有目标客户** 页面。 然后，可以在 Sales 中完成业务合作伙伴目标客户审批流程。

启用 Sales 和 Commerce 之间的集成后，在 Commerce 中创建业务合作伙伴目标客户会在 Sales 中创建 *潜在顾客*。

下图显示了 Sales 中业务合作伙伴目标客户的潜在顾客创建页面的一个示例。

![Dynamics 365 Sales 中的潜在顾客创建页面。](../media/LeadInSales.png)

在图中，**联系人** 部分显示提交加入请求的人员，**公司** 部分显示组织。 **时间线** 部分的注释指示潜在顾客是由双写入基础结构生成的。 由于是由双写入基础结构创建的，因此此潜在顾客不会出现在 **我的已打开潜在顾客** 下拉列表中。 而是将出现在名为 **所有商务 B2B 潜在顾客** 的新视图下。

根据 Sales 中的标准潜在顾客资格授予流程，当用户“授予”潜在顾客资格时，*商机* 记录、*联系人* 记录和 *客户* 记录将创建。 双写入基础结构用于将联系人和客户记录写入 Commerce。 联系人被创建为 *个人* 类型的客户，公司被创建为 *组织* 类型的客户。 如果用户为商机选择 **作为赢单结束**，目标客户将在 Commerce 中获得批准。 目标客户被批准时会创建客户层次结构。

Commerce 中将执行所有其余的业务流程。 这些流程包括向业务合作伙伴发送电子邮件、为用户定义信用额度管理以及向 B2B 站点添加更多用户。 但是，如果用户取消潜在顾客资格或将商机标记为丢单，而不是授予潜在顾客资格，Commerce 中的目标客户将被标记为拒绝，拒绝加入电子邮件将发送给请求者。

## <a name="enable-integration-between-sales-and-commerce"></a>实现 Sales 和 Commerce 之间的集成

Sales 和 Commerce 之间的集成依赖于双写入基础结构。 因此，应启用双写入并使其正常工作，以将在一个系统中创建的客户写入另一个系统。 有关双写入基础结构的详细信息，请参阅[双写入概述](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview)。

双写入设置完成后，实现伙伴可以转到 [Microsoft AppSource](https://appsource.microsoft.com/) 搜索名为[双写入 Commerce 解决方案](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview)的解决方案。 使用标准安装向导安装包，然后通过在 B2B 站点上创建目标客户进行测试。 创建目标客户后，验证请求是否显示在 Commerce 中的 **所有目标客户** 上，然后验证该目标客户是否在 Sales 中显示为潜在顾客。

## <a name="additional-resources"></a>其他资源

[在 B2B 电子商务网站上管理业务合作伙伴用户](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
