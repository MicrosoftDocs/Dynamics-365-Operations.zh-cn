---
title: 标识假设并确定试验指标
description: 本主题描述了如何在 Dynamics 365 Commerce 中标识您在电子商务网站上运行的试验的假设和成功指标。
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930146"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>标识假设并确定试验的成功指标
试验生命周期的第一阶段包括标识试验假设并确定要跟踪以评估成功与否的指标。 下图显示了在 Dynamics 365 Commerce 中的电子商务网站上[设置和运行试验](experimentation-overview.md)所涉及的所有步骤。 其他步骤在单独的主题中介绍。 

[![试验用户旅程 - 标识](./media/experimentation_identify.svg)](./media/experimentation_identify.svg#lightbox)

假设是您可以预测试验结果的语句。 定义一个假设有许多因素，例如，有关用户行为的研究和您已收集的网站数据。 通过假设，您将定义要通过试验验证的假定或理论。 试验假设的一个示例可能是“*在夏季，我主页上的白色 T 恤图片比海军毛衣的点击率更高，因为人们希望在夏天穿轻便浅色的衣服。*” 在这种情况下，您将创建包括白色 T 恤和海军毛衣的变体，并同时发布它们。

为了验证假设，试验的成功与否应与用户的操作直接相关；例如，如果网站用户单击链接或按钮。 这些操作必须与将报告给跟踪试验的第三方服务的事件相对应。 随着时间的推移，将采取该操作的用户百分比作为一个指标，您可以使用该指标生成报告和进行分析。 请参阅 [Commerce 组件的诊断和疑难解答事件](dev-itpro/retail-component-events-diagnostics-troubleshooting.md)主题以查看所有可用的事件和属性。

## <a name="previous-step"></a>上一步
[Dynamics 365 Commerce 中的试验](experimentation-overview.md)


## <a name="next-step"></a>后续步骤
[设置试验](experimentation-setup.md)
