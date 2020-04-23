---
title: 服务模板
description: 您可以将某一服务协议定义为模板，并且以后将该模板上的行复制到其他服务协议或服务订单中。
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9d8ebcb2e59fae58f0701b529674cf1f9876c6b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206833"
---
# <a name="service-templates"></a>服务模板

[!include [banner](../includes/banner.md)]

您可以将某一服务协议定义为模板，并且以后将该模板上的行复制到其他服务协议或服务订单中。

## <a name="example"></a>示例

您向其提供服务的客户在 5 个不同的地点具有完全相同的服务电梯。

您想要为该客户设置 5 个服务协议，每个站点一个。
为了减少重复性的设置工作，并且确保服务协议中的设置信息完全相同，您创建了一个服务协议，并且将该服务协议指定为用于电梯服务工作的模板。

您现在可以将模板行复制到这 5 个新的服务协议中，以便每个服务协议都用来自该模板的行填充。

## <a name="create-a-template"></a>创建模板

在您创建服务模板时，创建一个服务协议，在该服务协议上创建所需行，然后将该服务协议附加到某一服务模板组。

> [!NOTE]
> 只有当没有服务订单附加其上时，某一个服务协议才能定义为一个模板。 此外，不能从已定义为模板的服务协议生成服务订单。

## <a name="copy-template-lines"></a>复制模板行

您可以将模板行从一个服务模板复制到其他服务协议或服务订单中。

在您将模板行复制到您的服务订单或服务协议中时，您的模板组将显示在一个树视图中，其中每个组都可以扩展。 通过此显示，您可以查看每个模板和模板行。

如果您已基于反映模板用途的名称对模板进行分组，则可以更容易地确定要复制哪些服务模板行。

## <a name="related-topics"></a>相关主题

[复制服务模板行](copy-service-template-lines.md)
