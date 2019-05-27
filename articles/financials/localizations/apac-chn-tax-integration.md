---
title: 配置中国的税务集成
description: 本主题描述配置中国的税务集成的流程。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
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
ms.openlocfilehash: f2aa323eaf5552acd4aec17145f4c95d4a335688
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538420"
---
# <a name="configure-tax-integration-for-china"></a>配置中国的税务集成

[!include [banner](../includes/banner.md)]

本主题描述配置中国的税务集成的流程。

## <a name="prerequisites-for-finance-and-operations-version-100-and-later"></a>Finance and Operations 版本 10.0 及更高版本的先决条件

要让系统生成此代码以充当导出的文件中的输出，必须按照以下任务的列出顺序完成这些任务。

| 必备项 | 说明 | 更多信息 |
|------------|-------------|------------------------|
| 设置产品分类的层次结构。 | 必须为货物和服务的分配设置类别层次结构，还必须将产品物料（货物或服务）与类别节点关联。 通过使用此功能，可以设置公司中需要的所有层次结构。 | [创建产品分类的层次结构](../../supply-chain/pim/tasks/create-hierarchy-product-classification.md) |
| 为税务集成模板分配新层次结构。 | 转到**应收帐款 &gt; 税务集成 &gt; 税务集成模板**，然后在**商品代码层次结构**字段中选择新类别。 | |
| 选择发票行的商品代码。 | 对于与产品物料无关的发票行（如普通发票行和项目发票行），或基于工时、支出和费用日记帐创建的发票行，可在**税务集成模板**页面中设置默认商品代码。 | |
| 标识用于导入文件的模型映射。 | 转到**应收帐款 &gt; 定期任务 &gt; 增值税发票金税集成**，然后选择**导入**。 为来自其中一个提供商（Aisino 或 BaiWang）的导入文件选择模型映射，具体取决于公司将导出的发票与哪个提供商的软件集成。 此项选择应仅进行一次。 （系统将保存选择的值。）<ul><li>若要导入文本文件（\<file name\>\_invoicing result.TXT），请将**导入 BaiWang TXT 文件**选项设置为**是**。 然后，在**模型映射**字段中，选择 **BaiWang – txt 文件映射**。</li><li>要导入来自 Aisino 的文本文件或来自 BaiWang 的 XML 文件（从 BaiWang 软件导出的文件），请将**导入 BaiWang txt 文件**选项设置为**否**。 然后，在**模型映射**字段中，选择 **Aisino 或 BaiWang – xml 文件映射**。</li></ul> | |
| 从 Microsoft Dynamics Lifecycle Services (LCS) 导入配置。 | 对于与 Aisino 软件的集成，必须从 LCS 导入以下配置：<ul><li>GoldenTax 模型</li><li>GST 导出模型映射 (CN)</li><li>GTS 导出格式 (Aisino) (CN)</li><li>GTS 导入模型映射 (CN)</li><li>GTS 导入格式 (Aisino) (CN)</li></ul>对于与 BaiWang 软件的集成，必须从 LCS 导入以下配置：<ul><li>GoldenTax 模型</li><li>GST 导出模型映射 (CN)</li><li>GTS 导入模型映射 (CN)</li><li>GTS 导出格式 (BaiWang) (CN)</li><li>GTS 导入格式 (BaiWang)-txt) (CN)</li><li>GTS 导入格式 (BaiWang)-xml) (CN)</li></ul> | [从 Lifecycle Services 下载电子申报配置](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) |

> [!NOTE]
> 可将作为导入后的响应收到的文本文件导入 BaiWang 软件。 也可以导入从 BaiWang 软件导出的 XML 文件。

## <a name="configure-tax-integration-for-china"></a>配置中国的税务集成

必须先开启，才能配置税务集成。 转到**应收帐款 \> 设置 \> 应收帐款参数**，然后在**分类帐和销售税** 选项卡的**常规**快速选项卡上，将**与税收系统集成** 选项设置为**是**。

若要配置中国的税收集成，请执行以下步骤。

1. 在**增值税发票描述**页中，创建新的增值税（VAT）发票描述。 例如，可能必须设置以下值：

    - **增值税发票描述 ID：** InvoiceDescID01
    - **描述：** 设备
    - **单位：** 箱

2. 在**税务集成模板**页中，创建一个新税务集成模板。 可以设置导入或导出发票时使用的税务集成模板。 在税务集成模板中，可以指定以下信息：

    - 增值税代码
    - 最大发票金额
    - 金税发票的默认描述和单位

    也可以指定是否应包含普通增值税发票。

下图显示了税务集成流程。

[![税务集成流程](./media/ic666469.gif)](./media/ic666469.gif)

## <a name="additional-resources"></a>其他资源

- [导入中国金税数据实体](apac-chn-import-golden-tax-data-entity.md)（不适用于 Microsoft Dynamics 365 for Finance and Operations 版本 10.0 \[2019 年四月\]及更高版本）
- [增值税客户发票的中国税务集成修改常见问题](apac-chn-tax-integration-vat-customer-invoices.md)
- [设置中国的基本税务集成模板](./tasks/set-up-basic-tax-integration-profile-china.md)
