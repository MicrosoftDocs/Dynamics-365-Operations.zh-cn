---
title: "管理电子申报配置生命周期"
description: "本主题介绍如何管理 Microsoft Dynamics 365 for Operations 解决方案的电子申报 (ER) 配置的生命周期。"
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cecbb5bd57aa24a942d10241bd83e4c1996a3805
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>管理电子申报配置生命周期

[!include[banner](../includes/banner.md)]


本主题介绍如何管理 Microsoft Dynamics 365 for Operations 解决方案的电子申报 (ER) 配置的生命周期。

<a name="overview"></a>概览
--------

电子申报 (ER) 是一个引擎，可支持 Microsoft Dynamics 365 for Operations 中的法律要求的和国家/地区特定的电子文档。 一般来说，ER 假设执行一个电子文档的以下任务的能力。 有关详细信息，请参阅[电子申报概览](general-electronic-reporting.md)。

-   设计电子文件的模板：
    -   标识可在此文档中提供的所需数据源：
        -   基础 Dynamics 365 for Operations 数据（如数据表、数据实体和类）。
        -   处理特定的属性（如执行日期和时间，以及时区）。
        -   用户输入参数（在运行时由最终用户指定）。
    -   定义所需文档的元素及其拓扑结构以指定最终文档格式。
    -   配置从所选数据源到定义的文档元素的所需数据流（通过绑定到文档格式组件的数据源）并指定流程控制逻辑。
-   将一个模板变为可用，以便可以在其他 Dynamics 365 for Operations 实例中使用：
    -   将在 Dynamics 365 for Operations 中创建的文档模板转换为 ER 配置，并且从当前 Dynamics 365 for Operations 实例导出配置为可以存储在本地或 LCS 中的 XML 包。
    -   将 ER 配置转换为 Dynamics 365 for Operations 文档模板。
    -   将存储在本地或 LCS 中的 XML 包导入到当前的 Dynamics 365 for Operations 实例。
-   自定义电子文档模板：
    -   从 LCS 将模板作为 ER 配置导入到当前的 Dynamics 365 for Operations 实例。
    -   设计自定义版本的 ER 配置，并保留对其基础版本的引用。
-   将模板与特定业务流程集成，以使它在 Dynamics 365 for Operations 中可用：
    -   通过在流程相关参数中引用该配置来配置设置以便 Dynamics 365 for Operations 开始使用 ER 配置。 例如，引用特定应付帐款付款方式中的 ER 配置以生成用于处理发票的电子付款消息。
-   使用特定的业务流程中的模板：
    -   在特定的业务流程中运行 ER 配置。 例如，要在选择了引用 ER 配置的付款方式时生成用于处理发票的电子付款消息。

## <a name="concepts"></a>概念
以下角色和相关活动与 ER 配置生命周期相关。

| 角色                                       | 活动                                                      | 说明                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 电子申报功能顾问 | 创建和管理 ER 组件（模型和格式）。           | 设计 ER 域特定数据模型、设计电子文档的所需模板并将它们进行相应绑定的业务人员。                                                                           |
| 电子申报开发人员             | 创建和管理数据模型映射。                          | 选择所需的 Dynamics 365 for Operations 数据源并将它们绑定到 ER 域特定数据模型的 Dynamics 365 for Operations 专业人员。                                                                 |
| 会计主管                      | 配置引用 ER 项目的流程相关设置。 | 例如，允许 ER 配置设置用于特定应付帐款付款方式来生成用于处理发票的电子付款消息的**会计主管**角色。 |
| 应付帐款付款员            | 使用特定业务流程中的 ER 项目。                | 例如，允许基于为特定付款方式配置的 ER 格式为处理发票生成电子付款消息的**应付帐款付款员**。           |

## <a name="er-configuration-development-lifecycle"></a>ER 配置开发生命周期
出于以下与 ER 相关的原因，我们建议您在开发环境中将 ER 配置设计为单独的 Dynamics 365 for Operations 实例：

-   担当**电子申报开发人员**角色或**电子申报功能顾问**角色的用户可编辑配置，并运行配置以进行测试。 此情况可能会导致调用类和表的方法，可能对业务数据和 Dynamics 365 for Operations 实例的性能产生负面影响。
-   在调用作为 ER 配置的 ER 数据源的类和表的方法时，不受 Dynamics 365 for Operations 入口点和记录的公司内容的限制。 因此，担当**电子申报开发人员**角色或**电子申报功能顾问**角色的用户可访问业务敏感数据。

在开发环境中设计的 ER 配置可上传到测试环境以进行配置评估（适当的流程集成、结果的正确性、性能）和质量保证（如角色驱动的访问权限的正确性和职责划分）。 启用 ER 配置交换的功能可以用于此目的。 最后，已审核的 ER 配置可上传到 LCS，在其中这些配置可与服务订阅者共享，也可上传到生产环境以供内部使用，如下图所示。 ![ER 配置生命周期](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>请参阅
--------

[电子申报概览](general-electronic-reporting.md)




