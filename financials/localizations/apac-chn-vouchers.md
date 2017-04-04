---
title: "中国式凭证"
description: "此主题描述中文凭证，以及如何在 Microsoft Dynamics 365。工序。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerVoucherType_CN, VoucherTypeWizard_CN
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261454
ms.assetid: b5a50142-b48c-4b1b-8828-6c436ea91238
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: dc16f087b3872a41ba277b309b2d50a5442a50b4
ms.lasthandoff: 03/31/2017


---

# <a name="chinese-vouchers"></a>中国式凭证

此主题描述中文凭证，以及如何在 Microsoft Dynamics 365。工序。

您必须为各已过帐的日志创建凭据文档。 可以打印纸质凭证和已过帐日志。 基于常用于您的需求，则可以使用凭证类型安装向导设置**获取** **，工资** **和凭证转移**类型，或者可以创建在**的设置凭证类型**新凭证的页面的类型。 您可以使用凭证输入预订组和交易记录分为收货凭证、付款凭证或凭证转移。 

从第一天开始第一个的连续编号规则应赋给每个凭证类型。 仅可以定义会计科目的中国式凭证类型。 您可以将凭证类型于特定会计科目。 然后，在**的设置凭证类型**页上，可以定义过帐的凭证交易记录验证规则到指定的会计科目。 在凭证过帐期间，验证基于在的序列运行，**的设置凭证类型**指定页面。 您将收到消息，则为所选会计科目选择凭证的类型不正确。 

例如，您选择会计科目**为贷方** ** **获取凭证输入类型。 不过，您用于的验证规则** **获取凭证定义类型指定会计科目必须是借方科目。 在这种情况下，您将收到消息中文凭证类型使用"无效"状态。 然后可以进行相应的更改后再次过帐凭证。 

## <a name="voucher-creation-methods"></a>凭证创建方法
您可以创建在**普通记帐日志** **使用简单** **或高级**方法，页面的凭证交易记录。 如果您创建单个凭证的日志凭证输入使用** **简单方法，在所有日志行选择应该相同凭证的类型。 **高级**方法可以创建不同的凭证类型多个日志行中。 

## <a name="check-for-continuity-in-voucher-numbers"></a>支票将按照凭证号的连续性
中文凭证号应是连续的，不应在会计期间的间隔。 您可以运行批处理进程确定是否在以中文凭证号的间隔。 验证批次流程交易记录日期然后对连续性的凭证。 为目的跟踪，可以生成凭证中文**连续性检查**报表。 此报告显示对中文凭证的历史记录。 

## <a name="printing-a-chinese-voucher"></a>打印某一凭证中文
在过帐凭证之前或之后，您可以打印一凭证中文以下内容之一。 打印的凭证显示诸如将对以中文凭证的历史记录，并且，在凭证过帐之前或之后的税务信息。 您可以随时查看打印的信息之后验证过帐之前或之后，信息完全相同，并且，信息正确。 例如，如果选择，在日志凭证的增值税，则最终凭证信息包括增值税。 但是，销售税可能是不同于日志中产生部分的增值税不同。 该打印的结果必须是准确的，则必须相同。在进行最终过帐后生成的结果。 因此，可以打印具有不同日志凭证和凭证交易记录的凭证。中文中的信息 在以中文，按凭证和会计期间前类型后，筛选信息还可以打印在以中文批次的凭证。



