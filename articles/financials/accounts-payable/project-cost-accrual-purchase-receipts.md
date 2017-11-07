---
title: "采购收据中的应计项目成本"
description: "此主题介绍如何在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中跟踪采购收据内的应计项目成本。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ba4eedb9895feda6b8c664654f30d0bd0a3a172a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="project-cost-accrual-on-purchase-receipts"></a>采购收据中的应计项目成本

[!include[banner](../includes/banner.md)]


此主题介绍如何在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中跟踪采购收据内的应计项目成本。 

项目的发票通常比货物和服务的交付时间晚，这可能对项目关键绩效指标 (KPI) 造成极大影响。 在财务报表和产品报表中跟踪这些交易记录的能力至关重要。

以下示例方案对此进行了说明。 

Contoso Consulting 已启动了一个新的云部署项目。 创建了采购订单，以便为该项目购买一台计算机。 该计算机成本为 1500 美元，安装服务为 150 美元。 供应商已交货并安装了计算机，但是 Contoso Consulting 尚未收到发票。 项目经理希望在收到发票前看到 1650 美元的应计项目成本。 应在公司的月底财务报表中体现此成本。 

需要同时在财务级和项目级为申报目的记录这笔应计成本。 在 Finance and Operations 中，可以为物料和采购类别跟踪产品收据的财务更新。 

对于物料，请在**应付账款参数**页面中选择**将产品收据过帐到分类帐**选项。
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

对于采购类别，请在**目录策略规则**页面中选择**采购**策略，然后为各采购类别选择**接收后的应计采购支出**。
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

过帐与产品收据有关的凭证时，将使用**过帐设置**中的**采购支出，未开具发票**和**采购应计**科目。
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

我们同样使用这个方案查看过帐产品收据对总帐和项目信息有何影响。 

**步骤 1：**为项目创建一个新采购订单并确认，以便记录采购费用为 1500 美元，安装服务费为 150 美元的一台计算机的购买。
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

确认了采购订单之后，将为该项目创建承诺成本的交易记录。 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> 承诺成本的交易记录的**交易记录来源**字段设置为**采购订单**。 创建并确认采购订单不会为项目创建交易记录。 

**步骤 2：**交付货物和服务，并登记产品收据。 

过帐产品收据将生成凭证并过帐到分类帐。 凭证将把采购支出、未开票的科目和应计科目记入借方。 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> 过帐产品收据将使用采购类别和产品的过帐设置，而不是项目类别的过帐设置。 需要调整此设置，才能正确体现对采购应计的财务影响。 

可以在**采购类别**页面中将采购类别映射到项目类别。
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**步骤 3：**创建供应商形式发票。 

在 Finance and Operations 中，过帐产品收据不影响项目信息。 解决方案是，过帐采购收据后立即生成供应商形式发票。 转至**采购订单**页面 &gt; **发票**选项卡 &gt; **生成** &gt; **发票**。 这将创建一张待定发票单据，用于更新项目信息。 

创建供应商形式发票将生成挂起项目交易记录。 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

在**承诺成本**页面中，将关闭步骤 1 中创建的记录，并创建新记录以体现待定供应商发票产生的成本承诺。 承诺成本的**交易记录来源**字段将设置为**供应商发票**。
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

实际供应商发票到达前，此供应商发票将保持待定状态。




