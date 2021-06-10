---
title: Finance insights 主页（预览）
description: Finance insights 提供可配置和可扩展的模型，以帮助您准确，智能地预测公司的现金流，预测何时收到未清应收款的付款，并生成可以加快预算编制过程的预算提案。 所有这些功能都基于智能机器学习模型。
author: ShivamPandey-msft
ms.date: 07/20/2020
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 3a78a162469790d797344ce9311c55bfcecd19f4
ms.sourcegitcommit: 273903b7b73ac726d447c50f7086e6d8b0f0f74e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/21/2021
ms.locfileid: "6086981"
---
# <a name="finance-insights-home-page-preview"></a>Finance insights 主页（预览）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance insights 提供可配置和可扩展的模型，以帮助您准确，智能地预测公司的现金流，预测何时收到未清应收款的付款，并生成可以加快预算编制过程的预算提案。 所有这些功能都基于智能机器学习模型。 将这些新功能与供应商付款和收款中的自动化相结合时，它们将提供丰富而智能的财务系统，以推动决策制定，并帮助您采取行动以有效应对当前和预期的业务挑战。

Finance insights 预览版可用于美国、欧洲和英国的试用部署。 Microsoft 将逐渐增加对更多地区的支持。

可以并且应该仅在第 2 层沙盒环境中启用预览版功能。 在沙盒环境中创建的设置和人工智能 (AI) 模型不能迁移到生产环境。 有关详细信息，请参阅 [Microsoft Dynamics 365 Previews 补充使用条款](/dynamics365/legal/supp-dynamics365-preview#:~:text=Supplemental%20Terms%20of%20Use%20for%20Microsoft%20Dynamics%20365,%28governing%20your%20use%20of%20Microsoft%20Dynamics%20365%20Online%29.)。

## <a name="prerequisites"></a>先决条件

本节列出了使用 Finance insights 的要求。 将尽可能提供指向其他信息源的链接。

### <a name="legal-requirements"></a>法律要求

要申请预览项目，请填写 [Finance insights Preview for Dynamics 365 Finance 协议](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u)。

### <a name="system-requirements"></a>系统要求

需要第 2 层沙盒环境（多盒）才能预览 Finance insights。 有关环境的背景信息，请参阅[环境计划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。

### <a name="version-requirements"></a>版本要求

本文适用于 Finance and Operations 应用版本 10.0.11（平台更新 35）及更高版本。

### <a name="historical-data-requirements"></a>历史数据要求

需要至少一年的客户发票价值才能正确训练用于客户付款预测功能的机器学习模型。

示例数据可用于具有 Contoso 演示数据集的演示系统。

### <a name="role-and-permission-requirements"></a>角色和权限要求

将对 Microsoft Dynamics 365 Finance、Microsoft Dynamics Lifecycle Services (LCS)、Power Apps 和 Azure 进行更改。 这些环境中需要正确的权限。 下面是将进行的更改的一些示例：

- 将在 Microsoft Power Platform 中创建一个新环境。
- 将在 Azure 中创建存储帐户、密钥保管库和应用程序。
- Active Directory 租户管理员将必须授权 AI Builder 应用程序访问数据湖。
- 该功能将在 Dynamics 365 中打开。

熟悉在 Azure、Microsoft Dataverse 和 LCS 中创建和管理资源的过程有助于完成此过程。

## <a name="configure-finance-insights"></a>配置 Finance insights

您必须先完成一些配置步骤，然后才能使用 Finance insights。 有关如何配置 Finance insights 的详细信息，请参阅 [Finance insights 的配置](configure-for-fin-insites.md)。

## <a name="create-a-data-integrator-project"></a>创建数据集成器项目

您需要创建一个数据集成器项目，以便机器学习模型生成的数据可以传输到 Dynamics 365 Finance 中。 有关创建该项目的步骤，请参阅[创建数据集成器项目](create-data-integrate-project.md)。

## <a name="enable-finance-insights-capabilities"></a>启用 Finance insights 功能

完成配置步骤并设置演示数据后，必须打开并设置计划使用的每种功能：客户付款预测、现金流预测和预算提案。

### <a name="enable-customer-payment-predictions"></a>启用客户付款预测
如果您使用演示数据测试客户付款预测，则可能必须导入更多演示数据才能成功创建 AI 模型。 

要启用客户付款预测，您必须完成一组步骤来构建一个机器学习模型，该模型使用组织的数据生成有关客户何时可能会支付未清发票和何时可能要支付特定发票的预测。 有关详细信息和要完成的具体步骤，请参阅[启用客户付款预测](enable-cust-paymnt-prediction.md)。 

### <a name="enable-cash-flow-forecasting"></a>启用现金流预测
要启用现金流预测，您必须完成一组步骤来构建机器学习模型，该模型使用组织的数据生成现金流预测。 有关详细信息和要完成的具体步骤，请参阅[启用现金流预测](enable-cash-flow-forecasting.md) 

### <a name="set-up-and-use-cash-flow-forecasting"></a>设置和使用现金流预测
有关如何设置和使用现金流预测的详细信息，请参阅[启用现金流预测](enable-cash-flow-forecasting.md)。 有关如何使用此功能的详细信息，请参阅[现金流预测](cash-flow-forecast-intro.md)。

### <a name="enable-budget-proposals"></a>启用预算提案

预算提案功能使用机器学习模型以及组织的历史数据生成预算提案。 生成的提案可以帮助您开始执行比手动过程更有效的预算过程。 有关启用此功能的具体步骤，请参阅[启用预算提案](enable-budget-proposal.md)。 

## <a name="using-finance-insights-features"></a>使用 Finance insights 功能

### <a name="using-customer-payment-predictions"></a>使用客户付款预测

智能现金流预测功能基于 Dynamics 365 Finance 中的现有现金流预测功能。 要查看现有功能，请参阅[现金流预测](../cash-bank-management/cash-flow-forecasting.md)。

- 要了解客户付款预测如何提供主动收款活动所需信息，请参阅[使用客户付款预测](use-customer-payment-predictions.md)。
- 有关可帮助您在开始使用该功能后评估预测模型的有效性的信息，请参阅[评估初始客户付款预测模型](evaluate-payment-prediction.md)。
- 有关可帮助您调整用于构建预测并由此提高其有效性的数据的信息，请参阅[改进预测模型](improve-model.md)。

要了解有关 AI 预测模型结果的详细信息，请参阅[机器学习模型的结果](confusion-matrix.md)。

### <a name="using-cash-flow-forecasts"></a>使用现金流预测

现金流预测功能可以帮助您更准确地估计现金头寸。 

- 要了解现金流预测中的新功能，请参阅[现金流预测](cash-flow-forecast-intro.md)。
- 有关在此处导入要包括在现金流预测中的外部数据的信息，请参阅[在现金流预测中使用外部数据](external-data-in-cash-flow.md)。 
- 有关如何使用 AI 模型预测长期现金流的信息，请参阅[现金流预测概述](cash-position.md)。
- 有关将现金流头寸和现金流预测另存为快照以及将快照与实际值进行比较的信息，请参阅[快照概述](payment-snapshots.md)。

### <a name="using-budget-proposal"></a>使用预算提案

有关加快预算创建速度的信息，请参阅[预算提案](budget-proposals.md)。 

预算提案的演示数据：

## <a name="feedback-and-support"></a>反馈和支持

如果对提供反馈感兴趣或需要支持，请向 [客户付款见解（预览）](mailto:fiap@microsoft.com)发送电子邮件。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
