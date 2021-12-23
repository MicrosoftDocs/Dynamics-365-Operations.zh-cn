---
title: 导入和导出税款计算
description: 本主题提供有关税款计算服务的导入和导出功能的信息。
author: Kai-Cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 76ea99510455e984d94a93d87ee788fdcf00c376
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891303"
---
# <a name="import-and-export-tax-calculations"></a>导入和导出税款计算

本主题提供有关税款计算服务的导入和导出功能的信息。 此功能有助于确保灵活高效的配置体验。

## <a name="import-and-export-tax-codes"></a>导入和导出税代码

### <a name="export-templates"></a>导出模板

1. 登录 [Regulatory Configuration Service (RCS)](https://marketing.configure.global.dynamics.com/)。
2. 在 **全球化功能** 工作区，选择 **功能**，然后选择 **税款计算** 磁贴。
3. 选择现有功能，或[创建新功能](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs)。
4. 在 **版本** 网格中，选择 **编辑**。
5. 在 **税款计算** 功能页面上，设置[配置版本](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs)。
6. 在 **税代码** 选项卡上，选择 **导入**。
7. 选择 **导出税代码模板** 下载 **TaxCodesTemplate.zip** 文件。
8. 解压缩 **TaxCodesTemplate.zip**。 税代码模板根据 **计算来源** 值分别压缩。
9. 解压缩 **By Net Amount.zip**，获取以下逗号分隔值 (CSV) 文件：

    - **TaxCode.csv** – 输入税代码。
    - **TaxLimit.csv** – 输入每个税代码的税金限制。
    - **TaxRate.csv** – 输入每个税代码的税率。

> [!NOTE]
> 默认情况下，模板中会有 **示例** 税代码的条目。 如果 **示例** 税代码未从 CSV 文件中删除，它将被导入到功能中。

### <a name="import-tax-codes"></a>导入税代码

按照以下步骤将模板中的 **示例** 税代码导入您的税款计算功能。

1. 在 RCS 中，在 **税款计算** 功能页面上，在 **税代码** 选项卡上，选择 **导入**。
2. 选择 **浏览**，查找并选择 **TaxCode.csv** 文件，然后在 **目标表** 字段中，选择 **税代码**。
3. 选择 **确定** 导入税代码。
4. 查找并选择 **TaxRate.csv** 文件，然后在 **目标表** 字段中，选择 **税率**。
5. 选择 **确定** 导入税率。
6. 查找并选择 **TaxLimit.csv** 文件，然后在 **目标表** 字段中，选择 **税金限制**。
7. 选择 **确定** 导入税金限制。

您还可以直接导入包含所有三个 CSV 文件的 zip 文件。 这样，您可以快速轻松地完成导入。

1. 在 RCS 中，在 **税款计算** 功能页面上，在 **税代码** 选项卡上，选择 **导入**。
2. 选择 **浏览**，查找并选择 **By Net Amount.zip** 文件，然后选择 **确定**。

### <a name="export-tax-codes"></a>导出税代码

1. 在 RCS 中，在 **税款计算** 功能页面上，在 **税代码** 选项卡上，选择 **导出**。

    当 **税代码** 网格中至少有一个税代码时，**导出** 按钮才可用。

2. 选择 **确定** 将功能的所有税代码导出到 zip 文件。

> [!NOTE]
> 使用导出的文件作为模板将税代码导入到相应的功能中。

## <a name="import-and-export-applicability-rules"></a>导入和导出适用性规则

### <a name="export-applicability-rules"></a>导出适用性规则

1. 登录 [RCS](https://marketing.configure.global.dynamics.com/)。
2. 在 **全球化功能** 工作区，选择 **功能**，然后选择 **税款计算** 磁贴。
3. 选择现有功能，或[创建新功能](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs)。
4. 在 **版本** 网格中，选择 **编辑**。
5. 在 **税款计算** 功能页面上，设置[配置版本](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs)。
6. 在 **税组适用性** 选项卡上，选择 **设置税组适用性** 网格中的行。
7. 选择 **在 Microsoft Office 中打开** 按钮，然后选择 **税务服务动态适用性矩阵**。

    [![在税款计算功能页面上将适用性规则导出到 Microsoft Excel。](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. 选择 **下载** 将所选行导出到 Microsoft Excel 工作表。

### <a name="import-applicability-rules"></a>导入适用性规则

您下载的 Excel 工作表将包含 **设置税组适用性** 网格的结构。 您可以直接在工作表中添加新规则。 完成后，按照以下步骤将新规则导回到 **设置税组适用性** 网格。

1. 在 Excel 工作表中，选择并复制要导入的行。
2. 在 RCS 中，在 **税款计算** 功能页面上，在 **税组适用性** 选项卡上，选择 **添加** 在 **设置税组适用性** 网格的底部插入一个空记录。
3. 选择 **Ctrl+V** 将复制的行粘贴到网格中。
4. 选择 **保存**。
