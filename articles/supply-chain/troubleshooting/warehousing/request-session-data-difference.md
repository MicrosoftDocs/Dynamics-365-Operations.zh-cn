---
title: 测试期间请求和会话数据之间的意外差异
description: 仓库应用任务验证结果中的请求和会话数据之间出现意外差异。
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456931"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>测试期间请求和会话数据之间的意外差异

错误代码：WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>故障特征

当您使用[仓库应用任务验证框架](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat)时，验证器返回以下错误消息：

> 请求和会话数据之间的意外差异。 违反了仓库移动设备 XML 协议。REQUEST_XML_TAMPERING

## <a name="cause"></a>原因

测试运行中成功运行的最后一步的输出与为下一步记录的输入不匹配时，就会发生错误。 这种情况可能会出现，因为任务验证器不使用前一步的输出作为后续步骤的输入。 相反，它使用记录的 XML 作为每个步骤的输入。

大多数情况下，重新运行任务时会出错，但测试需要一些由以前运行的同一任务所修改或删除的记录。

## <a name="resolution"></a>解决方法

仓库应用任务验证测试运行不是等幂操作，但会修改底层数据。 因此，在重新运行任务之前，您可能必须重置相关数据。

1. 查看上次成功测试步骤的输出 XML 以确定您的测试运行停止的位置。
1. 检查您的测试，并确保所有必需的销售订单、转移订单、工作表头和其他记录仍然存在并处于预期状态。
1. 重新创建或编辑缺失或修改的记录。 或者，创建新的测试设置，并设计测试以使用有效的现有记录。
