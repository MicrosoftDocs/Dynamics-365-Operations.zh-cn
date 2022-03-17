---
title: 将付款计划应用于发票日记帐
description: 本主题介绍如何将付款添加到供应商发票日记帐。
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f6481c3fc033acf4bb563bf1716789216646b60b
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358331"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>将付款计划应用于发票日记帐

[!include [banner](../includes/preview-banner.md)]

在 Microsoft Dynamics 365 Finance 版本 10.0.25 中，**供应商发票日记帐** 上现在支持付款计划。

要使用此功能，您必须在“功能管理中”启用 **将付款计划应用于发票日记帐** 功能。

启用此功能后，一个新的 **付款计划** 字段将被添加到 **发票日记帐** 页面。 当您创建发票日记帐行时，如果在供应商上维护付款期限，并且在付款计划中选择了付款期限，**付款计划** 字段将在 **发票日记帐** 页更新。

您可以根据业务要求更改所使用的付款计划。 在过帐供应商发票日记帐期间，将根据付款计划创建供应商未结交易记录。

 - 要查看从付款计划生成的多个供应商未结交易记录，转到 **应付帐款 \> 发票 \> 未结供应商发票**，输入发票编号或供应商帐户。
 - 要查看或配置付款计划，转到 **应付帐款 \> 付款设置 \> 付款计划**。
 - 要配置付款期限并分配付款计划，转到 **应付帐款 \> 付款设置 \> 付款期限**。
 - 要在供应商上维护付款期限，转到 **应付帐款 \> 所有供应商**，选择供应商帐户，然后在 **付款** 选项卡上，设置 **付款期限** 字段。

付款计划功能在 **供应商发票登记** 流程中也可用。 如果在发票登记日记帐上选择了付款计划，在过帐发票登记时将 **不会** 生成多个供应商付款行。 将在审核发票时生成供应商付款行。

## <a name="limitation"></a>限制

对于待定供应商发票，如果付款计划位于发票标头上，将有允许用户编辑付款行的高级页面。 （例如，用户可以编辑每个付款行的截止日期和值。）从发票日记帐生成的付款行将具有付款计划中的值。

此功能将可用于将来版本中的 **供应商发票日记帐** 和 **待定发票**。
