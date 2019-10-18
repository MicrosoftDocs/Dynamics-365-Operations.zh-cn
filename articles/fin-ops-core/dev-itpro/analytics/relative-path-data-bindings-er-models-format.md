---
title: 在 ER 模型和格式的数据绑定中使用相对路径
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a026eec379f98fd32080df50b5e114b423db34ad
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182799"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>在 ER 模型和格式的数据绑定中使用相对路径

[!include[banner](../includes/banner.md)]

用户可通过电子申报 (ER) 工具定义电子格式结构，然后描述应如何使用应用程序中的数据和算法填充这些结构。 有关详细信息，请参阅[创建电子申报 (ER) 配置](electronic-reporting-configuration.md)。 若要指定用于检索 Finance and Operations 数据并将其用于生成电子文档的数据流，需要执行以下操作：

- 将配置的数据源绑定到特定于域的所设计数据模型的元素。 模型结构和所选数据源可能是复杂层次结构的组成部分。 因此，最终绑定可能相当大，并且包含不同类型的大量元素（例如，关系、表和方法）。 绑定可能变得可读性不高且相当复杂，难以查看和理解，尤其是对于非负责人而言。 
- 将具有用于定义使用来自数据模型的哪些数据进行填充的格式组件的数据模型元素绑定到生成的格式的输出。

为了提高 ER 映射设计器的可用性，已发布了相对路径功能。 默认情况下，将为应用程序的所有新实例（其中启用了 ER 设计体验，即 Microsoft Dynamics 365 Finance、Microsoft Regulatory Configuration Service）开启相对路径表示选项。 实施相对路径参数是为了让用户在使用 ER 绑定的此表示时继续使用完整路径。

[![用户参数](./media/relative-path-01.png)](./media/relative-path-01.png)

 
开启相对路径使用参数后，将在当前模型元素的绑定中使用一个 @ 字符替换父项的路径。 整个绑定路径将变短，从而让整个映射更明显，更容易理解。 大多数情况下，不需要在 ER 设计器中再滚动即可查看数据模型的所有绑定。

[![模型映射设计器](./media/relative-path-02.png)](./media/relative-path-02.png)
 
开始设计新的 ER 表达式时，只需输入一个字符即可定义与父项之间的绑定。

[![配方设计器](./media/relative-path-03.png)](./media/relative-path-03.png)
 
如果决定使用绝对路径更改模型父项的数据源，则必须将此模型项和所有嵌套项重新绑定到新数据源。 开启使用相对路径并选择要绑定到父项的新数据源之后，将提供一个选项，单击一次即可自动重新绑定此父项的所有嵌套元素。

[![替换现有路径消息](./media/relative-path-04.png)](./media/relative-path-04.png)
 
如果确认重新绑定嵌套项，则将把新父项放到包含现有父项的每个嵌套项的路径中。
此功能不会破坏 ER 框架的向后兼容性。 以前设计的所有 ER 配置都支持这项新功能，不需要升级或转换。

> [!NOTE]
> 将把通过大量修改模型映射中嵌套元素的绑定造成的所有更改正确保存到配置增量（即更改跟踪）中。 这样，客户就可以将其模型映射派生版本的基本值重定为使用这项新功能修改的任何新基础版本。
