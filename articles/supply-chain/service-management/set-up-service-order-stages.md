---
title: 设置服务订单阶段
description: 设置服务订单阶段。
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
ms.openlocfilehash: 557e688ddd1155aa475320365a5b6048759904fd
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670711"
---
# <a name="set-up-service-order-stages"></a>设置服务订单阶段 

[!include [banner](../includes/banner.md)]


1.  转到 **服务管理** \> **设置** \> **服务订单** \> **服务阶段**。

2.  选择 **新建** 创建新记录。

3.  在 **服务阶段** 和 **说明** 字段中，指定服务阶段 ID 和描述。

4.  为该阶段选择适当的参数。

5.  为当前阶段选择父阶段；如果该阶段是阶段设置中的初始阶段，则将 **父** 字段保留为空。


> [!NOTE]
> <P>在您保存了该阶段后，您不能修改<STRONG>父</STRONG>字段。 而是可以删除该记录，然后在<STRONG>父</STRONG>字段中使用不同的选择再次创建该记录。</P>
> <P>此外，您只能使用空白<STRONG>父</STRONG>字段创建一个阶段。 也就是说，只运行一个初始阶段。</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]