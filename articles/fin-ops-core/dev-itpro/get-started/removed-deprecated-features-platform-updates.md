---
title: 已删除或已弃用的平台功能
description: 本主题介绍已经或计划从 Finance and Operations 应用的平台更新中移除的功能。
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087875"
---
# <a name="removed-or-deprecated-platform-features"></a>已删除或已弃用的平台功能

[!include [banner](../includes/banner.md)]

本主题介绍已经或计划从 Finance and Operations 应用的平台更新中移除的功能。

- *已移除*的功能在产品中不再可用。
- *已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。 

> [!NOTE]
> [技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。 可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。

## <a name="platform-update-32"></a>平台 update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>“工作流请求更改”对话框中不再包含用户选择下拉列表
|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 这是一个安全问题，因为可能会将更改请求发送给非预期用户。 这也是一个可用性问题，因为它会强制用户确定工作流发起者是谁和谁手动选择它们。  |
| **被另一个功能取代？**   | 否 |
| **影响的产品区域**         | 工作流 |
| **部署选项**              | 所有 |
| **状态**                         | 已从平台更新 32 中的请求更改对话框内删除了用户选择下拉列表。 将把请求更改请求正常自动发送到发起者。 有关此功能的详细信息，请参阅[工作流审核流程中的操作](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change)。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>之前有关已删除或已弃用功能的声明
若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../migration-upgrade/deprecated-features.md)。

