---
title: 设置移动设备菜单项以提供领料行概览
description: 本主题说明如何定义何时向在移动设备上处理仓库工作的仓库工作人员显示所有工作行的列表。 对于经常需要在工作订单中查看领料行概览以便可以优化领料顺序的仓库工作人员，此功能会很有用。
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3a2c8a69a2c64214a38a654042ea2f62575e7f52
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422879"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>设置移动设备菜单项以提供领料行概览

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本主题说明如何为用于处理领料工作的移动设备菜单项配置与领料行概览相关的选项。 领料行概览让仓库工作人员可以查看与其当前任务相关的所有工作行的列表并从中进行选择。 此功能可以帮助工作人员优化领料顺序。 此功能提供的选项可代替标准 **跳过** 按钮，该按钮让工作人员可以固定的顺序每次循环浏览一行。 （不过，使用该按钮的选项仍然可用。）

管理员可以单独配置每个菜单项，来控制仓库应用显示领料行概览的方式、时间和位置。

## <a name="turn-on-the-work-pick-line-overview-feature"></a>打开工作领料行概览功能

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块：**_仓库管理_
- **功能名称**：_工作领料行概览_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>配置菜单项以显示所有工作行的列表

要设置移动设备菜单项以提供领料行概览，请按照下列步骤操作。

1. 转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。
1. 选择或创建与领料工作相关的菜单项，然后设置以下值：

    - **模式：***工作*
    - **使用现有工作**：*是*
    - **导向方式**：*用户导向* 或 *系统导向*

    有关如何创建菜单项以及如何使用 **移动设备菜单项** 页上提供的各种设置的详细信息，请参阅[为仓库工作设置移动设备](configure-mobile-devices-warehouse.md)。

1. 在 **常规** 快速选项卡上，通过将 **显示工作行列表** 字段设置为以下值之一来配置功能：

    - **仅根据要求显示** – 工作人员可以选择通过选择仓库应用中的 **跳至** 按钮来查看领料行列表。
    - **在每次领料开始时显示** – 工作人员在每次开始或完成领料行时会看到列表。 他们还可以通过选择仓库应用中的 **跳至** 按钮来再次查看列表。
    - **仅在第一次领料开始时显示** – 工作人员每次开始新的领料工作时都会看到列表，但在每行之后不会看到。 他们还可以通过选择仓库应用中的 **跳至** 按钮来再次查看列表。
    - **从不显示** – 标准 **跳至** 按钮出现在仓库应用中，工作行列表的显示关闭。 **跳至** 按钮让工作人员可以按固定的顺序每次循环浏览一行。 他们还可以根据需要多次循环浏览列表，直到处理完所有行。

1. 在操作窗格上，选择 **保存**。

    如果将 **显示工作行列表** 字段设置为除 *从不显示* 以外的任何值，操作窗格上的 **字段列表** 按钮将变为可用。

1. 在操作窗格上，选择 **字段列表**。
1. 在 **字段列表** 页上，配置仓库应用为列表中的每一行显示的信息。

    - **主要控件** 字段始终设置为 *LineNum*。 因此，列表中的每一行都以行号开头。
    - 使用其余的 **显示字段** 字段来根据需要添加其他显示字段，最多可添加七个。 每个 **显示字段** 字段中，选择工作行字段的名称。 然后每行将为该字段显示一个值。 这些值将按照您在此处选择的顺序显示。 如果七个值您不是全部需要，可以将某些 **显示字段** 字段保留为空白。

1. 在操作窗格上选择 **保存**，然后关闭 **字段列表** 页。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]