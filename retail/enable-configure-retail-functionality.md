---
title: "初始化新 Retail 环境中的种子数据"
description: "本主题介绍 Microsoft Dynamics 365 for Operations - Retail 的初始化流程期间创建的数据。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: b5290bb62ab8ad71b06b0478ccaf6dbb61454170
ms.contentlocale: zh-cn
ms.lasthandoff: 04/26/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>初始化新 Retail 环境中的种子数据

[!include[banner](includes/banner.md)]


本主题介绍 Microsoft Dynamics 365 for Operations - Retail 的初始化流程期间创建的数据。

在通过 Microsoft Dynamics Lifecycle Services (LCS) 部署零售解决方案后，您必须初始化零售配置以创建基本配置数据。 **重要提示：**在初始化零售配置之前，请确保为您将设置零售商店的每个法人指定语言和邮政地址。 必须为您为零售使用的每个法人完成此步骤。 若要初始化零售配置，请执行以下步骤。

1.  启动 Dynamics 365 for Operations 客户端。
2.  单击**零售和商业** &gt; **总部设置** &gt; **参数** &gt; **零售参数**。
3.  单击**初始化**。

初始化创建以下默认配置数据：

-   零售调度作业和子作业
-   零售通道架构
-   零售配送计划
-   默认屏幕布局，包括按钮网格、图像和主题
-   时区信息
-   销售点 (POS) 操作
-   POS 权限
-   渠道报表
-   属性元数据
-   实体验证模板
-   清除商业数据交换的会话历史记录的批处理作业

此外，与支付卡行业 (PCI) 相关的日志记录为 Dynamics 365 for Operations 数据库启用。 **注意：**具有单独配置零售调度的选项。 此选项可以将零售调度配置重置为其默认设置。 在完成初始化后，必须配置附加的零售数据。 下面举了一些示例加以说明：

-   零售参数
-   零售调度参数设置
-   零售渠道
-   登记簿和设备
-   分类





