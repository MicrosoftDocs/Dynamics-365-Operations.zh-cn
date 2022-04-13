---
title: 库存日记帐工作流一直没有完成，日记帐无法处理
description: 提交日记帐审批工作流后，工作流处理将停止响应，您无法编辑或处理日记帐。
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 5e8168a20a1fa4f52d28129eebb9931b31157ced
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/26/2022
ms.locfileid: "8488958"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>库存日记帐工作流一直没有完成，日记帐无法处理

## <a name="symptoms"></a>故障特征

提交日记帐审批工作流后，工作流处理将停止响应，您无法编辑或处理日记帐。

## <a name="resolution"></a>解决方法

有几种原因可能导致工作流处理无法完成。 请检查以下问题：

- 转到 **库存管理 &gt; 设置 &gt; 库存管理工作流**，查看受影响的工作流的配置。 有关详细信息，请参阅[库存日记帐审批工作流](../../inventory/inventory-journal-workflow.md)。
- 工作流可能遇到异常或错误。 查看受影响的工作流的工作项历史记录是否包含终止工作流的应用程序错误。
- 库存日记帐只有在获得批准后才能进行更新或编辑。 如果撤回可用，您可以尝试撤回日记帐。 工作流批处理作业的执行可能由于多个原因被暂停。 有些原因可能是由工作流框架问题引起的。
