---
title: Dynamics 365 Human Resources 基础结构合并 - 版本 10.0.25 更新
description: 本主题提供有关 Microsoft Dynamics 365 Human Resources 版本 10.0.25 的信息，此版本在基础结构合并中带来第一波功能。
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf7ce43785e3ef485074f2b0294caea381f8f726
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688083"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources 基础结构合并 - 版本 10.0.25 更新

10.0.25 版本在基础结构合并中带来第一波功能。 在基础结构合并期间，Microsoft Dynamics 365 Human Resources 将与 Finance and Operations 基础结构合并。 但是，它将继续作为 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 等独立应用程序获得许可。 有关基础结构合并的详细信息，请参阅 [Dynamics 365 Human Resources 基础结构合并常见问题解答](../human-resources/hr-infrastructure-merge-faq.md)。

此合并将通过以下方式为人力资源用户提供一致性：

- [环境管理和集成在 Human Resources 和 Finance and Operations 应用之间是一致的。](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - 在 Microsoft Dynamics Lifecycle Services、问题搜索和 Regression Suite Automation Tool 中管理环境。
    - 存在单个代码库，其中将在常规一个版本更新过程中发布 Human Resources 的新功能。
    - 将升级、更新和修补程序应用于环境的方式是一致的。

- [可扩展性选项经过了改进。](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options)

    - 您可以继续使用 Microsoft Power Platform Tools 根据需要进行扩展。
    - 您可以通过窗体、表、方法和应用编程接口 (API) 扩展功能。
    - 您可以创建和扩展实体。

    有关可用扩展选项的详细信息，请参阅 [Dynamics 365 中的可扩展性概览](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md)。

- [在 Dynamics 365 中创建一组人力资源功能。](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/create-one-set-human-resources-capabilities-within-dynamics-365)

    在 10.0.25 版本中，已在 Finance and Operations 基础结构中提供以前仅存在于 Human Resources 中的功能性功能。 要使客户在 Finance and Operations 环境中利用这些功能，必须在功能管理中启用以下 Human Resources 功能。

    | 功能名称 | 概览 | 发放状态 | 
    |--------------|----------|----------------| 
    | 服务年限计算 | 通过设置选项，您可以选择用于 **服务年限** 计算的日期。 | 正式发布 | 
    | 工作流体验增强 | 此功能提供了增强的工作流提交和审核用户体验。 | 正式发布 | 
    | 打印绩效审核 | 您可以打印 PDF 格式的绩效考核。 | 正式发布 | 
    | **经理自助服务** 中的自定义链接 | 您可以创建 **经理自助服务** 的 **相关链接** 部分中显示的自定义链接。 | 正式发布 | 
    | 跨公司薪酬视图 | 用户可以在 **经理自助服务** 中查看所有法人的薪酬计划，而无需切换公司。 | 正式发布 | 
    | 按工作配置多个薪酬级别\*&dagger; | 工作现在支持多种薪酬级别。 | 预览版 | 
    | 任务管理\* | 您可以创建入职、离职和调动流程的核对清单和任务。 | 预览版 | 
    | 简化了员工输入 | 此功能在现有 **工作人员** 页面上提供更新的用户体验。 | 预览版 | 
    | 人力资源用户体验增强 | 查看下一节中的表。  | 预览版 | 

\*必须先启用此功能，然后才能使用 **Human Resources 用户体验增强** 功能。

&dagger; 此功能在启用后不能被禁用。

## <a name="human-resource-user-experience-enhancements"></a>人力资源用户体验增强

| 功能名称 | 概览 | 
|--------------|----------| 
| 删除雇用关系 | 您可以删除员工雇用。 | 
| 工作系列 | 您可以跟踪一组涉及相似工作并且需要相似培训、技能、知识和专业知识的工作。 | 
| 附加雇用字段 | 添加了以下字段：**雇用类别**、**雇用类型** 和 **雇用状态**。 | 
| **未雇用的工作人员** 页面 | 页面显示了没有雇用记录的工作人员的列表。 | 
| 职位维度用户体验更新 | 增强了按法人分配职位维度的用户体验。 | 
| **人事管理** 工作区中的地址更改 | 此功能提供了在 **Human Resources 参数** 页面上指定的天数期间发生的所有地址更改的计数。 | 
| **人事管理** 工作区中的过期记录 | 此功能提供已过期或即将过期的证书、身份证明、试用、筛选或测试项列表。 | 
| **职位层次结构验证** 页面 | 已对职位行层次结构中的循环引用进行了检查。 | 
| 特定于国家/地区的工资单信息 | 根据雇用工作人员的法人所在的国家或地区，**工作人员雇用** 页面上有可用的其他工资单字段。 | 
| 合规性报告增强功能 | 其他报告选项可用于 EEO-1、Vets 4212 和 OSHA300a。 | 
| **人事管理** 工作区更新 | 已进行更新以跟踪地址更改和即将过期的记录。 此外，新选项卡列出了工作人员和职位变动。 | 
