---
title: 未为批次订单审核选择的配方编号
description: 当您尝试确认计划订单时，将收到一条错误消息，指示未为批次订单审核选择的配方编号。
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
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712902"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>未为批次订单审核选择的配方编号

错误代码：PRO2614

## <a name="symptoms"></a>故障特征

当您尝试确认计划订单时，将收到以下错误消息：

> 未为批次订单审批选择的配方编号。

## <a name="cause"></a>原因

系统验证确认操作以确保审核的配方可用于活动物料。 您可能必须审核该配方。

## <a name="resolution"></a>解决方法

若要审核配方，请按照以下步骤操作。

1. 转到 **产品信息管理 \> 物料清单和配方 \> 配方**。
1. 选择相关配方。
1. 在操作窗格上的 **配方** 选项卡上，在 **维护** 组中，选择 **审核配方**。
1. 在 **审核物料清单或配方** 对话框中，选择审批者，然后选择 **确定**。
