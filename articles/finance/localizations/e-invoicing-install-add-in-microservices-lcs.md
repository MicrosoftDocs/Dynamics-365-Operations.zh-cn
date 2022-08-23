---
title: 在 Lifecycle Services 中安装微服务的加载项
description: 本文介绍如何在 Microsoft Dynamics Lifecycle Services (LCS) 中安装电子开票加载项。
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: a837b85d4893f2915b5fbb5ffaae8eb95f19bc0e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272246"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>在 Lifecycle Services 中安装微服务的加载项

[!include [banner](../includes/banner.md)]

电子开票服务中的身份验证需要您通过在 Microsoft Dynamics Lifecycle Services (LCS) 中安装适用于您的环境的插件，来在服务平台中注册您的 Microsoft Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 环境。

要注册环境，请按照下列步骤操作。

1. 登录您的 LCS 帐户。
2. 在项目仪表板上，选择一个 LCS 项目。
2. 在该项目中，在 **环境** 仪表板上，选择您的已部署环境。 所选环境必须正在运行。
3. 在 **Power Platform 集成** 选项卡上，在 **环境加载项** 部分，选择 **安装新加载项**。
4. 选择 **电子开票**。
5. 在 **AAD 应用程序 ID** 字段中，输入 **091c98b0-a1c9-4b02-b62c-7753395ccabe**。 此值是一个固定值。 确保仅输入全局唯一标识符 (GUID)。 不要包含任何其他符号，如空格、逗号、句点或引号。
6. 在 **AAD 租户 ID** 字段中，输入您的 Azure 订阅帐户的租户 ID。 您指定的 Azure Active Directory (Azure AD) 租户应该是用于 Regulatory Configuration Service (RCS) 的同一个租户。
7. 查看条款和条件，然后选中相应的复选框。
8. 选择 **安装**。 几分钟后，状态应从 **正在安装** 变为 **已安装**。 可能必须刷新页面才能看到此更改。

电子开票现在已经可以使用。

> [!NOTE]
> 公司通常有多个 Finance 或 Supply Chain Management 环境。 这些环境包括生产环境、用户验收测试 (UAT) 环境和开发（沙盒）环境。 对于要连接到电子开票的所有环境，均必须完成上述过程。
