---
title: 解决 Finance Insights 设置问题
description: 本文列出了您使用 Finance Insights 功能时可能会出现的问题。 它还介绍了如何解决这些问题。
author: panolte
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 1ee354a1c3d9b45eb12eeb3a6a29f2a6d5e4c34c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846906"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>解决 Finance Insights 设置问题

[!include [banner](../includes/banner.md)]

本文列出了您使用 Finance Insights 功能时可能会出现的问题。 它还介绍了如何解决这些问题。

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>症状：为什么我无法映射客户付款见解数据集成模板目标列？

### <a name="resolution"></a>解决方法

您可能正在使用早期版本的模板。 在 10.0.17 版本发布之前，预览版客户使用 **付款预测结果（预览版）** 实体配置了 **客户付款见解结果（CDS 到 Fin and Ops）** 数据集成 (DI) 模板。 升级到 10.0.17 及更高版本后，您应该使用 **客户付款见解结果（CDS 到 Fin and Ops 10.0.17 及更高版本）** DI 模板来完成映射。 在刷新数据管理实体列表并且其中出现 **付款预测结果** 实体之前，您可能无法映射 DI 模板目标列。 若要刷新实体列表并显示付款预测结果，您将在 Microsoft Dynamics 365 Finance 和 Dataverse（以前称为 Common Data Service\[CDS \] 管理员门户）中完成相关步骤。

### <a name="in-finance"></a>在 Finance 中

升级后在 Finance 中执行以下步骤。

1. 转到 **系统管理 \> 工作区 \> 数据管理**。
2. 在 **数据管理** 工作区中，选择 **框架参数** 磁贴。
3. 在 **数据导入/导出框架参数** 页面上，选择 **实体设置**，然后选择 **刷新实体列表**。
4. 关闭 **数据导入/导出框架参数** 页。
5. 在 **数据管理** 工作区中，选择 **数据实体** 磁贴。
6. 搜索“付款预测结果”。 验证 **付款预测结果** 实体是否不是预览版。 预览版本的名称以“（预览版）”结尾。 如果您只看到实体的预览版本，请与 Microsoft 支持人员联系。

### <a name="in-dataverse"></a>在 Dataverse 中

在 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/environments)中执行这些步骤，以更新您的数据集成项目。

1. 如果您使用的是 Finance Insights 预览版，请删除与 **客户付款见解结果（CDS 到 Fin and Ops）** 模板关联的 DI 项目。
2. 按照[创建数据集成器项目](create-data-integrate-project.md)中的步骤操作。 使用 **客户付款见解结果（CDS 到 Fin and Ops 10.0.17 及更高版本）** 模板。

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>问题：当我尝试使用客户付款预测设置页面上的链接打开 AI Builder 时，为什么会收到以下错误消息：“抱歉，已断开连接”？

### <a name="resolution"></a>解决方法

Dynamics 365 Finance 用户必须具有环境的 Microsoft Power Apps 用户帐户，并且该用户帐户必须具有系统定制员角色。 Microsoft Power Apps 系统管理员可以创建此用户帐户并分配角色。 然后，您可以转到 <https://make.preview.powerapps.com/>，使用该用户帐户登录，然后再次尝试链接。

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>症状：为什么“现金流预测”工作区中的“现金预测”选项卡未显示任何数据？

### <a name="resolution"></a>解决方法

必须设置并启用“现金和银行管理”中的现金流预测功能以及 Finance Insights 中的现金流预测功能，才能在 **现金流预测** 工作区中正确显示数据。

首先，设置并启用现金流预测和流动性帐户。 有关详细信息，请参阅[现金流预测](../cash-bank-management/cash-flow-forecasting.md)。 如果此设置已完成，但您看不到所期望的结果，请参阅[现金流预测设置疑难解答](../cash-bank-management/cash-flow-forecasting-tsg.md)，以了解详细信息。

