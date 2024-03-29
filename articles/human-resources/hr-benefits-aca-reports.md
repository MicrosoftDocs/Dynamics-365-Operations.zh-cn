---
title: 创建平价医疗法案 (ACA) 报告
description: 平价医疗法案 (ACA) 报告生成表单 1095-B 和 1095-C，来支持平价医疗法案的 **雇主授权单** 部分。
author: twheeloc
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 9ef67fba97282d1fc641f0281cd51c8ff08c65e5
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690825"
---
# <a name="generate-aca-reports"></a>生成 ACA 报表


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

平价医疗法案 (ACA) 报告生成表单 1095-B 和 1095-C，来支持平价医疗法案的 **雇主授权单** 部分。

> [!NOTE]
> ACA 报告仅对美国的法人启用。

## <a name="getting-started"></a>入门

要跟踪表单 1095-B 和 1095-C 的信息，必须先创建一个或多个平价医疗保险范围组。 平价医疗保险范围组指示：

- 为员工提供的保险范围
- 如果成本高于联邦贫困线，员工应承担的最低成本每月保费的份额
- 雇主使用的安全港（如果适用）

平价医疗保险范围组让您可以管理这些字段的信息，而无需更改条件相同的每个员工记录。 您可以使用页面上的 **成批分配** 选项轻松地将平价医疗保险范围组分配给一个或多个员工。

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>维护保险范围组的多个版本

您可以任何维护保险范围组的多个版本。 此功能让您可以进行更改，而无需创建新组，然后将员工重新分配到组中。 

创建 ACA 保险范围组后，您可以使用 **成批分配** 选项将组分配给员工。 您还可以单独指示是否跟踪和报告 ACA 信息，以及将员工分配到平价医疗保险范围组。

您不需要跟踪某些 ACA 保险范围信息，如兼职员工的信息。 在这种情况下，将 **报告保险范围** 字段设置为 **否**。 虽然您必须将每个具有可追踪 ACA 信息的员工分配到平价医疗保险范围组，但您仍可以在几个月内使用不同的值更改以下选项：

- **提供的保险范围**
- **员工承担的成本比例**
- **安全港**

要输入平价医疗保险范围组值的例外，选择 **工作人员详细信息** 页上的 **平价医疗保险范围** 链接，该链接位于 **雇用选项卡** 上的 **附加信息** 部分下。

## <a name="reporting-health-care-coverage"></a>报告医疗保险范围

除了跟踪已向全职员工提供的健康保险范围以外，如果雇主为登记的员工（无论其雇佣状态是否为全职或兼职）提供由雇主赞助的自保型保险健康保险范围，则需要在 1095-C 上报告附加信息。 由雇主赞助的福利计划涵盖的每位员工（包括依赖方）需要包含在保险的月份的报表上。 

您可以通过选择 **ACA 可报告** 复选框指示是否必须报告每个福利计划。

此外，如果员工已选择将其任何依赖方涵盖在福利下，您可以在 **维护福利** 页上指示为每位员工的依赖方投保的日期。 要指示依赖方是否涵盖在福利下，选择 **依赖方** 快速选项卡的操作窗格中的 **编辑** 按钮。

在 **依赖方保险范围日期管理器** 页面，可以指示福利涵盖依赖方的日期。 在此页面上输入日期将自动选择 **维护福利** 页面上的 **已涵盖** 复选框。

## <a name="generate-1095-b-and-1095-c-forms"></a>生成 1095-B 和 1095-C 表单

您还可以从产品内部生成 1095-B 和 1095-C 表单，并将其分配给每个员工。 系统还可以电子生成 1095-C 表单和 1094-C IRS 传送单。  

在生成 1095-C 表单时，请输入相应的纳税年度并指示是否应隐藏社会保险号。 如果您为 500 名以上员工打印 1095-C 表单，您将收到多个 PDF 文件。 建议您在 **文档管理参数** 窗口中将 **最大文件大小** 增加到 150 MB。

## <a name="viewing-information"></a>查看信息

您可以使用 **工作人员的平价医疗保险范围** 页查看哪些员工已分配到各保险范围组、哪些员工不需要包括在报表上以及哪些员工未分配。

如果平价医疗保险范围组的任何默认值已被替代，被更改的值的旁边将显示星号。 如果所有 12 个月的值相同且未被覆盖，该值将打印在 **所有 12 个月** 列。

您还可以使用查询窗口来了解哪些员工被标记为非 ACA 可报告。 您无需跟踪是否向他们提供了保险范围，也不需要在年底向他们发放 1095-C。 在 **筛选方式** 字段中选择 **非 ACA 可报告** 将生成不会收到 1095-C 的所有员工的列表。

此外，您还可以查看未分配（**ACA 报告保险范围** 字段为空）的任何员工或已分配到平价医疗保险范围组但在 **年度** 字段所选年份到期的任何员工。

您可以将使用任何筛选方式生成的员工列表导出到 Excel。

如果由于您提供自保型保险范围而需要报告投保的个人，可以查看标记为 **ACA 可报告** 的福利计划覆盖的任何依赖方。 在操作窗格上选择 **查看依赖方保险范围**。

> [!NOTE]
> 仅标记为 **ACA 可报告** 的福利计划将显示在查询窗口中。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
