---
title: 维护条码类型
description: 该过程显示如何设置新条码定义，这可作为领料单报表的一部分。
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 052311e15aeb20b927cbed217a2bda600dad60a5
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345642"
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