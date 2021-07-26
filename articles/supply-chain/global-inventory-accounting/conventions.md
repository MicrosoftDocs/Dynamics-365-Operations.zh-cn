---
title: 惯例
description: 本主题介绍了如何设置惯例以确定应如何在全球库存核算中核算成本。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 74d99d3eefdcaaa7f6551668990b702396b32ffc
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273120"
---
# <a name="conventions"></a>惯例

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

惯例是一组影响系统行为的策略的容器。 基于您的业务需求，必须使用各种策略的组合来定义惯例，这些策略用于确定应如何在全球库存核算中核算成本。 您可以将每个惯例与一个或多个分类帐相关联，以确保跨分类帐应用的核算策略的一致性。

若要设置您的惯例，请转到 **全球库存核算 \> 设置 \> 惯例**。 对于每个惯例，设置以下字段：

- **名称** – 输入惯例的名称。
- **描述** – 输入惯例的描述。
- **成本对象策略** – 选择成本对象策略。 这些策略确定系统应用于计算和维护库存值的粒度级别。 以下预定义选项可用：

    - 产品
    - 产品 – 站点
    - 产品 – 站点 – 仓库

    例如，如果您选择 *产品 – 站点*，对于每个库存移动（流入或流出），系统都会在站点级别计算和维护每个产品的库存成本。 因此，较低级别（例如仓库级别）的库存移动不会影响库存价值。 （仓库级别转移的一个示例是一个站点中两个仓库之间的物料转移。）同样，您无法在较低级别（例如仓库级别）查看库存成本。

- **输入度量依据策略** – 选择输入度量依据策略。 这些策略确定应流入库存科目的成本和应收取的成本。 以下选项与贸易公司相关：

    - **普通历史** – 所有成本构成都流入库存科目。
    - **标准** – 标准成本流入库存科目，向差异科目收取应用成本与实际成本之间的差额。 如果您想要创建 *标准* 输入度量依据策略，必须首先创建一个价目表，策略可以在其中查找物料的标准成本。
    - **价目表** – 全球库存核算支持从多个法人获取物料价格。 您可以定义输入度量依据策略将使用的价目表。 这样，系统就会知道在哪里查找物料价格。 按照以下步骤设置价目表：

        1. 在 **名称** 字段中输入名称。
        1. 在 **描述** 字段中，输入描述。
        1. 在 **成本计算类型** 字段中，选择成本计算类型（*标准成本* 或 *计划成本*）。
        1. 在 **价格类型** 字段中，选择价格类型（*成本*、*购买* 或 *销售价*）。
        1. 添加成本计算版本。
        1. 在操作窗格上，选择 **价格** 以验证价目表上的物料价格。

- **成本流假设政策** – 选择成本流假设策略。 这些策略确定如何从库存中删除成本并将其报告为所售货物成本。 以下预定义选项可用：

    - 平均
    - 特定 – 批次

    > [!NOTE]
    > 全球库存核算是一个永久库存系统。 因此，系统基于每笔交易跟踪库存价值。

- **成本元素策略** – 您可以定义成本元素策略并将它们链接到此字段。 *成本元素* 是事件所消耗的资源的成本。 您可以使用成本元素跟踪成本并对其进行分类。 若要创建成本元素策略，请在以下位置输入信息：

    - **名称** 字段
    - **描述** 字段
    - **成本元素** 列表
    - **规则** 网格

    如果您不想要对库存价值进行进一步细分，必须仍然创建具有单个成本元素的成本元素列表。 然后，必须创建成本元素策略，以将所有相关的度量类型（成本构成）映射到该成本元素。