---
title: 零售交易记录一致性检查器
description: 本主题将介绍 Microsoft Dynamics 365 for Retail 中的零售交易记录一致性检查器功能。
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 972c4d6b244eebc85cc801353ce8fb25ecbc0655
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517009"
---
# <a name="retail-transaction-consistency-checker"></a>零售交易记录一致性检查器


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

本主题将介绍 Microsoft Dynamics 365 for Finance and Operations 版本 8.1.3 中推出的零售交易记录一致性检查器功能。 一致性检查器在对帐单过帐流程选择交易记录之前标识和隔离不一致的交易记录。

在 Retail 中过帐对帐单时，过帐会由于零售交易记录表中存在不一致的数据而失败。 导致数据问题可能是由于销售点 (POS) 应用程序中不可预料的问题，或者如果从第三方 POS 系统未正确导入交易记录。 这些不一致可能的显示方式包括： 

  - 标题表中的交易记录总计与行中的交易记录总计不匹配。
  - 标题表中的行计数与交易记录表中的行数不匹配。
  - 标题表中的税额与行中的税额不匹配。 
  
当对帐单过帐流程选择不一致的交易记录时，将创建不一致的销售发票和付款日记帐，因此整个对帐单过帐流程将失败。 从此类状态恢复对帐单涉及跨多个交易记录表的复杂数据修复。 零售交易记录一致性检查器可预防此类问题。

下图描述了使用交易记录一致性检查器的过帐流程。

![使用零售交易记录一致性检查器的对帐单过帐流程](./media/validchecker.png "使用零售交易记录一致性检查器的对帐单过帐流程")

**验证商店交易记录**批处理流程将检查以下方案的零售交易记录表的一致性。

- 客户帐户 - 验证零售交易记录表中的客户帐户是否存在于 HQ 客户主数据中。
- 行计数 - 验证交易记录标题表中获取的行数是否与销售交易记录表中的行数匹配。

## <a name="set-up-the-consistency-checker"></a>设置一致性检查器
通过**零售 \> 零售 IT \> POS 过帐**配置定期运行的“验证商店交易记录”批处理流程。 批处理作业可以基于商店组织层次结构进行计划，这与设置“成批计算对帐单”和“成批过帐对帐单”流程的方式相似。 我们建议您将此批处理流程配置为一天运行多次并对此进行计划，以便该批处理在每次执行 P 作业结束后运行。

## <a name="results-of-validation-process"></a>验证流程的结果
相应零售交易记录中标记了批处理流程执行的验证检查的结果。 零售交易记录中的**验证状态**字段设置为**成功**或**错误**，并且上次运行验证的日期显示在**上次验证时间**字段中。

要查看更多与验证失败相关的描述性错误文本，请选择相关的零售商店交易记录，然后单击**验证错误**按钮。

未通过验证检查的交易和尚未验证的交易将不会导入对帐单中。 在“计算报表”流程期间，如果存在本可以包括在对帐单中，但却未包括的交易，将会通知用户。

如果发现验证错误，则修复错误的唯一方式是与 Microsoft 支持联系。 在将来的版本中，将会增加相应功能，以便用户可以通过用户界面修复失败的记录。 此外，还将提供记录和审计功能，以跟踪修改历史记录。

> [!NOTE]
> 未来的版本中将增加支持多种方案的其他验证规则。
