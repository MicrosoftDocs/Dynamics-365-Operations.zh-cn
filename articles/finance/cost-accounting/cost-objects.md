---
title: 成本对象维度
description: 在分析成本时，使用成本元素维度确定成本流向。 您可以使用成本对象维度确定应在何处分配成本。。 本文提供了有关成本对象维度的信息。
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3ee481b9dafe202e0a850a31b6ab036d52a20547
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874629"
---
# <a name="cost-object-dimensions"></a>成本对象维度

[!include [banner](../includes/banner.md)]

在分析成本时，使用成本元素维度确定成本流向。 您可以使用成本对象维度确定应在何处分配成本。。 本文提供了有关成本对象维度的信息。

成本对象可以是您要估计、分配成本或直接衡量的任何对象类型。 典型的成本对象包括产品、项目、资源、部门、成本中心和地理区域。 管理层使用成本对象量化成本，也推动盈利分析。

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>成本对象维度和成本对象维度成员
成本对象被称为“*成本对象维度*”。 在您决定成本对象维度应引用哪个实体后，您必须指定单独的维度值或者将它们从其他源系统导入到成本核算中。 这些单独的维度值被称为“*成本对象维度成员*”。 例如，您要使用名为“成本中心”的财务维度作为成本对象维度。 要查看成本如何流向各个成本中心，您必须导入成本对象维度成员。 在这种情况下，成本对象维度成员是实际成本中心，例如销售、生产、管理和地理位置。 以下屏幕截图举例说明了作为成本对象维度的成本中心及其作为成本对象维度成员的实际成本中心。 

[![显示作为成本对象维度的成本中心的屏幕截图。](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>通过数据连接器导入成本对象维度成员
要更加轻松地导入成本对象维度成员，您可以使用数据连接器从您要作为成本对象维度使用的实体中检索值。 您可以使用预构建的数据连接器或您构建的自定义数据连接器。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
