---
title: "项目上采购收货的成本应计"
description: "此主题描述从采购收货的成本应计项目如何在工序的 Microsoft Dynamics 365 中可跟踪。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>项目上采购收货的成本应计

此主题描述从采购收货的成本应计项目如何在工序的 Microsoft Dynamics 365 中可跟踪。 

项目的发票。货物和服务。通常迟到，可能影响项目关键绩效指标 (KPI) 中的重要影选项。 它跟踪重要可以在财务和项目报表的这些交易记录。

以下示例说明此方案。 

Contoso 咨询启动新的云部署项目。 创建采购订单采购项目的一台计算机上。 计算机将成本$1500，并且设置服务成本将$150。 供应商已和安装计算机上，发票，但尚未达到 Contoso 咨询。 在将发票发送前，项目经理要查看项目成本应计$1650。 在公司的月底财务报表还应反映此成本。 

应计成本在财务和项目级别级需要出于申报目的记录。 在工序的 Dynamics 365，产品收据的财务更新可用于跟踪和物料采购类别。 

对于物料，在** **应付帐款参数"页上，选中该**请过帐到会计**产品收据选项。
[] (![accruals1。/media/accruals1-1024x409.png)](。/media/accruals1.png) 

对于采购类别，在**类别策略规则**页，选择采购** **策略，为每个采购类别然后选择**应计采购收货的支出**。
[] (![accruals2。/media/accruals2-1024x569.png)](。/media/accruals2.png) 

**未开票的采购支出** **，并且应计采购** **将使用过帐设置**帐户，则与产品收据的凭证均已过帐。
[] (![accruals3。/media/accruals3-1024x429.png)](。/media/accruals3.png) 

使用此同一方案，我们查看过帐和产品收据将如何影响总帐和项目信息。 

**第 1 步：**创建并确认项目的新采购订单可以记录一计算机和$150 的设置服务的采购$1500 的。
[] (![accruals4。/media/accruals4-1024x497.png)](。/media/accruals4.png) 

在确认时，采购订单承诺成本的交易记录以用于项目已创建。 
[] (![accruals5。/media/accruals5-1024x219.png)](。/media/accruals5.png) 

> [!NOTE]
> 承诺成本的交易记录。有**交易记录来源**字段设置** **采购订单。 创建和确认采购订单不创建项目的交易记录。 

**第 2 步：**货物和服务而发送，并且产品收据登记。 

过帐和产品收据将生成和过帐一凭证到分类帐。 凭证采购、非支出将借记已开票帐户和赊购应计科目。 
[] (![accruals6。/media/accruals6-1024x214.png)](。/media/accruals6.png)

> [!NOTE]
> 过帐和产品收据为采购类别和产品将使用过帐设置项目，类别的而非过帐设置。 正确地反映采购应计项目的财务影响，此设置为要求进行调整。 

映射采购类别项目类别。** **采购类别是可能的页面。
[] (![accruals7。/media/accruals7-1024x390.png)](。/media/accruals7.png)

**第 3 步：**创建汇票供应商发票。 

在工序的 Dynamics 365，将不影响产品收据项目信息。 作为工作区，您可生成{{在：right_after}}过帐采购收货后的一张汇票供应商发票。 **到采购订单转到 &gt; ** **页面的发票选项卡** &gt; ** ** &gt; ** **则生成发票。 这将创建用于更新项目信息的未决发票单据。 

创建汇票供应商发票将生成未决项目交易记录。 
[] (![accruals8。/media/accruals8-1024x225.png)](。/media/accruals8.png) 

**在承诺成本**页，在步骤 1 创建的记录将关闭，并且新记录将创建未决反映来自供应商的发票的承诺成本。 **承诺成本的交易记录来源**字段将设置** **供应商发票。
[] (![accruals9。/media/accruals9-1024x200.png)](。/media/accruals9.png)

供应商发票上保留未决状态，直到实际供应商发票到达。


