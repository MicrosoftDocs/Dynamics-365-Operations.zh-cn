---
title: 采购协议
description: 文本提供有关采购协议的信息。 采购协议是提交到某一组织，随时间推移通过使用多个采购订单购买指定的数量或金额的合同。 以此承诺作为交换，买方接收特价和折扣。
author: GalynaFedorova
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal, PurchLine, AgreementLines
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 188a71ec660787b0b942a3d3bf4967b747c4469f
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335876"
---
# <a name="purchase-agreements"></a>采购协议

[!include [banner](../includes/banner.md)]

文本提供有关采购协议的信息。 采购协议是提交到某一组织，随时间推移通过使用多个采购订单购买指定的数量或金额的合同。 以此承诺作为交换，买方接收特价和折扣。 

采购协议可应用于采购类别中的产品的特定数量、产品的特定币种金额或该产品的特定币种金额。 采购协议的价格和折扣覆盖存在的所有贸易协议中指定的价格和折扣。  

在 **采购协议** 页上，您可以创建、应用和跟进您的组织及供应商之间存在的采购协议。 例如，在创建采购协议后，您可以直接从中进行订购。 每个采购协议都具有由创建采购协议的人员定义的有效期间。 采购的交货日期必须处于此有效期间的生效日期。  

在您创建某一采购协议后，必须激活它，然后它才会生效。 若要激活采购协议，请将 **将协议标记为有效** 选项设置为 **是**。 

为防止使用和确认您的购买协议，请将协议状态标记为 **关闭**。 进行此更改后，您仍然可以随时将状态更新为 **有效**。

## <a name="responsible-workers-on-purchase-agreements"></a>采购协议中的负责工作人员

您可以在采购协议分类中标识主要负责工作人员和次要负责工作人员。 这些值将由生成的采购协议继承。 您不需要在采购协议中添加负责工作人员，他们可以在采购协议上针对每个案例直接进行修改。 没有主要负责工作人员无法指定次要负责工作人员，但您不是必须指定次要负责工作人员。 您不能将同一个工作人员同时指定为主要负责工作人员和次要负责工作人员。

> [!IMPORTANT]
> 要使用负责方功能，必须在您的系统中打开它。 从 Supply Chain Management 版本 10.0.25 开始，此功能默认开启。 从 Supply Chain Management 版本 10.0.29 开始，此功能是强制性的，无法关闭。 如果您运行的版本早于 10.0.29，管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *采购协议负责方* 功能来打开或关闭此功能。

## <a name="commitment-types"></a>承诺类型
采购协议的每一行都是采购的承诺。 您可以使用来自多个采购订单行 (PO) 履行承诺。 有以下四种承诺类型：

-   **产品数量承诺** – 您购买产品的特定数量。
-   **产品价值承诺** – 您购买产品的特定币种金额。
-   **产品类别价值承诺** – 您在采购类别中购买某一特定币种金额。 可为目录物料或非目录物料的金额。
-   **价值承诺** – 您在任何采购类别中购买任何产品（一个或多个）的特定币种金额。

## <a name="pricing-terms-for-purchase-agreements"></a>采购协议的价格条款
价格条款可以根据承诺类型的不同而不同。 采购协议中的价格条款覆盖设置为贸易协议的任何其他价格条款。 下表描述受每个承诺类型影响的价格相关的字段。 包含 **是** 的字段可在订单行更新。

| 承诺类型                   | 单位价格 | 计价单位 | 折扣率 | 现金折扣金额 |
|-----------------------------------|------------|------------|------------------|----------------------|
| 产品数量承诺       | 是        | 是        | 是              | 是                  |
| 产品价值承诺          |            |            | 是              |                      |
| 产品类别价值承诺 |            |            | 是              |                      |
| 价值承诺                  |            |            | 是              |                      |

## <a name="policies-for-purchase-agreements"></a>采购协议策略
以下策略影响采购协议承诺和相应采购订单行工作之间的链接的方法：

