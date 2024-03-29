---
title: 标识假设并确定试验指标
description: 本文描述了如何在 Dynamics 365 Commerce 中标识您在电子商务网站上运行的试验的假设和成功指标。
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0b6bdf160522fc93e841ec2f8a4542ff80d8f67f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852778"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>标识假设并确定试验的成功指标
试验生命周期的第一阶段包括标识试验假设并确定要跟踪以评估成功与否的指标。 下图显示了在 Dynamics 365 Commerce 中的电子商务网站上[设置和运行试验](experimentation-overview.md)所涉及的所有步骤。 其他步骤在单独的文章中介绍。 

[![试验用户旅程 - 标识。](./media/experimentation_identify.svg)](./media/experimentation_identify.svg#lightbox)

假设是您可以预测试验结果的语句。 定义一个假设有许多因素，例如，有关用户行为的研究和您已收集的网站数据。 通过假设，您将定义要通过试验验证的假定或理论。 试验假设的一个示例可能是“*在夏季，我主页上的白色 T 恤图片比海军毛衣的点击率更高，因为人们希望在夏天穿轻便浅色的衣服。*” 在这种情况下，您将创建包括白色 T 恤和海军毛衣的变体，并同时发布它们。

若要验证假设，试验的成功与否应与用户的操作直接相关；例如，如果网站用户单击链接或按钮。 这些操作必须与将报告给跟踪试验的第三方服务的事件相对应。 随着时间的推移，将采取该操作的用户百分比作为一个指标，您可以使用该指标生成报告和进行分析。 若要查看所有可用的事件和属性，请参阅 [Commerce 组件的诊断和疑难解答事件](dev-itpro/retail-component-events-diagnostics-troubleshooting.md)。

## <a name="previous-step"></a>上一步
[Dynamics 365 Commerce 中的试验](experimentation-overview.md)


## <a name="next-step"></a>后续步骤
[设计试验](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]