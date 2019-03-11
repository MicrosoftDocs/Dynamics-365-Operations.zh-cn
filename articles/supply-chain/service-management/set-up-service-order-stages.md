---
title: 设置服务订单阶段
description: 设置服务订单阶段。
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30f6a6afa6ab91bed41bb19b8312dc7e25bd2478
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "366757"
---
# <a name="set-up-service-order-stages"></a>设置服务订单阶段 

[!include [banner](../includes/banner.md)]


1.  单击**服务管理** \> **设置** \> **服务订单** \> **服务阶段**。

2.  按 Ctrl+N 创建一条新记录。

3.  在**服务阶段**和**说明**字段中，指定服务阶段 ID 和描述。

4.  为该阶段选择适当的参数。

5.  为当前阶段选择父阶段；如果该阶段是阶段设置中的初始阶段，则将**父**字段保留为空。


> [!NOTE]
> <P>在您保存了该阶段后，您不能修改<STRONG>父</STRONG>字段。 而是可以删除该记录，然后在<STRONG>父</STRONG>字段中使用不同的选择再次创建该记录。</P>
> <P>此外，您只能使用空白<STRONG>父</STRONG>字段创建一个阶段。 也就是说，只运行一个初始阶段。</P>


  


