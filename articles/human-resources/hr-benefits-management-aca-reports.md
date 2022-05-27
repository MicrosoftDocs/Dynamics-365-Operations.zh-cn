---
title: 在“福利管理”中生成平价医疗法案报告
description: 本主题介绍“福利管理”如何跟踪平价医疗法案 (ACA) 雇主授权单的表单 1095-B 和表单 1095-C 上报告的信息。
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 118dace557c7c8a8d101e2f2ad1d94fb14547c1b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688704"
---
# <a name="generate-aca-reports-in-benefits-management"></a>在“福利管理”中生成 ACA 报告


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

“福利管理”跟踪平价医疗法案 (ACA) 雇主授权单的表单 1095-B 和表单 1095-C 上报告的信息。 与旧 **福利** 工作区中的 ACA 报告功能一样，此功能仅适用于美国的法人。

要使用此功能，必须首先打开 **高级福利管理**。 有关详细信息，包括有关“福利管理”的重要说明，请参阅[启用或禁用“福利管理”](hr-admin-manage-features.md#enable-or-disable-benefits-management)。

> [!IMPORTANT]
> 您只能从 **福利管理** 工作区或旧 **福利** 工作区使用 ACA 报告，不能同时在两个位置使用。 例如，如果您切换到“福利管理”，则只能从 **福利管理** 工作区使用 ACA 报告，而不能从旧 **福利** 工作区使用。
>
> 如果您在注册年份中间切换到“福利管理”，则必须在“福利管理”中为全年正确配置员工数据。 这样，可以确保会在全年收到准确的报告信息。

## <a name="getting-started"></a>入门

要跟踪 1095 表单的信息，首先创建一个或多个平价医疗保险范围组。 这些组指示以下信息：

- 提供给员工的保险范围
- 如果成本高于联邦贫困线，员工应承担的最低成本每月保费的份额
- 雇主使用的安全港（如果适用）

平价医疗保险范围组帮助您管理具有相同条件的多个员工记录的这一信息。 您可以轻松地将组分配给一个或多个员工。

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>创建或编辑平价医疗保险范围组

1. 在 **福利管理** 工作区，选择 **平价医疗保险范围组**。

    ![选择“平价医疗保险范围组”。](./media/hr-benefits-management-aca-coverage-group.png)

2. 选择 **新建** 创建新的平价医疗保险范围组，或选择 **编辑** 更改现有组。

    ![选择“新建”或“编辑”。](./media/hr-benefits-management-aca-new.png)

3. 设置以下字段。

    | 字段 | 说明 |
    |---|---|
    | 姓名 | 为组输入名称。 |
    | 说明 | 输入组的描述。 |
    | 提供的保险范围 | 提供给员工、员工配偶或伴侣和员工依赖方的保险范围。 |
    | 员工承担的成本比例 | 员工负责的金额。 |
    | 适用的部分 4980H 安全港 | 4980H 安全港或过渡救济代码。 |
    | 计划开始月份 | 选择您的福利计划年份开始的日历月。 |
    | 组生效日期 | 此记录有效的第一个日期。 |
    | 组失效日期 | 此记录有效的最后一个日期。 如果没有到期日期，输入 **从不**。 |

    ![创建保险范围组。](./media/hr-benefits-management-aca-new-group.png)

4. 选择 **保存**。

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>将多个员工分配到平价医疗保险范围组

1. 在 **福利管理** 工作区，选择 **平价医疗保险范围组**。
2. 选择要向其中分配员工的组。
3. 选择 **成批分配**。

    ![选择“成批分配”。](./media/hr-benefits-management-aca-mass-assignment.png)

4. 在列表中选择员工，然后选择 **分配**。

    ![将选定的员工分配到组。](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>维护保险范围选项的多个版本

您可以任何维护保险范围组的多个版本。 当您的组织或所提供的福利发生变化时，您可以保持组的信息为最新，而不必创建新组，然后将员工重新分配到组中。

创建平价医疗保险范围组后，您可以将员工成批分配到组中。 您还可以将员工单独分配到组，并指示是否跟踪和报告 ACA 信息。

如果您不必跟踪和报告员工的 ACA 信息，可以将 **报告保险范围** 选项设置为 **否**。 例如，您可能有不需要 ACA 报告的兼职员工。

### <a name="override-default-values-for-an-employee"></a>替代员工的默认值

对于分配到平价医疗保险范围组的员工，您可以在需要不同值的任何月份更改以下选项：

- 提供的保险范围
- 员工承担的成本比例
- 适用的部分 4980H 安全港

> [!NOTE]
> 对于 2020 ACA 报告，您必须在表单 1095-C 中报告工作和家庭邮政编码。 值将根据当前活动位置自动填充。 如果一年中的任何时候两个位置都不同，则必须替代此值。 仅当 **提供的保险范围** 代码包含 **1L** 到 **1Q** 时，1095-C 报告的 **邮政编码** 字段（第 17 行）才会填充，如下所示：
>
> - **1L、1M 或 1N：** 主要住所的邮政编码
> - **1O、1P、1Q：** 主要工作邮政编码

要为平价医疗保险范围组的任何值输入例外，请执行以下步骤。

1. 在 **人事管理** 工作区，选择 **链接**，然后选择 **工作人员**。
2. 在列表中选择员工。
3. 在 **雇用** 选项卡上，在 **更多信息** 部分，选择 **平价医疗保险范围**。

    ![为一个员工更改选项。](./media/hr-benefits-management-aca-change-single-employee.png)

4. 选择 **编辑**。
5. 对于需要更改的每个月份，选中 **替代默认值** 复选框，然后根据需要更改其他值。

    ![替代默认值。](./media/hr-benefits-management-aca-override-default.png)

6. 选择 **保存**。

## <a name="report-health-care-coverage"></a>报告健康医疗保险范围

您必须跟踪全职和兼职员工的任何雇主赞助的自保型保险健康保险范围。 将每个员工及其依赖方包括在保险覆盖月份的 1095-C 报告中。

要指示是否必须报告福利计划，请按照下列步骤操作。

1. 在 **福利管理** 工作区中，选择 **福利计划**。
2. 选择要报告的福利计划。
3. 选择 **编辑**。
4. 将 **根据平价医疗法案进行报告** 选项设置为 **是**。

    ![报告医疗保险范围。](./media/hr-benefits-management-aca-report-coverage.png)

5. 选择 **保存**。

如果员工为依赖方选择健康医疗保险范围，依赖方的覆盖期间由依赖方登记或删除的日期确定。 依赖方的覆盖日期根据登记年中份依赖方在计划中具备资格且处于活动状态的持续期间自动计算。

## <a name="generate-1095-b-and-1095-c-forms"></a>生成 1095-B 和 1095-C 表单

您可以生成 ACA 1095-B 和 1095-C 表单，然后将其分配给每个员工。 您还可以电子方式生成表单 1095-C 和相应的 1094-C 传送单，来发送给美国国税局 (IRS)。

1. 在 **福利管理** 工作区，选择 **ACA 1095-B 表单** 或 **ACA 1095-C 表单**。
2. 根据需要更改参数，然后选择 **确定**。

    > [!NOTE]
    > 如果您为 500 名以上员工打印 1095-C 表单，您将收到多个 PDF 文件。 我们建议您将 **文档管理参数** 页上的 **最大文件大小(MB)** 字段的值增加到 **150**。 （若要快速打开该页面，请使用导航栏上的搜索字段。）
    >
    > ![更改最大文件大小。](./media/hr-benefits-management-aca-maximum-file-size.png)

3. 要检查报告的状态以及查看报告，使用导航栏上的搜索字段打开 **电子报告作业** 页。

    ![搜索电子报告作业页面。](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. 选择要查看的报告，然后选择 **显示文件**。

    ![显示文件。](./media/hr-benefits-management-aca-show-files.png)

5. 选择 **打开**。

    ![打开文件。](./media/hr-benefits-management-aca-open-file.png)

6. 从显示在浏览器窗口底部的通知栏中，打开 zip 文件，然后选择报告。 您可以查看或打印 PDF 文件。

    ![示例 1095-C 窗体。](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>查看 ACA 保险范围信息

**工作人员平价医疗保险范围** 页显示以下信息：

- 分配到每个保险范围组的员工
- 不必包含在报告中的员工
- 未分配的员工

若要查看此信息，请按照下列步骤操作。

1. 在 **福利管理** 工作区，选择 **工作人员平价医疗保险范围**。
2. 在 **组名称** 字段中，选择一个组。

    ![查看 ACA 保险范围。](./media/hr-benefits-management-aca-view-coverage.png)

如果平价医疗保险范围组的任何默认值已被替代，被更改的值的旁边将显示星号。 如果所有 12 个月的值相同且未被替代，该值将出现在 **所有 12 个月** 列中。

您可以查看标记为非 ACA 可报告、不需要表单 1095-C 的员工。 在 **筛选方式** 字段中，选择 **非 ACA 可报告**。

您可以查看未分配到组的员工，或分配到过期组的员工。 在 **筛选方式** 字段中，选择 **未分配或过期组**。

### <a name="export-to-excel"></a>导出到 Excel

要将任何列表导出到 Microsoft Excel，请按照以下步骤操作。

1. 选择 **在 Microsoft Office 中打开** 按钮。
2. 选择 **供内部使用的 HCM Human Resources 临时表**。
3. 选择 **下载**。

### <a name="view-aca-reportable-dependents"></a>查看 ACA 可报告依赖方

如果由于您提供自保型保险范围而必须报告投保的个人，可以查看标记为 **ACA 可报告** 的福利计划覆盖的依赖方。 在操作窗格上，选择 **查看依赖方保险范围**。

![查看依赖方保险范围。](./media/hr-benefits-management-aca-view-dependent-coverage.png)

员工依赖方的保险范围信息将显示。

![依赖方保险范围。](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> 此页面仅显示标记为 **ACA 可报告** 的福利计划。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