-   **强制为最大** – 所有订单行的总数量或金额不能超过在相关的承诺中指定的数量或金额。
-   **价格和折扣是固定的** – 订单行上的价格和相关承诺上的价格必须相同。 如果更改订单行上价格，违反该承诺的链接。 如果违反了该链接，该订单行不有助于承诺的履行。
-   **最小发放金额和最大发放金额** – 如果指定了金额，则如果更改导致订单行与相关承诺不同的订单行，您会收到一条消息。

## <a name="fulfillment-calculations-for-purchase-agreements"></a>采购协议的履行计算
履行数量和金额显示在 **采购协议** 页的 **行明细** 快速选项卡上的 **履行** 选项卡上。  

**履行** 区域显示要求履行承诺的剩余金额或数量。  

**协议** 区域显示销售协议行有效的总数量或总金额。  

您可以通过选择采购订单行和发票行上或采购协议的标题上的 **相关信息** 操作，来访问对履行计算有贡献的采购订单行和发票行。

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>采购协议的确认和版本历史记录
在确认某一采购协议时，将采购协议的当前版本存储在历史记录表中。 如果您更改该采购协议，您可以在历史记录中再次确认，以存储采购协议的其他版本。 如果未确认某一采购协议，您还可以将其用于创建采购订单。 但是，不存储采购协议的历史记录信息。 您可以预览或打印协议的所有版本。 然后可以与您的供应商共享该修订供审核。

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>将采购协议应用于订购过程
在创建采购订单时，可以对它应用采购协议。 协议条款中的信息，例如付款期限、交货期限和交货地址，随后会复制到采购订单的标题中。 如果采购订单包含协议所涉及的一个或多个产品或类别行，则采购协议中的价格和折扣用于这些行。 订单行上的金额或数量对履行采购协议中的承诺有贡献。 同一个采购订单可以包括不与采购协议和具有采购协议承诺的行的两行。  

只有当您创建采购订单时，才可以选择采购协议。 在已创建采购订单后，您不能选择采购协议。  
在某些情况下间接创建采购订单，您可以控制 Supply Chain Management 是否自动搜索适用的采购协议。 例如，在您自动确定计划的采购订单或基于销售订单创建的采购订单时，您可以执行这些操作。

## <a name="matching-policy-on-purchase-agreements"></a>采购协议的匹配政策
您可以在采购协议的标头上定义行匹配政策。 当 **应付帐款参数** 页面上的 **允许匹配政策覆盖** 字段（在 **价格和数量匹配** 快速选项卡上）设置为 **高于公司政策** 时，此行匹配政策将遵守应付帐款参数行匹配政策。 引用采购协议的文档将使用在采购协议标头上定义的行匹配政策，除非在相应的物料、物料和供应商或类别采购策略上另有定义。

## <a name="purchase-agreements-and-intercompany-trade"></a>采购协议和内部公司交易
内部公司贸易关系可以在不同的法人中的供应商帐户和客户帐户之间创建。 在为其中一个当事方创建销售订单或采购订单时，创建内部公司订单链。 在订单链中，在相应法人中创建销售订单和采购订单。  

您可以为内部公司贸易当事方之一创建采购协议或销售协议。 然后，您可以为其他法人中的其他内部公司贸易当事方生成相应的销售协议或采购协议。  

如果您一个法人中创建使用内部公司采购协议的内部公司采购订单，则其他法人中的相应的内部公司采购订单使用相应的内部公司销售协议。 同步销售协议承诺的履行和采购协议的履行，就如同同步内部公司销售订单和内部公司采购订单。

## <a name="financial-dimensions-on-purchase-agreements"></a>采购协议财务维度
您可以将财务维度复制到采购协议的文档抬头或单独的行。 如果您在协议标题中或在协议行上更改维度，则更改不影响任何已下达的订单，但会在所有新订单中得到反映。

## <a name="additional-resources"></a>其他资源

- [创建采购协议](tasks/create-purchase-agreement.md)
- [创建采购订单时应用采购协议](tasks/create-purchase-release-order-purchase-agreement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]