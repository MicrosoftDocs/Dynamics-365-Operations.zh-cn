---
title: 财务报告常见问题解答
description: 本主题提供有关财务报告的一些常见问题的解答。
author: jiwo
ms.date: 01/13/2021
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266625"
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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
