---
title: 处理生命事件
description: 在 Microsoft Dynamics 365 Human Resources 中的员工生命周期中，每个员工可能会遇到各种生命事件的变化。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6bfbb9e31a7d8973c2b993f3792a7216f41924e0ff4c24b08c0dd954ab327c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775009"
---
# <a name="process-life-events"></a>处理生命事件

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

在 Microsoft Dynamics 365 Human Resources 中的员工生命周期中，每个员工可能会遇到各种生命事件的变化。 例如，婚姻、就业变化或依赖方/受益人变化。 要使用生命事件，必须在福利参数窗体中启用生命事件，设置生命事件类型，并为计划类型设置生命事件选项。

您必须在招聘时间范围内至少已经运行了一次开放登记，之后才能够处理生命事件。 在美国，开放登记通常每年一次。 在美国以外地区，开放登记可以在雇用时进行。 工作人员无需选择福利计划即可让生命事件被处理，但需要将其包括在开放登记处理中。 

当您的工作人员有将在未来发生的生命事件时，请使用生命事件处理。 此事件将处理所有尚未处理的生命事件（例如，未来的生命事件或已添加的并非针对任何一个工作人员的生命事件 – 一个例子是一项新的福利）。 实时生命事件是隐藏的。

例如，如果今天是 2 月 1 日，而工作人员 Joe Smith 在 2 月 14 日计划了要更改法人，如果您为 2 月 15 日运行了生命事件处理，系统将处理 2 月 15 日以前的所有事件。 

1. 在 **福利管理** 工作区中，在 **处理** 下，选择 **生命事件处理**。

2. 在 **运行生命事件流程** 对话框中，为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **登记期间** | 要处理其间的生命事件的登记期间。 |
   | **法人** | 要为其处理生命事件的法人。 |
   | **生命事件日期** | 系统将处理在登记期间直到该日期为止的所有事件。 |
   | **工作线程** | 要为其处理生命事件的工作人员。 如果将此字段留为空白，将处理所有工作人员的生命事件。 |

3. 如果要在后台运行此流程，请选择 **在后台运行** 并执行以下任务：

   1. 输入流程的信息。

   2. 要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。

   3. 要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。

   4. 选择 **确定**。 流程将使用您设置的参数运行。

4. 选择 **确定**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]