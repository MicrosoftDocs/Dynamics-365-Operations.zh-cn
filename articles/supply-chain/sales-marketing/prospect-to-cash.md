---
title: 从目标客户到现金
description: 本主题提供在 Dynamics 365 Supply Chain Management 与 Dynamics 365 Sales 之间从目标客户到现金解决方案的概述。
author: ChristianRytt
manager: tfehr
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: b2f2f7d95d3f0e6bd774c43024836aac1f729abd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977630"
---
# <a name="prospect-to-cash"></a>现金的目标客户

[!include [banner](../includes/banner.md)]

从目标客户到现金解决方案提供跨 Dynamics 365 Supply Chain Management 与 Dynamics 365 Sales 的直接同步。 提供“数据集成”功能的“从目标客户到现金”模板启用帐户、联系人、产品、销售报价、销售订单和销售发票的数据流。 当数据流动时，您可以在 Sales 中执行销售和市场营销活动，并可以使用 Supply Chain Management 中的库存管理处理订单履行。 

有关“从目标客户到现金”集成的详细信息，请观看下面的 YouTube 短视频：[目标客户到现金集成](https://www.youtube.com/watch?v=AVV9x5x-XCg)。

在当前版本中，从目标客户到现金解决方案提供以下类型的直接同步：

- [将 Sales 的客户直接同步到 Supply Chain Management 中的客户](accounts-template-mapping-direct.md)
- [将 Supply Chain Management 的产品直接同步到 Sales](products-template-mapping-direct.md)
- [将 Sales 的联系人直接同步到 Supply Chain Management 中的联系人或客户](contacts-template-mapping-direct.md)
- [将 Sales 的销售报价单标题和行直接同步到 Supply Chain Management](sales-quotation-template-mapping-sales-fin.md)
- [直接在 Sales 和 Supply Chain Management 之间同步销售订单](sales-order-template-mapping-direct-two-ways.md)
- [将 Sales 的销售发票头和行直接从 Supply Chain Management 同步到 Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a>Supply Chain Management 的系统要求
以下版本支持“从目标客户到现金”集成：

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations Enterprise edition 7.3（2017 年 12 月）

- Dynamics 365 for Finance and Operations Enterprise edition（2017 年 12 月）- 具有平台更新 12 的应用程序版本 7.3.11971.56116 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations Enterprise edition（2017 年 7 月）

- Dynamics 365 for Finance and Operations Enterprise edition（2017 年 7 月）- 具有平台更新 8（具有平台版本 7.0.4565.16212 的应用程序版本 7.2.11792.56024）。
- 必须包含以下修补程序：

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – 此修补程序可以通过数据集成功能将销售订单从 Sales 同步到 Supply Chain Management。 它还提供多个其他增强。
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – 此修补程序可以通过数据集成功能将销售订单行从 Supply Chain Management 同步到 Sales。
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – 此修补程序可以通过数据集成功能将销售订单从 Supply Chain Management 同步到 Sales。

    > [!NOTE]
    > 您只需安装 KB4045570，因为该安装包括来自其他修补程序的更改。 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations 版本 1611（2016 年 11 月）

- 具有平台更新 8 或更高版本的 Dynamics 365 for Finance and Operations 版本 1611（2016 年 11 月）

- 必须包含以下修补程序：

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - 使用数据集成器将销售订单从 Supply Chain Management 同步到 Sales。 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - 使用数据集成器将销售订单头和行从 Supply Chain Management 同步到 Sales。
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - 需要支持通过数据实体进行从目标客户到现金的集成。
    
    > [!NOTE]
    > 安装修补程序后，您必须从 **SalesPopulateProspectToCash** 窗体触发以下批处理作业。 因为只需要一次，因此此窗体会隐藏。 若要访问此窗体，请登录环境，然后将以下信息添加到您的浏览器地址中的 URL：*&mi=action:SalesPopulateProspectToCash*，例如，`https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`。 打开窗体后，单击“确定”。 这将在 **SalesLine**、**SalesQuotationLine** 和 **CustInvoiceTrans** 表中使用唯一值填充新的 **LineCreationSequnceNumber** 字段，并刷新产品列表。 这是执行从目标客户到现金的集成所必需的。


## <a name="system-requirements-for-sales"></a>Sales 的系统要求

若要使用从目标客户到现金解决方案，必须安装以下组件：

- Dynamics 365 Sales 版本 1612 (8.2.1.207) (DB 8.2.1.207) online 或更高版本
- Dynamics 365 Sales 版本 1.15.0.0 或更高版本的从目标客户到现金解决方案。 可从 AppSource 下载此解决方案。 [下载 Dynamics 365 从目标客户到现金](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]