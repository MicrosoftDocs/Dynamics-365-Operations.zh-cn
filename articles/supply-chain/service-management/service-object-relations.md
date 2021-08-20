---
title: 服务对象关系
description: 您可以在服务对象和服务协议或服务订单之间创建服务对象关系。
author: ShylaThompson
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f69d9a73f5d6858c2e898999d068c5f7c7ada68812d3cf5f9557fe6ed9765b0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767967"
---
# <a name="service-object-relations"></a>服务对象关系 

[!include [banner](../includes/banner.md)]

您可以在服务对象和服务协议或服务订单之间创建服务对象关系。 在您创建某一关系时，将服务对象附加到服务协议或服务订单。

在创建该关系后，您可以将服务对象附加到服务协议或服务订单上的任何行。

## <a name="template-boms"></a>物料清单模板

您还可为对象关系指定物料清单模板。 物料清单模板是您对其执行服务的对象的物料清单。 如果您在执行服务的过程中更换了服务对象的某一组件部分，则可以通过使用“服务对象”窗体在服务物料清单中登记此更改。

## <a name="example"></a>示例

您针对在客户站点为两台电梯提供的服务创建了一个服务协议。
该服务协议的 ID 标识符为 SAL-001。

这两台电梯在“服务对象”窗体中分别作为 EL-S/1000 对象和 EL-L/1000 对象设置。

您将这两个服务对象（EL-S/1000 和 EL-L/1000）附加到该服务协议。

您想要在物料清单中登记服务对象的更改，因为您更换了该对象的组件部分；因此，您将某一服务物料清单附加到该服务对象关系，如下表中所述。

| 服务对象 | 关系 – 服务协议 | 服务物料清单   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | BOM-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | BOM-EL-L/1000 |

因为存在该协议的服务对象关系，所以您现在可以创建服务协议行，行中具有下表中显示的这些对象。

| 交易记录类型 | 类别           | 服务对象 |
|------------------|--------------------|----------------|
| 工时             | 检查         | EL-S/1000      |
| 工时             | 变速箱清洁  | EL-S/1000      |
| 物料             | 清洁材料 | EL-S/1000      |
| 工时             | 检查         | EL-L/1000      |
| 工时             | 变速箱清洁   | EL-L/1000      |
| 物料             | 清洁材料 | EL-L/1000      |

在登门服务期间，您必须更换电梯 EL-S/1000 的变速箱。 为了更换该对象的零部件，您可以通过使用为当前服务协议设置的服务对象关系访问物料清单设计器。

通过使用服务对象关系访问物料清单设计器

1. 服务协议
2. 双击某个服务协议，或单击“服务协议”以创建一个服务协议。
3. 单击“设置”选项卡。
4. 若要将某一物料清单模板附加到该服务协议，请单击“服务对象”。
5. 在“服务对象”窗体中，单击“设计器”打开“设计器”窗体以修改模板“物料清单”。

## <a name="automatically-created-service-orders"></a>自动创建了服务订单

如果为某一服务协议自动创建服务订单，则该协议中的服务对象关系也处于已创建的服务订单中。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]