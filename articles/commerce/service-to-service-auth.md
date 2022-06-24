---
title: 配置服务对服务身份验证
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中配置服务对服务身份验证以安全调用服务 API 来获取评分和评价。
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: acb3a6220d146d32bbeb5bd8169033bc897ec3fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871599"
---
# <a name="configure-service-to-service-authentication"></a>配置服务对服务身份验证

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中配置服务对服务 (S2S) 身份验证以安全调用服务应用编程接口 (API) 来获取评分和评价。

Dynamics 365 Commerce 提供[评分和评价](ratings-reviews-overview.md)作为全渠道解决方案。 此解决方案允许从 Commerce 外部访问服务 API，以便能够执行各种任务。 这些任务包括将来自外部系统的评分和评价导入到 Commerce，以及从 Commerce 导出评分和评价。 要使 Commerce 能够安全地调用评分和评价服务 API，您必须先通过完成本文中的程序来配置 S2S 身份验证。

## <a name="add-a-new-app-registration"></a>添加新的应用注册

添加新的应用注册之前，必须使用 [Azure 门户](https://portal.azure.com)创建应用程序。 若要在 Azure Active Directory (Azure AD) 中注册应用并启用身份验证，请按照[将 Azure Active Directory 与 Power Automate 中的自定义连接器配合使用](/connectors/custom-connectors/azure-active-directory-authentication)中的步骤执行操作。

从 Azure 门户收集以下 ID。 您将需要在后面的步骤中使用这些 ID。

- 客户端应用程序 ID
- 客户端目录（租户）ID

若要在 Commerce 站点构建器中添加新应用注册，请执行以下步骤。

1. 转到 **主页 \> 审阅 \> 设置**。
1. 在 **服务对服务 (S2S) 身份验证** 下面，选择 **管理**。

    ![Commerce 站点生成器内“服务对服务 (S2S) 身份验证”部分中的“管理”按钮。](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. 在右侧显示的 **S2S 应用条目** 窗格中，选择 **添加新的 S2S 应用注册**。
1. 在 **添加 S2S 应用条目** 对话框中，输入以下必需信息。 使用 Azure 应用程序注册中的值。

    - **名称** - 输入您的应用程序的名称（例如，**Fabrikam App**）。
    - **客户端应用 ID** - 输入应用程序 ID（例如 **00000000-0000-0000-0000-000000000000**）。
    - **目录（租户）ID** - 输入目录 ID（例如 **00000000-0000-0000-0000-000000000000**）。

    ![在 Commerce 站点构建器中添加“S2S 应用条目”对话框。](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. 选择 **提交**。 您的应用程序名称应出现在 **S2S 应用条目** 窗格的列表中。
1. 关闭 **S2S 应用条目** 窗格。
1. 选择 **保存**。

## <a name="edit-an-existing-app-registration"></a>编辑现有的应用注册

若要在 Commerce 站点构建器中编辑现有应用注册，请执行以下步骤。

1. 转到 **主页 \> 审阅 \> 设置**。
1. 在 **服务对服务 (S2S) 身份验证** 下面，选择 **管理**。
1. 在 **S2S 应用条目** 窗格中，选择要编辑的条目旁边的铅笔符号。
1. 根据需要更新 **名称**、**客户端应用 ID** 和 **目录（租户）ID** 字段中的值。
1. 选择 **提交**。
1. 关闭 **S2S 应用条目** 窗格。
1. 选择 **保存**。

## <a name="remove-an-existing-app-registration"></a>删除现有的应用注册

若要在 Commerce 站点构建器中删除现有应用注册，请执行以下步骤。

1. 转到 **主页 \> 审阅 \> 设置**。
1. 在 **服务对服务 (S2S) 身份验证** 下面，选择 **管理**。
1. 在 **S2S 应用条目** 窗格中，选择要删除的条目旁边的垃圾桶符号。 从列表中删除了该条目。
1. 关闭 **S2S 应用条目** 窗格。
1. 选择 **保存**。

## <a name="additional-resources"></a>其他资源

[评分和评价概览](ratings-reviews-overview.md)

[选择使用评分和评价](opt-in-ratings-reviews.md)

[管理评分和评价](manage-reviews.md)

[配置评分和评价](configure-ratings-reviews.md)

[同步产品评分](sync-product-ratings.md)

[启用审查者手动发布评分和评价](manual-publish-rating-reviews.md)

[导入和导出评分和评价](import-export-reviews.md)

[评分和评价常见问题解答](ratings-reviews-faq.md) 
