---
title: 设置和处理重复发票
description: 本文说明如何设置和处理重复发票。 如果您必须定期为客户开具相同金额的发票，可以使用重复发票。
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce734567f0c5bf02e30c36484449c3869b82dc84
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724746"
---
# <a name="set-up-and-process-recurring-invoices"></a>设置和处理重复发票

[!include [banner](../includes/banner.md)]

本文说明如何设置和处理重复发票。 如果您必须定期为客户开具相同金额的发票，可以使用重复发票。

## <a name="create-a-recurring-free-text-invoice-template"></a>创建重复执行普通发票的模板

若要定期就相同服务为客户开票，必须定义可以重新用于创建发票的普通发票模板。 此模板包含以下信息：

-   标题信息，如税组、付款期限和付款方法
-   行信息，例如服务描述、收入帐户、单位价格和发票金额
-   装运或处理的费用
-   与财务维度信息一起的会计分配，例如成本中心和业务单位

实际上，您创建整个发票并将其保存为模板。 可以使用 **重复发票** 页设置模板。

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>将普通发票模板分配给客户并输入重复详细信息
在模板创建后，必须将该模板分配到您要为其开票的客户。 此外，必须指定发票使用的时间和频率。 您可以将在 **客户** 页的 **发票** 选项卡上分配模板。 将该模板添加到列表，并更新以下信息：

-   重复计费的开始日期和结束日期（可选）
-   重复计费的频率（例如，每天或每月一次）
-   最大计费金额（如果需要此信息）

客户有具有不同频率的多个模板。

## <a name="generate-the-recurring-invoices"></a>生成重复发票
在 **重复发票** 页，存在处理重复发票模板的任务。 您指定发票日期和以及从中生成发票的模板。 发票将生成并且为处理的每个发票组分配单一重复执行 ID 号。

## <a name="post-recurring-free-text-invoices"></a>过帐重复执行普通发票

在重复发票生成后，发票重复执行 ID 出现在 **重复发票** 页的过帐任务中。 您可以通过单击该链接查看重复执行 ID 的所有发票。 在您审查重复执行 ID 的发票时，您可以删除单个发票。 客户的重复执行设置将为该模板重置，以便它可在以后重新生成。 您可以过帐一个、许多或所有重复执行 ID 的发票。 如果启用工作流，您必须单击 **提交**，然后才能过帐发票。

## <a name="print-recurring-free-text-invoices"></a>打印重复执行普通发票

在重复发票过帐后，可以从普通发票列表页打印发票。 您可以打印选择的发票，或者可以选择要打印的发票范围。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
