---
title: 通过计划优化自动确认
description: 本主题说明如何通过计划优化使用自动确认。
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: d014fcd542462e092f6e88232dff8fd5ee2253c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963452"
---
# <a name="autofirming-with-planning-optimization"></a>通过计划优化自动确认

[!include [banner](../../includes/banner.md)]

自动确认可以使您作为主计划流程的一部分确认（即下达）计划订单。 确认计划订单后，它们将转换为实际的采购订单、转移单或生产订单。 使用计划优化时，如果订单日期（即开始日期）在用于确认的时间范围内，在主计划运行期间将确认计划订单。

> [!NOTE]
> 仅当物料与供应商关联时，才可自动确认计划采购订单。

## <a name="turn-on-autofirming"></a>开启自动确认

若要开启自动确认，请执行以下步骤。

1. 在 **功能管理** 工作区中的 **新** 选项卡上，在列表中选择 **计划优化自动确认**。 如果该功能未出现在 **新** 选项卡上，请查看 **未启用** 和 **所有** 选项卡。
1. 选择 **立即启用**。 或者，选择 **时间表**，然后选择要启用该功能的时间。

## <a name="set-up-the-firming-time-fence"></a>设置确认时限

确认时限是基于主计划运行日期向前推算的。 它由您输入的天数定义。 您可以通过以下方式控制确认时限：

- 要定义覆盖范围组的默认确认时限，请转到 **主计划** \> **设置** \> **覆盖范围** \> **覆盖范围组**，并选择一个覆盖范围组。 然后，在 **其他** 快速选项卡上的 **自动确认时限(天)** 字段中，输入天数。
- 要覆盖为特定物料的覆盖范围组定义的确认时限，请转到 **产品信息管理** \> **已发布产品**，然后从操作窗格中选择 **计划**，然后选择 **物料覆盖范围**。 然后，在 **常规** 选项卡上，选择 **覆盖时限**，然后在 **自动确认时限(天)** 字段中输入天数。
- 要覆盖为特定主计划的覆盖范围组和物料覆盖范围定义的确认时限，请转到 **主计划** \> **设置** \> **主计划**，然后选择一个主计划。 然后，在 **时限(天)** 快速选项卡上，将 **确认** 设置为 **是**，然后输入天数。

如果为使用计划优化的主计划运行打开了自动确认，自动确认流程将根据自动确认设置完成。 如果未启用自动确认，或者从 **净需求** 页面开始了计划，则会跳过自动确认流程。

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>计划优化与内置的 Supply Chain Management 计划引擎

计划优化和 Microsoft Dynamics 365 Supply Chain Management 中内置的计划引擎都可以用来自动确认计划订单。 不过，也存在某些重要差异。 例如，计划优化使用订单日期（即开始日期）来确定要确认的计划订单，而内置的 Supply Chain Management 计划引擎则使用需求日期（即结束日期）。 以下是区别汇总。

**计划优化**

- 自动确认基于订单日期（开始日期）。
- 由于订单日期（开始日期）触发确认，因此您不必将提前期视为确认时限的一部分。
- 如果要确认必须在当前一周开始的所有订单，则确认时限必须为一周。

**内置 Supply Chain Management 计划引擎**

- 自动确认基于需求日期（结束日期）。
- 为了帮助确保按到期时间确认订单，确认时限必须长于提前期。
- 如果要确认必须在当前一周开始的所有订单，则确认时限必须为提前期再加上一周时间。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]