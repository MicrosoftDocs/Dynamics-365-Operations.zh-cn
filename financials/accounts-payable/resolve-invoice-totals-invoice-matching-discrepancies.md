---
title: "解决发票合计匹配期间出现的差异"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: 8ccc1af0e1bd7909b7810d359a916849ecc1a709
ms.contentlocale: zh-cn
ms.lasthandoff: 08/09/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>解决发票合计匹配期间出现的差异

[!include[banner](../includes/banner.md)]




发票合计匹配是发票匹配验证的类型之一。 要指定系统应执行发票合计匹配，请在**“应付帐款参数”**页上的**“发票验证”**选项卡上，将**“匹配发票合计”**选项设置为**“是”**。 

您可以使用发票合计匹配来帮助确保发票总金额与预期金额之间的差异不会超出可接受的差异。 在**“发票合计匹配详细信息”**页面上比较六项合计。 如果任一合计偏离预期的相应采购订单合计，则标记匹配差异。 

要检查具有合计匹配差异的发票，请在**“供应商发票项”**工作区中，单击**“待定发票”**磁贴。 然后，在“操作”窗格的**“检查”**选项卡上，单击**“匹配详细信息”**。 如果检测到匹配差异，则发票金额旁边会显示警告图标。 您可以通过查看发票合计匹配详细信息来查看有关合计的更多详细信息。 

在标识差异后，如果您认为发票上的信息不正确，则可能必须与供应商联系。 根据与供应商签订的最终协议，您随后可执行以下任一操作：

-   接受价格差异并过帐具有匹配差异的发票。 您的系统可能设置为在存在匹配差异的情况下要求先获得批准，然后才能过帐。 在此情况下，您必须批准匹配差异，并且可以选择性地输入批准注释。 然后，您可以选择过帐发票。
-   将发票金额修正为预期金额并过帐该发票。
-   从供应商处请求完全信用和新的纠正后的发票。

有关详细信息，请参阅[研究或解析异常](tasks/research-resolve-exceptions.md)。



