---
title: 创建服务对象关系
description: 本主题介绍如何为服务协议和服务订单创建服务对象关系。
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 352d3b790da340102b7dbe116d9deeb2f3cbfc4e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985961"
---
# <a name="create-service-object-relations"></a>创建服务对象关系 

[!include [banner](../includes/banner.md)]


本主题介绍如何为服务协议和服务订单创建服务对象关系。 在您创建服务对象关系时，将服务对象关联到服务协议或服务订单。 当客户针对作为服务对象的物料请求服务时，您可以从服务对象关系列表中选择服务对象。

## <a name="create-a-service-object-relation-for-a-service-agreement"></a>为服务协议创建服务对象关系

使用以下步骤来为服务协议创建服务对象关系：

1.  单击**服务管理** \> **常用** \> **服务协议** \> **服务协议**。

2.  在**服务协议**列表中，选择某一现有服务协议，或单击**新建**来创建新服务协议。

3.  在**服务协议**窗体**操作窗格**，**服务协议**选项卡**关系**组中，单击**服务对象**。

4.  在**服务对象**窗体中，单击**新建**，然后为该服务协议选择服务对象。

5.  要将模板物料清单物料 (BOM) 分配到服务协议，请单击**功能**，然后选择 **附加物料清单模板**。 在**选择物料清单模板**窗体的**物料清单模板**字段中，选择一个模板。 

## <a name="create-a-service-object-relation-for-a-service-order"></a>为服务订单创建服务对象关系

使用以下步骤来为服务订单创建服务对象关系：

1.  单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。

2.  在**服务订单**列表中，选择某一现有服务订单，或创建新服务订单。

3.  在**服务订单**窗体**操作窗格**，**服务订单**选项卡**关系**组中，单击**服务对象**。

4.  在**服务对象**窗体中，单击**新建**，然后为该服务订单选择服务对象。

5.  要将物料清单模板分配到服务协议，请单击**功能**，然后选择 **附加物料清单模板**。 在**选择物料清单模板**窗体的**物料清单模板**字段中，选择一个模板。 


## <a name="see-also"></a>请参阅

[服务对象概览](service-objects.md)

[服务对象关系](service-object-relations.md)

[物料清单模板](template-boms.md)

  


