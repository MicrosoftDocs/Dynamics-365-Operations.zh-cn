---
title: 已删除或已弃用的平台功能
description: 本主题介绍已经或计划从 Finance and Operations 应用的平台更新中移除的功能。
author: sericks007
manager: AnnBe
ms.date: 04/17/2020
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
ms.openlocfilehash: f6365d42de5d19d960641f188cb6052ef07d721f
ms.sourcegitcommit: 6d6aa016c4971b0673d461b82fd80b060ae5f7a1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/17/2020
ms.locfileid: "3268739"
---
# <a name="removed-or-deprecated-platform-features"></a>已删除或已弃用的平台功能

[!include [banner](../includes/banner.md)]

本主题介绍已经或计划从 Finance and Operations 应用的平台更新中移除的功能。

- *已移除*的功能在产品中不再可用。
- *已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。 

> [!NOTE]
> [技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。 可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Finance and Operations 应用版本 10.0.11 的平台更新

### <a name="field-groups-containing-invalid-field-references"></a>其中包含无效字段引用的字段组

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 表元数据定义中的字段组中可能包含无效的字段引用。 如果部署这些字段组，可能导致 Financial Reporting 和 Microsoft SQL Server Reporting Services (SSRS) 中发生运行时失败。 平台更新 23 引入了编译器*警告*，从而解决了这个元数据问题。 Finance and Operations 应用版本 10.0.11 的平台更新将此问题归类为编译器*错误*。<p>若要解决此问题，请按照以下步骤操作。</p><ol><li>删除表字段组定义中的无效字段引用。</li><li>重新编译。</li><li>确保解决了所有错误。</li></ol> |
| **被另一个功能取代？**   | 此编译器错误将永久替代编译器警告。  |
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | **已弃用**：在 Finance and Operations 应用版本 10.0.11 的平台更新中，此编译器警告已成为编译器错误。 |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>使用 SHA1 哈希算法创建的 ISV 许可证

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 已经改变了独立软件供应商 (ISV) 许可证的创建方法。 有关详细信息，请参阅[独立软件供应商 (ISV) 许可](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes)。 |
| **被另一个功能取代？**   | 是。 使用 Windows PowerShell 创建许可证。 |
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | <strong>已弃用：</strong>使用 SHA1 哈希算法创建的 ISV 许可证。 此算法依赖于使用 MakeCert 实用程序创建的证书，但现在已弃用了该实用程序。<p><strong>已弃用：</strong>SHA1 用于安全或哈希用途。 SHA1 将于 2021 年年初停止工作。 因此不应再使用它。<p><strong>已去除：</strong>对传输层安全 (TLS) 1.0 和 TLS 1.1 传入或传出请求的支持。 |

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

