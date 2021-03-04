---
title: 开始使用成本核算服务（私人预览版）
description: 本主题提供成本核算服务的许可详细信息和安装说明。
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: a82af9e8ec1806f470103897389d0316d33a4a06
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422899"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a>开始使用成本核算服务（私人预览版）

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> 本主题中介绍的功能作为专用预览版的一部分提供。 本主题的内容及所介绍的功能可能会发生变化。 有关预览版的详细信息，请参阅[一个版本服务更新常见问题](../../fin-ops-core/fin-ops/get-started/one-version.md)。

成本核算服务使您可以在已设置的成本核算分类帐中执行多个库存核算。 您将每个成本核算分类帐与一个 *惯例* 关联。 惯例是以下几种会计政策的集合：

- 成本对象
- 输入度量依据
- 成本流假设
- 成本元素

> [!NOTE]
> 即使您打开了成本核算服务，仍然可以照常在 Microsoft Dynamics 365 Supply Chain Management 中执行库存核算。

成本核算服务是一个加载项。 要使其功能可用，必须从 Microsoft Dynamics Lifecycle Services (LCS) 进行安装。 因此，您可以选择在测试环境中对其进行评估，然后再将其打开用于生产环境。

成本核算服务当前不支持 Dynamics 365 Supply Chain Management 内置的所有成本管理功能。 因此，重要的是要评估当前可用的功能集是否满足您的要求。

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a>如何获取成本核算服务（私人预览版）

> [!IMPORTANT]
> 若要使用成本核算服务，您必须具有启用 LCS 的高可用性环境（不是 OneBox 环境），并且您必须运行 Dynamics 365 Supply Chain Management 版本 10.0.11 或更高版本。

若要注册成本核算服务私人预览版，请通过电子邮件向[成本核算服务（私人预览版）](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29)发送 LCS 环境 ID。 批准您参加此计划之后，我们将向您发送跟进电子邮件，其中包含成本核算服务测试密钥。 收到测试密钥之后，您可以继续[安装加载项](#install)。

## <a name="licensing"></a>许可授权

成本核算服务与可用于 Supply Chain Management 的库存核算标准功能一起获得许可。 您无需购买其他许可证即可使用成本核算服务。

## <a name="install-the-add-in"></a><a name="install"></a>安装加载项

要使用成本核算服务，请按照以下过程中的说明安装用于 Supply Chain Management 的成本核算服务加载项。

1. [注册](#sign-up)成本核算服务（私人预览版）。

1. 登录 LCS。

1. 转到 **预览功能管理**。

1. 选择加号 (**+**)。

1. 在 **代码** 字段中，输入您的成本核算服务的加载项测试密钥。 （您应该已经通过电子邮件收到了密钥。）

1. 选择 **解锁**。

1. 打开要在其中添加服务的 LCS 环境。

1. 转到 **完整详细信息**。

1. 向下滚动到 **环境加载项** 快速选项卡。

1. 选择 **安装新加载项**。

1. 选择 **成本核算服务**。

1. 按照安装指南操作，并同意条款和条件。

1. 选择 **安装**。

1. 在 **环境加载项** 快速选项卡上，您应该会看到正在安装成本核算服务。 几分钟后，状态应从 **正在安装** 变为 **已安装**。 （您可能必须刷新页面才能看到此改变。）此时，成本核算服务已经可以使用。

## <a name="set-up-the-integration"></a>设置集成

要设置成本核算服务与 Dynamics 365 Supply Chain Management 之间的集成：

1. 转到 **系统管理 > 功能管理**。

1. 选择 **检查更新**。

1. 打开 **所有** 选项卡，搜索名为 *成本核算服务* 的功能。

1. 选择 **立即启用**。

1. 转到 **成本管理 > 成本核算服务 > 设置 > 成本核算服务参数 > 集成参数**。

1. 在 **应用程序 ID** 字段中，输入以下代码：<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. 在 **数据服务终结点** 字段中，输入以下 URL：<br>https://operationsdataservice.operations365.dynamics.com/

1. 在 **成本核算服务终结点** 字段中，输入以下 URL：<br>https://costaccountingservice.operations365.dynamics.com/

1. 成本核算服务现在可以使用了。

## <a name="related-resources"></a>相关资源

[成本核算服务主页](cost-accounting-service-home.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]