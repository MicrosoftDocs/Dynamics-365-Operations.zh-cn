---
title: 创建配置提供程序并将其标记为有效
description: 本文介绍获分配“系统管理员”或者“电子报告开发人员”角色的用户如何创建配置提供程序。
author: kfend
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
ms.openlocfilehash: db5226720a4e0c0f167921a972429c0a5ecdd2e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267804"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>创建配置提供程序并将其标记为有效

[!include [banner](../../includes/banner.md)]

本文介绍获分配“系统管理员”或者“电子报告开发人员”角色的用户如何为“电子报告 (ER)”创建配置提供程序。 每个 ER 配置都将把该提供程序归类为其作者。 以样本公司 Litware，Inc. 为例，新建一个配置提供程序。这些步骤适用于所有公司，因为所有公司都共享 ER 配置提供程序。

## <a name="create-a-provider"></a>新建一个提供程序
1. 转到 **导航窗格** 的左上角，然后选择 **组织管理**。
2. 转到 **工作区 > 电子申报**
3. 转到 **相关链接 > 配置提供程序**。
4. 选择 **新建**。
    - 提供程序具有唯一名称和 URL。 如果已存在 Litware 公司 (https://www.litware.com) 的记录，则查看此页内容并跳过此步骤。  
5. 在“名称”字段中，键入 `Litware, Inc.`。
6. 在”Internet 地址“字段中，键入 `https://www.litware.com`。
7. 选择 **保存**。
8. 关闭该页面。

## <a name="select-as-an-active-provider"></a>选择为当前运行的提供程序
1. 选择 Litware 提供商。
2. 选择 **设置有效**。

![电子报告工作区页面。](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
