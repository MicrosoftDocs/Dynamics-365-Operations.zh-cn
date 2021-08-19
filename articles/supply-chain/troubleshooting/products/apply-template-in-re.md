---
title: 您不能将模板应用于已发布产品
description: 您不能将模板应用于已发布产品。
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 566686b6a86e67c87f75f9f2e397592174d3d749034f18997ca8ce651c2594a2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760386"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>您不能应用模板来创建已发布产品

知识库编号：4612097

## <a name="symptoms"></a>故障特征

使用 **新建已发布产品** 对话框创建新的已发布产品时，可以选择一个模板。 模板应会为新的已发布产品的很多字段提供默认设置。 但是，选择模板后部分或全部字段并未设置。

## <a name="cause"></a>原因

通过 Microsoft Dynamics 365 Supply Chain Management 中的很多页面，您都可以创建模板来为这些页面上显示的记录建立初始设置。 您可以通过在操作窗格的 **选项** 选项卡上选择 **记录信息** 来创建一个模板。 不过，已发布产品比大多数其他类型的记录要复杂得多。 虽然您可以在 **已发布产品** 页上选择 **记录信息** 来创建模板，并且可以在创建已发布产品时选择该模板，但是此模板不会为新的已发布产品提供预期的字段值。 因此，您不能为已发布产品使用“记录信息”模板。 而是必须创建专用的产品模板。

## <a name="resolution"></a>解决方法

要创建产品模板，使用操作窗格的 **产品** 选项卡上的 **模板** 菜单，不要使用 **选项** 选项卡上的 **记录信息** 按钮。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 在操作窗格上，在 **产品** 选项卡上的 **新建** 组中，选择 **模板**，然后视情况选择 **创建个人模板** 或 **创建共享模板**。
