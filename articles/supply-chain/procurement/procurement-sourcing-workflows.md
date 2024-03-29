---
title: 采购工作流
description: 某些组织要求采购申请和采购订单由输入交易记录的人之外的用户进行审核。 若要设置审核流程，您可以创建一个工作流。
author: GalynaFedorova
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebfd96690eea762d0797db1b485544d957d17ce0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671917"
---
# <a name="procurement-and-sourcing-workflows"></a>采购工作流

[!include [banner](../includes/banner.md)]

某些组织要求采购申请和采购订单由输入交易记录的人之外的用户进行审核。 若要设置审核流程，您可以创建一个工作流。

“工作流”代表业务流程。 它定义单据如何在系统中流动并指示必须由谁完成任务或审核单据。 在组织内使用工作流系统具有若干优点：

- **一致的流程**— 您可定义特定单据（如采购申请和支出报表）的审核流程。 使用工作流系统有助于确保以一致且有效的方式来处理和审核单据。
- **流程可见性**— 您可跟踪特定工作流实例的状态、历史记录和绩效指标。 这帮助您确定是否需要对该工作流做出更改，以提高效率。
- **集中的工作列表**— 用户可以查看集中的工作列表，以便跨他们所参与的所有工作流查看分配给他们的工作流任务和审核。 这在“工作项”页上可用。

## <a name="the-types-of-workflows-that-you-can-create"></a>您可以创建的工作流类型

以下工作流类型可用于采购。

| 类型 | 使用此类型可以 |
|---|---|
| 采购申请审核 | 为采购申请创建审核和批准工作流。 |
| 采购申请行审查 | 为采购申请行创建审核和批准工作流。 |
| 采购订单工作流 | 针对采购订单创建检查和审核工作流。 |
| 采购订单行工作流 | 针对采购订单行创建检查和审核工作流。 |
| 供应商添加申请工作流 | 为通过供应商请求添加新供应商创建审核和批准工作流。 |

> [!IMPORTANT]
> 当您添加新的工作流时，您可能还会在 **创建工作流** 对话框中看到列出的以下过时工作流。 这些与 [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows) 中提供的 *收货确认* 功能有关，但现在已弃用。 目前不支持这些工作流。
> 
> - 交货到期日期通知工作流
> - 收到的账单通知工作流
> - 物料收货失败通知工作流
> - 未确认的物料收货拒绝通知工作流

## <a name="creating-a-workflow"></a>创建工作流

若要创建工作流，请转到“采购”&gt;“设置”&gt;“采购”工作流，并通过选择您要创建的工作流类型创建新工作流。 

在工作流画布中，您可以将工作流元素拖动到设计器并将元素链接到流。 应配置工作流元素。 对于审核和任务工作流元素，您可以配置哪个参与者应采取行动。

## <a name="types-of-participants"></a>参与者类型

您可以将审核步骤分配到以下的参与者组。

| 用户组 | 描述 |
|---|---|
| 参与者 | 将审核步骤分配到组的成员或角色。 |
| 层次结构 | 将审核步骤分配给特定组织层次结构中的用户。 |
| 工作流用户 | 将审核步骤分配给此工作流的用户。 |
| 队列 | 将审核步骤分配给工作项队列。 |
| 用户 | 将审核步骤分配给特定用户。 |

## <a name="additional-resources"></a>其他资源

- [定义采购申请的业务流程工作流](https://www.microsoft.com/download/details.aspx?id=101821)
- [采购申请工作流](purchase-requisitions-workflow.md)
- [载入供应商](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]