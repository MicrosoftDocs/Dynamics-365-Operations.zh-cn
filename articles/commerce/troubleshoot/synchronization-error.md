---
title: 异步订单同步问题
description: 本文介绍 Microsoft Dynamics 365 Commerce 中异步订单创建失败的常见原因，并提供故障排除步骤，帮助系统用户和合作伙伴了解问题所在。
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815748"
---
# <a name="asynchronous-order-synchronization-issues"></a>异步订单同步问题

[!include [banner](../../includes/banner.md)]

本文介绍 Microsoft Dynamics 365 Commerce 中异步订单创建失败的常见原因，并提供故障排除步骤，帮助系统用户和合作伙伴了解问题所在。

## <a name="symptom"></a>问题

从 Dynamics 365 Commerce 电子商务或销售点 (POS) 创建的异步订单不会反映在 Commerce headquarters 中。

## <a name="troubleshooting"></a>疑难解答

Headquarters 中的订单创建可能因不同原因而失败，具体取决于订单创建过程失败的阶段。 下面的故障排除步骤会找出可能的根本原因。

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>验证与异步订单相关的交易是否已到达 headquarters

对于电子商务订单，在 headquarters 中，转到 **Retail 和 Commerce \> 查询和报表 \> 在线商店交易**。 如果您有订单的确认编号，通过在 **渠道引用 ID** 字段中输入确认编号来筛选交易。 如果您没有确认编号，输入帐号来筛选交易。

对于 POS 订单，打开 **商店交易** 页面，按收据编号或客户帐号筛选记录。 如果未找到交易，运行 **P-0001** 渠道交易作业，将交易从渠道同步到 headquarters。 如果 **P-0001** 作业失败，为作业失败开启支持票证。 如果 **P-0001** 作业成功，但交易仍未出现在 headquarters 中，开启包含相关信息的支持票证。
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>如果交易在 headquarters 中存在但未与销售订单链接，请检查同步状态

如果交易在 headquarters 中存在，但尚未创建销售订单，打开 **在线商店交易** 页面，选择 **同步状态** 快速选项卡。 如果 **同步订单** 作业尝试同步此交易，**待定订单状态** 字段应显示 **成功** 或 **失败** 状态。 如果状态为 **成功**，销售订单字段必须在此交易中存在。 如果状态为 **失败**，您可以在 **同步状态** 快速选项卡上的 **订单错误详细信息** 字段中查看错误详细信息。 如果这些状态均未显示，则未尝试处理交易。 在这种情况下，您可以选择页面顶部的 **同步订单** 来运行同步作业。

确保 **同步订单** 作业计划为定期运行，以可以在 headquarters 中将异步交易创建为订单。

以下几节提供有关一些常见错误及其建议修复方法的信息。

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>“订单错误详细信息”字段显示以下错误消息：“已超出编号规则”

编号规则用于在 headquarters 中创建销售订单。 如果编号规则允许的所有编号都用完，系统会生成此错误消息。 用于创建销售订单的编号规则可在 **应收帐款参数 \> 编号规则 \> 销售订单** 中找到。 要修复此错误，修复现有的编号规则，或将其替换为新的编号规则。

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>“订单错误详细信息”字段显示以下错误消息：“必须有默认的付款服务才能处理信用卡交易”

要修复此错误，确认在 headquarters 中定义了默认付款。 如果未定义默认付款，您必须进行定义。 转到 **应收帐款 \> 付款设置 \> 付款服务**，确保有一个付款服务的 **新信用卡的默认处理程序** 选项设置为 **是**。
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>“订单错误详细信息”字段显示科目结构错误消息

科目结构错误消息的文本可能会有所不同，如以下示例所示。 但是，这些错误有一个与科目结构配置相关的共同的根本原因。

- “公司 usrt 中凭证 ARP-000959899 的日记帐批号 0009656328 凭证 ARP-000959899 1.00 的过帐结果将作为超额支付或支付不足过帐”
- “组合 618160 的日记帐批号 0009656328 凭证 ARP-000959899 凭证 ARP-000959901 科目结构的过帐结果对于分类帐公司共享主帐户无效”
- “公司帐户 usrt 报告的日记帐批号 0009656328 凭证 ARP-000959899 凭证 ARP-000959901 的过帐结果”
- “日记帐批号 0009656328 凭证 ARP-000959899 过帐的过帐结果已被取消”
    
要修复这些错误，请检查科目结构的准确性。 有关详细信息，请参阅[配置科目结构](/dynamics365/finance/general-ledger/configure-account-structures)。
    
错误修复后，选择失败的交易，然后选择页面顶部的 **同步订单** 运行同步作业。
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>可能需要修复交易数据的其他类型的错误

要修复可能需要修复交易数据的其他类型的错误，您可以使用“编辑和审计交易”功能。 有关详细信息，请参阅[编辑和审计交易](../edit-order-trans.md)。
