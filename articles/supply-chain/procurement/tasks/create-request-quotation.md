---
title: 创建询价
description: 此过程向您说明如何创建询价。
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59202cb6678660ae035f9f76ebe4267bac01d78f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019896"
---
# <a name="create-a-request-for-quotation"></a>创建询价

[!include [banner](../../includes/banner.md)]

此过程向您说明如何创建询价。 这通常由采购代理完成。 您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。 在您开始之前，您需要设置申请类型。 一旦您完成此任务，并且您已创建和发送了询价，然后您可以输入每个供应商的回复，比较它们并授予合同。


## <a name="prepare-a-new-rfq"></a>准备新询价
1. 转到 **导航窗格 > 模块 > 采购 > 询价 > 所有询价**。
2. 单击 **新建**。
    提供以下采购类型：采购订单（这是默认值）：确认购买产品的优惠的文档，或对交换付款的产品销售的优惠的接受。 采购申请：如果您直接从采购申请创建一个询价，则此类型将自动选中。 如果您手动选择此选项，您将收到错误消息。 采购协议：一段时间内采购特定数量或特定价值产品的协议。 如果您选择此选项，则必须选择适用于采购协议的日期范围。  
3. 在 **文档标题** 字段中，键入一个值。
4. 在 **申请类型** 字段中，输入或选择一个值。
    + 如果计分方法与申请类型关联，这将是您创建的 RFQ 的默认计分方法。 以后可以更改计分方法。  
    + 在 **交货日期** 字段中，输入一个日期。  
    + 选择您要接收物料的最晚日期。  
    + 在 **到期日期和时间** 字段中，输入日期和时间。  
    + 指定供应商必须响应 RFQ 的日期和时间。  
5. 在 **仓库** 字段中，输入或选择一个值。 交货地址将默认为仓库地址。  
6. 单击 **确定**。

## <a name="add-lines"></a>添加多行

在 RFQ 中指定基本信息后，请指定希望供应商出价的货物或服务。 物料是默认的行类型。

1. 在 **物料编号** 字段中，输入或选择一个值。 如果您正在使用 USMF，可以选择 T0020。  
2. 在 **数量** 字段中，输入一个数字。
3. 单击 **添加行**。
4. 在 **行类型** 字段中选择“类别”。 您可以使用类别行类型类别创建非库存货物或服务的询价。 您将需要从采购类别层次结构中选择货物或服务的类型。  
5. 在 **采购类别** 字段中，输入或选择一个值。
6. 在 **产品名称** 字段中，键入一个值。
7. 在 **数量** 字段中，输入一个数字。
8. 在 **单位** 字段中，输入或选择一个值。

## <a name="add-vendors"></a>添加供应商
1. 单击 **标题** 将行视图更改为标题视图。 
2. 展开 **供货商** 部分。
3. 单击 **自动添加供应商**。 您可以基于请求物料的采购类别，自动添加供应商到 RFQ。 如果没有包括在行中的类别的通过审批的供应商，您可以手动添加供应商。  
4. 单击 **添加**。
5. 在 **供应商帐户** 字段中，输入或选择一个值。
6. 单击 **添加**。
7. 在 **供应商帐户** 字段中，输入或选择一个值。 一旦选择了供应商，状态将为“已创建”。 这意味着供应商信息已保存在询价中，但您尚未发送该询价给供应商。 无论供应商状态为何，您可以将供应商添加到询价。  

## <a name="send-the-rfq-to-vendors"></a>将 RFQ 发送给供应商
1. 在 **操作窗格** 上，单击 **发送**。 在发送询价页面，检查列表中的供应商是您要接收询价的供应商。  
2. 单击 **打印**。 此对话框允许您打印询价。 如果您选择打印回复表，此字段的内容在采购参数中定义。 若要选择如何打印回复表，在您开始打印对话框后，单击高级打印选项。 将为包含具有状态“已创建”或“已发送”的行的每个供应商打印一个询价。 已取消的行以及具有已登记回复的行将不打印。   
3. 单击 **取消**。
4. 单击 **确定**。
5. 关闭该页面。
6. 关闭该页面。

## <a name="view-the-rfq-journal"></a>查看询价日记帐。
1. 转到 **采购 > 询价 > 询价跟进 > 报价单日记帐**。
2. 单击 **预览/打印**。
3. 单击 **原件预览**。
4. 关闭该页面。
5. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]