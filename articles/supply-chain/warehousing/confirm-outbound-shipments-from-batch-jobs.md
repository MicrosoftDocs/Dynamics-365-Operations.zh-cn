---
title: 确认来自批处理作业的出站装运
description: 本主题介绍如何设置自动确认准备装运负荷的出站转移单装运的批处理作业。
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422763"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>确认来自批处理作业的出站装运

[!include [banner](../includes/banner.md)]

本主题介绍如何设置自动确认准备装运负荷的出站转移单装运的批处理作业。 这里介绍的批处理作业仅适用于转移单装运，不适用于销售订单。

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>启用“从批处理作业确认出站装运”功能

此功能只有在系统中启用了之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)页面检查功能状态，并在需要时启用。 此功能的清单如下：

- **模块** - *仓库管理*
- **功能名称** - *从批处理作业确认出站装运*

## <a name="process-outbound-shipments"></a>处理出站装运

设置计划的批处理作业来为准备装运的负荷运行出站装运确认：

1. 转到 **仓库管理 \> 定期任务 \> 处理出站装运**。
1. **确认装运** 对话框将打开。 在 **要包括的记录** 快速选项卡中，选择 **筛选**。
1. 查询编辑器对话框将打开。 在 **范围** 选项卡上，添加具有以下值的行：
    - **表** - *负荷*
    - **派生表** - *负荷*
    - **字段** - *负荷状态*
    - **条件** - *已装载*
1. 选择 **确定** 返回到 **确认装运** 对话框。
1. 在 **在后台运行** 快速选项卡上，将 **批处理** 设置为 **是**。
1. 在 **在后台运行** 快速选项卡上，选择 **重复执行**。
1. **定义重复执行** 对话框将打开。 根据业务需要设置运行计划。
1. 选择 **确定** 返回到 **确认装运** 对话框。
1. 在 **确认装运** 对话框中选择 **确定**，将批处理作业添加到批处理队列中。

有关详细信息，请参阅[批处理概览](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]