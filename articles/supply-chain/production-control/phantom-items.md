---
title: 虚拟物料
description: 此主题详细介绍如何在 Dynamics 365 Supply Chain Management 中在物料清单 (BOM) 和配方的行中使用虚拟行类型。
author: ShylaThompson
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 1118d7334602e450e5d503632895f73ba19066a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814770"
---
# <a name="phantom-items"></a>虚拟物料

[!include [banner](../includes/banner.md)]

此主题详细介绍如何在物料清单 (BOM) 和配方的行中使用虚拟行类型。 在下图中，(a) 是产品 H 和部件 F 和 G 的物料清单，而 (b) 则是产品 H 和部件 F 的工艺路线单。

![产品 H 和部件 F](media/product-H-part-F.png)


此图显示的示例为分两个级别的物料清单结构。 成品 H 表示需要进行机器装配的产品。 这个机器装配由两个部件、一个含两种物料（A 和 B）的电子单元 (F)，以及也含两种材料（C 和 D）的一组包装材料构成。 另一种材料 (E) 则在常规装配该机器时使用。

![产品 H 和部件 F](media/product-H-part-B.png)

上图表示产品 H 的工程物料清单。此结构很好地囊括了整个机器装配的部件和组件。 但是，尽管产品设计师可能希望以这种方式表示物料清单，此结构可能无法正确地表示机器在车间中是如何制造地。 

例如，上图中的工程物料清单指示电子单元 F 作为单独工作订单中的独立部件进行装配。 但是在车间中，可能根据判断最好是将该电子单元作为整个机器装配的一部分进行装配，而不是作为单独的工作订单进行装配。

工程物料清单还指示部件 G 是一个单独的部件。 但是在此结构中，部件 G 表示的不是一个物理部件，而是包装材料的集合。 

因此，尽管工程物料清单对设计产品和保持该设计很有价值，可能并不是最具有逻辑性的产品制造执行过程支持方式。 相对而言，制造物料清单则最适合制造产品。

下图显示如何将上面的工程物料清单转换为制造物料清单。 在该图中，(a) 是产品 H 的物料清单，而 b 则是产品 H 的工艺路线单。

在此结构中，可看到部件 F 和 G 没有标注，而这些部件所含材料尚未升级到下一个物料清单级别。 

与工程物料清单不同（这种清单有两个工序单），制造物料清单只有一个工序单。 链接到部件 G 的包装工序也已升级，现在是产品 H 的工序单的一部分。第一个工序是装配电子单元。 这个顺序很有道理，因为下一个工序（即机器装配）中将使用该单元。 最后一个工序是包装工序，会用到两种包装材料（C 和 D）。

通过虚拟物料清单行类型实现工程物料清单与制造物料清单之间的转换。 就像术语“虚拟”的含义所示，两种物料清单类型转换期间，部件 F 和 G 已消失。 在此示例中，虚拟行类型应用于工程物料清单中部件 F 和 G 的物料清单行。 创建生产订单或批处理订单时，将把工程物料清单复制到生产订单或批处理订单。 然后，估计订单时，将从工程物料清单转换为制造物料清单，如上面的图中所示。 从第二个图中的工序单开始，包装材料 C 和 D 是工序的输入。 

## <a name="multilevel-phantom-bom-structures"></a>多级虚拟物料清单结构
可以在多级虚拟物料清单结构中使用虚拟行类型，如下图中所示。 在该图中，(a) 是产品 G 的物料清单，而 (b) 则是部件 E 和 F 及产品 G 的工艺路线单。 

![带工艺路线单的产品 G 和部件 F](media/product-G-route-sheet-G.png)


下图显示配置了部件 E 和 F 的物料清单行以便让行类型为虚拟时生成的制造物料清单和工艺路线单。 在该图中，(a) 是产品 G 的物料清单，而 (b) 则是产品 G 的工艺路线单。

![产品 G](media/product-G.png)


## <a name="phantom-and-route-network"></a>虚拟和工艺路线网络
也可以将虚拟物料清单用于具有工艺路线网络的物料清单。 在工艺路线网络中，一个或多个工序同时运行。 下图显示多级物料清单中使用的工艺路线网络的示例。 在该图中，(a) 是产品 G 和部件 F 的物料清单，而 (b) 则是产品 G 和部件 F 的工艺路线单，后者具有工艺路线网络。

![产品 G 和部件 F](media/product-G-part-F.png)


在下图中，(a) 是产品 G 和部件 F 的物料清单，而 (b) 则是产品 G 和部件 F 的工艺路线单。

![带工艺路线单的产品 G 和部件 F](media/product-G-part-F-with-route-sheet.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]