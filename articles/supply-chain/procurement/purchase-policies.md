---
title: 采购策略概览
description: 文本提供有关采购策略的信息。 采购策略是控制申请流程的规则的集合。 采购策略通过创建符合组织的战略采购需求的策略结构帮助采购管理员实现其采购战略。
author: GalynaFedorova
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage, PurchReqControlRule, RequisitionReplenishCatAccessPolicyRule, PurchReApprovalPolicyRule, RequisitionReplenishControlRule, PurchReqControlRFQRule
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11614"
- intro-internal
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56d8f11d1bb53ef580e33ea43c84369c9e7fc0cc
ms.sourcegitcommit: 0f33f7b7d34d4f9c31ae0faf06a7a5c04b0195a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2022
ms.locfileid: "9804892"
---
# <a name="purchasing-policies-overview"></a>采购策略概览

[!include [banner](../includes/banner.md)]

文本提供有关采购策略的信息。 采购策略是控制申请流程的规则的集合。 采购策略通过创建符合组织的战略采购需求的策略结构帮助采购管理员实现其采购战略。

采购策略包含一组策略规则。 当您定义策略规则时，您要首先选择一个规则类型。 然后，为该规则类型创建一个规则，方法为定义该规则的设置、开始日期和结束日期。  

例如，管理员创建策略，选择 **目录策略** 规则类型，然后向策略添加目录策略规则。 此目录策略规则指定了必须将 Adventure Catalog 用于内部采购。 采购策略与特定组织关联后，该组织的员工将在创建申请时看到 Adventure Catalog。

## <a name="assigning-policies-to-organizations"></a>向组织分配策略
策略必须在与组织关联后才可生效 采购策略与 **采购内部控制** 层次结构目的关联。 因此，采购策略仅适用于层次结构目的为 **采购内部控制** 的层次结构中的组织。 您还可从 CompanyInfo 表中的法人简单列表选择组织。 这些法人在策略框架中指定为“公司”。

## <a name="determining-which-rule-to-apply"></a>确定要应用的规则
根据您配置采购策略的方式，多个规则可能影响组织中的用户。 以下示例说明了可配置采购策略和指定在交易记录出现时如何应用策略的不同方法。

### <a name="example-1-simple-purchasing-policy-configuration"></a>示例 1：简单采购策略配置

规模小、复杂程度低的组织可按法人设置采购策略，并可仅使用“公司”组织层次结构。  

对于小型企业 Fabrikam，组织范围内的采购需求差别很小。 采购规则仅在组织的法人间有所不同。 例如，加拿大 Fabrikam 的员工和美国 Fabrikam 的员工从不同的目录和不同的供应商采购货物和服务。 因此，Fabrikam 在法人级别设置其采购策略。  

Fabrikam 创建两个采购策略。 策略 A 适用于其美国法人 1111。 策略 B 适用于其加拿大法人 2222。 法人 1111 中的员工创建采购申请时，策略规则从策略 A 派生。例如员工看到的产品目录是策略 A 的目录策略规则中指定的目录。  

法人 2222 中的员工创建采购申请时，策略规则从策略 B 派生。  

**注意：** 如果法人 1111 的员工代表法人 2222 的员工采购物料，则适用为法人 2222 指定的策略规则（即策略 B 的策略规则）。

### <a name="example-2-complex-purchasing-policy-configuration"></a>示例 2：复杂采购策略配置

在前面的示例中，所有采购规则都在单个组织层次结构（“公司”组织层次结构）中定义。 但是，复杂的组织可以为多个组织层次结构定义策略。  


Contoso 是需要复杂采购规则来控制请流程的一家大型公司。 Contoso 已为两个不同的组织层次结构定义规则：部门和全球采购控制。  

策略 123 为英国销售 - 销售部门的“部门”组织层次结构定义。 在策略 123 中，采购申请控制规则指定了必须对最小订单数量强制实施的限制。 在此规则中，将选择 **强制实施最小订单数量限制** 选项卡。  

策略 456 为销售和市场营销部门的“全局采购控制”组织层次结构定义。 在策略 456 中，采购申请控制规则未指定必须对最小订单数量强制实施的限制。 在此规则中，将取消选择 **强制实施最小订单数量限制** 选项卡。  

Sam 在 Contoso 的英国办事处的英国销售 - 销售部门中工作。 “部门”和“全球采购控制”组织层次结构的策略适用于其部门。 Sam 创建采购申请时，系统必须确定适用的策略。 系统管理员设置采购策略参数来指定必须按以下优先级顺序应用采购策略：

