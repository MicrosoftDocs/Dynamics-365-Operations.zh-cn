---
title: 负责审核不符合项的工作人员
description: 本主题介绍如何配置负责审核不符合项的工作人员。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d3f647de2c188661c2c9c5f31e2642c3f8ca0b5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021772"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>负责审核不符合项的工作人员

[!include [banner](../includes/banner.md)]

本主题介绍如何配置负责审核不符合项的工作人员。

必须先审核不符合项，然后用户才能够开始输入更正或操作等详细信息。 必须先将用户的用户 ID（用户记录）链接到工作人员记录，然后用户才能够批准或拒绝不符合项。 您可以选择配置负责质量的工作人员，然后允许一个工作人员代表另一个工作人员审核工作。

## <a name="enable-a-user-for-nonconformance-processing"></a>支持用户进行不符合项处理

您必须先将用户的用户记录链接到工作人员记录，然后用户才能够批准或拒绝不符合项。 然后审核字段可以自动设置，并可以为工时单自动填充当前用户。 您必须先在用户的用户选项中启用文档处理，然后用户才能够使用文档注释。

1. 转到 **系统管理 \> 用户 \> 用户**。
1. 查找并打开应该可以批准或拒绝不符合项的用户。
1. 将 **人员** 字段设置为与当前用户记录相关的工作人员的姓名。
1. 在操作窗格上，选择 **用户选项**。
1. 在当前用户记录的 **选项** 页面上的 **首选项** 选项卡上，将 **启用文档处理** 选项设置为 *是*。
1. 关闭页面。

## <a name="define-workers-that-are-responsible-for-quality"></a>定义负责质量的工作人员

1. 转到 **库存管理 \> 设置 \> 质量控制 \> 负责质量的工作人员**。
2. 在操作窗格上，选择 **新建**。
3. 在 **工作人员** 字段中，选择输入质量数据的工作人员。
4. 在 **负责工作人员** 字段中，选择所选工作人员代表其参与工作的工作人员。 不符合项创建和更新时，此工作人员默认将被输入到 **工作人员** 字段中。

## <a name="additional-resources"></a>其他资源

- [质量管理概览](quality-management-processes.md)
- [启用质量和不符合项管理](enable-quality-management.md)
- [质量费用](quality-charges.md)
- [不符合项的隔离区域](quality-quarantine-zones.md)
- [不符合项的诊断类型](quality-diagnostic-types.md)
- [不符合项的质量费用](quality-charges.md)
- [不符合项的操作](quality-operations.md)
- [仓库流程质量管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
