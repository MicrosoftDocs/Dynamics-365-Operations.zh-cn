---
title: 项目预测和预算
description: Microsoft Dynamics 365 Finance 提供项目预测和项目预算来管理和控制您的项目。
author: KimANelson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85a5577968024bf42449c50d72a11414f9207eec
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185581"
---
# <a name="project-forecasts-and-budgets"></a>项目预测和预算

[!include [banner](../includes/banner.md)]

可通过两种方式管理和控制您的项目:项目预测和项目预算。 

如果您的组织有操作视角，并且它侧重于产生自特定交易处理的收入和成本，请使用项目预测。 如果您的组织注重详细的财务金额，请使用项目预算。 

项目预测和项目预算使用预测模型包含项目的交易记录金额。 

每个方法都有自己的优点。 您应该在为您的组织选择方法之前考虑以下各点。

|                           |                                          |                                                    |
|---------------------------|------------------------------------------|----------------------------------------------------|
|                           | **项目预测**                  | **项目预算**                              |
| **期间分配**     | 您不能在会计期间内明确分配交易记录。 预测和预测的控制基于项目的使用年限。 由于预测基于特定日期，因此您必须从该日期推断期间。 | 您可以在整个项目或会计期间分配交易记录。 如果您在期间分配，则可以将不使用的金额结转到下一会计期间。 |
| **查看交易记录**  | 您可以在预测窗体中查看交易记录，在其中您将看到整个公司和所有项目的预测，无论层次结构如何。 若要在特定项目，必须筛选数据。                                       | 您可以查看单个项目层次结构的预算交易记录。 因此，您可以查看父级项目及其子级项目的交易记录详细信息。                 |
| **交易记录变量** | 当您输入预测交易记录时，您可以使用为实际交易记录而存在的各个属性。 这允许在预测的更高的详细信息。 例如，您可以输入数量的详细信息，工人、物料或记录属性。         | 当您输入预算详细信息时，您只能使用金额、类别和活动。                    |
| **安全性**              | 预测基于您在预测窗体中输入的交易记录，并且不涉及流程控制机制。 对预测窗体具有权限的所有工作人员可以修改信息，而无需审核。                                        | 预算使用工作流系统，该系统启用更改管理并让您能够保留版本的历史记录。         |
| **输入类型**           | 预测交易记录基于单位的数量和成本和销售单位价格。  | 预算详细信息基于在成本和收入之间拆分的金额。                                          |
| **预测模型**       | 因为每个预测必须与一个模型关联，您可以创建多个预测模型，以及设置子模型。           | 项目预算的限制为预算使用的预测模型。 数量预测模型可以帮助提高中的信息的一致性。                           |
| **费用超限**         | 您可以只允许或禁止将生成费用超限的交易记录条目。   | 项目预算为用户提供附加控件选项。 您可以允许警告和超限。                    |
| **控制**               | 通过使用缩减预测，预测进行控制。 实际金额基于预测交易记录余额减去的天数，没有任何审计线索。 这可能有助于更确定跟踪实际交易记录将出现的位置。                   | 在项目预算管理，实际金额。在剩余预算金额中减去的天数。 这样更广的审计线索。                                   |

## <a name="project-forecasts"></a>项目预测
当您使用项目预测时，您可以为每个交易记录类型在预测窗体中输入预测交易记录。 对实际交易记录可用的每个特性都能用于预测交易记录 — 例如，行利润，行特性，工作人员或描述。 您也可以计划发生了成本之后你将开发票给客户的时间长短。 

项目预测交易记录是基于单位和金额的。 

您必须将每个项目预测与某个预测模型相关联。 当您输入预测交易记录时， 将自动建议一个预测模型。 预测模型充当预测交易记录的容器。 

您可以将预测模型指定为模型的子模型。 这能让您按地区、时段或部门预测。 您可以复制某个模型中的预测交易记录来创建新模型，并将这些交易记录转移到总帐。 由于在预测和模型之间具有一对一的关系，每个预测模型为项目构成了一个单独的预算。 

预测模型可以把预测缩减用作项目的控制结构。 在预测缩减中，实际交易记录减少预测交易记录余额。 但是，因此预测缩减应用于该层次结构中的最高的项目，所以它提供了预测中更改的一个受限查看。 例如，如果工作人员与下级项目相关联，那么该工作人员的实际交易记录已过帐到父项目。 这可能会使跟踪更改很困难，因为您不能很容易地确定子项目在哪一个交易记录中导致预测金额。 因此，最好为要使用的预测缩减创建预测模型的副本。 然后，您可以使用报告来查看最初预测的内容。 

您可以修订、复制、删除或转移项目预测到总帐预算。 但是，没有流程控制。 对预测窗体有权限的任何工作人员可以进行修订而不复查。

-   **修订** – 您可以在与创建原始条目相同的窗体中修订预测交易记录。
-   **复制或删除** – 当您复制预测交易记录时，您将一个预测模型的交易记录行复制到了另外一个预测模型。 当您删除预测时，您把预测交易记录从预测模型中删除。 为了限制要复制或删除的预测交易记录，请选择特定交易记录类型和日期。 这能让您仅复制或删除某个预测的特定部分。
-   **转移** – 当您将项目预测转移到总帐预算中时，您将预测模型的预测交易记录转移到了总帐预算。 您可以覆盖您将转移项目预测所到的总帐预算中的任何先前已转移的交易记录。

## <a name="project-budgets"></a>项目预算
项目预算是比项目预测更简单的方法，尽管项目预算与预测模型相集成。 它将单个条目窗体用于原始预算明细和修订，而且它只允许基于金额、类别或活动的计划。 

在项目预算中，必须将所有原始预算和修订发送到项目工作流以供审核。 工作流提供给您对流程的增强了的控制，并创建了一个更改历史记录。 

项目预算类似于总帐预算，但是项目预算更快速、更容易设置。 总账预算中的编号规则或币种等许多选项不必为项目单独设置。

项目预算自动与两个预测模型相关联，其中一个预测模型是针对原始预算，而另一个预测模型针对剩余预算。 因此，基于预测模型的报告可使用预算数据。 当承诺了一个项目预算时，系统将基于用于报告和控制目的的相关模型创建预测交易记录。

## <a name="forecast-models"></a>预测模型
预测模型具有单层层次结构。 这意味着，一个项目预测必须与一个预测模型相关联。

如果您使用项目预测，您可以标识设计为子模型。 然后您可以按部门、时段或地区创建预测。 例如，可以创建一年的预测模型，然后为由地区标题提交的东北部、东南部、西北部和西南部区域预测创建子模型。 通过在可用报表中选择不同的选项，可以按总预测或由子模型查看信息。


