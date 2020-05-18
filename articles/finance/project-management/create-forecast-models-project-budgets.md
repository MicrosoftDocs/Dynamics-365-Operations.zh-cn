---
title: 创建项目预算的预测模型
description: 本主题描述如何为剩余预算创建预测模型。
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321771"
---
# <a name="create-forecast-models-for-project-budgets"></a>创建项目预算的预测模型 

[!include [banner](../includes/banner.md)]

本主题描述如何为剩余预算创建预测模型。 受预算控制的项目使用两种类型的预算：原始预算和剩余预算。 创建项目预算时，必须指定在**预测模型**页面中创建的原始和剩余预算预测模型。 当您提交项目预算时，创建基于指定模型的项目预算。

> [!NOTE]
> 用于预算控制的预测模型不能具有子模型，也不能用作子模型。

1. 选择**项目管理与会计** > **设置** > **预测**  > **预测模型**。
2. 选择**新建**以创建新的预测模型，然后输入新模型的模型 ID 号和名称。 
3. 将**已停止**选项设置为**是**，以防止对预测模型的预测行进行任何更改。 
4. 如果与模型关联的预测行应在总账中生成现金流预测，请将**包括在现金流预测中**设置为**是**。 
5. 要将项目日期用作发票日期，请将**预测发票日期**设置为**是**。 
6. 在**预算类型**字段中，选择以下模型类型之一：

   - **原始预算**：使用在创建和批准初始预算时承诺的原始预算金额。
   - **剩余预算**：在项目生命周期内使用剩余预算金额。 此预算模型的余额减去实际交易记录，它根据预算版本增加或减少。
   - **结转**：使用项目的结转预算金额。 结转是一个可选的流程，运行结转以将未使用的预算金额从一个会计年度转移到另一个会计年度。

7. 根据需要设置以下选项：

   - 启用**预测发票日期**以使用项目日期作为发票日期。
   - 启用**根据 WIP 进行预测**以基于在建项目(WIP) 进行预测，然后选择 WIP 的类型。 
   - 您可以将默认的**预算类型**保留为**无**，或输入新的类型。 更改记录后，无法更改预算类型。     
    > [!NOTE]
    > 如果您更改默认预算类型，则所有其他选项将无法更新，并且您无法重复使用此预测模型。 
   


 

