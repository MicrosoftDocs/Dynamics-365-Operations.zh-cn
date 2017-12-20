---
title: "从目标客户到现金"
description: "本主题提供在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 与 Microsoft Dynamics 365 for Sales 之间从目标客户到现金解决方案的概述。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: zh-cn
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a>从目标客户到现金

[!include[banner](../includes/banner.md)]

从目标客户到现金解决方案提供跨 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 与 Microsoft Dynamics 365 for Sales 的直接同步。 提供“数据集成”功能的“从目标客户到现金”模板启用 Finance and Operations 与 Sales 之间的帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。 当数据在 Finance and Operations 与 Sales 之间流动时，您可以在 Sales 中执行销售和市场营销活动，并可以使用 Finance and Operations 中的库存管理处理订单履行。

在当前版本中，从目标客户到现金解决方案提供以下类型的直接同步：

- [维护 Sales 中的帐户并将它们直接从 Sales 同步到 Finance and Operations](accounts-template-mapping-direct.md)
- [维护 Finance and Operations 中的产品并将它们直接同步到 Sales](products-template-mapping-direct.md)
- [在 Sales 中维护联系人并将它们直接同步到 Finance and Operations 的联系人或客户](contacts-template-mapping-direct.md)
- [将 Sales 中的销售报价单直接同步到 Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [将 Finance and Operations 中的销售订单直接同步到 Sales](sales-order-template-mapping-direct.md)
- [将 Sales 与 Finance and Operations 的销售订单直接同步](sales-order-template-mapping-direct-two-ways.md)
- [将 Finance and Operations 中的销售发票直接同步到 Sales](sales-invoice-template-mapping-direct.md)

在早期版本中，从目标客户到现金解决方案提供以下类型的非直接同步：

- [维护 Sales 中的帐户并将它们同步到 Finance and Operations](accounts-template-mapping.md)
- [维护 Sales 中的联系人并将它们同步到 Finance and Operations](contacts-template-mapping.md)
- [维护 Finance and Operations 中的产品并将它们同步到 Sales](products-template-mapping.md)
- [在 Sales 中创建销售报价并将它们同步到 Finance and Operations](sales-quotation-template-mapping.md)
- [在 Finance and Operations 中创建销售订单并将它们同步到 Sales](sales-order-template-mapping.md)
- [在 Finance and Operations 中创建发票并将它们同步到 Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations 的系统要求

若要使用从目标客户到现金解决方案，必须安装以下组件：

### <a name="july-2017"></a>2017 年 7 月 

- 具有平台更新 8（使用平台版本 7.0.4565.16212 的应用程序版本 7.2.11792.56024）的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）
- 以下 Finance and Operations 修补程序：

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – 此修补程序可以通过数据集成功能将销售订单从 Sales 同步到 Finance and Operations。 它还提供多个其他增强。
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – 此修补程序可以通过数据集成功能将销售订单行从 Finance and Operations 同步到 Sales。
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – 此修补程序可以通过数据集成功能将销售订单从 Finance and Operations 同步到 Sales。

    > [!NOTE]
    > 您只需安装 KB4045570，该安装包括来自其他 Microsoft 知识库 (KB) 文章的更改。

### <a name="november-2016-version-1611"></a>2016 年 11 月（版本 1611）

- 具有平台更新 8 或更高版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2016 年 11 月）

- 以下 Finance and Operations 修补程序：

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - 使用数据集成器将销售订单从 Microsoft Dynamics 365 for Finance and Operations 同步到 Sales 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - 使用数据集成器将销售订单标头和行从 Microsoft Dynamics 365 for Finance and Operations 同步到 Sales
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - 需要支持通过数据实体进行从目标客户到现金的集成
    
    > [!NOTE]
    > 安装修补程序后，您必须从 SalesPopulateProspectToCash 触发以下批处理作业。 因为只需要一次，因此此窗体会隐藏。 若要访问此窗体，请在登录到环境后将以下信息添加到您的浏览器地址：&mi=action:SalesPopulateProspectToCash E.g. https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash 在打开的窗体中单击“确定”。
    这将在“SalesLine”、“SalesQuotationLine”和“CustInvoiceTrans”表中使用唯一值填充新的“LineCreationSequnceNumber”字段，并刷新产品列表。 若要让 P2C 集成在 7.1 上运行则需要此设置


## <a name="system-requirements-for-sales"></a>Sales 的系统要求

若要使用从目标客户到现金解决方案，必须安装以下组件：

- Microsoft Dynamics 365 for Sales 版本 1612 (8.2.1.207) (DB 8.2.1.207) 联机
- Microsoft Dynamics 365 for Sales 版本 1.15.0.0 (v15) 的从目标客户到现金解决方案 

   > [!NOTE]
   >
   > 具有版本 1.0.0.0 和 1.0.0.1 的模板在 Microsoft Dynamics 365 for Sales 版本 1.14.1.0 的从目标客户到现金解决方案上受支持
   >
   > 具有版本 2.0.0.0 和 2.1.0.0 的模板在 Microsoft Dynamics 365 for Sales 版本 1.15.0.0 的从目标客户到现金解决方案上受支持

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>安装用于 Sales 的从目标客户到现金解决方案

1. 从 CustomerSource 下载[用于 Dynamics 365 for Sales 的从目标客户到现金解决方案包 zip 文件](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash)。
2. 确保 zip 文件是否未锁定。 否则，在尝试安装解决方案包时，您将收到以下错误消息：“找不到导入包”。 若要解锁 zip 文件，右键单击文件，然后选择**属性**。 然后选择**解锁**。
3. 解压缩和运行 **PackageDeployer.exe**。
4. 在 Sales 实例中安装从目标客户到现金解决方案：

    1. 选择 **Office 365** 作为部署类型。
    2. 选择**显示高级**。
    3. 对于快速安装，请选择一个区域。 如果您选择**不知道**，系统将搜索所有区域并且安装需要更长时间。
    4. 输入具有安装权限的管理员用户的用户名和密码。

