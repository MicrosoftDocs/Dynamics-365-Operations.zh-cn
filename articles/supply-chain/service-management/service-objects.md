---
title: 服务对象概览
description: 本主题概述了如何处理服务对象。
author: kamaybac
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad758d32c6e9de0758c6fddb57a7dea886ab73d4
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986427"
---
# <a name="service-objects-overview"></a>服务对象概览

[!include [banner](../includes/banner.md)]

服务对象是您可以对其执行服务的客户的资产和产品。 根据您提供的服务类型，对象可以是有形对象或无形对象：

-  有形对象是您可对其执行实际服务任务的事物，例如机器或建筑物。

    有形服务对象还可以是您在“已发布产品详细信息”窗体中创建的库存物料。 根据您附加到该物料的库存维度组，您可以将服务对象创建为包括物料序列号的详细信息级别。 这在您必须跟踪服务对象表示的确切物料时非常有用。

    有形服务对象还可以是与公司的直接生产或供应链不直接相关的物料。 例如，服务订单中所于维修的工具包可以是库存中不包括的服务对象。 在这种情况下，您不能将其登记为库存物料。

-  无形对象是对其执行服务任务的抽象实体，例如一组帐户或法律文档。

## <a name="example-of-an-intangible-service-object"></a>无形的服务对象的示例

公司 A 维护多个小公司的财务记录。 公司 A 的客户之一是当地的足球队，公司 A 每周对其进行记帐并且每年审计该俱乐部的帐户。 该俱乐部的帐户在“服务对象”窗体中设置，并且指定为服务协议中的对象。 对于该对象有两个服务协议行。 第 1 行是具有分配到行的每周间隔的每周记帐；第 2 行是具有分配到行的每年间隔的每年审计。

## <a name="related-topics"></a>相关主题

[创建服务对象](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]