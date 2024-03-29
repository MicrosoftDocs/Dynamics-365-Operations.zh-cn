---
title: 收入确认捆绑
description: 本文将介绍应收帐款的收入确认功能中包含的捆绑功能。 一个捆绑包含一个父级项目和多个组件项目。
author: bking
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 9b33906fd1907ce476eec5ba36ab243aa072cf6f
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348288"
---
# <a name="revenue-recognition-bundles"></a>收入确认捆绑

[!include [banner](../includes/banner.md)]

本文将介绍应收帐款的收入确认功能中包含的捆绑功能。 一个捆绑包含一个父级项目和多个组件项目。 父级项目在销售订单上输入，因此订单输入效率更高。 但是，它随后将分解为组件项目。 内部文档（例如装箱单）将列出组件项目。 但是，外部文档将仅显示父级项目。

> [!NOTE]
> Microsoft Dynamics 365 Commerce 渠道（例如在线、销售点 (POS) 和呼叫中心）不支持收入确认（包括捆绑功能）。 此外，这还包括从目标客户到现金的解决方案，适用于 Dynamics 365 Supply Chain Management 和 Dynamics 365 Sales。 在 Commerce 渠道或从目标客户到现金解决方案中创建的订单或交易记录中，不应添加配置为使用收入确认的项目。

要设置捆绑，必须输入用于收入确认的 Configuration Key。 但是，即使未设置收入确认，您也可以使用捆绑。 同样，即使未设置捆绑，您也可以使用收入确认。 如果设置了收入确认，则组件项目将确定在对销售订单开票时用于收入确认或延期的收入价格和收入计划。

捆绑设置使用物料清单 (BOM) 功能。 有关如何设置捆绑项目的信息，请参阅[收入确认设置](revenue-recognition-setup.md)。 如果将父级项目标记为捆绑，则其将以与其他物料清单项目不同的方式进行处理。 下面列出了具体的差异：

- 必须通过销售订单确认来分解捆绑，方法是在销售订单页面上的“操作”窗格的 **销售** 选项卡上选择 **确认销售订单**。 捆绑项目的分解不得采用在 **销售订单行** 快速选项卡的 **销售订单行** 菜单上的 **分解** 下选择 **物料清单行** 的方式来进行。 否则，该项目将视为物料清单而不是捆绑。
- 只有在确认包含捆绑项目的销售订单后，才能创建装箱单或发票。
- 通过销售订单确认来分解捆绑时，父级项目将被取消，并且其单价和折扣将被分配到捆绑的组件项目中。
- 组件项目的总和必须始终等于父级项目的价格。 因此，组件项目中可以更新或更改的字段存在限制。 例如，不能手动更改单价。 此外，无法通过将新的价格协议设为生效来间接更改单价。 要阻止新的价格协议，不能更改组件项目的库存维度。
- 打印面向外部的文档（例如销售订单确认函或发票）时，打印的是父级项目，而不是组件项目。

## <a name="bundles-on-sales-orders"></a>销售订单上的捆绑

USMF 演示公司包括以下捆绑设置。 请注意，用于收入确认的所有设置（例如收入计划设置）已从此方案中包括的项目中删除。

**父级项目：** 笔记本电脑捆绑

- **组件项目：** 项目 1000 的数量为 1
- **组件项目：** 项目 S0021 的数量为 1
- **组件项目：** 项目支持的数量为 1

组件项目的 *基本销售价* 是组件设置的重要部分。 基本销售价在项目的 **销售** 快速选项卡上定义。 当将父级项目的单价分配给组件项目时，将使用基本销售价计算分配系数。 不得将贸易协议销售价用于此目的。

为组件项目定义了以下基本销售价：

- **1000：**$1,900.00
- **S0021：**$150.00
- **支持：**$500.00

为客户 US-004 Cave Wholesales 输入了销售订单。 输入的唯一一行是针对笔记本电脑的捆绑项目。 可以从多个位置获取父行的默认单价，例如贸易协议或基本销售价。 在此示例中，手动输入单价 $2,300。

