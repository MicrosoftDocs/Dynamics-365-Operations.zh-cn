---
title: "(CHN) 增值税客户发票的中国税务集成修改常见问题"
description: "您可以生成增值税 (VAT) 客户发票，然后以文本文件导出。 接下来，您可以导入可与原始发票关联的增值税客户发票的参考编号。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264894
ms.assetid: 9d255220-9a19-4436-87a6-f78d92c02062
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f7fd20ef0c78bc781f0ef9f17fc612723906ac78
ms.openlocfilehash: f14d5ca33ca5baa1a3bd08f2c2565ca1f4388f61
ms.lasthandoff: 03/31/2017


---

# <a name="chn-chinese-tax-integration-modification-for-vat-customer-invoices-faq"></a>(CHN) 增值税客户发票的中国税务集成修改常见问题

[!include[banner](../includes/banner.md)]


您可以生成增值税 (VAT) 客户发票，然后以文本文件导出。 接下来，您可以导入可与原始发票关联的增值税客户发票的参考编号。

在导出增值税客户发票前，您可以拆分增值税客户发票以创建多个发票单据。 您还可以合并多个增值税客户发票，以创建一个包含原始发票行明细的发票导出单据。

## <a name="what-is-a-vat-customer-invoice"></a>增值税客户发票是什么？
当您过帐使用了增值税的销售税组和物料销售税组的客户交易时，则需要生成增值税客户发票。 您可以通过销售订单、退货销售订单、普通发票、贷方通知单或项目销售发票创建增值税款客户发票。

## <a name="can-i-create-one-tax-integration-profile-for-multiple-types-of-documents"></a>我是否可以创建一个用于多种类型单据的纳税集成模板？

是。 您可以创建一个用于多种类型单据的纳税集成模板。

## <a name="when-should-i-split-a-vat-customer-invoice"></a>我该何时拆分增值税客户发票？
如果在**增值税发票集成**页中选中了**超过最大发票金额**复选框，则您应该拆分增值税客户发票。 **超过最大发票金额**选项是为了发票总金额超过您在**最大发票金额**字段（位于**税务集成模板**页中）中指定的金额限制的发票选择的。

## <a name="which-vat-customer-invoices-can-i-combine"></a>我可以合并哪些增值税客户发票？
您可以合并使用相同发票帐户和销售税代码的增值税客户发票。

## <a name="how-many-times-can-i-export-an-invoice"></a>我可以导出发票多少次？
一次只能导出一张发票。

## <a name="can-i-customize-or-add-new-information-on-vat-customer-invoices"></a>我是否可以在增值税客户发票中自定义或添加新信息？
是。 您可以通过添加其他字段对增值税客户发票自定义，然后以文本文件导出增值税客户发票。

若要自定义增值税客户发票，使其包括其他详细信息，请执行以下步骤：

-   在**电子申报**页中，选择**申报配置**以打开**配置**，然后选择树结构中的**金税(CN)**。
-   单击“设计器”****。 在树结构中的**导出的发票** &gt; **发票**下添加其他字段，然后保存 GER 模型。
-   单击**将模型映射到数据源**，然后选择**金税** &gt; **设计器**。

若要将添加的字段映射到表，请执行以下步骤：
1.  单击**保存**并返回到**配置**。
2.  在树结构中，选择**金税(CN)**。
3.  单击**更改状态** &gt; **完成**以获取模型的新版本。
4.  在树结构中，展开**金税(CN)**。
5.  在树结构中，选择**金税(CN)** 格式。
6.  单击**重定基本值**。 确认目标版本是新完成的版本。
7.  单击**确定**完成重定基本值过程。
8.  单击**设计器**打开格式设计器。
9.  在格式设计器中，在树结构中添加文本文件表示的新字段。
10. 选择新添加的字段，然后单击右窗格中的**映射**选项卡。
11. 在树结构中展开该模型。
12. 选择新添加的模型字段，然后单击**绑定**。
13. 单击**保存**以保存格式映射。
14. 单击**更改状态** &gt; **完成**以获取新版本。



<a name="see-also"></a>请参阅
--------

[配置中国的税务集成](apac-chn-tax-integration.md)

[导入中国金税数据实体](apac-chn-import-golden-tax-data-entity.md)




