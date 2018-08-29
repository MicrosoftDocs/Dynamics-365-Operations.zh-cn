---
title: "电子设备 (ER) 中的公司间数据源"
description: "本主题介绍如何在电子申报 (ER) 中使用公司间数据源。"
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 201d0f1e3fddd662748008c7304d67ef6003ef02
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---

# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>电子设备 (ER) 中的公司间数据源

[!include[banner](../includes/banner.md)]

可以设计电子申报 (ER) 格式以生成各种格式的传出单据。 生成单据时，ER 格式调用在相应 ER 模型映射中配置的数据源。 若要配置对申请表的访问以检索记录，可使用**表记录**类型的 ER 数据源。 访问表为共享表（即表中的数据在保存时不带公司标识符）时，此数据源将返回所有记录。 访问表为依赖于公司的表（即表中的数据按公司保存）时，此数据源仅返回已为当前公司保存的记录（即，运行 ER 格式的公司环境）。

现在可将模型映射中类型为**表记录**的每个数据源标记为公司间。 因此，可使用类型为**表记录**的数据源访问申请表中的公司间数据。 

如果将一个数据源标记为公司间数据源，则将发生行为：

- 对于引用除 CompanyInfo 外的任何共享表的数据源，该数据源将返回所引用表中的全部记录。 
- 对于引用 CompanyInfo 表的数据源，即使 CompanyInfo 是共享表，该数据源仍然返回包含定义的范围中一家公司的标识符的记录。
- 对于任何依赖于公司的表，该数据源返回包含定义的范围中一家公司的标识符的所引用表的记录。

在系统查询对话框中，如果为标记为公司间的任何数据源开启了**要求查询**选项，则可在**公司范围**选项卡中手动选择要包括的一家或多家公司。

> [!IMPORTANT]
> 与其他筛选器不同，公司筛选器标记为在您运行 ER 格式时为查询最后使用的值。 如果更改数据源的公司间值，将不自动更改该筛选器。 若要为另一个数据源使用其他公司间值，请删除相应的用户特定选择。

对于标记为公司间的每个数据源，可通过在 ER 表达式中使用 **FILTER** 和 **WHERE** 函数选择所需记录。 **dataAreaID** 字段也可以用作公司标识符。 现在如果使用 **FILTER** 函数，则将 **dataAreaID** 字段限制为以下类型的条件： 

- 仅支持只有一个 **dataAreaID** 字段的条件。
- 仅允许具有的表达式不依赖于记录列表项的比较。

因此，以下表达式有效。

    FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
    While shown below expressions will not pass the validation:
    FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
    FILTER (MyTable, 
        OR(
            MyTable.dataAreaID = $StringUserInputParameter1,
            MyTable.dataAreaID = $StringUserInputParameter2
        )
    )

默认情况下，范围包括当前申请表的所有公司。 但是可以进行限制。 要对单个 ER 格式限制公司间数据访问的范围，请为该格式分配特定组织层次结构。 如果为 ER 格式定义层次结构，则仅返回所分配层次结构中存在的法人的记录，即使该格式调用公司间数据源也不例外。 如果为 ER 格式定义了对不再存在的层次结构的引用，将应用默认范围，并且该格式将调用公司间数据源。 在此情况下，将返回所有申请公司的记录。 

请注意，如果为分配给单个 ER 格式的组织层次结构开启**使用草稿**选项 ，将使用该层次结构的草稿版本中的法人识别公司间数据源的范围。 如果不存在草稿版本，则为其使用该组织层次结构的最近发布版本中的法人。

请注意，如果为分配给单个 ER 格式的组织层次结构关闭**使用草稿**选项 ，将使用该组织层次结构的最近发布版本中的法人识别公司间数据源的范围。 ER 框架中不支持组织层次结构的日期有效性。

可在可从 ER 工作区访问的特定页中将该层次结构分配给某个格式，或通过使用**组织管理 -> 电子申报 -> 格式的法人筛选器**菜单项分配。 若要访问该页，必须为用户授予**维护格式的法人筛选器**权限 (ERMaintainFormatMappingLegalEntityFilters)。 除了用户可以在系统查询对话框中手动指定的限制，还将应用格式的基于层次结构的法人的范围限制。 运行格式时，将使用这些限制的重合部分。

若要了解此功能的详细信息，请播放任务指南 **ER 以公司间模式访问依赖于公司的表的记录**，该任务指南属于 7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程，可从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载。 此任务指南将引导您完成配置 ER 模型映射和 ER 格式以便以公司间模式访问申请表这一过程。

请下载以下文件以完成本任务指南：

- [ER 模型配置 - CrossCompanyDataAccessModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [ER 格式配置 - CrossCompanyDataAccessFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)

