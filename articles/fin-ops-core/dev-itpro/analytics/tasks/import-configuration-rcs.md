---
title: (ER) 从 RCS 导入配置
description: 本文介绍用户如何从 RCS 导入 ER 配置的新版本。
author: kfend
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 55e7a3ae23b708acecb5ac219b885f43b4c7aa0a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290025"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) 从 RCS 导入配置

[!include [banner](../../includes/banner.md)]

以下步骤说明系统管理员或电子报表开发人员角色的用户可如何从 Microsoft Regulatory Configuration Services (RCS) 导入新电子申报 (ER) 配置版本。 在此示例中，将选择 RCS 中已配置的 ER 配置版本，并将其导入示例公司 Litware, Inc. 的当前实例。可以在任何公司执行这些步骤，因为公司共享 ER 配置。 为了完成这些步骤，您必须首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)一文中的步骤。 若要完成这些步骤，还必须可以访问其中包含至少一个状态为 **已完成** 或 **共享** 的 ER 配置的 RCS 实例。

1. 转到 **组织管理** > **工作区** > **电子申报**。 
2. 确保示例公司 Litware 公司的配置提供程序可用且标记为 **有效**。 如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)一文中的步骤。 
3. 如果没有为公司设置 RCS 环境，请选择 **Regulatory services – 配置** 外部链接，然后按照说明设置 RCS 环境。 
4. 选择 **电子申报参数**。 
5. 选择 **RCS** 选项卡。 
6. 如果已经为您的公司设置了 RCS 环境，请使用页面中提供的 URL 访问。 
7. 关闭该页面。 

## <a name="register-a-new-er-repository"></a>注册新的 ER 存储库。 
1. 在列表中，标记所选的行。 
2. 选择 Litware, Inc. 提供商。 
3. 选择存储库。 
4. 选择添加以打开下拉对话框。 
5. 在“配置存储库类型”字段中，输入”RCS“。 
6. 选择创建存储库。 
7. 在 RCS 环境显示名称字段中，输入或选择一个值。 
8. 选择所需的 RCS 实例。 可以选择多个。 
9. 选择确定。 

## <a name="import-er-configurations-from-rcs-based-repository"></a>从基于 RCS 的存储库导入 ER 配置
1. 选择 **显示筛选器**。 
2. 使用 **开头为** 筛选器运算符在 **名称** 字段中输入筛选器值”RCS“。 
3. 打开所选存储库时，在 **连接 Regulatory Configuration Services** 页上，选择 **选择此处连接 Regulatory Configuration Services** 链接。 
4. 选择 **打开**。 
5. 选择 **关闭**。 
6. 选择所需 ER 配置版本，然后选择 **导入** 将其导入到当前实例中。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
