---
title: "初始化在新的零售环境的种子数据"
description: "此描述文章创建作为 Microsoft Dynamics 365 初始化的过程的一部分的操作的节点-零售的数据。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>初始化在新的零售环境的种子数据

此描述文章创建作为 Microsoft Dynamics 365 初始化的过程的一部分的操作的节点-零售的数据。

在通过 Microsoft Dynamics Lifecycle Services (LCS) 部署零售解决方案后，您必须初始化零售配置以创建基本配置数据。 **重要提示：**在初始化零售配置之前，请确保为您将设置零售商店的每个法人指定语言和邮政地址。 必须为您为零售使用的每个法人完成此步骤。 若要初始化零售配置，请执行以下步骤。

1.  启动客户工序的 Dynamics 365。
2.  单击**和商务** &gt; **零售总部参数设置。** &gt; ** ** &gt; **零售**参数。
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

此外，记录与的支付卡行业 (PCI) 为数据库启用工序的 Dynamics (PCI)。 **注意：**具有单独配置零售调度的选项。 此选项可以将零售调度配置重置为其默认设置。 在完成初始化后，必须配置附加的零售数据。 下面举了一些示例加以说明：

-   零售参数
-   零售调度参数设置
-   零售渠道
-   登记簿和设备
-   分类



