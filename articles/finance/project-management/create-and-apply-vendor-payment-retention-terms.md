---
title: 创建和应用供应商付款保留条款
description: 本主题提供有关如何设置和维护供应商付款保留条款的信息。
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410197"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>创建和应用供应商付款保留条款

[!include [banner](../includes/banner.md)] 

当您的组织希望保留对供应商的部分付款时，为项目设置供应商付款保留条款非常有用。 例如，当您希望将给供应商的付款保留到交付的产品符合您期望时。 您可以在协商供应商合同时指定供应商付款保留条款。

## <a name="create-vendor-payment-retention-terms"></a>创建供应商付款保留条款

您可以输入要保留的供应商付款的百分比和发放以前保留的金额的百分比。 金额将供应商发票自动保留，直到到达完成的合同中所指定的状态。 在您设置保留条款后，您可以将其应用于该供应商的任何项目。

使用以下步骤设置和维护供应商付款的保留条款。 

1. 转到**项目管理与核算** > **保留** > **供应商付款保留条款**。
2. 选择**新**添加新的供应商保留条款。 新条件的**规则 ID** 值自动输入。 
3. 在**描述**字段中输入简短描述，然后在**条款**快速选项卡上，选择**添加行**为以下项输入条款值：

   - **已交货单位的百分比**：输入条款完成的百分比。 金额将自动保留在供应商发票上，直到完成项目阶段与指定的百分比相等。 例如，如果您输入 50.00，金额将保留，直到完成 50% 的项目。
   - **要保留的百分比**：输入要保留的供应商发票金额的百分比。 例如，如果您输入 10.00，那么供应商发票上的金额将保留 10%，直到项目达到您在**已交货单位的百分比**字段中设置的完成百分比。
   - **要发放的百分比**：选择**添加行**以输入要为选定的项目完成级别发放的任何先前保留金额的百分比。

> [!NOTE]
> 如果您具有多个项目完成的不同级别里程碑，输入每个留成规则的单独的供应商留成条款行。 每一行可以指定不同的保留百分比和项目完成的每个指定级别的不同发放百分比。

为供应商创建供应商保留条款后，可以将其应用于项目。

## <a name="apply-vendor-retention-terms-to-a-project"></a>将供应商保留条款应用于项目

1. 转到**项目管理与核算** > **项目** > **所有项目**，从项目列表页面打开一个项目。
2. 在**供应商协议**快速选项卡上，请选择**添加行**。
3. 在**帐户代码字段**中，选择以下选项之一： 

   - **表**：供应商保留条款应用于单个供应商。
   - **组**：供应商留成条款在供应商组中应用于所有供应商。
   - **所有**：供应商留成条款应用于所有供应商。

4. 在**供应商/供应商组字段**中，选择供应商保留条款应用的供应商或供应商组。 如果您在上一步中已选择**所有**，则此字段不可用。
5. 在**供应商保留条款**字段中，选择在上一个过程中创建的供应商保留条款。
6. 如果项目还有为供应商设置的即收即付 (PWP) 条款，则在 **PWP 阈值百分比**字段中输入项目的阈值百分比。

供应商留成条款也将在您为供应商创建的采购订单中显示。
