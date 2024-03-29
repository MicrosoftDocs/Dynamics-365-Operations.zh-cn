---
title: 初始化新 Commerce 环境中的种子数据
description: 本主题介绍 Dynamics 365 Commerce 的初始化流程期间创建的数据。
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 14d56636b48d8f8ff15863bb04c762e398f8c370664fbd52f80ed5f05f0e4895
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718723"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>初始化新 Commerce 环境中的种子数据

[!include [banner](includes/banner.md)]

本主题介绍 Dynamics 365 Commerce 的初始化流程期间创建的数据。

在通过 Microsoft Dynamics Lifecycle Services (LCS) 部署商业解决方案后，您必须初始化商业配置以创建基本配置数据。

> [!IMPORTANT]
> 在初始化商业配置之前，请确保为您将设置商店的每个法人指定语言和邮政地址。 必须为您为商业使用的每个法人完成此步骤。

若要初始化配置，请执行以下步骤。

1. 启动 Commerce 客户端。
2. 单击 **Retail 和 Commerce** &gt; **总部设置** &gt; **参数** &gt; **商业参数**。
3. 单击 **初始化**。

初始化创建以下默认配置数据：

- 商业调度作业和子作业
- 商业通道架构
- 商业配送计划
- 默认屏幕布局，包括按钮网格、图像和主题
- 时区信息
- 销售点 (POS) 操作
- POS 权限
- 渠道报表
- 属性元数据
- 实体验证模板
- 清除 Commerce Data Exchange 会话历史记录的批处理作业

此外，为 Commerce 数据库启用了与支付卡行业 (PCI) 相关的日志记录。

> [!NOTE]
> 具有单独配置商业调度的选项。 此选项可以将商业调度配置重置为其默认设置。

在完成初始化后，必须配置附加的商业数据。 下面举了一些示例加以说明：

- 商业参数
- 商业调度程序参数
- 商业渠道
- 登记簿和设备
- 分类


[!INCLUDE[footer-include](../includes/footer-banner.md)]