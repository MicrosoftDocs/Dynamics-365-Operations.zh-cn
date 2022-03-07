---
title: 维护条码类型
description: 该过程显示如何设置新条码定义，这可作为领料单报表的一部分。
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b689d1fc85d59ac87efa1903fd7122ae5ff011da
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571105"
---
# <a name="maintain-bar-code-types"></a>维护条码类型

[!include [banner](../../includes/banner.md)]

该过程显示如何设置新条码定义，这可作为领料单报表的一部分。 您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。 如果您正在使用 USMF，则可以使用显示的示例值。 这些任务通常由仓库管理员完成。

1. 转到 **条码**。
1. 选择 **新建**。
1. 在 **条码设置** 字段中，键入一个值。
1. 在 **描述** 字段中，键入一个值。
1. 在 **条码类型** 字段中，选择一个选项。
    * 如果您使用 USMF，您可以选择“代码 39”。
1. 在 **掩码 ID** 字段中，指定条码掩码 ID。 条码掩码用于创建条码，以及快速标识扫描到销售点 (POS) 系统中的条码。 有关详细信息，请参阅[设置条码掩码](../../../commerce/set-up-bar-code-masks.md)。
1. 在 **大小** 字段中，输入一个数字。
1. 在 **最大长度** 字段中，输入一个数字。
1. 选择 **保存**。
1. 关闭该页面。
1. 转到 **库存和仓库管理参数**。
1. 在 **条码设置** 字段中，输入或选择一个值。
    * 选择您先前创建的条码设置，但请注意，条码格式必须匹配流程中使用的记录类型的唯一标识符的格式。 例如，对于领料路径，条码格式必须匹配领料路径引用的格式，这通常为一个序号。  
1. 选择 **保存**。
1. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
