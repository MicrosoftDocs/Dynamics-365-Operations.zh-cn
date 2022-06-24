---
title: 配置云和边缘缩放单元的 Warehouse Management 移动应用
description: 本文介绍如何为由云或边缘缩放单元提供服务的仓库设置 Warehouse Management 移动应用。
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865229"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>配置云和边缘缩放单元的 Warehouse Management 移动应用

[!include [banner](../includes/banner.md)]

本文介绍如何设置您的 Warehouse Management 移动应用，让它们可以在由云或边缘缩放单元提供服务的仓库中使用。

## <a name="prerequisites"></a>先决条件

在您开始设置移动设备以连接到云或边缘缩放单元之前，请确认它们可以连接到企业中心。 有关说明，请参阅[安装和连接 Warehouse Management 移动应用](../warehousing/install-configure-warehouse-management-app.md)。

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>对缩放单元运行 Warehouse Management 移动应用时的其他设置

作为[仓库缩放单元工作负荷部署流程](cloud-edge-landing-page.md#scale-unit-manager-portal)的一部分，连接您的 Warehouse Management 移动应用设备所需的大部分数据会自动从企业中心同步到缩放单元。 但是，您必须在缩放单元部署的 **Azure Active Directory 应用程序** 页面（**系统管理 \> 设置 \> Azure Active Directory 应用程序**）输入数据。 此外，您可能必须更新用户 ID 的默认 **公司** 值或创建新用户。 当 Warehouse Management 移动应用连接到缩放单元时，与缩放单元部署中不存在的公司关联的用户将无法登录。

> [!NOTE]
> 由于 **Azure Active Directory 应用程序** 页面上的数据不同步，如果您要将仓库工作负荷移动到其他缩放单元，则必须手动维护此数据。

请记住，作为每个 Warehouse Management 移动应用连接设置的一部分，指定 Azure Active Directory 的资源 URL 必须是针对缩放单元而不是企业中心。
