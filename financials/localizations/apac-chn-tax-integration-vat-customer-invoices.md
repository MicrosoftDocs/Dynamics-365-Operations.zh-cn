---
title: "(CHN) 中文增值税客户发票的税务集成 FAQ 修改"
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

# <a name="chn-chinese-tax-integration-modification-for-vat-customer-invoices-faq"></a>(CHN) 中文增值税客户发票的税务集成 FAQ 修改

您可以生成增值税 (VAT) 客户发票，然后以文本文件导出。 接下来，您可以导入可与原始发票关联的增值税客户发票的参考编号。

在导出增值税客户发票前，您可以拆分增值税客户发票以创建多个发票单据。 您还可以合并多个增值税客户发票，以创建一个包含原始发票行明细的发票导出单据。

## <a name="what-is-a-vat-customer-invoice"></a>增值税客户发票是什么？
当您过帐使用了增值税的销售税组和物料销售税组的客户交易时，则需要生成增值税客户发票。 可以生成从销售订单、退货订单、销售贷方通知单、普通发票或销售发票。项目的增值税客户发票。

## <a name="can-i-create-one-tax-integration-profile-for-multiple-types-of-documents"></a>我是否可以创建一个用于多种类型单据的纳税集成模板？

是。 您可以创建一个用于多种类型单据的纳税集成模板。

## <a name="when-should-i-split-a-vat-customer-invoice"></a>我该何时拆分增值税客户发票？
应增值税客户发票，拆分如果**在金额限制**复选框。**增值税发票金税集成**选择页。 **该金额在限制**选项可用于具有发票总金额超过您在的发票选择** **发票金额"字段中指定在税务集成模板** **页。

## <a name="which-vat-customer-invoices-can-i-combine"></a>我可以合并哪些增值税客户发票？
您可以合并使用相同发票帐户和销售税代码的增值税客户发票。

## <a name="how-many-times-can-i-export-an-invoice"></a>我可以导出发票多少次？
只能一次导出发票。

## <a name="can-i-customize-or-add-new-information-on-vat-customer-invoices"></a>我自定义或可以添加有关增值税客户发票的新信息？
是。 您可以通过添加其他字段对增值税客户发票自定义，然后以文本文件导出增值税客户发票。

若要自定义增值税客户发票与包括其他详细信息，请执行以下步骤：

-   **在电子国家/地区报告** "页上，选中**报告 Configuration ** **打开配置** **和选择金黄税 (CN) **树中。
-   单击“设计器”****。 树添加下**导出的发票** **发票的 &gt; 其他字段中，热镇**并保存模型。
-   **映射到模型单击"数据源** **和选择金黄税** &gt; ** **设计器。

若要表添加到表的字段，请执行以下步骤：
1.  **单击，并且保存**退货到** **配置。
2.  **选择 GoldenTax (CN) **树中。
3.  **单击"更改状态** &gt; **请完成**获取模型的新版本。
4.  **展开 GoldenTax (CN) **树中。
5.  **选择 GoldenTax (CN) **在树的格式。
6.  **单击 Rebase **。 确认目标版本是新的版本已完成。
7.  **单击"完成 rebase **流程。
8.  **格式打开设计器**单击"设计器"。
9.  在树形格式设计器，添加的新字段当前在文本文件。
10. 选择新毛利的字段，然后单击在右窗格的映射** **选项卡。
11. 展开树中的模型。
12. 选择新的添加的模型字段并单击**绑定**。
13. **保存格式映射**单击"保存。
14. **单击"更改状态** &gt; **请完成**获取新版本。



<a name="see-also"></a>请参阅
--------

[Configure tax integration for China](apac-chn-tax-integration.md)

[Import the Chinese Golden Tax data entity](apac-chn-import-golden-tax-data-entity.md)


