---
title: 库存日记帐已锁定，工作流批处理作业不工作
description: 您的其中一个库存日记帐被某个操作锁定，没有解锁
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
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475661"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>库存日记帐已锁定，工作流批处理作业不工作

## <a name="symptoms"></a>故障特征

您的其中一个库存日记帐被某个操作锁定，没有解锁。 例如，如果在过帐过程中发生未知错误（这是系统锁定操作），日记帐可能保持系统锁定状态。 在这种情况下，工作流工作项处理程序在进行锁定验证时将抛出错误。

## <a name="resolution"></a>解决方法

请登录到 Supply Chain Management 的 SQL Server 实例，检查 **InventJournalTable.SystemBlocked** 是否设置为 *1*。 如果是，请确保该日记帐不应该处于锁定状态，然后将 **InventJournalTable.SystemBlocked** 重置为 *0*。
