---
title: Dynamics 365 Supply Chain Management 10.0.6（2019 年 11 月）中的新增功能或更改
description: 此主题介绍了 Dynamics 365 Supply Chain Management 10.0.6 中的新增功能或更改的功能。
author: josaw1
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: d72bc060685fa5d4bd49043a29249717786e2b46b5572f2b127023e016ba4c49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773457"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Dynamics 365 Supply Chain Management 10.0.6（2019 年 11 月）中的新增功能或更改

[!include [banner](../includes/banner.md)]

此主题介绍了 Microsoft Dynamics 365 Supply Chain Management 10.0.6 中的新增功能或更改的功能。 此版本的内部版本号为 10.0.234。 虽然公开发布日期在 11 月，新增功能在 10 月的提前版本中就已提供。 有关版本 10.0.6 的详细信息，请参阅[其他资源](whats-new-scm-10-0-6.md#additional-resources)。

## <a name="product-configuration-models-v2-data-entity"></a>产品配置模型 V2 data 数据实体

已发布了“产品配置模型”数据实体的第二个版本（称为“产品配置模型 V2”）。 还需要有默认模板“418 - 产品配置模型”，这样才能在导入/导出框架模板中使用新增的“产品配置模型 V2”数据实体。 不会自动更新此模板，所以您必须手动从默认位置加载该模板。 V2 实体将一行作为附件中的一个单独文件导出，而不是以内联方式导出，从而解决了 V1 实体的大小限制问题。 
 
若要采用此更新，需要执行什么操作？
-    因为 V1 实体已弃用，所以您应该从 V1 迁移到 V2。 如果您在使用“418 - 产品配置模型”模板，可以单击“加载默认模板”按钮并重新加载“418 – 产品配置模型”
-    如果您需要保持与现有系统兼容，您可以暂时继续使用现有模板和（已弃用的）V1 实体，直到将您的集成移到新模板。 

## <a name="feature-management-enhancements"></a>功能管理增强功能
功能管理现在允许默认启用所有新功能，要求执行功能确认和启用尚未启用的所有功能。 


## <a name="purchase-agreement-responsible-party"></a>采购协议负责方
现在可以在采购协议分类窗体和生成的采购协议中定义主负责方和副负责方。  这使用户可以访问协议的监督者。

## <a name="rfq-link-on-the-purchase-order-line"></a>采购订单行中的 RFQ 链接
可以将采购订单行中的引用链接添加回其对应的来源 RFQ 行，从而轻松地为用户提供询价单支持。

## <a name="additional-resources"></a>其他资源

### <a name="bug-fixes"></a>缺陷修复
有关 10.0.6 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7)。

### <a name="platform-update-30"></a>平台 update 30
Microsoft Dynamics 365 Supply Chain Management 10.0.6 中包含平台更新 30。 若要了解有关平台更新 30 的详细信息，请参阅[平台更新 30 中的新增功能或更改的功能](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md)。

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365：2019 发布波次 2 计划
是否对我们的任何商业应用或平台即将推出和最近发布的功能感兴趣？

查看 [Dynamics 365：2019 发布波次 2 计划](/dynamics365-release-plan/2019wave2/)。 一个文档汇总了所有端到端、上至下的详细信息，可用其进行规划。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>已删除和已弃用的 Supply Chain Management 功能

[Dynamics 365 Supply Chain Management 中中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)主题介绍 Supply Chain Management 中已经或计划删除或弃用的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

从该产品中删除任何功能之前 12 个月，将在 [Dynamics 365 Supply Chain Management中已删除或弃用的功能](removed-deprecated-features-scm-updates.md)主题中发布弃用通知。

对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常是需要对编译器进行的功能更新。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]