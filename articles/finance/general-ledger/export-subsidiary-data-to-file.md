---
title: 将子公司数据导出到文件
description: 本主题说明如何为从 Microsoft Dynamics 365 Finance 导出数据，然后将其导入到合并的法人作准备。
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 179a401178935b8a76d6718a7fb1f63e08344f50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968671"
---
# <a name="export-subsidiary-data-to-files"></a>将子公司数据导出到文件

[!include [banner](../includes/banner.md)]

您使用 **导出** 页（**系统管理 \> 工作区 \> 导入/导出**）来准备将子公司数据导出到文件，然后再将其导入到合并的法人。 有关导入和导出流程的详细信息，请参阅[数据导入和导出作业概述](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)。

1. 为合并流程创建一个法人。 有关如何创建法人的信息，请参阅[创建法人](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md)。 有关详细信息，请参阅[准备一个法人以供在合并流程中使用](prepare-company-for-consolidation.md)和[设置要合并的子公司法人](set-up-subsidiary-company-for-consolidation.md)。 

2. 转到 **合并 \> 导出公司余额**。 在 **导出公司余额** 页上的 **条件** 选项卡上，通过设置以下字段指定合并的详细信息。

    | 字段                             | 说明 |
    |-----------------------------------|-------|
    | 主帐户                      | 指定要合并的帐户。 要包括所有帐户，请将此字段留空。 |
    | 使用合并帐户         | 如果您指定了合并帐户，请将此选项设置为 **是**。 |
    | 选择合并帐户的来源 | 选择 **主帐户** 或 **合并帐户组**。 |
    | 合并帐户组       | 为您选择的合并帐户选择合并帐户组。 |
    | 合并期间              | 为合并指定“开始”和“结束”日期。 |
    | 包括实际金额            | 将此选项设置为 **是** 将包括实际金额。 |
    | 包括预算金额            | 将此选项设置为 **是** 将在合并中包括预算金额。 |
    | 预算模型                     | 指定要包括的预算模型。 |

3. 在 **财务维度** 选项卡上，指定合并的详细信息：

    - 指定应从子公司帐户交易记录转移到合并法人中的交易记录的财务维度信息。
    - 在列表中选择财务维度。
    - 为合并的每个财务维度确定正确的规范。 可用选项包括 **维度**、**组维度**、**公司帐户** 和 **帐户**。

        > [!NOTE]
        > **组维度** 选项可让您定义要合并的公司组使用的维度值。

    - 指定合并的段顺序。

4. 在 **法人** 选项卡上，按照以下步骤指定要导出的法人实体：

    1. 选择 **新建**。
    2. 在 **源法人** 字段中，输入法人。

        如果将相同的条件应用于同一数据卡中的若干子公司，您可以在一个操作中将这些子公司的数据转移到单独的导出文件中：

        1. 为帐户应导出到文件的每个子公司法人创建一行。 这些文件以后将导入到合并的法人中。
        2. 对于每个子公司，输入该子公司名称和在导出作业期间将创建的导出文件的名称。

    3. 在 **换算差额的科目类型** 字段中，选择 **损益** 或 **资产负债表**。
    4. 为将要创建的导出文件输入文件名。

5. 选择 **确定** 运行导出。

在导出完成后，您将收到一则消息，其中显示已在各文件中保存的记录的数目。 然后您可以将文件导入到合并的法人。
