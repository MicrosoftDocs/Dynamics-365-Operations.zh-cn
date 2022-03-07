---
title: 不符合项的问题类型
description: 本主题介绍如何创建和使用不符合项的问题类型。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ded53fd273ace8a6ed7f37219ca50ade329d9f08249596b524b1e3673d6ad547
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744814"
---
# <a name="problem-types-for-nonconformances"></a>不符合项的问题类型

[!include [banner](../includes/banner.md)]

本主题介绍如何创建和使用不符合项的问题类型。

您将使用 **问题类型** 页定义各个不符合项类型可能遇到的质量问题的分类。 对于创建的每个问题类型，您必须指定可以使用该问题类型的不符合项类型。 您可以设置以下不符合项类型：

- **内部** – 此类型的不符合项与现有库存量相关（例如，质检订单或隔离订单）。
- **客户** – 此类型的不符合项与销售订单相关。
- **供应商** – 此类型的不符合项与采购订单相关。
- **服务请求** – 此类型的不符合项与服务订单相关。
- **生产** – 此类型的不符合项与批次订单或生产订单相关。
- **联产品生产** – 此类型的不符合项与联产品的批次订单相关。

当您创建新的问题类型时，在操作窗格上选择 **不符合项类型** 可以创建一个或多个为该问题类型授权的不符合项类型的列表。 例如，与某一缺陷代码相关的问题类型可以应用于所有不符合项类型。 但是，与客户投诉相关的问题类型只能应用于 **客户** 和 **服务请求** 不符合项类型。

## <a name="examples-of-problem-types"></a>问题类型的示例

以下是可用于不同不符合项类型的问题类型的一些场景示例：

- **客户：** 客户提出投诉、客户发起退货或未达到质量规范。
- **供应商：** 产品损坏、未达到质量规范或接收了错误产品。
- **服务请求：** 未达到质量规范、客户提出投诉或需要维修机器。
- **生产：** 未达到质量规范、需要维修机器或产品损坏。
- **联产品生产：** 未达到质量规范、需要维修机器或产品损坏。

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>创建问题类型并将其分配给不符合项类型

1. 转到 **库存管理 \> 设置 \> 质量管理 \> 问题类型**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，针对新行设置以下字段：

    - **问题类型** – 输入问题类型的唯一 ID 或名称。
    - **描述** – 输入问题类型的详细描述。

1. 在仍选择新行的同时，在操作窗格上选择 **不符合项类型**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，对于新行，将 **不符合项类型** 字段设置为您要允许问题类型使用的不符合项类型。
1. 对要为问题类型授权的每个其他不符合项类型重复上述步骤。
1. 关闭页面。

## <a name="additional-resources"></a>其他资源

- [质量管理概览](quality-management-processes.md)
- [启用质量和不符合项管理](enable-quality-management.md)
- [负责审核不符合项的工作人员](quality-responsible-workers.md)
- [不符合项的隔离区域](quality-quarantine-zones.md)
- [不符合项的诊断类型](quality-diagnostic-types.md)
- [不符合项的质量费用](quality-charges.md)
- [不符合项的操作](quality-operations.md)
- [仓库流程质量管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
