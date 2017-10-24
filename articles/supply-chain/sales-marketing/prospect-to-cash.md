---
title: "从目标客户到现金"
description: "本主题提供在 Dynamics 365 for Finance and Operations Enterprise Edition 与 Dynamics 365 for Sales 之间从目标客户到现金解决方案的概述。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a>从目标客户到现金  

[!include[banner](../includes/banner.md)]

从目标客户到现金解决方案使用[数据集成](/common-data-service/entity-reference/dynamics-365-integration) 通过 Common Data Service 跨 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 和 Dynamics 365 for Sales 实例同步数据。 提供数据集成功能的从目标客户到现金模板启用 Finance and Operations 与 Sales 之间的帐户、联系人、产品、销售报价、销售订单和销售发票数据流。 当数据在 Finance and Operations 与 Sales 之间流动时，您可以在 Sales 中执行销售和市场营销活动以及使用 Finance and Operations 中的库存管理处理订单履行。 

此解决方案提供在以下区域的集成： 

-   [维护 Sales 中的帐户并将它们同步到 Finance and Operations](accounts-template-mapping.md)
-   [维护 Sales 中的联系人并将它们同步到 Finance and Operations](contacts-template-mapping.md)
-   [维护 Finance and Operations 中的产品并将它们同步到 Sales](products-template-mapping.md)
-   [在 Sales 中创建销售报价并将它们同步到 Finance and Operations](sales-quotation-template-mapping.md)
-   [在 Finance and Operations 中创建销售订单并将它们同步到 Sales](sales-order-template-mapping.md)
-   [在 Finance and Operations 中创建发票并将它们同步到 Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Dynamics 365 for Finance and Operations Enterprise Edition 的系统要求

若要使用从目标客户到现金解决方案，必须进行以下安装：

- 具有平台更新 8（使用平台 7.0.4565.16212 的应用 7.2.11792.56024）的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）

- Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）的两个修补程序。

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - 此修补程序可以通过数据集成功能将销售订单行从 Finance and Operations 同步到 Sales。
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - 此修补程序可以通过数据集成功能将销售订单从 Finance and Operations 同步到 Sales。
    
**注意**：您只需安装 KB4036524，该安装包括来自 KB4036461 的更改。
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Dynamics 365 for Sales 的系统要求

若要使用从目标客户到现金解决方案，必须进行以下安装：

- Dynamics 365 for Sales 版本 1612 (8.2.1.207) (DB 8.2.1.207) 联机或更高版本。
- Dynamics 365 for Sales 版本 1.14.0.0 (v14) 或更高版本的从目标客户到现金解决方案。

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>安装用于 Sales 的从目标客户到现金解决方案

- 在 CustomerSource 上下载[用于 Dynamics 365 for Sales 的从目标客户到现金解决方案包 zip 文件](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash)。

- 确保 zip 文件未锁定，否则当您安装解决方案包时会收到错误消息“找不到导入包”。 要解锁文件，请执行以下操作：

    -  右键单击 zip 文件。
    -  选择**属性**，然后选择**解锁**。 

- 解压缩和运行 PackageDeployer.exe。

- 在 Sales 实例中安装从目标客户到现金解决方案。

    - 选择 **Office 365** 部署类型。
    - 选择**显示高级**。
    - 对于快速安装，请选择**区域**。 如果您选择**不知道**，系统将搜索所有区域并且需要更长的安装时间。
    - 输入具有安装用户权限的管理员用户的**用户名**和**密码**。

