---
title: 科目结构激活性能增强
description: 本文将介绍科目结构激活流程的新性能增强。
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713990"
---
# <a name="account-structure-activation-performance-enhancement"></a>科目结构激活性能增强

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

此性能增强将帮助您通过同时运行多个交易记录更新来加快激活科目结构。 此外，此结构在经过验证后将被标记为“活动”，并且在将现有未过帐交易记录更新到新结构时，交易记录处理可以继续进行。 由于交易记录更新可能需要花费一些时间，因此您可以通过选择 **科目结构** 页面中网格上方的 **查看激活状态** 来跟踪激活状态。 您还可以通过选择操作窗格上的 **查看**，然后选择下拉菜单中的 **激活状态** 来查看激活状态。

[![科目结构页面。](./media/AccountStructure1.png)](./media/AccountStructure1.png)

在选择 **查看激活状态** 后，将出现一个对话框，显示作为激活流程的一部分运行的各个任务。 您可以查看每个任务的状态，并在任务完成后查看完成日期和时间。

[![科目结构激活时间线。](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>科目结构激活提示

在为草稿科目结构选择 **激活** 后，将出现科目结构激活对话框，该对话框包含一个名为 **更新未过帐的交易记录** 的选项卡部分。 该部分包括一个名为 **强制更新** 的选项。 您可以选择此选项以将所有未过帐的交易记录更新到当前结构。 但是，仅当出现错误或 Microsoft 支持部门指示您使用此选项时，才应使用此选项。

以下是可能会影响激活流程性能的一些因素：

- 大量未过帐的日记帐记录
- 大量未结的原始凭证记录，例如普通发票、供应商发票以及使用原始凭证框架并具有未完成会计分配的相关单据
- TaxUncommitted 中的数据量
- 未结预算数据量
- 在激活任务仍在运行时导入日记帐数据

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
