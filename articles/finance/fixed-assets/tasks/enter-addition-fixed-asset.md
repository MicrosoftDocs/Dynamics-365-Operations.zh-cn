---
title: 输入对固定资产的添加件
description: 本流程展示如何对现有固定资产表添加新的成员。
author: moaamer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d23f60963466249b332b759ee72ebc8387aee4b
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713013"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a>输入对固定资产的添加件

[!include [banner](../../includes/banner.md)]

本流程展示如何对现有固定资产表添加新的成员。 固定资产添加功能的目的就是追踪添加的资产项目，对固定资产进行维护和改进，也只是以提供信息为目的。 任何对固定资产价值或服务年限的改变要单独进行。   

本流程需要用到会计角色，使用来自法定实体 USMF 的演示数据。

1. 在导航窗格中，转到 **模块 > 固定资产 > 固定资产 > 固定资产**。
2. 在列表中，查找并选择要添加的固定资产。
3. 在列表中，单击所选行中的链接。
4. 在操作窗格上，单击 **固定资产**。
5. 单击 **固定资产物料添加**。
6. 单击 **新建**。
7. 在 **名称** 字段中，键入一个值。
8. 在 **购置日期** 字段中，设置添加采购或服务的日期。
9. 在 **单位成本** 字段中，输入资产物料、维护或其他改善成本。
10. 在 **数量** 字段中，输入一个数字。 总成本对固定资产的值没有影响，仅用于跟踪和提供信息。 如果要将成本资本化，则必须单独过帐调高交易。  
11. 单击 **常规** 选项卡。

    * 如果增加物提供了资产的服务年限，怎讲 **增加服务年限** 设置为 **是**。  
    * 该字段仅用于提供信息。 要提高使用年限，请修改资产价值模型和折旧帐簿中的使用年限。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
