---
title: 创建物料清单模板
description: 您可以使用多种方法创建物料清单模板。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2e06283f3b95c5ff6b4376bba63cf5a42d5feeb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423119"
---
# <a name="create-a-template-bom"></a>创建物料清单模板   

[!include [banner](../includes/banner.md)]


您可以使用以下任一方法创建物料清单模板。 对于所有方法，**开始日期** 字段和 **结束日期** 字段都是可选的，仅供参考。

## <a name="create-a-template-bom-manually"></a>手动创建物料清单模板

1.  单击 **服务管理** \> **设置** \> **服务对象** \> **物料清单模板**。

2.  按 CTRL+N 打开 **创建物料清单模板** 窗体。

3.  在 **从引用复制物料清单行** 下，选择 **手动** 选项。

4.  在 **物料编号** 字段中，键入类型为 **物料清单** 的项。

5.  在 **名称** 字段中，为模板输入一个名称。

6.  在 **开始日期** 字段和 **结束日期** 字段中，输入物料清单模板处于活动状态的日期间隔。

7.  单击 **确定**。

将创建新的空物料清单模板。

## <a name="create-a-template-bom-based-on-another-template-bom"></a>基于其他物料清单模板创建物料清单模板

1.  单击 **服务管理** \> **设置** \> **服务对象** \> **物料清单模板**。

2.  按 CTRL+N 打开 **创建物料清单模板** 窗体。

3.  在 **从引用复制物料清单行** 下，选择 **物料清单模板** 选项。

4.  在 **参考编号** 字段中，选择要复制到您的新物料清单模板的现有物料清单模板。

5.  在 **名称** 字段中，为模板输入一个名称。

6.  在 **开始日期** 字段和 **结束日期** 字段中，输入物料清单模板处于活动状态的日期间隔。

7.  单击 **确定**。

将创建一个新的物料清单模板，该模板中的行与原始物料清单模板中的行相对应。

## <a name="create-a-template-bom-based-on-an-item-bom"></a>基于某一物料的物料清单创建物料清单模板

1.  单击 **服务管理** \> **设置** \> **服务对象** \> **物料清单模板**。

2.  按 CTRL+N 打开 **创建物料清单模板** 窗体。

3.  在 **从引用复制物料清单行** 中，选择 **物料清单**。

4.  在 **参考编号** 字段中，选择一个物料清单版本。 该类型的物料清单的物料将复制到 **物料编号**。

5.  在 **名称** 字段中，为模板输入一个名称。

6.  在 **开始日期** 字段和 **结束日期** 字段中，输入物料清单模板处于活动状态的日期间隔。

7.  单击 **确定**。

通过使用与在 **物料清单** 中列出的物料清单行相对应的行，创建新的物料清单模板。

## <a name="create-a-template-bom-based-on-a-production-bom"></a>基于某一生产物料清单创建物料清单模板

1.  单击 **服务管理** \> **设置** \> **服务对象** \> **物料清单模板**。

2.  按 CTRL+N 打开 **创建物料清单模板** 窗体。

3.  在 **从引用复制物料清单行** 中，选择 **生产**。

4.  在 **参考编号** 字段中，选择一个生产物料清单。

5.  在 **名称** 字段中，为模板输入一个名称。

6.  在 **开始日期** 字段和 **结束日期** 字段中，输入物料清单模板处于活动状态的日期间隔。

7.  单击 **确定**。

通过使用与在 **物料清单** 中列出的物料清单行相对应的行，创建新的物料清单模板。

## <a name="see-also"></a>请参阅

[物料清单模板](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]