---
title: 创建服务协议
description: 本文描述如何在服务管理和项目管理与核算模块中使用功能创建服务协议。
author: sorenva
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d18d279cd437e98cad6495def953978cb78e723e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901754"
---
# <a name="create-service-agreements"></a>创建服务协议

[!include [banner](../includes/banner.md)]

本文描述如何在服务管理和项目管理与核算模块中使用功能创建服务协议。

## <a name="create-a-service-agreement-from-service-management"></a>从服务管理创建服务协议

1. 导航到 **服务管理**。
2. 选择 **服务协议** 在页标题中创建一个新的服务协议行。 
3. 选择 **新建**。 输入描述，在 **项目 ID** 字段中选择对某一项目的引用，并填写相应字段和行的其余的服务协议。 选择 **保存**。
4. 在 **关系** 选项卡中，选择 **服务对象** 或 **服务任务** 创建服务协议的服务对象关系或服务任务关系。 您为其创建了关系的服务对象和服务任务可以附加到服务协议行上。
5. 在页面的下部，通过从服务模板或其他服务协议复制行来创建服务协议行，或者通过手动创建服务协议行。

> [!NOTE]
> 如果您将来自其他服务协议的行复制到该服务协议中，则可以指示是否还要复制服务对象和服务任务关系。 如果您复制这些关系，则它们将添加到该服务协议的任何现有关系上。 如果您从某一服务模板复制服务协议行，则服务对象和服务任务关系将自动复制为新的服务协议行上的服务对象关系和服务任务关系。

## <a name="create-service-agreement-lines-manually"></a>手动创建服务协议行

1. 从 **服务协议** 页，在行网格中添加服务协议行。 
2. 输入服务协议行的适当信息。 
3. 选择 **保存** 保存该行，然后关闭页面。

## <a name="create-a-service-agreement-from-project"></a>从项目创建服务协议

1. 选择 **项目管理与会计**。
2. 选择 **所有项目**。
3. 从列表中选择项目。
4. 在 **操作窗格** 上，选择 **管理**。 在 **新建** 操作组中，选择 **服务** 并选择 **服务协议**。
5. 按照本文前面标题为 **创建服务协议** 的章节中的步骤输入项目参考。


## <a name="related-articles"></a>相关文章

[形成和确定服务协议概览](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]