1.  全局采购控制
2.  部门
3.  公司

因此，策略 456 适用于 Sam 创建的采购申请，而该采购申请不需要最小订单数量。

## <a name="policy-rules"></a>政策规则
### <a name="catalog-policy-rule"></a>目录政策规则

内容策略规则确定了用户在创建采购申请时看到的采购目录。 如果为某个用户授予了代表其他用户订购产品的权限，申请将使用为申请人的法人和营运单位定义的用于确定要显示的目录的目录策略规则。 在定义目录策略规则之前，您必须创建并发布采购目录。

### <a name="category-access-policy-rule"></a>类别访问策略规则

类别访问策略规则确定了用户在创建采购申请时有权访问的类别。 如果未指定任何规则，则可以将所有采购类别添加到采购申请。

1.  选择 **包括父规则** 选项以将父组织的类别访问策略规则应用于该类别。
2.  在 **可用类别** 窗格中，选择该规则适用的类别。 当您选择某一类别时，该层次结构中所有较高的类别也将添加到 **所选类别** 列表。
3.  选择 **包括子类别** 选项以将该规则应用于所选类别的所有子类别。

### <a name="category-policy-rule"></a>类别策略规则

类别策略规则定义了用户为每个类别选择供应商的方式。 它还定义了收货和开票流程的要求。

### <a name="re-approval-rule-for-purchase-orders"></a>采购订单的重新审核规则

重新审批规则是一个可选规则，用于在更改采购订单后定义必须进行重新审批的条件。 当在工作流中设置了“采购订单需要重新审批”条件时，所选字段将在采购订单工作流中评估。

> [!NOTE]
> 当启用的更改管理的已审核采购订单被更改时，会计分配将始终重置。 因此应意识到，如果要避免在某些字段被更改时重新审核采购订单，字段 Accounting distribution.changed 不应作为所选字段包括在重新审核范围内。 

### <a name="purchase-requisition-rfq-rule"></a>采购申请询价规则

采购申请询价规则定义了采购申请行需要询价 (RFQ) 的条件。 如果某个行满足条件，“非正式询价”或“正式询价”戳记将出现在申请行上。

### <a name="purchase-requisition-control-rule"></a>采购申请控制规则

**消耗量** 类型申请的采购申请控制规则是一项可选规则。 当您创建此规则的类型时，您可以在各个选项卡上设置选项：

-   在 **工作流提交** 选项卡上，您可以配置必须在申请行上输入的字段，以提交申请供审批。
-   在 **订单数量** 选项卡上，您可以配置采购申请在特定条件下需要的字段。 您还可以强制实施订单数量。
-   在 **日期** 选项卡上，您可以配置会计日期是否与请求的日期相同
-   在 **地址** 选项卡上，您可以定义是否允许用户在系统中创建要应用于采购申请的新地址。

### <a name="requisition-purpose-rule"></a>申请用途规则

申请目的规则是一个可选规则，用于确定允许用于特定法人的申请目的的类型。 除非此规则中指示了其他目的，否则申请在其创建时自动具有 **消耗** 目的。

### <a name="replenishment-category-access-policy-rule"></a>补货类别访问政策规则

补货类别访问策略规则是一个可选规则，用于在申请目的为 **补货** 时确定可用于满足特定法人的申请需求的产品。

### <a name="replenishment-control-rule"></a>补货控制规则

补货控制规则是一个可选规则，用于在申请目的为 **补货** 时定义必须在申请行上输入以便让申请提交审核的字段。

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>采购订单创建和需求合并规则

采购订单创建和需求合并规则定义了要在从获批的采购申请生成采购订单后使用的策略规则。 当您创建此规则的类型时，您可以在各个选项卡上设置选项：

-   在 **采购订单拆分** 选项卡上，您可以定义将采购申请行拆分到单独的采购订单上的条件。
-   在 **价格/折扣转移** 选项卡上，您可以在创建采购订单后定义重新计算价格协议的时间：
    -   **只要没有贸易协定** – 只要没有适用的贸易协定或基价，就可以将价格和折扣从采购申请中转移。 如果物料或供应商存在贸易协议或基价，则会根据贸易协议或基价重新计算价格和折扣并将其应用于采购订单。 除非具体说明，否则就是默认行为。
    -   **总是**– 始终从采购申请中转移价格和折扣。

    您还可以允许申请者更改各个采购申请行的价格和折扣转移方法，不管定义的价格/折扣转移规则。 选择 **允许按采购申请行手动覆盖** 选项可启用此功能。
