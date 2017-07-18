---
title: "重复使用产品配置"
description: "可以指定要自动重用产品的现有配置。 然后，当用户完成配置会话后，系统会验证匹配用户选择的配置是否存在。 如果找到匹配配置，则再用配置 ID、相应的物料清单 (BOM) 以及路径。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a06b821bd8e23abb8af5e7e7ef93acc85e87386a
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017

---

# <a name="reuse-product-configurations"></a>重复使用产品配置

[!include[banner](../includes/banner.md)]


可以指定要自动重用产品的现有配置。 然后，当用户完成配置会话后，系统会验证匹配用户选择的配置是否存在。 如果找到匹配配置，则再用配置 ID、相应的物料清单 (BOM) 以及路径。

<a name="requirements-for-reusing-configurations"></a>要再用配置的要求
---------------------------------------

若要启用将重复使用的配置，必须在“**产品配置模型详细信息**”页上指定组件和属性的以下信息：

-   **组件和子组件** - 在“**常规**”快速选项卡上，在“**重复使用配置**”字段中，选择“**是**”。
-   **属性** – 在“**属性**”快速选项卡上，选择“**包括在重复使用中**”选项。 仅在相关组件启用重复使用时才显示此选项。 如果未选择要重复使用的任何属性，则始终重复使用该配置，这与配置会话期间的用户选择无关。 现有配置中的属性值必须匹配用户的选择。 例如，如果在配置会话期间，用户选择颜色为“**蓝色**”，则系统将验证组件的现有配置是否具有蓝色。

## <a name="resetting-configuration-reuse"></a>重置配置重复使用
在您重置配置重复使用后，不再考虑以前创建的配置。 更改物料清单或工艺路线，但不更改相关属性时，您可能要重置配置重复使用。 在该组件的“**常规**”快速选项卡上重置配置重复使用。




