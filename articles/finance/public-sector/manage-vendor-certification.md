---
title: 维护供应商认证
description: 本文介绍供应商可以用来使用供应商协作工作区维护认证的步骤。
author: TaylorVH
ms.date: 04/27/2021
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c66952d19cddd9d4a9a102ba59e8d6d97b75ed4d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/22/2022
ms.locfileid: "9583197"
---
# <a name="maintain-vendor-certification"></a>维护供应商认证

[!include [banner](../includes/banner.md)]

本文介绍供应商可以用来使用 **供应商协作工作区** 维护认证的步骤。 认证的示例可能包括 Woman Business Enterprise (WBE) 或 Leadership in Energy and Environment Design (LEED) 公司。 供应商需要在 **供应商信息** 工作区输入认证信息。 从那里，供应商将选择 **更多详细信息**，然后选择 **认证**。

## <a name="turn-on-the-vendor-certification-feature"></a>启用供应商认证功能

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)页面检查功能状态，并在需要时启用。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块** - *应付帐款*
- **功能名称** - *启用供应商协作认证管理*

## <a name="add-a-new-certification"></a>添加新认证

要添加新认证，选择 **供应商信息** 工作区中 **认证** 网格上方的 **添加** 按钮。 输入以下信息：

- 证书编号
- 证书类型
- 证书颁发组织
- 证书日期
- 负债金额（如果适用）
- 生效日期
- 到期日期
- 注释（可选）

如果存在与特定认证有关的文档，可以选择 **文档** 按钮附加这些文档。

您的供应商在此页面上输入的认证将被指定为“供应商”来源。 您可以在供应商银行帐户下代表您的供应商输入证书信息。 这些信息将显示在此处，来源将显示 **客户**。

供应商可以根据需要编辑或删除证书。

## <a name="vendor-collaboration-generated-certification-records"></a>供应商协作生成的认证记录

供应商添加了认证信息后，该信息将显示在 **供应商协作生成的认证** 页上。 要打开此页面，转到 **应付帐款 > 查询 > 供应商报表 > 供应商协作生成的认证**。 默认情况下，所有新的或修改的认证记录都可见。 应付帐款职员可以查看更改并通过确认流程验证信息来进行验证。 确认信息后，可以选择页面上列出的认证记录并将其标记为已审核。 将记录标记为已审核会将其从默认列表中删除。

所有认证更改都可以在 **供应商协作生成的认证** 页上看到。 如果页面上未显示更改，您可以通过调整供应商帐户、有效日期范围的筛选器，或选择是否包括已审核的认证更改信息来查看更改。

