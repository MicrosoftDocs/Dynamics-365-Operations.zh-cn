---
title: 查看供应商发票自动化结果（预览）
description: 本主题说明了如何查看自动提交到工作流程中的供应商发票的状态。
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: baa2f1f55dfb9bb93b4f27c45db563e39850dd37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969718"
---
# <a name="view-vendor-invoice-automation-results"></a>查看供应商发票自动化结果

[!include [banner](../includes/banner.md)]

本主题说明了如何查看自动提交到工作流程中的供应商发票的状态。 将为每个导入的供应商发票维护自动化历史记录的详细信息。 根据您自动化的业务流程，**待定供应商发票** 页面显示 **自动化收货匹配状态** 和 **自动提交到工作流状态** 值。 您可以查看详细信息并制定计划以侧重于自动化步骤失败的发票。 然后，在更正问题后，您可以恢复导入的发票的自动化流程。

在编辑已提交的发票之前，必须暂停自动化流程。 如果必须暂停自动提交到工作流程中的发票，请在 **供应商发票** 页面上将 **包括在自动化流程中** 设置为 **否**。 然后，直到 **包括在自动化流程中** 设置为 **是**，才能运行自动化。 如果发票尚未在工作流系统中并且未被自动化流程使用，则可以暂停发票进行进一步自动化。

如果导入的发票执行提交到工作流程，则可以在 **供应商发票** 页面上查看其 **自动化状态** 值。 跟踪以下状态：

- **已包括** – 在 **应付帐款参数** 页面上定义的自动化流程运行正常，但尚未完成。
- **已暂停** – 在 **应付帐款参数** 页面上定义的自动化流程已运行，但流程中至少有一个步骤失败。 如果 **包括在自动化流程中** 字段设置为 **否**，还应用 **已暂停** 状态。 您可以通过选择 **查看最新结果** 来查看失败。
- **在工作流中** – 导入的发票已通过自动提交到工作流程或手动提交到工作流系统。
- **工作流完成** – 已完成导入的发票的工作流程。
