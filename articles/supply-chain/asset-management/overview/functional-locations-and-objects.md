---
title: 功能位置和资产
description: 本主题介绍资产管理中的功能位置和资产。 资产管理是 Dynamics 365 Supply Chain Management 中的一个高级模块，用于管理资产和维护作业。
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3a42d36fd137aa780886276a4235f1b8f3a3680
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653339"
---
# <a name="functional-locations-and-assets"></a>功能位置和资产

[!include [banner](../../includes/banner.md)]

 

本主题介绍资产管理中的功能位置和资产。 资产管理是 Dynamics 365 Supply Chain Management 中的一个高级模块，用于管理资产和维护作业。

## <a name="overview"></a>概览

资产管理与其他 Finance and Operations 应用的多个模块无缝集成。 下图显示界面和其他模块。

![显示资产管理如何与其他模块交互的图](media/01-overview-image.png)

资产管理可用于高效管理和执行与管理和服务公司中大量类型的设备有关的所有任务。 这些设备包括机器、生产设备和交通工具。 资产管理还支持多个行业的解决方案。

下图显示资产管理中包含的主要功能的概览。

![显示资产管理中的主要功能的图](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>功能位置和资产

功能位置用于管理位置中的资产。 此类管理包括跟踪功能位置的资产成本。 功能位置采用分层结构，而位置则可以具有子位置。 功能位置的结构为静态结构。 换句话说，位置不能更改地点。 资产可以安装到功能位置上，也可以在以后根据需要安装到其他功能位置上。

资产成本始终采用资产的位置。 换句话说，如果将资产安装到新的功能位置，该资产将自动使用与新功能位置关联的财务维度。 因此，资产成本始终与当前安装资产的功能位置关联。 在公司对功能位置执行项目控制和报告时，对财务维度的此项自动处理有助于确保完全跟踪成本。

功能位置层次结构的创建方法取决于公司对维护内部设备或服务客户设备的要求。 下图显示基于地理位置的功能位置的示例。

![显示基于地理位置的功能位置的图](media/03-overview-image.png)

下图显示基于客户的功能位置的示例。

![显示基于客户的功能位置的图](media/04-overview-image.png)
