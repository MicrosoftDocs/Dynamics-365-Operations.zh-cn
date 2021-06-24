---
title: 埃及增值税申报
description: 本主题说明如何配置和生成埃及增值税退税表。
author: sndray
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9c776cedb65804f8cadbe324082c2abac435f906
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186606"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>埃及增值税申报 (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

本主题说明如何为埃及中的法人设置和生成增值税退税单和买卖账簿。

埃及的增值税退税表是一份官方文件，其中汇总了应缴的销项增值税总额、应退回的进项增值税总额以及相关的增值税额负债。 该表适用于所有类型的纳税人，应通过税务机关门户手动填写。 增值税退税表通常称为增值税退税申报表。

Dynamics 365 Finance 中的增值税退税表包括以下报告：

- 增值税退税表编号 10，按法律规定，此表提供了增值税退税表中各行项目的金额、调整和增值税额的明细。
- 销售交易簿
- 采购交易簿

## <a name="prerequisites"></a>先决条件
法人的主地址必须在埃及。
在 **功能管理** 工作区中，启用以下功能：

   - （埃及）销售和采购税报表的类别层次结构。

有关如何启用功能的详细信息，请参阅[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。

在 **电子报告** 工作区中，从存储库中导入以下电子报告格式：

- 增值税申报 Excel (EG)

> [!NOTE]
> 上面的格式基于 **税申报模型** 并使用 **税申报模型映射**。 系统将自动导入附加配置。

有关如何导入电子报告配置的更多信息，请参见[从 Lifecycle Services 下载电子报告配置](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)。

## <a name="download-electronic-reporting-configurations"></a>下载电子报告配置

埃及增值税退税表的实施基于电子报告 (ER) 配置。 有关可配置报告的功能和概念的更多信息，请参见[电子报告](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)。

对于生产和用户验收测试 (UAT) 环境，请参阅[从 Lifecycle Services 下载电子报告配置](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)。

要在埃及法人中生成增值税退税表和相关报表，请上传以下配置：

- Tax declaration model.version.70.xml 或更高版本
- Tax declaration model mapping.version.70.120.xml 或更高版本
- VAT Declaration Excel (EG).version.70.32 或更高版本

从 Lifecycle Services (LCS) 或全局存储库下载 ER 配置后，请完成以下步骤。

1. 转到 **电子申报** 工作区中，并选择 **报告配置** 磁贴。
1. 在 **配置** 页上的“操作”窗格中，选择 **交换** > **从 XML 文件加载**。
1. 按照上面列出的顺序上载文件。 在上传所有配置之后，配置树应该会出现在 Finance 中。

## <a name="set-up-application-specific-parameters"></a>设置特定于应用程序的参数

特定于应用程序的参数使您可以建立关于在生成报告时如何在每行中对税务交易进行分类和计算的标准。 该决定基于商品销售税组、销售税组、销售税代码以及在查找定义中建立的其他条件的配置。

埃及的销售和购买帐簿报表包括一组列，这些列作为特定于埃及的业务、产品和单据的类型与特定的交易分类相对应。 在过帐交易时，不要将这些新分类作为新录入数据包括在内，而是要根据 **配置** > **设置特定于应用程序的参数** > **设置** 中引入的不同查找来确定分类，以满足埃及增值税报告的要求。 

![应用程序特定参数页面](media/egypt-vat-declaration-setup1.png)

以下这些查找配置用于对采购和销售增值税帐簿报告中的交易进行分类：

- **PurchaseItemTypeLookup** > 列 O：项目类型
- **VATRateTypeLookup** > 列 B：税收类型
- **VATRateTypeLookup** > 列 C：表格项类型
- **PurchaseOperationTypeLookup** > 列 A：单据类型
- **CustomerTypeLookup** > 列 A：文档类型
- **SalesOperationTypeLookup** > 列 N：操作类型
- **SalesItemTypeLookup** > 列 O：项目类型

完成以下步骤以设置用于生成增值税申报和相关帐簿报告的不同查找。 

1. 在 **电子报告** 工作区中，选择 **配置** > **设置**，以在增值税退税表的相关框中标识税收交易。
2. 选择当前版本，然后在 **查询** 快速选项卡上选择查找名称。 例如，**SalesItemTypeLookup**。 此查找标识税务机关要求的销售增值税簿中的分类列表。
3. 在 **条件** 快速选项卡上，选择 **添加**，并在 **查询结果** 列内的新行中，选择代表 **列 O** 中的类别的相关行。
4. 在 **销售税组** 列中，选择用于识别分类的销售税组。 例如，**国内销售发票**。 如果以其他方式定义配置，则还可以使用商品销售税组、税码或树属性组合。 
5. 在 **名称** 列中，选择税收交易分类。
6. 对所有可用的查找重复步骤 3-5。
7. 选择 **添加**，以包含最终记录行，并在 **查询结果** 列中，选择 **不适用**。 
8. 在其余列中，选择 **非空**。 
9. 在 **状态** 字段中，选择 **已完成**。
10. 选择 **保存**，然后关闭 **应用程序特定参数** 页面。

> [!NOTE]
> 当您添加最后一条记录（**不适用**）时，您可以定义以下规则：当销售税组、商品销售税组、税码和作为参数传递的名称不满足任何先前的规则时，交易将不包含在销售增值税帐簿中。 尽管在生成报告时未使用此规则，但是当缺少规则配置时，该规则确实有助于避免在生成报告时出现错误。

下表表示所描述的查找配置的建议配置示例。 

**SalesItemTypeLookup**

| 查找结果         | 扁平 | 销售税组    | 物料销售税组    | 税码（代码） | 姓名                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| 国内              | 1    | VAT_LOCAL          | *非空白*             | *非空白*     | 销售额                 |
| 国内              | 2    | VAT_LOCAL          | *非空白*             | *非空白*     | SalesCreditNote       |
| 国内              | 3    | VAT_FINALC         | *非空白*             | *非空白*     | 销售额                 |
| 国内              | 4    | VAT_FINALC         | *非空白*             | *非空白*     | SalesCreditNote       |
| 国内              | 5    | VAT_PUBLIO         | *非空白*             | *非空白*     | 销售额                 |
| 国内              | 6    | VAT_PUBLIO         | *非空白*             | *非空白*     | SalesCreditNote       |
| 出口                | 7    | VAT_EXPORT         | *非空白*             | *非空白*     | 销售额                 |
| 出口                | 8    | VAT_EXPORT         | *非空白*             | *非空白*     | SalesCreditNote       |
| 机械和设备 | 9    | *非空白*        | VAT_M&E                 | *非空白*     | 销售额                 |
| 机械和设备 | 10   | *非空白*        | VAT_M&E                 | *非空白*     | SalesCreditNote       |
| 零件机器        | 11   | *非空白*        | VAT_PARTS               | *非空白*     | 销售额                 |
| 零件机器        | 12   | *非空白*        | VAT_PARTS               | *非空白*     | SalesCreditNote       |
| 免税额            | 13   | VAT_EXE            | *非空白*           | *非空白*     | SaleExempt            |
| 免税额            | 14   | VAT_EXE            | *非空白*           | *非空白*     | SalesExemptCreditNote |
| 不适用        | 15   | *空白*            | *空白*                 | VAT_ADJ         | *非空白*           |
| 不适用        | 16   | *非空白*        | *非空白*             | *非空白*     | *非空白*           |

 **SalesOperationTypeLookup**

| 查找结果  | 扁平 | 物料销售税组    | 税码    | 姓名                  |
|----------------|------|-------------------------|-------------|-----------------------|
| 货物          | 1    | VAT_GOODS               | *非空白* | 销售额                 |
| 货物          | 2    | VAT_GOODS               | *非空白* | SalesCreditNote       |
| 货物          | 3    | VAT_GOODS               | *非空白* | SaleExempt            |
| 货物          | 4    | VAT_GOODS               | *非空白* | SalesExemptCreditNote |
| 服务       | 5    | VAT_SERV                | *非空白* | 销售额                 |
| 服务       | 6    | VAT_SERV                | *非空白* | SalesCreditNote       |
| 服务       | 7    | VAT_SERV                | *非空白* | SaleExempt            |
| 服务       | 8    | VAT_SERV                | *非空白* | SalesExemptCreditNote |
| 调整    | 9    | *空白*                 | VAT_ADJ     | 销售额                 |
| 调整    | 10   | *空白*                 | VAT_ADJ     | SalesCreditNote       |
| 不适用 | 11   | *非空白*             | *非空白* | *非空白*           |

**PurchaseItemTypeLookup**

| 查找结果          | 扁平 | 物料销售税组    | 税码    | 姓名                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| 货物                  | 1    | VAT_GOODS               | *非空白* | 采购                 |
| 货物                  | 2    | VAT_GOODS               | *非空白* | PurchaseCreditNote       |
| 服务               | 3    | VAT_SERV                | *非空白* | 采购                 |
| 服务               | 4    | VAT_SERV                | *非空白* | PurchaseCreditNote       |
| 机械和设备  | 5    | VAT_M&E                 | *非空白* | 采购                 |
| 机械和设备  | 6    | VAT_M&E                 | *非空白* | PurchaseCreditNote       |
| 零件机器         | 7    | VAT_PARTS               | *非空白* | 采购                 |
| 零件机器         | 8    | VAT_PARTS               | *非空白* | PurchaseCreditNote       |
| 免税额             | 9    | VAT_EXE                 | *非空白*  | PurchaseExempt           |
| 免税额             | 10   | VAT_EXE                 | *非空白* | PurchaseExemptCreditNote |
| 不适用         | 11   | *非空白*             | *非空白* | *非空白*              |

**PurchaseOperationTypeLookup**

| 查找结果  | 扁平 | 销售税组  | 税码    | 姓名                     |
|----------------|------|------------------|-------------|--------------------------|
| 国内       | 1    | VAT_LOCAL        | *非空白* | 采购                 |
| 国内       | 2    | VAT_LOCAL        | *非空白* | PurchaseCreditNote       |
| 国内       | 3    | VAT_LOCAL        | *非空白* | PurchaseExempt           |
| 国内       | 4    | VAT_LOCAL        | *非空白* | PurchaseExemptCreditNote |
| 已导入       | 5    | VAT_IMPORT       | *非空白* | 采购                 |
| 已导入       | 6    | VAT_IMPORT       | *非空白* | PurchaseCreditNote       |
| 已导入       | 7    | VAT_IMPORT       | *非空白* | PurchaseExempt           |
| 已导入       | 8    | VAT_IMPORT       | *非空白* | PurchaseExemptCreditNote |
| 调整    | 9    | *空白*          | VAT_ADJ     | PurchaseCreditNote       |
| 调整    | 10   | *空白*          | VAT_ADJ     | 采购                 |
| 不适用 | 11   | *非空白*      | *非空白* | *非空白*              |

**CustomerTypeLookup**

|    查找结果    | 扁平 | 销售税组 |
|---------------------|------|-----------------|
| 组织        |  1   | VAT_LOCAL       |
| 组织        |  2   | VAT_EXPORT      |
| 组织        |  3   | VAT_EXE         |
| 最终消费者      |  4   | VAT_FINALC      |
| 公共组织 |  5   | VAT_PUBLIO      |
| 不适用      |  6   | *非空白*     |

**VATRateTypeLookup**

| 查找结果  | 扁平 | 税码（代码） |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| FirstTable     | 3    | *非空白*     |
| SecondTable    | 4    | *非空白*     |
| 不适用 | 5    | *非空白*     |


## <a name="set-up-general-ledger-parameters"></a>设置总帐参数

要以 Microsoft Excel 格式生成增值税退税表报告，请在 **总帐参数** 页上定义 ER 格式。

1. 转到 **税** > **设置** > **总帐参数**。
2. 在 **销售税** 选项卡上的 **税选项** 部分，在 **增值税对帐单格式映射** 字段中，选择 **增值税申报 Excel (EG)**。 如果您将该字段留空，则标准销售税报告将以 SSRS 格式生成。
3. 选择 **类别层次结构**。 此类别启用“外贸”选项卡交易中的商品代码，以允许用户选择和分类商品和服务。 在销售和购买交易报告中详细描述了此分类。 此配置为可选配置。

![申报表](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>生成增值税退税报表
一段时间的增值税退税报告的准备和提交过程基于在结算和过帐销售税作业期间过帐的销售税付款交易。 有关销售税结算和报告的详细信息，请参阅[销售税概览](../general-ledger/indirect-taxes-overview.md)。

完成以下步骤以生成纳税申报报表：

1. 转到 **税** > **申报** > **销售税** > **报告结算期的销售税** 或 **结算和过帐销售税**。
2. 选择 **结算期**。
3. 选择起始日期，然后选择销售税支付版本。
5. 选择 **确定**。 
6. 输入上一期间的贷方金额（如果适用），或将金额保留为零。
7. 在 **报告详细信息** 字段中，选择以下可用选项。 
   - **购买增值税簿**：生成采购税交易明细报表。
   - **销售增值税簿**：生成销售税交易明细报表。
   - **增值税申报**：仅生成增值税申报退税表。
8. 输入为分配表单而注册的人员的姓名。
9. 选择语言。 所有报告均翻译成 **en-us** 和 **ar-eg**。
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


