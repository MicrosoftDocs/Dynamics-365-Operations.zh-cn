---
title: 资产服务等级
description: 本文介绍资产管理中的资产服务级别。
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7429b30253f540925e67ff9239667a0a404f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908676"
---
# <a name="asset-service-levels"></a>资产服务等级

[!include [banner](../../includes/banner.md)]

 

本文介绍资产管理中的资产服务级别。 资产服务级别与资产关联，并转化为维护请求和工作订单。 用于在工作订单排产期间计算工作订单的优先级。 如果需要更改资产服务级别，则可更改。

有关与计算工作订单排产的等级评分关联的设置的详细信息，请参阅[资产管理参数](../setup-for-objects/enterprise-asset-management-parameters.md)。 必须为资产服务级别设置至少一个默认记录。 如果工作订单排产期间未找到其他匹配项，则使用默认记录。

**示例 1：** 未找到其他匹配项时使用的默认服务级别。 在此记录中，仅选择一个服务级别。

**示例 2：** 用于为沃尔沃卡车引擎安排作业的高服务级别。 在此记录中，选择相关资产类型（如 **卡车引擎**）、制造商（**沃尔沃**）和服务级别。

## <a name="set-up-asset-service-levels"></a>设置资产服务级别

1. 选择 **资产管理** \> **设置** \> **资产服务级别**。
2. 选择 **新建** 创建记录。
3. 根据资产服务级别所需默认级别，在 **功能位置**、**资产类型**、**制造商**、**模型**、**资产**、**工作订单类型** 和 **服务级别** 字段中进行相关选择。

    > [!NOTE]
    > 将资产服务级别用于维护请求和工作订单时，资产管理检查所有资产服务级别记录以查找可能的匹配项。 始终先检查最具体的组合。 换句话说，资产管理首先会检查 **工作订单类型** 字段的匹配项。 如果未找到匹配项，将检查 **资产** 字段的匹配项，以此类推。 如 **资产服务级别** 页面布局中显示，此行为表示为了找到最具体的组合，资产管理从右到左检查每个记录以查找匹配项。 如果未找到匹配项，将使用这些字段中无可供选择的内容的默认记录。

4. 在 **服务级别** 字段中，选择一个数字，用于指示服务级别（优先级）。


> [!NOTE]
> 如果在 **资产服务级别** 页中更改已用于工作订单的资产服务级别记录，则不会相应更改维护请求和工作订单的服务级别。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]