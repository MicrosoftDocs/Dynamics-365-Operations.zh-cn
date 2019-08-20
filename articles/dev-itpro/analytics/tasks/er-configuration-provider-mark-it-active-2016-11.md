---
title: 创建配置提供程序并将其标记为有效
description: 本主题介绍获分配“系统管理员”或者“电子电子报表开发人员”角色的用户在 Dynamics 365 for Finance and Operations 中如何为“电子申报 (ER)”创建配置提供程序。
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0dfbcf70493a43320e17d4d2734fe6343d43eaf3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850319"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>创建配置提供程序并将其标记为有效

[!include [task guide banner](../../includes/task-guide-banner.md)]

本主题介绍获分配“系统管理员”或者“电子电子报表开发人员”角色的用户在 Dynamics 365 for Finance and Operations 中如何为“电子申报 (ER)”创建配置提供程序。 每个 ER 配置都将把该提供程序归类为其作者。 以样本公司 Litware，Inc. 为例，新建一个配置提供程序。这些步骤适用于所有公司，因为所有公司都共享 ER 配置提供程序。

## <a name="create-a-provider"></a>新建一个提供程序
1. 转到**导航窗格**的左上角，然后选择**组织管理**。
2. 转到**工作区 > 电子申报**
3. 转到**相关链接 > 配置提供程序**。
4. 选择**新建**。
    - 提供程序具有唯一名称和 URL。 如果已存在 Litware 公司 (https://www.litware.com) 的记录，则查看此页内容并跳过此步骤。  
5. 在“名称”字段中，键入 `Litware, Inc.`。
6. 在”Internet 地址“字段中，键入 `https://www.litware.com`。
7. 选择**保存**。
8. 关闭该页面。

## <a name="select-as-an-active-provider"></a>选择为当前运行的提供程序
1. 选择 Litware 提供商。
2. 选择**设置有效**。

