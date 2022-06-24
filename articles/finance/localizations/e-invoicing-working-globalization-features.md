---
title: 全球化功能组件
description: 本文提供全球化功能组件的概述。
author: dkalyuzh
ms.date: 02/11/2022
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
ms.openlocfilehash: 5525332fe3f1a3ea96da630dc34bab82e4117f99
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891479"
---
# <a name="globalization-feature-components"></a>全球化功能组件

[!include [banner](../includes/banner.md)]

全球化功能是一组组件，用于定义电子报告 (ER) 配置中的数据转换规则。 这些组件包括处理电子单据，然后将它们发送到外部渠道或从外部渠道接收它们的指令。 另外还包括定义何时应为传入业务数据运行功能的条件。

所有组件相互依赖。 全球化功能使创建和维护这种依赖关系变得容易，同时支持组件集的生命周期管理和版本控制。

## <a name="access-electronic-invoicing-feature-components"></a>访问电子开票功能组件 

1. 登录到您的 Regulatory Configuration Service (RCS) 帐户。
2. 在 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。

    全球化功能包含多个组件。 **电子开票功能** 页面包括每个组件的单独选项卡。

    - **版本** – 组件支持功能的生命周期管理。 您可以使用它来管理功能的不同版本的状态。
    - **配置** – 此组件允许您管理、查看和编辑在处理管道中使用的相关 ER 格式和格式映射配置。
    - **设置** – 此组件使全球化服务（如电子开票服务）的用户可以管理相关功能版本的设置。 因此，它支持通信和响应规则的灵活构造。
    - **环境** – 此组件使全球化服务（如电子开票服务）的用户可以管理使用功能版本设置的环境。 另外还允许他们向有权访问功能版本设置的用户授予授权。
    - **组织** – 此组件使用户可以与外部组织共享功能。
    - **标记** – 此组件允许您标记可在全球化蓝图中使用的功能以进行引用。
