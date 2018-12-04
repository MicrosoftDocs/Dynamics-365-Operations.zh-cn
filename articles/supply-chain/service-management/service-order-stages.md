---
title: "服务订单阶段"
description: "通过定义服务订单的阶段并将其分配给工作人员，您可以通过服务组织中的不同人员所执行的任务来控制服务订单的流程。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9aa90dfcfc4b30d6cb4fa7ed4e6faaf505548d41
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="service-order-stages"></a>服务订单阶段   

[!include [banner](../includes/banner.md)]


您可以设置服务订单的阶段来定义必须完成的任务、完成的订单以及负责完成它们的工作人员。 通过定义服务订单的阶段并将其分配给工作人员，您可以通过服务组织中的不同人员所执行的任务来控制服务订单的流程。 阶段序列中必须包含一个初始阶段。

还可以定义每个阶段中所允许的操作。 例如，如果清除所有阶段（最后阶段除外）的**过帐**复选框，您可以防止过帐尚未经过完整阶段序列处理的任何服务订单。

## <a name="branching-in-service-order-stages"></a>服务订单阶段中的分支

在您设置服务阶段时，可以创建多个选项或分支，以便下一个服务阶段从中进行选择。 在完成初始阶段后，您可以从所有创建可用的分支中进行选择。 例如，您设置**计划**作为初始阶段。 创建名为**进行中**和**取消**的两个阶段，然后选择**计划**作为它们的父阶段。 将**计划**阶段分配到销售订单。 在完成销售订单的计划阶段后，如果销售订单准备工作，您可以选择**进行中**阶段，或者如果取消了销售订单，则可以选择**取消**阶段。

## <a name="see-also"></a>请参阅

[设置服务订单阶段](set-up-service-order-stages.md)

[更改服务订单阶段](change-service-order-stage.md)

  



