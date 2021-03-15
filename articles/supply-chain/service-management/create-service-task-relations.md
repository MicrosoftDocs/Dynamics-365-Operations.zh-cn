---
title: 创建服务任务关系
description: 您可以将服务任务和服务管理或服务订单进行关联，以便介绍针对协议或订单要完成了的服务任务。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e5fd978c1e9db7e7ce3c06bbeb45b59854f1582
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974652"
---
# <a name="create-service-task-relations"></a>创建服务任务关系    

[!include [banner](../includes/banner.md)]

您可以将服务任务和服务管理或服务订单进行关联，以便介绍针对协议或订单要完成了的服务任务。 此信息可用于服务技术人员和客户。

## <a name="create-a-relation-with-a-service-agreement"></a>创建与服务协议的关系

1.  单击 **服务管理** \> **常用** \> **服务协议** \> **服务协议**。

2.  选择某一现有服务协议，或者创建新的服务协议。

3.  在“操作窗格”上，单击 **服务任务** 按钮。

4.  在 **服务任务** 窗体上，按 Ctrl+N 创建新行，然后从 **服务任务** 列表中选择某个服务任务以将该服务任务附加到服务管理。

5.  在 **说明** 选项卡上，在自由文本字段中输入任何内部工作记录或外部工作记录描述。

6.  关闭该窗体以保存记录。

重复此步骤，直到为该服务协议创建了所有必需的服务任务关系。 您现在可为任何附加的协议行指定这些服务任务。

对某一服务协议创建的服务任务关系将可用于附加到该服务协议的所有服务订单。

## <a name="create-a-relation-with-a-service-order"></a>创建与服务订单的关系

1.  单击 **服务管理** \> **通用** \> **服务订单** \> **服务订单**。

2.  选择某一现有服务订单，或者创建新的服务订单。

3.  在“操作窗格”上，单击 **服务任务** 按钮。

4.  从 **服务任务** 窗体，按 Ctrl+N 创建新行，然后从 **服务任务** 列表中选择某个服务任务以将该服务任务附加到服务管理。

5.  在 **说明** 选项卡上，在自由文本字段中输入任何内部工作记录或外部工作记录描述。

6.  关闭该窗体以保存记录。

重复此步骤，直到为该服务订单创建了所有必需的服务任务关系。 您现在可选择在创建服务订单行时创建了其关系的服务任务。

在某一服务订单上创建的服务任务关系可用于特定的服务订单。

## <a name="see-also"></a>请参阅

[服务任务概览](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]