接下来，确认已启用 Finance Insights（**现金和银行管理设置 \> 设置 \> Finance Insights \> 现金流预测**）中的现金流预测功能，并且已完成 AI 模型训练。 如果尚未完成训练，请选择 **立即预测** 以启动模型训练流程。

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>症状：为什么“安装新加载项”按钮在 Microsoft Dynamics Lifecycle Services 中不可见？

### <a name="resolution"></a>解决方法

首先，验证 **环境管理员** 或 **项目负责人** 角色是否已分配给 Microsoft Dynamics Lifecycle Services (LCS) 内 **项目安全角色** 字段中的登录用户。 安装新加载项需要这些项目安全角色之一。

如果为您分配了正确的项目安全角色，您可能需要刷新浏览器窗口才能看到 **安装新加载项** 按钮。

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>症状：Finance Insights 加载项似乎未安装。 为什么？

### <a name="resolution"></a>解决方法

应完成以下步骤。

- 验证您在 Power Portal 管理中心是否具有 **系统管理员** 和 **系统定制员** 访问权限。
- 验证 Dynamics 365 Finance 许可证或等效许可证是否适用于正在安装加载项的用户。
- 验证以下 Azure AD 应用是否已在 Azure AD 中注册： 

  | 申请                  | 应用程序 ID           |
  | ---------------------------- | ---------------- |
  | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>故障：错误，“我们未找到所选筛选器范围的任何数据。 请选择其他筛选器范围，然后重试。” 

### <a name="resolution"></a>解决方法

检查数据集成器设置，验证它是否按预期运行以及是否将数据从 AI Builder 插入回 Finance。  
有关详细信息，请参阅[创建数据集成项目](../finance-insights/create-data-integrate-project.md)。

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>故障：客户付款预测训练失败，AI Builder 的错误状态为“预测应该只使用 2 个不同的结果值来训练模型。 请映射两个结果，然后重新训练”，“训练报告问题：IsNotMinRequiredDistinctNonNullValues”。

### <a name="resolution"></a>解决方法

此错误表示过去一年中没有足够的历史交易记录可以代表 **按时**、**逾期** 和 **严重逾期** 类别中描述的每个类别。 要解决此错误，请调整 **严重逾期** 交易记录的期间。 如果调整 **严重逾期** 交易记录的期间不能解决此错误，说明 **客户付款预测** 不是最佳解决方案，因为它需要使用每个类别的数据进行训练。

有关如何调整 **按时**、**逾期** 和 **严重逾期** 类别的详细信息，请参阅[启用客户付款预测](../finance-insights/enable-cust-paymnt-prediction.md)。

## <a name="symptom-model-training-failed"></a>故障：模型训练失败

### <a name="resolution"></a>解决方法

**现金流预测** 模型训练需要包含 100 个或以上跨度超过一年的交易记录的数据。 我们建议您有至少两年的超过 1,000 个交易记录的数据。

**客户付款预测** 功能需要在过去 6 到 9 个月内 100 个以上的交易记录。 交易记录可以包括普通发票、销售订单和客户付款。 此数据必须跨在 **配置** 页面上定义的 **按时**、**逾期** 和 **严重逾期** 设置分布。    

**预算提案** 功能需要至少三年的预算或实际数据。 此解决方案在预测中使用三到十年的数据。 超过三年会提供更好的结果。 当值有变化时，数据本身效果最好。 如果数据包含的全部是常量数据，如租赁费用，训练可能会失败，因为缺乏变化时不需要 AI 来预测金额。

## <a name="symptom-error-message-states-that-the-table-with-name-msdyn_paypredpredictionresultentities-does-not-exist-the-remote-server-returned-an-error-404-not-found"></a>症状：错误消息指出“名称为‘msdyn_paypredpredictionresultentities’的表不存在。 远程服务器返回错误：(404) 未找到…”

### <a name="resolution"></a>解决方法

环境已达到 Data Lake 服务的最大表限制。 有关限制的详细信息，请参阅文章 [导出到 Azure Data Lake 概览](../../fin-ops-core/dev-itpro/data-entities/Azure-Data-Lake-GA-version-overview.md)的 **启用准实时数据更改** 一节。
