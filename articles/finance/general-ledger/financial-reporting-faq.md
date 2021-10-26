---
title: 财务报告常见问题解答
description: 本主题提供有关财务报告的一些常见问题的解答。
author: jiwo
ms.date: 07/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3690a541b503281f204221a72bfb5a371984d9e4
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605271"
---
# <a name="financial-reporting-faq"></a>财务报告常见问题解答

本主题提供有关财务报告的常见问题的解答。

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>如何使用树安全限制对报表的访问？

以下示例说明了如何使用树安全来限制对报表的访问。

USMF 演示公司有一个 **资产负债表** 报表，并非所有财务报告用户都应具有对该报表的访问权限。 您可以使用树安全来限制对单个报表的访问，以便只有特定用户可以访问该报表。

1. 登录到 Financial Reporter Report Designer。
2. 选择 **文件 \> 新建 \> 树定义** 以创建一个新的树定义。
3. 两次点击（或双击）**单位安全性** 列中的 **摘要** 行。
4. 选择 **用户和组**。
5. 选择需要访问此报表的用户或组。
6. 选择 **保存**。
7. 在报表定义中，添加您的新树定义。
8. 在树定义中，选择 **设置**。 然后，在 **报告单位选择** 下，选择 **包括所有单位**。

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>如何确定哪些帐户与我的余额不匹配？

如果您的报表没有匹配的余额，可以按照以下过程来确定每一个帐户及差异。

### <a name="in-financial-reporter-report-designer"></a>在 Financial Reporter Report Designer 中

1. 创建一个新的行定义。
2. 选择 **编辑 \> 插入维度中的行**。
3. 选择 **MainAccount**。
4. 选择 **确定**。
5. 保存行定义。
6. 创建一个新的列定义。
7. 创建一个新的报表定义。
8. 选择 **设置** 并取消标记此选项。
9. 生成报表。 
10. 将报表导出到 Microsoft Excel。

### <a name="in-dynamics-365-finance"></a>在 Dynamics 365 Finance 中

1. 转到 **总帐 \> 查询和报表 \> 试算平衡表**。
2. 设置以下字段：

    - **开始日期** - 输入会计年度的开始日期。
    - **结束日期** - 输入报表的生成日期。
    - **财务维度** - 将此字段设置为 **主科目集**。

3. 选择 **计算**。
4. 将报表导出到 Excel。

您现在应该能够将 Financial Reporter Excel 报表中的数据复制到 **试算平衡表** 报表，以便可以比较 **期末余额** 列。

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>当我在 Report Designer 中设计报表或生成财务报表时，收到以下消息：“由于数据提供程序框架出现问题，无法完成此操作。” 我应如何处理？

该消息指示在您使用财务报告时，系统尝试从数据市场中检索财务元数据时出现问题。 处理此问题有两种方法：

- 通过转到 Report Designer 中的 **工具 \> 集成状态**，查看数据的集成状态。 如果集成未完成，请等待它完成。 然后，在收到消息时重试所执行的操作。
- 联系支持人员以确定并解决问题。 系统中可能存在不一致的数据。 支持工程师可以帮助您确定服务器上的问题，并找到可能需要更新的特定数据。

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>选择历史利率转换对报表绩效有何影响？

历史利率通常用于留存收益、财产、工厂和设备以及所有者权益科目。 根据财务会计标准委员会 (FASB) 或公认会计准则 (GAAP) 的指导，可能需要历史利率。 有关详细信息，请参阅[财务报告中的货币功能](financial-reporting-currency-capability.md)。

## <a name="how-many-types-of-currency-rate-are-there"></a>存在多少种类型的币种汇率？

一般存在三种类型：

- **当前利率** - 此类型通常用于资产负债表科目。 它通常称为 *即期汇率*，可以是当月最后一天或其他预先确定日期的汇率。
- **平均利率** - 此类型通常用于利润表（损益）帐户。 您可以设置平均利率以进行简单平均或加权平均。
- **历史利率** – 通常用于留存收益、财产、工厂和设备以及所有者权益科目。 根据 FASB 或 GAAP 准则，可能需要这些帐户。

## <a name="how-does-historical-currency-translation-work"></a>历史币种如何进行转换？

利率特定于交易日期。 因此，每项交易都是根据最接近的汇率单独换算的。

对于历史币种转换，可以使用预计算的期间余额，而不是单项交易的详细信息。 此行为不同于当前利率转换的行为。

## <a name="how-does-historical-currency-translation-affect-performance"></a>历史币种转换如何影响绩效？

更新报表上显示的数据时，可能会出现延迟，因为必须通过检查交易详细信息来重新计算金额。 每次更新利率或过帐更多交易时，都会触发此延迟。 例如，如果每天多次设置数千个帐户进行历史转换，可能在经历长达一小时的延迟后，报告上的数据才会更新。 但是，如果特定帐户的数量较少，则更新报表数据所需的处理时间可以缩短至数分钟或更少。

同样，当使用历史类型帐户的货币转换生成报表时，将需要对每笔交易进行额外的计算。 根据帐户数，报表生成所需时间可能延长一倍以上。

## <a name="what-are-the-estimated-data-mart-integration-intervals"></a>估计的数据市场集成间隔是多久？

Financial Reporter 使用 16 个任务将数据从 Dynamics 365 Finance 复制到 Financial Reporter 数据库。 下表列出了这 16 个任务，并显示指定每个任务的运行频率的间隔。 间隔无法更改。

| 名称                                                       | 间隔 | 间隔计时单位 |
|------------------------------------------------------------|----------|-----------------|
| AX 2012 科目类别到科目类别            | 41       | 分钟         |
| AX 2012 帐户到帐户                                | 7        | 分钟         |
| AX 2012 公司到公司                               | 300      | 秒         |
| AX 2012 公司到组织                          | 23       | 分钟         |
| AX 2012 维度组合到维度组合    | 1        | 分钟         |
| AX 2012 维度值到维度值                | 11       | 分钟         |
| AX 2012 维度到维度                            | 31       | 分钟         |
| AX 2012 汇率到汇率                    | 17       | 分钟         |
| AX 2012 会计年度到会计年度                        | 13       | 分钟         |
| AX 2012 总帐交易到事实                | 1        | 分钟         |
| AX 2012 组织层次结构到树                   | 3,600    | 秒         |
| AX 2012 方案到方案                              | 29       | 分钟         |
| AX 2012 交易类型限定符到事实类型限定符 | 19       | 分钟         |
| 维护任务                                           | 1        | 分钟         |
| MR 报表定义到 AX7 财务报表             | 45       | 秒         |
| MR 报表版本到 AX 财务报表版本         | 45       | 秒         |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
