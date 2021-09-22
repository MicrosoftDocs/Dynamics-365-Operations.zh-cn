---
title: 找不到库存日记帐的“工作流”下拉对话框
description: 在日记帐页上找不到“工作流”下拉对话框，或相关的工作流操作不可用
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475670"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>找不到库存日记帐的“工作流”下拉对话框

## <a name="symptoms"></a>故障特征

在日记帐页上找不到 **工作流** 下拉对话框，或相关的工作流操作不可用。

发生此问题可能由于三个原因，如以下部分所述。

## <a name="resolution-1"></a>解决方法 1

如果问题适用于所有用户，可能是由于未将审批工作流分配给日记帐名称。 若要解决此问题，请按照以下步骤操作。

1. 转到 **库存管理 &gt; 设置 &gt; 日记帐名称 &gt; 库存**。
1. 在列表窗格中，选择一个日记帐名称来打开其设置。
1. 在 **常规** 快速选项卡上，将 **审批工作流** 选项设置为 *是*。 如果提示确认更改，选择 **是**。
1. 在 **工作流** 字段中，选择要用于所选日记帐名称的工作流。

## <a name="resolution-2"></a>解决方法 2

如果您的工作流使用自定义代码，在升级系统后可能会出现问题。 例如，在日记帐工作流中，**提交** 按钮可能为灰色，因此您无法选择它来审批提交。

如果 **提交** 按钮是灰显，您的工作流可能已自定义，这意味着工作流的方法 `FormDataUtil` 中的 `canSubmitToWorkflow()` 已扩展。 要解决此问题，更改您扩展 `canSubmitToWorkflow()` 方法的方式以使用以下示例中的结构。

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>解决方法 3

如果此问题仅适用于少数几个特定用户，有可能是这些用户没有对库存日记帐运行工作流操作所需的安全特权。 请验证是否每个受影响的用户都有 *维护库存日记帐工作流* 安全特权。 默认情况下，此特权分配给具有相同名称的职责，该职责适用于 *仓库工作人员* 和 *仓库经理* 角色。