[![销售订单上的笔记本电脑捆绑销售项目。](./media/bundle-01.png)](./media/bundle-01.png)

由于销售订单包含捆绑销售，因此必须进行确认。 确认对话框显示捆绑的组件。

[![确认显示组件项目的销售订单对话框。](./media/bundle-02.png)](./media/bundle-02.png)

但是，打印的确认报告将仅显示捆绑销售的父级项目，因为该报告是面向外部的客户文档。

[![仅显示父级项目的确认报告。](./media/bundle-03.png)](./media/bundle-03.png)

确认销售订单后，父级项目仍显示在销售订单上，但其状态已更改为 **已取消**。 此外，还将在 **捆绑净额** 字段中跟踪净额。 需要此金额以打印发票，因为发票显示父级项目而不是组件项目。

组件项目的总和必须等于父级项目的 **捆绑净额** 值，因为该值是在打印的发票上呈交给客户的金额。 为了确保发票与过帐到总帐的金额匹配，将限制对组件项目进行编辑。 例如，无法更改站点和仓库，因为根据贸易协议，这些更改可能会触发价格变化。

父级项目的行中的单价将按以下方式分配到组件：

**组件中的基本销售价总计：**$1,900 + $500 + $150 = $2,550

- **组件 1：**$2,300 × (1,900 ÷ 2,550) = $1,713.73
- **组件 2：**$2,300 × (500 ÷ 2,550) = $450.98
- **组件 3：**$2,300 × (150 ÷ 2,550) = $135.29

组件的总和必须等于 $2,300，计算方式为 ($1,713.73 + $450.98 + $135.29 = $2,300)。

如果所有组件项目都需要更改，则可以删除父级项目。 在这种情况下，还将删除组件项目。 然后，可以再次添加父级项目，并且可以在确认销售订单之前完成所需的编辑。

[![包括对组件项目的更改的捆绑销售项目。](./media/bundle-04.png)](./media/bundle-04.png)

选取和打包销售订单后，文档将仅包括捆绑销售的组件。 装箱单和发票必须包括完整捆绑。 否则，将无法发布它们。 例如，对话框显示三个组件项目。 如果您尝试删除其中之一，将会显示一条错误消息，指出必须先对捆绑中的所有产品发货，然后才能开票。

必须先将捆绑作为完整捆绑进行发货和开票。 例如，如果将项目 1000 的数量更改为 4，但将其他组件项目的数量保留为 5，则无法过帐装箱单和发票。

仅当减少捆绑中所有组件的数量时，才可以对部分金额进行发货和开票。 例如，在销售订单上为笔记本电脑捆绑项目输入数量 5。 确认销售订单后，销售订单上将显示三个组件项目，每个项目的数量为 5。 默认情况下，在发货和开票期间，每个组件的数量将设置为 5。 但是，您可以将所有三个组件项目的数量降低至 3。 在这种情况下，将对三个完整捆绑进行发货和开票。 剩余的两个捆绑项目（三个组件项目中每一个的数量都为 2）可以在以后进行发货和开票。

最后一步是对销售订单开票。 在开票期间，“开票”对话框将显示组件项目。

[![显示组件项目的“开票”对话框。](./media/bundle-06.png)](./media/bundle-06.png)

但是，打印的发票将仅显示父级项目。
 
[![仅显示父级项目的打印发票。](./media/bundle-07.png)](./media/bundle-07.png)

过帐后创建的发票日记帐不包含捆绑销售中的父级项目，因为该项目的状态为 **已取消**。

[![不包含父级项目的发票日记帐。](./media/bundle-08.png)](./media/bundle-08.png)

务必注意，发票日记帐不包含捆绑销售中的父级项目，因为过帐发票后执行的任何流程都将基于该发票日记帐。 例如，如果您从操作窗格上的 **销售** 选项卡中创建贷方通知单，所创建的贷方通知单将包含组件项目而不是父级项目。

[![显示组件项目而不是父级项目的贷方通知单。](./media/bundle-09.png)](./media/bundle-09.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
