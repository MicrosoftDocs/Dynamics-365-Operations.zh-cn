---
title: 创建服务协议
description: 本主题描述如何在服务管理和项目管理与核算模块中使用功能创建服务协议。
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a094ce9f0d9323b089055e74d41cf1f45323a7d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "310936"
---
# <a name="create-service-agreements"></a>创建服务协议

[!include [banner](../includes/banner.md)]

本主题描述如何在服务管理和项目管理与核算模块中使用功能创建服务协议。

## <a name="create-a-service-agreement-from-service-management"></a>从服务管理创建服务协议

1. 导航到**服务管理**。
2. 单击**服务协议**在页标题中创建一个新的服务协议行。 
3. 单击**新建**。 输入描述，在**项目 ID** 字段中选择对某一项目的引用，并填写相应字段和行的其余的服务协议。 单击**保存**。
4. 在**关系**选项卡中，选择**服务对象**或**服务任务**创建服务协议的服务对象关系或服务任务关系。 您为其创建了关系的服务对象和服务任务可以附加到服务协议行上。
5. 在页面的下部，通过从服务模板或其他服务协议复制行来创建服务协议行，或者通过手动创建服务协议行。

> [!NOTE]
> 如果您将来自其他服务协议的行复制到该服务协议中，则可以指示是否还要复制服务对象和服务任务关系。 如果您复制这些关系，则它们将添加到该服务协议的任何现有关系上。 如果您从某一服务模板复制服务协议行，则服务对象和服务任务关系将自动复制为新的服务协议行上的服务对象关系和服务任务关系。

## <a name="create-service-agreement-lines-manually"></a>手动创建服务协议行

1. 从**服务协议**页，在行网格中添加服务协议行。 
2. 输入服务协议行的适当信息。 
3. 按 **CTRL+S** 保存该行，然后关闭该页。

## <a name="create-a-service-agreement-from-project"></a>从项目创建服务协议

1. 单击**项目管理与核算**。
2. 单击**所有项目**。
3. 从列表中选择项目。
4. 在**操作窗格**上单击**管理**。 在**新建** 操作组中，单击**服务**并选择 **服务协议**。
5. 按照本主题前文标题为**创建服务协议**的章节中的步骤输入项目参考。


## <a name="related-topics"></a>相关主题

[服务协议](service-agreements.md)


