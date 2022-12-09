---
title: 创建具有空白状态的支票
description: 本文将介绍如何为银行帐户创建空白支票。
author: angelad116
ms.date: 10/24/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 86020d9088d8135c83716128a77090608536a78f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804009"
---
# <a name="create-checks-that-have-blank-status"></a>创建具有空白状态的支票

[!include [banner](../includes/banner.md)]

本文将介绍如何创建空白支票。 例如，您可以创建一个空白支票以记录已损坏并且不能用于付款的支票。

在 **支票** 页面上，可对支票执行维护任务。 例如，您可以创建新支票编号以及删除支票。 您也可以创建具有 **空白** 状态的支票。 在创建空白支票之后，将无法在系统中删除或重用这些支票。

> [!NOTE]
> 仅当在 **功能管理** 页面中启用 **在“支票”页面中创建具有空白状态的支票** 功能时，此功能才在 **支票** 页面中可用。 如果未启用该功能，则只能在应付帐款的付款生成流程期间从 **支票付款** 对话框创建具有 **空白** 状态的支票。

若要打开 **支票** 页面，请转到 **现金和银行管理 \> 银行帐户 \> 银行帐户**，然后在操作窗格的 **管理付款** 选项卡的 **相关信息** 组中，选择 **支票**。 或者，请转到 **现金和银行管理 \> 查询和报表 \> 支票**。

然后，若要创建具有 **空白** 状态的支票，请在“操作”窗格中选择 **创建空白支票**。 创建空白支票时，关联的银行帐户将会暂时禁用。 此行为将会降低在创建空白支票时生成付款的风险。 处理完成后，关联的银行帐户将重新激活。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
