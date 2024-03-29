---
title: 开始和停止针对服务订单的时间录制
description: 开始和停止针对服务订单的时间录制。
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b110c6a08d946b4527f47f6d4181819f3508fee
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016324"
---
# <a name="start-and-stop-time-recording-on-a-service-order"></a>开始和停止针对服务订单的时间录制 

[!include [banner](../includes/banner.md)]


使用此过程为已定义的服务级别协议的服务订单开始和停止时间记录。

## <a name="start-time-recording"></a>开始时间记录

1.  单击 **服务管理** \> **服务订单** \> **服务订单**。

2.  单击 **服务订单** 选项卡。在 **操作窗格** 上，在 **服务级别协议** 组中，单击 **开始**。

3.  输入应开始时间记录的日期和时间。

## <a name="stop-time-recording"></a>停止时间记录

1.  单击 **服务管理** \> **服务订单** \> **服务订单**。

2.  单击 **服务订单** 选项卡。在 **操作窗格** 上，在 **服务级别协议** 组中，单击 **停止**。

3.  输入应停止时间记录的日期和时间。

4.  选择 **添加撤回原因**，然后在 **阶段原因代码** 列表中选择一个原因代码提供停止时间记录的原因。


> [!NOTE]
> <P>如果在<STRONG>服务管理参数</STRONG>窗体中选择了<STRONG>超过时间的原因代码</STRONG>，则必须先提供原因代码，才能停止时间记录。</P>



## <a name="see-also"></a>请参阅

[启动 SLA 时间记录（窗体）](https://technet.microsoft.com/library/hh242297\(v=ax.60\))

[停止 SLA 时间记录（窗体）](https://technet.microsoft.com/library/hh242241\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]