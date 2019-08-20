---
title: 费用报销管理中的增值税退税
description: 此主题介绍如何接收符合条件的增值税 (VAT) 交易记录的退税。
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70a53282bf1d140cb24108fe98e48aa82f783be5
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795140"
---
# <a name="vat-recovery-in-expense-management"></a>费用报销管理中的增值税退税

[!include [banner](../includes/banner.md)]

要接收符合条件的增值税 (VAT) 交易记录的退税，公司或组织必须标识、收集、验证并提交准确信息。 此过程包括多个任务，并根据您公司的大小，可以包括若干员工或角色。

要使用费用报销管理增值税退税，必须完成以下先决任务：

- 必须为分配给支出类别的国家 / 地区创建税码。
- 必须为每个税码创建增值税组。
- 必须为每个增值税组创建物料增值税代码。

在完成先决任务后，员工可以完成增值税交易记录退款请求所需要的步骤。

1. 在支出报表中，输入有关信用卡交易记录的税务信息来确定使用的增值税退款。
2. 确保所有税务信息已完成，然后过帐支出报表。
3. 处理满足国际增值税退税资格的费用。
4. 将增值税退税数据发给第三方供应商以提交国际退税收益。
5. 处理国内增值税退税的费用。

以下章节提供示例显示 Contoso 员工如何完成各步骤。

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>在支出报表中，输入有关信用卡交易记录的税务信息来确定使用的增值税退款

南希是 Contoso 的一位销售代表，她的基地在美国，最近刚从英国出差回来。 在旅行期间，她有一些用于餐费的个人信用卡费用。 南希现在必须创建支出报表来对帐自己的费用。

Nancy 在支出报表中输入信息时，在**编辑支出报表**页**国家/地区**字段中选择**英国**。 然后筛选销售税组列表，使其仅显示适用于英国的组。 南希选择**英国 001** 的增值税组然后选择了**餐费**增值税（物料）组。 然后她添加了食宿的新交易记录。 因为在英国只有一个住宿的增值税组和增值税（物料）组，此信息自动填充进南希的支出报表。

按照 Contoso 的政策，所有支出必须有相应的收据。 因此，Nancy 保存支出报表时，将收到一条消息，说明必须附加支出报表中所列每项交易记录的收据。 Nancy验证她已经将每条交易记录的收据的数据图像附加到她的支出报表，然后提交报表以供审核。 再将纸质收据发给后勤办公室处理团队。 该团队将把增值税退税数据发送给为 Contoso 开国际增值税退税的第三方供应商。

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>确保所有税务信息已完成，然后过帐支出报表

Contoso 的应付帐款协调员 April 必须在过账报表前输入支出报表中缺少的所有税务信息。 她打开**支出报表明细**页并查看 Nancy 的已核准支出报表。 然后，April 打开支出报表查看交易记录的详细信息。 她看到南希的一条交易记录未输入增值税（物料）组。 由于没有提供此信息，April 不能过帐支出报表。 因此，April 在费用报销管理中查看**税项配置**页，找到了该国家/地区和交易记录类型的相应增值税（物料）组。 April 现在可以将支出报表过帐到总帐。

在 April 过账支出报表时， 创建一个增值税可退工作项。 该工作项被分配给后勤办公室处理团队的一位成员。 April 收到一条消息，确认过帐成功。 此消息还列出了经确认可退款的增值税交易记录的数量。

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>处理满足国际增值税退税资格的费用

Arnie 是 Contoso 的后勤办公室处理团队的成员，负责确认所有增值税退税所需信息已包括在支出报表中。 他打开**费用退税**页并选择 Nancy 提交的支出报表。 Arnie 验证已附加所有必需的收据，并已输入正确的增值税组和增值税（物料）代码。

在 Arnie 从南希处接收纸质收货，他验证纸质收货对应数字收据，然后更改支出报表的状态为**准备退税**。

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>将增值税退税数据发给第三方供应商以提交国际退税收益。

在 Arnie 准备将支出报表数据发送给提交增值税退税收益的第三方供应商时，他打开**费用退税**。 他筛选该页以只显示标记为**准备退税**的支出报表。 Arnie 然后选择**文件** &gt; **导出到 Excel**。 将来自支出报表的增值税信息导出到 Microsoft Excel 工作表。 Arnie 此工作表提交给第三方供应商，包括说明已快递纸质收据的消息。

## <a name="process-expenses-for-domestic-vat-recovery"></a>处理国内增值税退税的费用。

Arnie 必须验证支出报表交易记录满足增值税的条件，并且报表附加了数字收据。 为了开始处理国内退税的合理费用，Arnie 打开**费用退税**页并选择需要验证的支出报表。 他验证收据是以公司而不是员工的名义开出的。 增值税退税的收据必须以公司的名义。 Arnie 然后确认应用了正确的增值税组和增值税（物料）代码。

Arnie 收到纸质收据时，将支出报表的状态更改为**准备退税**。 然后向相应的税务机构申请退税。 在这种情况下，在美国的相应的税务机构是美国国税局 (IRS)。
