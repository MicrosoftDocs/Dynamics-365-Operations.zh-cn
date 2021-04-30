---
title: 埃及预缴税金申报
description: 本主题说明如何配置和生成埃及预缴税金申报。
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e0d13a2de9acaa8b1c896e130b4dabb222e45dcb
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881414"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>埃及预缴税金申报 (EG-00005)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>概览
本主题说明如何为埃及中的法人创建和生成预缴税金申报以及预缴税金申报表 41 和 11 

所有埃及实体都必须准备表格 41，该表格概括了从本地供应商和服务提供商处保留的所有税款。 除表格 41 外，还必须生成表格 11 来详细说明从外国供应商处征收的所有保留税。 

Dynamics 365 Finance 中的 **预缴税金申报** 报表包括以下报告：

- 申报单编号 41
- 申报单编号 11
    
    
## <a name="prerequisites"></a>先决条件
法人的主地址必须在埃及。
在 **功能管理** 工作区中，必须启用以下功能：

   - **全球预缴税金**

有关如何启用功能的详细信息，请参阅[功能管理概述。](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

1. 转到 **税** > **设置** > **参数** > **总帐参数**，然后在 **预缴税金** 选项卡上，将 **启用全球预缴税金** 设置为 **是**。
2. 在 **电子报告** 工作区中，从存储库中导入以下电子报告格式：

    - WHT 申报 Excel (EG)

    > [!NOTE]
    > 上面的格式基于 **税申报模型** 并使用 **税申报模型映射**。 系统将自动导入此附加配置。

有关如何导入电子报告配置的更多信息，请参见[从 Lifecycle Services 下载电子报告配置](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)。

## <a name="download-electronic-reporting-configurations"></a>下载电子报告配置

埃及 WHT 申报表的实施基于电子报告 (ER) 配置。 有关可配置报告的功能和概念的更多信息，请参见[电子报告](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)。

对于生产和用户验收测试 (UAT) 环境，请按照[从 Lifecycle Services 下载电子报告配置](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)主题中的说明进行操作。

要在埃及法人中生成预缴税申报，您需要上传以下配置：

- Tax declaration model.version.82.xml 或更高版本
- Tax declaration model mapping.version.82.133.xml 或更高版本
- WHT Declaration Excel (EG).version.82.21 或更高版本

从 Lifecycle Services (LCS) 或全局存储库下载完 ER 配置后，请完成以下步骤。

1. 转到 **电子申报** 工作区中，并选择 **报告配置** 磁贴。
1. 在 **配置** 页上的“操作”窗格中，选择 **交换 > 从 XML 文件加载**。
1. 按照先前项目符号中列出的顺序上传所有文件。 在上传所有配置之后，配置树应该会出现在 Finance 中。

## <a name="set-up-application-specific-parameters"></a>设置特定于应用程序的参数

特定于应用程序的参数选项允许用户根据 **预扣税项目组** 配置或查找定义中建立的其他标准来建立以下相关标准：如何在生成的报告的每一行中分类和计算税收交易。

预缴税申报表 41 包含一个特定的列，在该列中，必须根据名为 **折扣代码类型** 的税务主管机构对预缴税金交易进行分类。 在过帐交易时，不要将这些新分类作为新录入数据包括在内，而是要根据 **配置** > **设置特定于应用程序的参数** > **设置** 中引入的不同查找来确定分类，以满足埃及预缴税报告的要求。 

以下配置用于在预缴税申报表 41 报告中对交易进行分类：

- **DiscountTaxTypeLookup** -> 第 18 列 

完成以下步骤以设置用于生成 WHT 申报和相关帐簿报告的不同查找。 

1. 在 **电子报告** 工作区中，选择 **配置** > **设置**，以设置规则来识别在 WHT 申报报表中如何对交易进行分类。 
2. 选择当前版本，然后在 **查询** 快速选项卡上选择查找名称。 例如，**DiscountTaxTypeLookup**。 此查找标识了税务机关要求的折扣类型的列表。
3. 在 **条件** 快速选项卡上，选择 **添加**，并在 **查询结果** 列内的新行中，选择代表 **第 18 列** 中的类别的相关行。
4. 在 **预扣税项目组** 列中，选择用于识别分类的相关代码。 例如，**允许的折扣**。  
5. 对所有可用的查找重复步骤 3 和 4。
6. 再次选择 **添加**，以包含最终记录行，并在 **查询结果** 列中，选择 **不适用**。 
7. 在其余列中，选择 **非空**。 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>设置总帐参数

要在 Microsoft Excel 中生成 WHT 申报表报告，请在 **总帐参数** 页上定义 ER 格式。

1. 转到 **税** > **设置** > **总帐参数**。
2. 在 **预扣税** 选项卡上的 **WHT 申报格式映射** 字段中，选择 **WHT 申报 Excel (EG)**。 如果您将该字段留空，则标准销售税报告将以 SSRS 格式生成。


![申报表](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>生成预扣税申报表
针对特定时期准备和提交预扣税申报表的过程基于在结算和过帐纳税作业期间过帐的预扣税交易。 有关全球预缴税金的更多信息，请参见[全球预缴税金](../general-ledger/global-withholding-tax-overview.md)。

完成以下步骤以生成纳税申报报表：

1. 转到 **税** > **申报** > **预缴税金**> **预缴税金付款*。
2. 选择结算期，然后选择报告的开始日期。 
3. 输入交易日期，然后选择 **确定**。
4. 在打开的对话框中，选择一种或多种表单类型：**表单编号 41**、**表单编号 11** 或 **无**。 如果选择 **无**，将生成标准报告。 
5. 选择语言。 所有报告均翻译成 **en-us** 和 **ar-eg**。
6. 输入将要支付税款的银行的分支机构和名称。
7. 选择业务类型，然后输入支票和单据编号。 
8. 输入实体类型。 
9. 输入为分配表单而注册的人员的姓名，然后选择 **确定** 以确认生成报告。 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
