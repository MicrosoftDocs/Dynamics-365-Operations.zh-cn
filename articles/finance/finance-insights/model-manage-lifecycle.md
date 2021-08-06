---
title: 模型管理生命周期（预览）
description: 本主题介绍维护组织的机器学习模型以优化它们生成的预测的方法。
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 3daec03b7ba349d8f72863317e2d601a83417d58
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638384"
---
# <a name="model-management-lifecycle-preview"></a>模型管理生命周期（预览）

[!include [banner](../includes/banner.md)]

本主题介绍维护组织的机器学习模型以优化它们生成的预测的方法。

我们建议您在沙盒环境中训练 AI 模型，然后使用托管解决方案将其部署到生产环境。 此方法有助于确保为管理模型生命周期采取正确的控制措施。

由于 AI 模型基于可用的发票和客户数据，因此沙盒环境具有生产数据的最新副本非常重要。 您可以按照[使用客户付款预测](use-customer-payment-predictions.md)中的步骤开始训练您的模型。 重新训练模型后，按[评估初始客户付款预测模型](evaluate-payment-prediction.md)中所述评估结果。 使用[改进预测模型](improve-model.md)中的信息试验有助于改进模型的功能和筛选器组合。

当您对训练结果感到满意时，请按照[分配您的 AI 模型](https://docs.microsoft.com/ai-builder/distribute-model)中的步骤将模型转换到您的生产环境。
