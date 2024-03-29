---
title: Finance Insights 主页
description: Finance insights 提供可配置和可扩展的模型，以帮助您准确，智能地预测公司的现金流，预测何时收到未清应收款的付款，并生成可以加快预算编制过程的预算提案。 所有这些功能都基于智能机器学习模型。
author: ShivamPandey-msft
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2f04ef1a0de815596f629fede25a247c58e026f4
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643869"
---
# <a name="finance-insights-home-page"></a>Finance Insights 主页

[!include [banner](../includes/banner.md)]

Finance insights 提供可配置和可扩展的解决方案，以帮助您智能地预测公司的现金流，预测何时可能会收到未清应收款的付款，并生成可以帮助加快预算编制过程的预算提案。 这些功能使用智能机器学习模板，以使用您提供的数据（包括来自第三方的数据，例如来自某个局的消费者报告信息）来构建模型。 这些智能功能为制定决策提供信息，并帮助您采取行动以有效应对当前和预期的业务挑战。 您对 Finance Insights 所使用或输出的任何数据负责。

> [!NOTE]
> Finance Insights 可用于美利坚合众国、加拿大、英国、欧洲、亚太、日本、澳大利亚和新西兰的部署。 Microsoft 将逐渐增加对更多地区的支持。

## <a name="prerequisites"></a>先决条件

本节列出了使用 Finance insights 的要求。 将尽可能提供指向其他信息源的链接。

### <a name="system-requirements"></a>系统要求

需要第 2 层环境（多盒）才能预览 Finance Insights。 有关环境的背景信息，请参阅[环境计划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。

### <a name="version-requirements"></a>版本要求

本文适用于 Microsoft Dynamics 365 Finance 版本 10.0.21 及更高版本。

### <a name="license-requirements"></a>许可要求证

Finance Insights 使用 AI Builder 积分创建财务预测。 完成此任务需要的所有许可证均包含在租户许可证中。 每个 Dynamics 365 Finance 租户每月获得 20,000 AI Builder 积分。 如果业务需要额外的积分，可以直接从 AI Builder 购买。

### <a name="historical-data-requirements"></a>历史数据要求

需要至少一年的客户发票价值才能正确训练用于客户付款预测功能的机器学习模型。 现金流预测建议使用三年历史数据。 对于智能预算提案，建议使用三年的历史预算和/或实际数据。

## <a name="configure-finance-insights"></a>配置 Finance Insights

您必须先完成配置步骤，然后才能使用 Finance insights。 有关如何配置 Finance insights 的详细信息，请参阅 [Finance insights 的配置](configure-for-fin-insites.md)。

## <a name="create-a-data-integrator-project"></a>创建数据集成器项目

您需要创建一个数据集成器项目，以便机器学习模型生成的数据可以传输到 Dynamics 365 Finance 中。 有关创建该项目的步骤，请参阅[创建数据集成器项目](create-data-integrate-project.md)。

## <a name="enable-finance-insights-capabilities"></a>启用 Finance insights 功能

完成配置步骤并设置演示数据后，必须打开并设置计划使用的每种功能：客户付款预测、现金流预测和预算提案。

### <a name="enable-customer-payment-predictions"></a>启用客户付款预测
如果您使用演示数据测试客户付款预测，则可能必须导入更多演示数据才能成功创建 AI 模型。 

要启用客户付款预测，您必须完成一组步骤来构建一个机器学习模型，该模型使用组织的数据生成有关客户何时可能会支付未清发票和何时可能要支付特定发票的预测。 有关详细信息和要完成的具体步骤，请参阅[启用客户付款预测](enable-cust-paymnt-prediction.md)。 

### <a name="enable-cash-flow-forecasting"></a>启用现金流预测
若要启用现金流预测，您必须完成一组步骤来生成机器学习模型，该模型使用组织的数据生成现金流预测。 有关详细信息和要完成的具体步骤，请参阅[启用现金流预测](enable-cash-flow-forecasting.md)。

### <a name="enable-budget-proposals"></a>启用预算提案

预算提案功能使用机器学习模型以及组织的历史数据生成预算提案。 生成的提案可以帮助您开始执行比手动过程更有效的预算过程。 有关启用此功能的具体步骤，请参阅[启用预算提案](enable-budget-proposal.md)。 

## <a name="using-finance-insights-features"></a>使用 Finance insights 功能

### <a name="using-customer-payment-predictions"></a>使用客户付款预测

- 要了解客户付款预测如何提供主动开始收款活动所需的信息，请参阅[使用客户付款预测](use-customer-payment-predictions.md)。
- 有关可帮助您在开始使用该功能后评估预测模型的有效性的信息，请参阅[评估初始客户付款预测模型](evaluate-payment-prediction.md)。
- 有关可帮助您调整用于构建预测并由此提高其有效性的数据的信息，请参阅[改进预测模型](improve-model.md)。
- 要了解有关 AI 预测模型结果的详细信息，请参阅[机器学习模型的结果](confusion-matrix.md)。

### <a name="using-cash-flow-forecasts"></a>使用现金流预测

现金流预测功能可以帮助您更准确地估计现金头寸。 智能现金流预测功能基于 Dynamics 365 Finance 中的现有现金流预测功能。 要查看现有功能，请参阅[现金流预测](../cash-bank-management/cash-flow-forecasting.md)。

- 要了解现金流预测中的新功能，请参阅[现金流预测](cash-flow-forecast-intro.md)。
- 有关在此处导入要包括在现金流预测中的外部数据的信息，请参阅[在现金流预测中使用外部数据](external-data-in-cash-flow.md)。 
- 有关如何使用 AI 模型预测近期现金流的信息，请参阅[现金头寸](cash-position.md)。
- 有关将现金流头寸和现金流预测另存为快照以及将快照与实际值进行比较的信息，请参阅[快照概述](payment-snapshots.md)。

### <a name="using-budget-proposal"></a>使用预算提案

有关加快预算创建速度的信息，请参阅[预算提案](budget-proposals.md)。 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
