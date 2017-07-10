---
title: "库存锁定"
description: "本文提供库存锁定的概览，这是 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中质量检查流程的一部分。 您可以使用库存锁定来阻止处理或消耗物料。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: 4c5ebea58630188615fb4c22cc9da5215461e513
ms.contentlocale: zh-cn
ms.lasthandoff: 06/13/2017


---

# <a name="inventory-blocking"></a>库存锁定

[!include[banner](../includes/banner.md)]


本文提供库存锁定的概览，这是 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中质量检查流程的一部分。 您可以使用库存锁定来阻止处理或消耗物料。

您可以按照以下方法锁定库存物料：
-   手动
-   通过创建质量订单
-   通过使用生成质量订单的流程
-   使用库存状态锁定

## <a name="blocking-items-manually"></a>手动锁定物料
您可以通过在**库存锁定**页中创建交易记录来锁定物料的数量。 只有作为现有库存可用的物料可以被手动锁定。 对于手动锁定的数量，您必须决定计划活动是否作为预期的现有数量包括预期收货。 预期收货锁定您希望在检查完成后作为现有库存可用的物料。 您可以维护预期日期。 默认情况下，**预期收货**选项为通过质检订单锁定的物料选中。 您可以通过删除**库存锁定**页中的交易记录取消数量的手动锁定。

## <a name="blocking-items-by-creating-a-quality-order"></a>通过创建质检订单锁定物料
您可以通过在**质检订单**页上创建质检订单来指定必须检查的物料。 当您创建一个质量订单时，将锁定您为物料指定的数量。 与质检订单控制关联的抽样计划只控制必须检查的物料的数量，而不控制被锁定的数量。 在质检订单上输入的数量是已锁定的数量，不管抽样计划指定的数量是否应发送供检查。

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>通过使用生成质检订单流程锁定物料
如果质量流程指定必须检查物料，则物料数量将被自动锁定。 因此，当自动生成质检订单时，与该质检订单相关联的物料抽样计划同时控制锁定的物料的数量和必须检查的数量。 如果选择了**物料抽样**页中的**完全锁定**选项，则不管物料抽样数量，在检查期间锁定采购订单行等的整个数量。
### <a name="example"></a>示例

在以下的示例中，过账采购订单的装箱单时生成了一个质量订单。 在**质量关联**页中，您指定了采购订单装箱单的过帐为激活质量订单的流程。

|设置                                                                     |用户操作                 |结果             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| 质量关联指定在采购订单装箱单过帐时必须生成质检订单。 质检订单的物料抽样设置指定必须检查 10% 的采购订单行数量。 此外，由于在物料抽样设置中选择了**完全锁定**选项，因此不管发送以供检查的数量，在检查期间必须锁定采购订单行的整个数量。 | 过账装箱单。 | 生成质量订单。 将物料的 10% 的采购订单数量送检。 锁定该采购订单行的整个数量。 |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>通过使用库存状态锁定锁定物料
您可以使用**库存状态**页上的**锁定库存**参数指定哪些库存状态是锁定状态。 您不能使用库存状态作为生产订单、销售订单、转移单、传出交易记录或项目集成的锁定状态。 对于出货工作，使用具有个可用库存状态的物料。 如果物料具有**中断**状态，并且主计划在这些物料上运行，则将物料视为缺失，库存会自动补货。



<a name="see-also"></a>请参阅
--------

[创建和维护库存锁定（任务指南）](https://ax.help.dynamics.com/en/wiki/create-and-maintain-an-inventory-blocking/)

[质量管理流程](quality-management-processes.md)

[检查货物的质量（任务指南）](https://ax.help.dynamics.com/en/wiki/inspect-the-quality-of-goods/)




