---
title: 不符合项操作的费用
description: 本主题介绍如何创建可与不符合项的操作一起使用的质量费用。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 382890232bff47a885840af1eb7e91d27bb46cae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022292"
---
# <a name="charges-for-nonconformance-operations"></a>不符合项操作的费用

[!include [banner](../includes/banner.md)]

本主题介绍如何创建可与不符合项的操作一起使用的质量费用。

您可以使用 **质量费用** 页定义可以向不合格项的操作添加的费用类型。 费用让您可以跟踪您因未达标产品欠客户的费用，或供应商因您收到的未达标产品而欠您的费用的详细信息。 您还可以使用费用跟踪外部供应商或服务执行操作所需的成本。

## <a name="examples-of-quality-charges"></a>质量费用示例

您在一家制造公司工作。 您的公司与多家供应商签订了合同。 这些合同概括了物料按时装运、损坏和产品质量的标准。 同样，您的一些客户与您的公司已就退货、损坏和产品质量达成协议。

每种情况都定义了费用结构，并在合同中加以指定。 您可以配置质量费用来概括各个费用类型，如 *损坏*、*延迟装运* 和 *质量*。 然后，当您创建不符合项时，您将添加一个或多个操作。 对于每个操作，您选择 **费用** 来定义有关费用的详细信息。

## <a name="create-a-quality-charge"></a>创建质量费用

1. 转到 **库存管理 \> 设置 \> 质量管理\> 质量费用**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，针对新行设置以下字段：

    - **费用代码** – 为质量费用输入唯一 ID 或名称。
    - **描述** – 输入质量费用的详细描述。

1. 关闭该页面。

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a>向不符合项的操作添加质量费用

有关如何将操作添加到不符合项并向其应用费用的详细信息，请参阅[不符合项的操作](quality-operations.md)。

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
