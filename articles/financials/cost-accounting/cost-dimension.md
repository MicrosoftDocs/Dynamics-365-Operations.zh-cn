---
title: 创建维度并导入维度成员
description: 成本核算是一个独立的模块，需要来自其他模块的主数据。
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d48ba0a0b80d251e107baa0ceeb66d8e328f13dc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565711"
---
# <a name="create-dimensions-and-import-dimension-members"></a>创建维度并导入维度成员

[!include [banner](../includes/banner.md)]

成本核算是一个独立的模块，需要来自其他模块的数据。 该数据分为以下类别：

-  成本元素
-  成本对象
-  统计维度

一个**成本元素**对应于会计科目表的成本相关物料。 **成本对象**对应于任何类型的财务维度，例如您要估算、分配成本或直接衡量的产品、成本中心和项目。 **统计维度**及其成员用于登记非货币条目。 统计维度成员可用作成本分配和成本分摊中的分配基础 

下图说明在成本核算中使用的维度。

[![成本会计维度](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

在数据导入到成本核算后，您可以使用它生成各种视角，为组织中的所有级别的经理提供见解。 以下主题提供有关创建维度和导入维度成员的信息。 

-  [成本元素维度](cost-elements.md)
-  [创建成本元素（任务指南）](./tasks/create-cost-elements.md)
-  [成本对象维度](cost-objects.md)
-  [创建成本元素（任务指南）](./tasks/create-cost-objects.md)
-  [将成本元素维度成员映射到一组常用维度成员](map-cost-elements-dimension-members.md)
-  [映射成本元素维度（任务指南）](./tasks/map-cost-element-dimension.md)
-  [统计维度成员和统计度量提供方模板](statistical-measure-provider-template.md)






