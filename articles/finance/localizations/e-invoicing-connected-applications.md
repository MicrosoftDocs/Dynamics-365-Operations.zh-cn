---
title: 已连接的应用程序
description: 本文说明如何在电子开票中设置连接的应用程序。
author: dkalyuzh
ms.date: 02/07/2022
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
ms.openlocfilehash: 7a0a9c19009c49b80ca8c182c31592c1a713a2aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906278"
---
# <a name="connected-applications"></a>已连接的应用程序

[!include [banner](../includes/banner.md)]

连接的应用程序是您可能希望通过 Regulatory Configuration Service (RCS) 到达的 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 的实例。 通过连接的应用程序，您可以在 Finance 或 Supply Chain Management 中配置全球化功能的一部分，以使电子开票方案运行。

当您部署全球化功能时，您的 Finance 或 Supply Chain Management 应用程序可用的设置信息可以直接从 RCS 发布到适当的已连接的应用程序。

当您有多个应用程序环境（如用户验收测试 (UAT) 和生产环境）并且您希望通过将相同参数部署到不同环境来保持设置一致时，可以使用 RCS 中的 Finance 或 Supply Chain Management 参数将非常有用。

## <a name="create-a-connected-application"></a>创建连接的应用程序

1. 登录您的 RCS 帐户。
2. 在 **全球化功能** 工作区的 **环境** 部分中，选择 **电子开票** 磁贴。
3. 在 **环境设置** 页上的操作窗格上，选择 **相连应用程序**。
4. 选择 **新建** 创建连接的应用程序。
5. 在 **名称** 字段中，输入要连接的应用程序的名称。
6. 在 **类型** 字段中选择 **Dynamics 365 Finance**。
7. 在 **应用程序** 字段中，输入要连接的环境的 URL。
8. 在 **租户** 字段中，输入环境的租户。
9. 选择 **保存**。
10. 在操作窗格上，选择 **检查连接** 测试与环境的连接。 然后关闭页面。

## <a name="link-connected-applications-to-environments"></a>将连接的应用程序链接到环境

1. 在 **环境设置** 页上，选择 **新建** 将连接的应用程序分配给环境。
2. 在 **相连应用程序** 字段中，选择一个连接的应用程序。
3. 在 **服务环境** 字段中，选择一个服务环境。
4. 选择 **保存**，然后关闭页面。
