---
title: 配置影响零售对帐单的参数
description: 此主题演示 Commerce 参数的配置，这些参数会影响如何创建和过帐对帐单。
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 7892a216d836ebcc297a5b7eb87bc996dd9b91bf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140822"
---
# <a name="configure-parameters-that-affect-retail-statements"></a>配置影响零售对帐单的参数

[!include [banner](../includes/banner.md)]

此主题演示 Commerce 参数的配置，这些参数会影响如何创建和过帐对帐单。 此程序使用 USRT 演示公司。

1. 在导航窗格中，转到**模块 > Retail 和 Commerce > 总部设置 > 参数 > Commerce 参数**。
2. 选择**过帐**选项卡。
    - 如果您想要专门过帐定期折扣金额，请选择**是**。  
    - 选择**标准**以使用默认科目，或者如果您想要定义每个定期折扣使用哪个科目，则选择**定期**。  
      - 如果库存行应尽可能进行合计，请选择**摘要**。  
      - 如果发票和付款应作为报表过帐流程的一部分自动结算，请选择**是**。  
      - 如果金库投箱交易应进行合计，请选择**是**。  
      - 如果金库投箱交易应进行合计，请选择**是**。  
      - 选择**是**以打开合并，以过帐报表。  
      - 将报表过帐时，选择**是**，以并行创建和处理订单。  
      - 输入每个批处理作业任务中处理的最大订单数。  
3. 选择**保存**。

