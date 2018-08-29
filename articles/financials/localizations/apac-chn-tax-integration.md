---
title: "配置中国的税务集成"
description: "本主题描述配置中国的税务集成的流程。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters, VATInvoiceDescTable_CN, TaxProfileTable_CN
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265264
ms.assetid: e5dbbbe1-935f-4fb4-a014-447916051628
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7f5a0049c1d32ab29ac8602bf32e9973eb923ce2
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---

# <a name="configure-tax-integration-for-china"></a>配置中国的税务集成

[!include [banner](../includes/banner.md)]

本主题描述配置中国的税务集成的流程。

## <a name="prerequisite"></a>必备项
必须先通过为**应收科目参数**页面（**应收帐款** > **设置** > **应收帐款参数** > **分类帐和销售税** > **常规**选项卡）中的**与税务系统集成**选项选择**是**启用税务集成，才能配置税务集成。

若要配置中国的税务集成，请完成以下任务。

1.  在**增值税发票描述**页中新建一个增值税发票描述。 例如，可能需要设置以下参数：
    -   将**增值税发票描述 ID** 设置为 InvoiceDescID01
    -   将**描述**设置为“详见销售清单”
    -   将**单位**设置为“箱子”

2.  在**税务集成模板**页中创建一个新税务集成模板。 可以设置导入或导出发票时使用的税务集成模板。 在税务集成模板中，可以指定以下信息：
    -   增值税代码
    -   最大发票金额
    -   金税发票的默认描述和单位
    -   是否包含普通增值税发票

下图是税务集成流程的示例。
[![IC666469](./media/ic666469.gif)](./media/ic666469.gif)

## <a name="additional-resources"></a>其他资源

- [导入中国金税数据实体](apac-chn-import-golden-tax-data-entity.md)

- [增值税客户发票的中国税务集成修改常见问题](apac-chn-tax-integration-vat-customer-invoices.md)

- [设置中国的基本税务集成](./tasks/set-up-basic-tax-integration-profile-china.md)



