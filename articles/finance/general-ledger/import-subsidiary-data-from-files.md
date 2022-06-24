---
title: 从文件导入子公司数据
description: 本文说明如何从外部系统准备数据，以可以将其导入 Microsoft Dynamics 365 Finance。
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 6886e2ee79ee9e4ccc067dc4f661c1eea646cfa6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846761"
---
# <a name="import-subsidiary-data-from-files"></a>从文件导入子公司数据

[!include [banner](../includes/banner.md)]

本文说明如何从外部系统准备数据，以可以将其导入 Microsoft Dynamics 365 Finance。 您使用 **与导入合并** 页（**合并 \> 与导入合并**）从外部系统准备子公司数据的转移。

1. 为合并创建子公司法人。 有关如何创建法人的信息，请参阅[创建法人](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md)。 有关详细信息，请参阅[准备一个法人以供在合并流程中使用](prepare-company-for-consolidation.md)和[设置要合并的子公司法人](set-up-subsidiary-company-for-consolidation.md)。

2. 准备一个将包含导入的数据的文件。 有关导入流程的详细信息，请参阅[数据导入和导出作业概述](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)。
3. 按照[数据导入和导出作业概述](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)中“数据导入/导出流程”过程中的步骤将数据导出到文件。 您可以使用该过程来合并来自 Dynamics 365 Finance 的另一个实例或来自 Dynamics 365 Business Central 的数据。 如果要从外部系统导入数据，数据必须采用[将子公司数据导出到文件](export-subsidiary-data-to-file.md)中所述的格式。
4. 转到 **合并 \> 与导入合并**。 在 **与导入合并** 页上的 **条件** 选项卡上，通过设置以下字段指定报表和/或导入的详细信息。

    | 字段                                 | 报表的值 | 导入的值 |
    |---------------------------------------|----------------------|----------------------|
    | 说明                           | 不适用 | 输入描述来标识导入。 |
    | 主帐户                          | 定义报表应包括的帐户范围。 如果您未定义范围，将包括所有帐户。 | 定义导入应包括的帐户范围。 如果您未定义范围，将包括所有帐户。 |
    | 合并期间                  | 定义合并的日期范围。 | 定义合并的日期范围。 |
    | 包括实际金额                | 将此选项设置为 **是** 将包括实际值。 | 将此选项设置为 **是** 将包括实际值。 |
    | 包括预算金额                | 将此选项设置为 **是** 将在合并中包括预算金额。 | 将此选项设置为 **是** 将在合并中包括预算金额。 |
    | 在合并过程中重新生成余额 | 如果重新生成流程应完全清除余额和新记录，并从一开始就重新创建余额，则将此选项设置为 **是**。 | 如果重新生成流程应完全清除余额和新记录，并从一开始就重新创建余额，则将此选项设置为 **是**。 |
    | 预算模型                         | 不适用 | 如果选择导入预算金额，请输入要合并的预算模型。 |
    | 预算汇率类型                      | 不适用 | 输入预算汇率的类型。 |

6. 如果您使用不同的会计货币，请使用 **货币折算** 选项卡上的字段来配置在合并期间进行的折算。

    | 字段                      | 说明 |
    |----------------------------|-------------|
    | 源法人        | 选择要从中导入的法人。 |
    | 源记帐币种 | 此默认货币是与您在 **源法人** 字段中选择的源法人关联的货币。 |
    | “从”和“到”帐户       | 定义要从源法人导入的帐户范围。 |
    | 汇率类型         | 选择汇率类型。 创建主科目时会分配汇率类型。 有关详细信息，请参阅[创建主科目](tasks/create-main-account.md)。 |
    | 应用来自以下对象的汇率   | 输入日期以应用在该日期生效的汇率。 或者，输入应该用作汇率的值。 |
    | 汇率              | 默认值取决于您在 **汇率类型** 字段中选择的汇率类型。 如果输入了用户定义的汇率，您可以定义汇率。 |

7. 将 **在后台运行** 选项设置为 **是** 可以让导入流程在后台运行。
8. 将 **批处理** 选项设置为 **是** 可以在特定时间将合并作为批处理作业运行。 要立即运行合并，请选择 **确定**。 

为子公司中的合并指定的交易记录和余额将添加到相应的合并法人帐户中。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
