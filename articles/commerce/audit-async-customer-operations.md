---
title: 审核 headquarters 中客户操作的同步
description: 本文介绍如何审核 Microsoft Dynamics 365 Commerce headquarters 中客户操作的同步，以帮助解决所有站点用户问题。
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691051"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>审核 headquarters 中客户操作的同步

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本文介绍如何审核 Microsoft Dynamics 365 Commerce headquarters 中客户操作的同步，以帮助解决所有站点用户问题。

随着组织开始采用异步创建和编辑客户的功能，站点管理员需要一种基于站点用户请求或流程失败来查看和解决操作问题的方法。 在这些场景中，站点管理员应该能够审核客户创建和编辑操作，并使用自助服务模型修复任何失败。

## <a name="customer-synchronization-status"></a>客户同步状态

当您选择客户管理的异步模式及其相应功能时，Commerce Headquarters 管理员必须为 **P 作业**、**从异步模式同步客户和业务合作伙伴** 作业和 **1010** 作业创建并计划一个重复执行的批处理作业，以便在 Commerce Headquarters 中将任何异步客户转换为同步客户。 每当这些作业运行时，都会发生客户管理操作的同步。 有关详细信息，请参阅[异步客户创建模式](async-customer-mode.md)。

作为企业主，您可以执行以下操作：

- 查看站点用户的所有创建/编辑操作。 详细信息包括状态和时间戳。
- 使用任意客户表字段和值来筛选操作以缩小审核日志的范围。
- 查看更改的简要说明以及状态详细信息，从更高层面了解操作。
- 对于出现的失败，编辑和修复有问题的字段，然后保存和同步特定的客户操作。

### <a name="elements-on-the-customer-synchronization-status-page"></a>客户同步状态页面上的元素

要查看所有同步操作的列表，在 Commerce headquarters 中，转到 **Retail 和 Commerce \> 客户 \> 客户同步状态**。 下图显示了一个 **客户同步状态** 页面的示例。

![Commerce headquarters 中的客户同步状态页面。](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

默认情况下，**客户同步状态** 页面左侧的客户同步操作列表包括以下列：

- 渠道名称
- 客户帐户
- 异步客户帐户
- 操作时间戳
- 客户同步状态

页面右上角显示客户帐户详细信息，如 **客户帐户**、**零售异步操作**、**客户同步状态** 和 **上一个已知错误** 值。

**更改描述** 部分包含对运行的客户管理操作类型的描述（例如，客户创建、帐户更新或同步失败与详细信息）。

**客户属性** 部分包含一个显示所有客户属性以及旧值和新值的网格。 如果您想要更改客户属性值来修复 bug，可以编辑此部分，然后再次同步。
