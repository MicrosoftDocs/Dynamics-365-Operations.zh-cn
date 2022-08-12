---
title: 返点管理交易工作流
description: 本文说明如何设置返点管理交易工作流以审核和激活交易。
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4f0590c4c906e746b54ac30fd6531b8c1cd67915
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067323"
---
# <a name="rebate-management-deal-workflows"></a>返点管理交易工作流

[!include [banner](../includes/banner.md)]

若要审核返点交易，返点管理使用与其他财务和运营应用相同的工作流平台。 每个工作流关联了两个作业流程：

- 工作流的另一个元素用于审核交易。
- 工作流的一个元素用于激活交易，以便用户或工作流程可以审核交易记录。

返点交易必须在 **返点管理** 模块中处于活动状态，然后才可供使用。 若要激活交易，必须首先创建和配置 *返点管理交易工作流*。

用户无法手动审核交易。 必须始终使用工作流。

## <a name="create-and-manage-rebate-management-deal-workflows"></a>创建和管理返点管理交易工作流

若要使用返点管理交易工作流，请转到 **返点管理 \> 设置 \> 返点管理工作流**。 在此处，您可以根据需要查看、创建和更新工作流。 一次只能激活此类型的一个工作流。 有关工作流的详细信息、如何使用 **返点管理工作流** 页面以及如何创建工作流，请参阅[工作流系统概述](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md)及其相关文章。

## <a name="use-a-workflow-to-activate-a-deal"></a>使用工作流激活交易

若要通过工作流激活交易，请打开交易（例如，在 **所有返点管理交易** 页面上）。 然后，在操作窗格上，选择 **工作流 \> 提交**。 通过工作流处理和审核新交易后，它将处于活动状态并且可供使用。

激活交易后，您将无法更改大多数设置。 如果您必须更改活动的交易，请首先取消激活它，然后创建新交易。 如果新交易类似于旧交易，则可以通过复制旧交易来创建它。

激活交易后，您可以更改交易的以下设置：

- 对帐依据
- 累积担保
- 过帐模板
- 担保的过帐配置文件
- 单据通知单
- 货币
- 开始日期
- 截止日期

此外，可以删除返点行。

