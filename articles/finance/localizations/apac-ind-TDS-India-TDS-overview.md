---
title: 印度从源扣缴税款 (TDS) 概述
description: 本主题提供有关印度从源扣缴税款 (TDS) 的详细信息。 TDS 文档涵盖了此功能的功能性。
author: kailiang
ms.date: 03/19/2021
ms.topic: overview
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d33faaff8be4821005b8772875eb91f0afe26cb0
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983895"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a>印度从源扣缴税款 (TDS) 概述

[!include [banner](../includes/banner.md)]

本主题提供有关印度从源扣缴税款 (TDS) 的详细信息。

TDS 文档涵盖了此功能的功能性。 它还说明了如何进行 TDS 的基本设置，计算交易的 TDS，完成 TDS 结算流程，记录 TDS 证书编号以及生成 TDS 查询、TDS 对帐单和 TDS 证书。 该文档包含以下主题：

- [TDS 的基本设置](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [用于 TDS 计算的公式设计器和阈值限制功能](apac-ind-TDS-Formula-designer.md)
- [发票、付款、本票和内部公司交易的 TDS 计算](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [定期 TDS 结算流程和针对 TDS 主管机构供应商的 TDS 金额结算](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [记录和更新 TDS 证书编号和日期](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>TDS 简介

根据 1961 年的《所得税法》，所得税由服务的接收方在预付款或信用赊帐（以先发生者为准）时从源扣除。 进行付款的人必须扣除税额，仅向服务的提供方支付净余额。 TDS 适用于政府指定的服务，使用政府在某个期间指定的费率扣除税款。 扣除费率基于接收付款或提供服务的实体的状态。 状态包括 **个人**、**印度教家庭** (**HUF**)、**公司**、**事务所**、**人员协会** (**AOP**)、**个人集合体** (**BOI**) 和 **本地主管机构**。

以下各节列出了印度政府指定的 TDS 适用的服务。

**居民**

- 薪金收入（根据第 192 节）
- 证券利息收入（根据第 193 节）
- 股息收入（根据第 194 节）
- 利息收入（根据第 194A 节）
- 彩票或益智游戏收入（根据第 194B 节）
- 赛马等奖金（根据第 194BB 节）
- 承包商和分包商（根据第 194C 节）
- 保险佣金（根据第 194D 节）
- 国民储蓄计划的存款收入（根据第 194EE 节）
- 共同基金或 UTI 收入（根据第 194F 节）
- 贱价抛售或抽奖的佣金、薪酬、奖金等（根据第 194G 节）
- 佣金或经纪费付款（根据第 194H 节）
- 租金（根据第 194I 节）
- 专业服务（根据第 194J 节）
- 单位收入（根据第 194K 节）
- 购置某些不动产的补偿费（根据第 194LA 节）

**非居民**

- 支付给非居民运动员或体育协会的费用（根据第 194E 节）
- 其他款项（根据第 195 节）
- 关于非居民单位的收入（根据第 196A 节）

    - 印度公司的外币债券或股票收入（根据第 196C 节）
    - 境外机构投资者的证券收入（根据第 196D 节）
    - 薪金和任何人均收入下的所有其他正收入（第 192 节）
    - 证券利息（第 193 节）
    - 除证券利息外的利息（第 194A 节）
    - 支付给承包商和分包商的费用（第 194C 节）
    - 彩票或填字游戏奖金（第 194B 节）
    - 赛马奖金（第 194BB 节）
    - 包括购买保险业务的所有付款的保险佣金（第 194D 节）
    - 除应付给不是公司或外国公司的非居民的证券利息以外的任何利息（第 195 节）
    - 支付给非居民运动员（包括运动员、体育协会或机构）的费用。 如果是非居民运动员，在印度的报纸、杂志等刊登任何比赛/体育的广告和文章等方面支付的费用。 包含的款项（第 194E 节）
    - 支付 NSS \[国民储蓄计划\] 的存款费用（第 194EE 节）
    - 支付共同基金或 UTI 的回购单位的费用（第 194F 节）
    - 支付佣金或经纪费（第 194H 节）
    - 支付租金（第 194I 节）
    - 支付专业或技术服务的费用（第 194J 节）
    - 彩票的发行者、分销商、买家、卖家的佣金，包括此类票证的薪酬或奖金（第 194G 节）
    - 外币买入单位或外币买入单位转让所产生的长期资本收益的收入（第 196B 节）
    - 向非居民支付债券和股票的利息或股息的任何收入（第 196C 节）

根据采购、销售、销售退货、贷方通知单、固定资产购置、预付款、提前付款、本票、就业税和内部公司交易计算 TDS。

> [!NOTE]
> 在当前的印度税务方案中，不根据销售交易计算 TDS。 但是，系统包括一项规定，根据销售交易（尤其是内部公司交易）计算可退税的 TDS。

计算 TDS 时始终考虑为 TDS 组分定义的阈值和异常阈值。

必须运行定期 TDS 结算流程，并且必须将 TDS 付款结算给 TDS 主管机构供应商。

可以记录和更新从供应商或客户收到的 TDS 证书的证书编号和日期。 此外，可以在 Finance 中生成表单 26Q 和表单 27Q 季度对帐单以及 TDS 的表单 16A 证书。

## <a name="setting-up-and-working-with-tds"></a>设置和使用 TDS

下面概述了设置和使用 TDS 的流程：

1. **TDS 设置：**

    - 参数设置：

        - 在总帐参数中，激活与 TDS 相关的参数。
        - 在总帐参数中，设置预缴税金付款的编号规则。
        - 在应付帐款和应收帐款中设置参数。

    - 基本设置：

        - 设置公司、客户和供应商的 TDS 登记编号。
        - 设置 TDS 组分组。
        - 设置 TDS 组分，向其附加 TDS 组分组，并为其定义阈值和异常阈值。
        - 设置 TDS 主管机构。
        - 设置 TDS 结算期间。
        - 设置 TDS 税码，并向其附加 TDS 组分。
        - 设置 TDS 税组，并向其附加 TDS 税码。
        - 在公式设计器中，定义一个公式以计算 TDS 组的 TDS。
        - 记录 TDS 减免证书编号。

    - 分类帐帐户和公司设置：

        - 设置 TDS 应付分类帐帐户和应收分类帐帐户。
        - 设置公司的减税和纳税帐户编号 (TAN) 和扣税类型类别。

    - 其他设置：

        - 设置包括 TDS 分配的付款计划。
        - 为 TDS 主管机构设置付款的付款费用类型。
        - 为供应商和客户设置有关 TDS 组，永久帐号 (PAN) 和 TAN 的信息。

2. **交易中的 TDS 计算：**

    - 账单和付款
    - 本票
    - 预先付款
    - 预付款

3. **TDS 结算：**

    - 定期 TDS 结算流程
    - 向 TDS 主管机构供应商结算 TDS 付款并生成 TDS challan

4. **TDS 查询、对帐单和证书：**

    - 记录和更新 TDS 证书编号和日期。
    - 生成 TDS 查询和已过帐的 TDS 查询。
    - 生成表单 27A、表单 26Q 和表单 27Q TDS 以及 e-TDS 季度对帐单。
    - 生成表单 16A TDS 证书。
