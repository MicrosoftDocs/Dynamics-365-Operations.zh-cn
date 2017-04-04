---
title: "管理电子申报配置生命周期"
description: "此主题描述如何管理电子国家/地区报告的 (ER) 配置的生命期 Microsoft Dynamics 的 (ER) 解决方案的工序。"
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>管理电子申报配置生命周期

此主题描述如何管理电子国家/地区报告的 (ER) 配置的生命期 Microsoft Dynamics 的 (ER) 解决方案的工序。

<a name="overview"></a>概览
--------

电子申报 (ER) 是一个引擎，可支持 Microsoft Dynamics 365 for Operations 中的法律要求的和国家/地区特定的电子文档。 一般来说，ER 假设执行一个电子文档的以下任务的能力。 有关更详细信息，请参阅报表概览国家/地区电子 [] (常规电子国家/地区 reporting.md)。

-   设计电子文件的模板：
    -   标识可在此文档中提供的所需数据源：
        -   工序数据的基础 Dynamics 365，如数据表、数据实体和类。
        -   流程特定属性，如日期和执行时间和时区。
        -   用户的输入参数，按用户指定最终在运行时。
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
    -   通过在流程相关参数中引用该配置来配置设置以便 Dynamics 365 for Operations 开始使用 ER 配置。 例如，请参阅在特定应付帐款付款方式的 ER 配置生成处理发票的一种电子支付消息。
-   使用特定的业务流程中的模板：
    -   运行在特定业务流程的一个 ER 配置。 例如，生成处理的一种电子支付开票消息，在 ER 引用配置的付款方式选择。

## <a name="concepts"></a>概念
下列角色和相关活动与 ER 配置生存期。

| 角色                                       | 活动                                                      | 说明                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 电子申报功能顾问 | 创建和管理 ER 组件（模型和格式）。           | 设计 ER 专门字段数据模型设计，电子文档所需的模板，并且相应绑定其企业人员。                                                                           |
| 电子申报开发人员             | 创建和管理数据模型映射。                          | 选择工序数据源所需的 Dynamics 365 并且 ER 绑定到基础数据工序字段模型的专业的 Dynamics 365。                                                                 |
| 会计主管                      | 配置引用 ER 项目的流程相关设置。 | 例如，ER 设置允许在配置特定应付帐款付款方式生成的**帐户主管**角色处理的一种电子支付开票消息。 |
| 应付帐款付款员            | 使用特定业务流程中的 ER 项目。                | 例如，允许电子付款处理消息。发票生成的一**应付帐款付款善写**角色，根据对特定付款方式配置的 ER 格式。           |

## <a name="er-configuration-development-lifecycle"></a>ER 配置开发生命周期
出于以下与 ER 相关的原因，我们建议您在开发环境中将 ER 配置设计为单独的 Dynamics 365 for Operations 实例：

-   担当**电子申报开发人员**角色或**电子申报功能顾问**角色的用户可编辑配置，并运行配置以进行测试。 此情况可能会导致调用类和表的方法，可能对业务数据和 Dynamics 365 for Operations 实例的性能产生负面影响。
-   在调用作为 ER 配置的 ER 数据源的类和表的方法时，不受 Dynamics 365 for Operations 入口点和记录的公司内容的限制。 因此，担当**电子申报开发人员**角色或**电子申报功能顾问**角色的用户可访问业务敏感数据。

在开发环境中的 ER 可以设计配置上载到配置的相应评估 (处理结果的集成、和) 正确性性能和质量保证的测试环境，例如角色先导访问权限和职责正确性划分的。 配置为交换启用的功能 ER 因此可以使用。 最后，您的 ER 配置在下图的任何可上载到 LCS，可以共享与服务订阅方，或者到生产环境出于内部使用目的，如显示。 ![配置 ER 生命周期](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>请参阅
--------

[电子申报概览](general-electronic-reporting.md)


