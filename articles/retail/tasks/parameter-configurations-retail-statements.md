---
title: 零售报表的参数配置
description: 此程序会演示零售参数的配置，这些参数会影响如何创建和过帐零售报表。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564285"
---
# <a name="parameter-configurations-for-retail-statements"></a>零售报表的参数配置

[!include[task guide banner](../includes/task-guide-banner.md)]

此程序会演示零售参数的配置，这些参数会影响如何创建和过帐零售报表。 此程序使用 USRT 演示公司。

1. 转到“零售和商业”>“总部设置”>“参数”>“零售参数”。
2. 单击“过帐”选项卡。
    * 如果您想要专门过帐定期折扣金额，请选择“是”。  
    * 选择“标准”以使用默认科目，或者如果您想要定义每个定期折扣使用哪个科目，则选择“定期”。  
    * 如果库存行应尽可能进行合计，请选择“摘要”。  
    * 如果发票和付款应作为报表过帐流程的一部分自动结算，请选择“是”。  
    * 如果金库投箱交易应进行合计，请选择“是”。  
    * 如果金库投箱交易应进行合计，请选择“是”。  
    * 选择“是”以打开合并，以过帐报表。  
    * 将报表过帐时，选择“是”，以并行创建和处理订单。  
    * 输入每个批处理作业任务中处理的最大订单数。  
3. 单击“保存”。

