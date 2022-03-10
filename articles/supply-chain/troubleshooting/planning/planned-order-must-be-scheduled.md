---
title: 计划生产订单必须在确认之前进行计划
description: 当您尝试确认计划订单时，将收到一条错误消息，指示订单必须在确认之前进行计划。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a89f5f98895be5b934dbdc1194fa58b9af34f9cbc7f5e2092f6f47791dd52400
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777735"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>计划生产订单必须在确认之前进行计划

错误代码：SYS309802

## <a name="symptoms"></a>故障特征

当您尝试确认计划订单时，将收到以下错误消息：

> 确认计划生产订单之前，必须对其进行计划。

## <a name="cause"></a>原因

计划的开始和结束日期不能为空。

## <a name="resolution"></a>解决方法

若要为计划订单指定开始和结束日期，请按照以下步骤操作。

1. 转到 **主计划 \> 主计划 \> 计划订单**。
1. 打开相关计划订单。
1. 在 **常规** 快速选项卡上的 **计划** 部分中，在 **开始日期** 和 **结束日期** 字段中指定日期。
