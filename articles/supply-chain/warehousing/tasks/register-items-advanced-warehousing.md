---
title: 使用物料到达日记帐登记启用了仓库管理流程的物料
description: 本文提供的场景显示在使用仓库管理流程 (WMS) 时如何使用物料到达日记帐登记物料。
author: Mirzaab
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5241c982675d6b9a9bc9596b8ac9ed2798903287
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066958"
---
# <a name="register-items-enabled-for-warehouse-management-processes-using-an-item-arrival-journal"></a>使用物料到达日记帐登记启用了仓库管理流程的物料

[!include [banner](../../includes/banner.md)]

本文提供的场景显示在使用仓库管理流程 (WMS) 时如何使用物料到达日记帐登记物料。 这将通常由一个收料员完成。

## <a name="enable-sample-data"></a>启用示例数据

若要使用在本文中指定的示例记录和值完成此场景，您必须使用安装了标准演示数据的系统，并且必须在开始之前选择 *USMF* 法人。

相反，如果您拥有以下可用数据，则可以通过从自己的数据中替换值来完成此场景：

- 您必须具有包含未结采购订单行的已确认采购订单。
- 必须贮存行中的物料。 它不得使用产品变体，也不得具有跟踪维度。
- 该物料必须与启用了仓库管理流程的存储维度组关联。
- 使用的仓库必须启用可供 WMS 使用，并且用于接收的库位必须受牌照控制。

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>创建使用仓库管理的物料到达日记帐标题

以下场景显示了如何创建使用仓库管理的物料到达日记帐标题：

1. 确保您的系统包含满足上一部分中概述的要求的已确认采购订单。 此场景使用公司 *USMF*、供应商帐户 *1001*、仓库 *51* 的采购订单，其中包含物料编号 *M9200* 的 *10 PL*（10 个托盘）的订单行。
1. 记下将使用的采购订单编号。
1. 转到 **库存管理 \> 日记帐条目 \> 物料到达 \> 物料到达**。
1. 在操作窗格上选择 **新建**。
1. **创建仓库管理日记帐** 对话框将打开。 在 **名称** 字段中选择日记帐名称。
    - 如果您使用 *USMF* 示例数据，选择 *WHS*。
    - 如果您使用自己的数据，则选择的日记帐必须将 **检查领料库位** 设置为 *否* 并将 **检验管理** 设置为 *否*。
1. 将 **引用** 设置为 *采购订单*。
1. 将 **帐户编号** 设置为 *1001*。
1. 将 **编号** 设置为您为此练习标识的采购订单的编号。

    ![物料到达日记帐。](../media/item-arrival-journal-header.png "物料到达日记帐")

1. 选择 **确定** 以创建日记帐标题。
1. 在 **日记帐行** 部分中，选择 **添加行** 并输入以下数据：
    - **物料编号** – 设置为 *M9200*。 将基于 10 个托盘（1000 个）的库存交易记录数据设置 **场地**、**仓库** 和 **数量**。
    - **库位** – 设置为 *001*。 此特定库位不跟踪牌照。

    ![物料到达日记帐行。](../media/item-arrival-journal-line.png "物料到达日记帐行")

    > [!NOTE]
    > **日期** 字段确定此现有数量的物料将记入库存的日期。  
    >
    > 如果可从提供的信息个别识别，系统将会自动填充 **批次 ID**。 否则将必须手动输入。 这是必填字段，用于将此登记链接到特定原始单据行。  

1. 在操作窗格上选择 **验证**。 这会检查准备好供过帐的日记帐。 如果验证失败，需要修复错误才能过帐日记帐。  
1. **检查日记帐** 对话框将打开。 选择 **确定**。
1. 查看消息栏。 应该有一条消息表示操作已完成。  
1. 在操作窗格上选择 **过帐**。
1. **过帐日记帐** 对话框将打开。 选择 **确定**。
1. 查看消息栏。 应该有消息表示操作完成。
1. 在操作窗格上选择 **功能 > 产品收货** 以更新订单行并过帐产品收货。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
