---
title: 质量管理测试仪器
description: 本主题介绍如何创建可用于在 Microsoft Dynamics 365 Supply Chain Management 中对质检订单进行测试的测试仪器。
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc09021f89a9064a3140a726fca74e3eceab13da
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956565"
---
# <a name="quality-management-test-instruments"></a>质量管理测试仪器

[!include [banner](../includes/banner.md)]

本主题介绍如何创建可用于在 Microsoft Dynamics 365 Supply Chain Management 中对质检订单进行测试的测试仪器。

您将使用 **测试仪器** 页定义和查看有关用于对质检订单执行测试的设备的详细信息。 测试仪器是可选的。 但是，它们可以帮助质量工作人员了解应该使用哪个设备或工具来执行特定测试。

## <a name="test-instrument-example"></a>测试仪器示例

您在对电气组件执行各项测试。 部分测试针对组件的电压输出，一项测试针对温度，另一项针对重量。 每项测试使用不同的工具或设备来执行。 例如，电压表用于测量电压，温度计用于测量温度，天平用于测量重量。 您可以将这些设备中的每一个配置为一个测试仪器，并指明记录测试结果应使用的度量单位。 例如，电压表得出的结果以伏特为单位记录，温度计得出的结果以华氏度或摄氏度为单位记录，天平得出的结果以磅或千克为单位记录。

## <a name="create-a-test-instrument"></a>创建测试仪器

1. 转到 **库存管理 \> 设置 \> 质量控制 \> 测试仪器**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，针对新行设置以下字段：

    - **测试仪器** – 为测试仪器输入唯一 ID 或名称。
    - **描述** – 输入测试仪器的详细描述。
    - **单位** – 选择仪器测量结果使用的单位。 **精度** 字段将根据您选择的单位自动设置。

1. 关闭该页面。

## <a name="additional-resources"></a>其他资源

- [质量管理测试](quality-tests.md)
- [质量管理测试组](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
