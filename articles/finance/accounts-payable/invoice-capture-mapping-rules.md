---
title: Invoice capture 解决方案映射规则
description: 本文提供有关 Invoice capture 解决方案中的映射规则设置的信息。
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691145"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Invoice capture 解决方案映射规则

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

映射规则从 Microsoft Dynamics 365 Finance 或企业资源计划 (ERP) 系统中获取基本主数据。 设置映射规则后，将派生在 Finance 中创建供应商发票所需的信息。 使用映射规则时，应付帐款 (AP) 职员将检查状态，而不是手动填写所有缺少的字段值。

有以下四种映射规则类型：

- 法人
- 供应商帐户
- 项目
- 支出类型

## <a name="manage-mapping-rules-by-using-the-app"></a>使用应用管理映射规则

要使用应用管理映射规则，选择 **设置**。 **映射规则设置** 选项卡提供四个选项：

- 法人 
- 供应商帐户 
- 物料映射 
- 支出类型

例如，您选择 **法人映射规则** 选项。 将使用公司名称、地址和税务登记编号来识别法人代码。 对于名为 **LE-USPM** 的规则，如果公司名称包含文本“Contoso Robotics USA”，法人代码将为 **USPM**。

此页面显示所有活动的映射规则。 如果要查看停用的映射规则，选择 **活动映射法人规则**，然后选择 **停用映射法人规则**。

以下操作可用于映射规则。

### <a name="create-a-mapping-rule"></a>创建映射规则

您可以使用两种方法来创建映射规则：

- 选择 **新建** 创建新映射规则。 然后输入映射规则的信息。 对于每种类型的映射规则，**规则名称** 值应该是唯一的。
- 如果您选择现有映射规则，**复制** 按钮将可用。 选择它，然后在出现的对话框中选择 **确定**。 通过复制选定的规则来创建映射规则。

### <a name="edit-a-mapping-rule"></a>编辑映射规则

要编辑映射规则，选择一个字段，然后更改值。

### <a name="activatedeactivate-mapping-rules"></a>激活/停用映射规则

要停用一个或多个映射规则，在 **活动映射规则** 页面选择这些规则，然后选择 **停用**。 规则将被从 **活动映射规则** 页面移动到 **停用映射规则** 页面。

同样，要激活映射规则，在 **停用映射规则** 页面选择这些规则，然后选择 **激活**。

### <a name="remove-mapping-rules"></a>删除映射规则

要删除映射规则，选择规则，然后选择 **删除**。

### <a name="check-for-conflicts"></a>检查冲突

如果两个映射规则具有相同的 **法人** 和 **供应商帐户** 值，但不同的 **物料名称** 值，将检测到冲突，该映射规则不会创建或更新。

## <a name="importexport-mapping-rules-from-excel"></a>从 Excel 导入/导出映射规则

Excel 加载项可用于批量管理规则。 选项如下：

- 下载 Excel 模板。
- 导出到 Excel。
- 从 Excel 导入。

### <a name="download-an-excel-template"></a>下载 Excel 模板

要下载 Excel 模板，选择 **下载模板**。 然后选择要包含在模板中的字段。

### <a name="export-to-excel"></a>导出到 Excel

您可以通过两种方式导出：

- 选择 **在 Excel Online 中打开** 在 Excel 中打开文件。 然后可以在线编辑文件。 当您完成时，选择 **保存**。 您的所有更改都将保存在 **映射规则** 页面。
- 选择 **下载工作表** 下载包含映射规则的 Excel 文件。 然后，您可以编辑该文件。 完成后，选择 **从 Excel 导入** 上载更新的工作表。

### <a name="import-from-excel"></a>从 Excel 导入

1. 选择 **从 Excel 导入** 从 XLSX 文件导入数据。 您还可以从逗号分隔值 (CSV) 或 XML 文件导入。 在导入之前，您应该决定是否允许重复。
2. 选择 **查看映射** 查看属性映射，确定它是否正确。 您可以修改映射关系。
3. 完成后，选择 **完成导入** 开始导入。
4. 您可以选择 **跟踪过程** 来跟踪导入过程的进度。

    导入状态将从 **完成** 更新为 **分析**，然后更新为 **转换**，最后是 **已完成**。

导入过程完成后，将显示成功、部分失败、错误和处理总数统计信息。
