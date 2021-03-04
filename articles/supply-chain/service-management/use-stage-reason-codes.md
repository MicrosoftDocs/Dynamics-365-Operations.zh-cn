---
title: 使用阶段原因代码
description: 使用原因代码指示服务级别协议 (SLA) 已取消的原因，或者服务订单超出您在 SLA 中定义的时限的原因。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74594871e9eeed86ae2914d1e5a08c0af28ab643
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423152"
---
# <a name="use-stage-reason-codes"></a>使用阶段原因代码 

[!include [banner](../includes/banner.md)]


使用原因代码指示服务级别协议 (SLA) 已取消的原因，或者服务订单超出您在 SLA 中定义的时限的原因。

您还可以指定在 SLA 取消时要求的原因代码，或者时限超出您在 SLA 中为服务订单指定的时间时的原因代码。

如果已指定要求的原因代码，则必须在以下情况中输入原因代码：

  - 当服务订单移到根据该服务订单 SLA 停止时间记录的阶段。

  - 在服务订单通过验证时。

  - 时间记录手动停止时。

## <a name="set-up-reason-codes"></a>设置原因代码

1.  单击 **服务管理** \> **设置** \> **服务订单** \> **阶段原因代码**。

2.  在 **阶段原因代码** 窗体中，单击 **新建** 以新建原因代码。

3.  在 **阶段原因代码** 字段中，输入唯一的阶段原因代码。

4.  在 **说明** 字段中，输入阶段原因代码的描述。

5.  关闭窗体以保存您所做更改。

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>在取消服务级别协议时要求提供原因代码

1.  单击 **服务管理** \> **设置**\> **服务管理参数**。

2.  在 **服务管理参数** 窗体中，单击 **常规** 链接，然后选中 **取消的原因代码** 复选框。

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>在服务订单超出服务级别协议设置的时限时需要原因代码。

1.  单击 **服务管理** \> **设置**\> **服务管理参数**。

2.  在 **服务管理参数** 窗体中，单击 **常规** 链接，然后选中 **超过时间的原因代码** 复选框。

## <a name="see-also"></a>请参阅

[开始和停止针对服务订单的时间录制](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]