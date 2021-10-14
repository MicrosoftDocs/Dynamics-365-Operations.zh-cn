---
title: 服务订单
description: 本主题概述了如何处理服务订单。
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8dc88d445e1331e1532cb3b7385cda39c4f22e80
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566111"
---
# <a name="service-orders"></a>服务订单

[!include [banner](../includes/banner.md)]

服务订单表示服务技术人员在特定日期对某一客户站点的访问。 每个服务订单都由一个或多个服务订单行构成。 服务订单行表示必须由服务技术人员执行的工时和相关物料、支出和费用。

您可以将任务和对象服务订单行。 然后可以对服务订单行按任务或按对象。 您还可以将库存中列出的物料附加到服务订单行。

## <a name="create-service-orders"></a>创建服务订单

您可以创建在该协议包含基于服务协议和行的服务订单。 但是，您可以创建与某一服务协议只在期间中协议的服务订单。 例如，如果服务协议，适用于 2011 日历年中，您可以为协议创建服务订单从 2011 年 1 月 1 日和 2011 年 12 月 31 日。

您可以单独，还创建服务订单，而无需将其与协议。 这些服务订单来处理不定期或一次性服务访问。 在三月，您的客户决定对两台机器以及为服务协议指定的那些机器进行服务。 对于此任务，您创建服务订单，但不将其与协议。


> [!NOTE]
> 若要创建不与服务协议关联的服务订单，必须选中 **服务管理参数** 页面中的 **允许，但没有服务协议** 复选框。

### <a name="scenario"></a>应用场景

以下方案描述创建服务订单不与服务协议的其他情况很有用。

公司调度人员接到了一个电话，要求对电梯进行紧急服务。 不时间设置服务协议和服务的一个项目。 因此，调度人员直接在 **服务订单** 页面中创建服务订单，将服务订单附加到现有项目，然后创建服务订单行。 您可为现有服务订单创建一个任务或对象关系，以便记录与该服务协议无关的工作 (B)。 有关详细信息，请参阅[手动创建服务订单](create-service-orders-manually.md)和[创建服务任务关系](create-service-task-relations.md)。

## <a name="monitor-the-progress-of-service-orders"></a>监控服务订单的进度

您可为服务订单设置阶段系统，以便通过公司中的不同团队和工作流程反映某一服务订单的进度。 对于每个阶段，您可以指定允许的操作。 有关原因代码的详细信息，请参阅[创建原因代码](create-reason-codes.md)。

### <a name="example"></a>示例

服务订单都是由该调度审核。 该调度更新服务订单的阶段并指定原因代码指示的服务订单已下达给服务技术人员。 该服务技术人员前往该客户站点并且执行该服务订单。

## <a name="specify-item-requirements-for-service-orders"></a>为服务订单指定物料需求

您可以指定的服务订单所需的库存物料。 但是，必须将该服务订单与项目。 服务订单创建物料需求通过项目进行处理。 

### <a name="example"></a>示例

调度人员然后处理根据该服务协议创建的服务订单。 在第一个服务订单上，调度人员认识到服务技术人员需要现有库存中没有的一个重要备件。 因此，她直接从服务订单为该备件创建了一个物料需求。

## <a name="move-and-post-lines"></a>对行进行移动和过帐

服务技术人员从服务访问返回，然后修改和更新服务订单行。 在服务访问期间，此技术人员执行计划在下一次服务访问的服务工作。 因此，他将这些行从后续服务访问移到当前服务访问 (E)。 此技术人员然后过帐服务订单。 有关详细信息，请参阅[移动服务订单行](move-service-order-lines.md)。

## <a name="cancel-service-orders"></a>取消服务订单

为一月生成的其他服务订单之一已作废，因为该工作已取消。 因此，服务调度人员取消该服务订单。 有关详细信息，请参阅[取消服务订单](cancel-service-orders.md)。

## <a name="post-from-projects"></a>从项目过帐

在每周结束时，调度人员想要过帐附加到特定项目的所有服务订单。 因此，该调度在 **项目** 页面中查找相关项目，然后过帐已完成的服务订单。 有关详细信息，请参阅[过帐服务订单（类窗体）](https://technet.microsoft.com/library/aa574685\(v=ax.60\))。

## <a name="delete-service-orders"></a>删除服务订单

在下半年，您的客户认为服务访问次数过少。 您必须为服务协议的剩余时间创建新的、更频繁的服务访问系列。 因此，您必须删除现有已创建的服务订单并创建新的服务订单。 有关详细信息，请参阅[删除服务订单](delete-service-orders.md)。

## <a name="see-also"></a>请参阅

[服务订单（窗体）](https://technet.microsoft.com/library/aa554361\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]