-   在 **物料描述转移** 选项卡上，当物料描述源自询价时，您可以从申请转移物料描述。
-   在 **价格容差** 选项卡上，当采购目录物料的价格上涨时，您可以定义通过查看流程传送已获批的采购申请的规则。 设置采购申请的行项上的净额的最大金额可以延长已审核的采购申请和已创建的采购订单之间的时间。 净额的计算公式如下：(\[数量 × (单位价格 – 折扣) ÷计价单位\] + 采购杂项费用) × (100 – 折扣百分比) ÷ 100。超过您设置的价格容差的采购申请行将被暂停以供手动处理。 您在 **错误处理** 选项卡上配置的规则将确定采购申请行的处理方式。
-   在 **错误处理** 选项卡上，您可以配置应用于采购申请（如果它在采购订单创建过程中由于供应商错误或价格容差而验证失败）的处理规则。 选择以下选项之一：
    -   **无操作** - 采购申请行在保留在 **发布已审核的采购申请** 页上。 采购申请行的状态将仍为 **已批准**。 但是，在采购订单可以生成采购申请行之前，必须解决错误。
    -   **取消采购申请行** - 将取消采购申请行。 如果仍想请求行项，申请者可以创建取消行的新的采购申请。
    -   **创建新采购申请行** - 将创建采购申请行。 随后将生成只包含验证失败的采购申请行的新采购申请。 生成的新采购申请具有 **草稿** 状态。 在验证错误解决后，这些采购申请可以重新提交。 采购申请行的准备人员被通知这些行已取消，并且已为失败的采购申请行创建新的采购申请。
-   在 **手动采购订单创建** 选项卡上，您可以定义是否必须手动处理采购申请或者它是否能自动转换为采购订单。 参数可以应用于内部列出物料、外部目录物料或非目录物料。 选择以下选项之一：
    -   **手动创建采购订单** - 为所有采购申请手动创建采购订单。
    -   **自动创建采购订单** - 为所有获批的采购申请自动创建采购订单。 没有手动创建的采购订单的采购申请暂停。
    -   **除这些情况之外自动创建采购订单** - 为满足您定义的条件的采购申请手动创建采购订单。 已审核的其他采购申请自动转换为采购订单。 如果您选择 **除这些情况之外自动创建采购订单**，则可以添加采购类别和供应商以指定哪些已获批的采购申请行被暂停以供手动处理。 此选项可以应用于内部列出物料、外部目录物料和非目录物料。 在您选择某一采购类别时，该采购类别的所有子类别也选中。 为特定类型的采购申请行选择 **全部** 选项以暂停该行类型的所有行以供手动处理。

    如果您希望在采购订单生成的批处理作业运行时从已获批的采购申请自动生成采购订单，请选择 **将自动采购订单创建作为批处理作业运行** 选项。 此选项仅适用于不需要手动处理的采购申请。 通过自动运行生成订单作为批处理作业，您在资源时间约束时执行此活动。 如果在采购申请行上选择了 **需要已付款** 选项，请选择 **在为预付款设置申请时** 选项以暂停已获批的采购申请以供手动处理。 可以筛选待手动处理的采购申请，因此，您只能查看要求预付款的那些采购申请行。
-   在 **需求合并** 选项卡上，您可以定义一些参数，用来确定手动处理的采购申请是否能被纳入合并的考虑范围。 参数可以应用于内部列出物料、外部目录物料或非目录物料。 选择以下选项之一：
    -   **不允许需求合并** - 已获批的采购申请行都没有资格进行需求合并。 默认情况下选择此选项并且只应用于要求手动处理采购订单创建的采购申请。
    -   **总是允许需求合并** - 所有已获批的采购申请行都有资格进行需求合并。 **注意：** 如果您选择了 **需求合并** 选项卡上的 **总是允许需求合并** 选项，但又选择了 **手动创建采购订单** 选项卡上的 **自动创建采购订单** 选项，所有采购申请都会被暂停以供手动处理。
    -   **在这些情况下允许需求合并** - 定义用来确定已获批的采购申请行是否有资格进行需求合并的条件。 对于采购申请行中的每种类型，可以按采购类别和供应商设置条件。 如果您选择了 **这些情况下允许需求合并**，则可以按采购类别和供应商为每种类型的采购申请行设置条件。 在您选择某一采购类别时，该采购类别的所有子类别也选中。 如果您为特定行类型选择了 **全部** 选项，则该行类型的所有采购申请行都有资格进行需求合并。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]