---
title: 使用配置
description: 本文概述了使用全球化功能工作区中的电子报告 (ER) 配置的主要场景。
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 359f00336811efd5f21463a325627df0e01a5f3a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875933"
---
# <a name="work-with-configurations"></a>使用配置

[!include [banner](../includes/banner.md)]

电子报告 (ER) 配置是电子开票功能的主要组件集之一。 ER 配置包含文件结构的设置和一组用于通过以下两种方式转换数据的转换规则：

- **导出 ER 格式配置** – 此配置将数据从统一的内部结构（ER 模型）转换为电子文件格式。
- **导入 ER 格式配置** – 此配置将数据从电子文件格式转换为统一的内部结构（ER 模型）。

除了以预定义格式生成传出电子文件外，ER 配置还广泛用于分析来自外部 Web 服务的作为响应的传入消息。 此功能有助于构建可配置逻辑以获取与外部渠道通信的结果，将这些结果（代码、消息和日志）转换为用户可读的结构，然后将这些信息传递到客户端应用程序。

要开始在您的电子开票功能中使用 ER 配置，您必须将它们链接到此功能，并在当前功能版本的 **配置** 选项卡上提供这些配置。 您可以通过选择 **添加**、**删除**、**编辑** 或 **查看** 来使用链接的 ER 配置。

ER 配置必须先存在于您的 Regulatory Configuration Service (RCS) 存储库中，然后您才可以添加指向该配置的链接。 要查看 RCS 存储库中可用的 ER 配置，请执行以下步骤。

1. 登录您的 RCS 帐户。
2. 在 **电子申报** 工作区的 **配置** 部分中，选择 **申报配置** 磁贴。

有关如何创建新 ER 配置或从全局存储库导入现有 ER 配置的信息，请参阅[电子报告](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)。

要调整链接的 ER 配置，在当前电子开票功能的 **配置** 选项卡上选择 **编辑**。 系统会自动创建 ER 配置的版本。 如果当前版本不是由活动配置提供程序创建的，系统会创建一个使用您的配置提供程序的派生版本。 如果当前版本是由活动配置提供程序创建的，系统会创建一个新版本。 在这两种情况下，您都可以修改创建的版本，然后自动执行所有必需的更新。
