---
title: 已删除或已弃用的平台功能
description: 本主题介绍已经或计划从 Finance and Operations 应用的平台更新中移除的功能。
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
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
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095766"
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

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>云托管服务呈现的分页文档中将不再支持嵌入式钻取链接 
|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 服务呈现的文档中嵌入的导航 URL 中可能包含敏感的业务数据。 我们将取消对文档中的嵌入式钻取链接的支持，这是我们为了进一步保护客户的数据采取的安全预防措施。 此项更改还将让用户在以交互方式生成文档时可以享受性能提升。  |
| **被另一个功能取代？**   | 无 |
| **影响的产品区域**         | 申报 |
| **部署选项**              | 所有 |
| **状态**                         | 正在从服务中努力移除此功能。<br><br>现代客户端提供大量选项，用于生成其中包含自动生成的链接的视图，以便帮助您在应用程序中导航。 将为收件人推荐通过电子邮件发送，归档和打印的外部通信使用服务呈现的分页文档。 我们改进了直接在浏览器中预览文档的体验，可以直接访问本地打印机。 有关详细信息，请参阅[使用嵌入式查看器预览 PDF 文档](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents)。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>之前有关已删除或已弃用功能的声明
若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../migration-upgrade/deprecated-features.md)。

