---
title: "高级银行对帐概览"
description: "高级银行对帐允许您在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中导入电子银行对帐单，并与银行交易记录自动对帐。  这篇文章将介绍对帐流程设置。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 89f895a9de9fa9863459ae6261b8c429d559d482
ms.contentlocale: zh-cn
ms.lasthandoff: 06/13/2017

---

# <a name="advanced-bank-reconciliation-overview"></a>高级银行对帐概览

[!include[banner](../includes/banner.md)]


高级银行对帐允许您在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中导入电子银行对帐单，并与银行交易记录自动对帐。  这篇文章将介绍对帐流程设置。  

在使用高级银行对帐功能之前有很多必须设置的部分。 有关设置银行对帐单导入的详细信息，请参阅[设置银行对帐单导入流程](set-up-advanced-bank-reconciliation-import-process.md)。  下面详细描述了对帐流程设置的要求。

## <a name="transaction-codes"></a>交易记录代码
可将交易记录代码用作银行对帐匹配规则的一部分。  交易记录代码有助于仅匹配 Finance and Operations 与您的银行对帐单之间类型相同的交易记录。  要执行此类型的匹配，必须首先从 Finance and Operations 定义用于银行交易记录的交易记录类型，然后将这些类型映射到您的银行使用的对帐单交易记录代码。  Finance and Operations 银行交易记录的交易记录类型在**银行交易记录类型**页面中定义。  这也是定义要用于与该交易记录类型关联的过帐的主科目。 

定义 Finance and Operations 银行交易记录代码之后，请将其映射到您的电子银行对帐单中使用的交易记录代码。  此映射流程使用**交易记录代码映射**页面执行。  将为各银行帐户分别完成交易记录代码映射。

## <a name="matching-rules-and-matching-rule-sets"></a>匹配规则和匹配规则集
匹配规则允许您定义 Finance and Operations 银行交易记录和银行对帐单交易记录之间的自动对帐条件。  匹配规则的设置在**对帐匹配规则**页面执行。  有关详细信息，请参阅[设置银行对帐匹配规则](set-up-bank-reconciliation-matching-rules.md)。 

匹配规则集用于定义在银行对帐流程中按顺序运行的一组匹配规则。  匹配规则集在**对帐匹配规则集**页面配置。

## <a name="cash-and-bank-management-parameters"></a>现金和银行管理参数
在**现金和银行管理参数**页有很多特定于高级银行对帐流程的参数。  **显示借方/贷方对帐单行金额**更改**银行对帐单**页上金额的视图。  如果选择此选项，将在单独的借方和贷方列显示银行对帐单交易记录金额。  如果未选中，银行对帐单交易记录金额将显示在具有适当符号的单个金额列。 

在参数页上设置的验证选项覆盖匹配规则中设置的选择。  例如，您不能手动或自动匹配在参数页上设置的日期差异以外的单据。  而且，如果选择**验证交易记录类型映射**，必须在 Finance and Operations 银行交易记录和银行对帐单交易记录之间映射交易记录类型，以手动或自动匹配交易记录。 

您还必须配置在**现金和银行管理参数**页配置必要的编号规则。  在**编号规则**选项卡上，为下载 **ID、报表 ID、对帐 ID 和银行对帐**引用设置编号规则。

## <a name="bank-account-reconciliation-options"></a>银行帐户对帐选项
您必须首先为银行帐户启用高级银行对帐。  启用高级银行对帐功后，**银行帐户**页将有很多其他选项可用。 

**作为电子支付的确认使用银行对帐单**功能将银行对帐功能与电子付款状态集成。  启用后，银行单据将为设置为**已发送**的电子付款状态自动创建。  此外，电子付款的状态将在匹配、对帐和过帐付款后，从**已发送**更新为**已接收**。 

**对帐单中的银行帐户名称**字段是用于电子银行对帐单的银行帐户的名称。   当确定为银行帐户从可能包含多个银行帐户信息的对帐单导入哪些交易记录时使用此名称。 

选项**在导入后对帐**将自动验证银行对帐单、创建新的银行对帐和工作表中，并运行默认匹配规则集。  此功能自动将流程运行到必须手动匹配的阶段。  导入时，将默认使用银行帐户上的设置。




