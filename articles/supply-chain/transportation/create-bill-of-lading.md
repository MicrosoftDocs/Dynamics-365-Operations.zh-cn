---
title: 创建提单
description: 本文介绍在使用仓库管理流程 (WMS) 时如何创建提单。
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68a703475191255ff6ceaee25ef8e2bdf33ba0c2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069687"
---
# <a name="create-a-bill-of-lading"></a>创建提单

[!include [banner](../includes/banner.md)]

本文介绍在使用仓库管理流程 (WMS) 时如何创建提单。  

提单是装运物料的公司和承运人之间的法律文档。 此文档随装运的物料一并提供，在物料在目的地交货时充当装运收据。 如果您使用仓库管理，有两种方法生成提单：

  -   使用 **提单** 页面手动创建报表。
  -   从 **装载计划工作台** 生成报表。

如果您从 **装载计划工作台** 生成提单，负荷状态必须为 **已装运**。 如果一个负荷中有多个装运，提单为每个装运创建。 提单创建后，您可以在 **提单** 页面对其进行更改。

## <a name="master-bill-of-lading"></a>主提单
当负荷中存在多个装运，您可以生成主提单。 这与提单有相同的布局和信息，但包含所有装运的汇总内容。 如果 **当负荷上存在多个装运时创建主提单** 在 **运输管理参数** 页面选项设置为 **是**，如果您从 **装载计划工作台** 创建提单，并且具有多个装运，主提单将自动生成。 您还可以通过单击 **相关信息** &gt; **提单** 获取提单的列表。 如果手动创建提单，则可以在 **提单** 页面创建主提单。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]