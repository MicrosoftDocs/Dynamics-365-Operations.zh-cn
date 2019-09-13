---
title: 过帐联机销售和付款
description: 此程序会逐步演示如何配置和运行某一重复批处理作业，以创建针对在线商店交易的销售订单和付款。
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d42b585a61214628980cd45a859215443ed55b5
ms.sourcegitcommit: c461758290d7ddc19f0b60701368937c35ef78b0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864145"
---
# <a name="posting-of-online-sales-and-payments"></a>过帐联机销售和付款

[!include[task guide banner](../includes/task-guide-banner.md)]

此程序会逐步演示如何配置和运行某一重复批处理作业，以创建针对在线商店交易的销售订单和付款。

过帐联机销售和付款是包含两个阶段的流程。

- 提取 HQ 的在线零售交易记录数据。
- 同步订单以在 HQ 创建销售订单。

可以通过运行 P 作业或通过创建重复执行批处理作业提取在线零售交易记录数据。

### <a name="manually-running-the-p-job"></a>手动运行 P 作业

1. 转至“所有工作区”>“零售 IT”。
2. 单击“配送计划”。
3. 选择 P-0001。
4. 如果需要，调整渠道数据库组。
5. 单击立即运行。
6. 单击“是”。

### <a name="scheduling-a-recurring-p-job"></a>为重复执行的 P 作业排产

1. 转至“所有工作区”>“零售 IT”。
2. 单击“配送计划”。
3. 选择 P-0001。
4. 单击“创建批处理作业”。
5. 单击“在后台运行”。
5. 启用“批处理”。
6. 单击“重复执行”。
7. 选择“无结束日期”选项。
8. 在“计数”字段中，输入运行之间以分钟为单位的时间间隔。 通常为 5-10。
9. 单击“确定”。
10. 单击“确定”。

可以通过运行“同步订单”作业或创建重复执行批处理作业同步订单。

### <a name="manually-running-order-synchronization"></a>手动运行订单同步 

执行以下步骤，以便手动运行一次“同步订单”作业。

1. 转至“所有工作区”>“零售商店财务”。
2. 单击“同步订单”。
3. 在“组织层次结构”字段中，选择“零售商店(按地区)”。
    * 选择一个特定在线商店，如果您想要为一组商店创建批处理作业，则选择一个节点。  
    * 单击箭头以添加您的选择。  
4. 单击“后台运行”选项卡。
5. 禁用“批处理”
6. 单击“重复执行”。
7. 选择“结束日期”选项
8. 在“结束日期”字段中，输入 1。
9. 单击“确定”。
10. 单击“确定”。

### <a name="scheduling-recurring-order-synchronization"></a>计划重复执行的订单同步

此程序会逐步演示如何配置和运行某一重复批处理作业，以创建针对在线商店交易的销售订单和付款。 此程序使用 USRT 演示数据公司。

1. 转至“所有工作区”>“零售商店财务”。
2. 单击“同步订单”。
3. 在“组织层次结构”字段中，选择“零售商店(按地区)”。
    * 选择一个特定在线商店，如果您想要为一组商店创建批处理作业，则选择一个节点。  
    * 单击箭头以添加您的选择。  
4. 单击“后台运行”选项卡。
5. 启用“批处理”
6. 单击“重复执行”。
7. 选择“无结束日期”选项。
8. 在“计数”字段中，输入运行之间以分钟为单位的时间间隔。 通常为 2-20
9. 单击“确定”。
10. 单击“确定”。

## <a name="data-entities-involved-in-the-process"></a>此流程中涉及的数据实体

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans
