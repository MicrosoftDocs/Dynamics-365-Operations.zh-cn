---
title: 创建开放式长期休假
description: 本文介绍如何在 Microsoft Dynamics 365 Human Resources 中创建开放式长期休假。
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08231d4139209387c3c76923fafdd2061fceb280
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805334"
---
# <a name="create-an-open-ended-leave-of-absence"></a>创建开放式长期休假

> [!IMPORTANT]
> 本文中介绍的功能将在 Microsoft Dynamics 365 Finance 版本 10.0.31 后作为未来版本的一部分在 Finance 基础结构上提供。

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

您可以提交开放式休假请求，并在 Dynamics 365 Human Resources 中查看休假请求的状态。

## <a name="prerequisites"></a>先决条件

1. 在 **功能管理** 下，确保 **开放式休假** 功能已开启。

    > [!IMPORTANT]
    > 此功能打开后无法关闭。

2. 创建休假类型。
3. 输入休假类型、说明和工作流 ID 等详细信息。
4. 在 **请求类型** 字段中，选择 **休假**。
5. 在详细信息部分，对于开放式休假，将 **开放式** 选项设置为 **是**。
6. 将 **重返工作岗位通知** 选项设置为 **是** 或 **否**。
7. 对于开放式休假请求，可以选择要求重返工作岗位通知。

> [!NOTE]
> 启用此功能后，将启用 **需要附件** 功能。

## <a name="request-an-open-ended-leave-of-absence"></a>申请开放式长期休假

1. 在 **员工自助服务** 工作区中，在 **休假余额** 磁贴中，选择 **更多 (...)**。
2. 要提交休假请求，请选择 **申请休假**。
3. 在 **休假类型** 和 **开始日期** 字段中输入信息。 在 **结束日期** 字段中输入暂定结束日期。
4. 如果您必须提交支持文档，在 **附件** 下选择 **上载**。
5. 准备好提交请求时选择 **提交**。 否则，选择 **保存草稿**。
6. 要更新开放式休假请求，选择请求，在 **结束日期** 字段中输入结束日期，将 **确认结束日期** 选项设置为 **是**，然后上载文档。
7. 如果 **重返工作岗位通知** 选项设置为 **是**，选择 **上载**，然后选中复选框确认已上载有效的重返工作岗位通知。
8. 输入所有详细信息后，选择 **提交**。
