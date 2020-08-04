---
title: 设置福利管理参数
description: 在 Microsoft Dynamics 365 Human Resources 中配置福利管理的参数。
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85bbe5d3b422f2f29f1d1fe8ee269b407da691c2
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599348"
---
# <a name="set-benefits-management-parameters"></a>设置福利管理参数

您必须先配置福利管理参数，然后才能在 Microsoft Dynamics 365 Human Resources 中设置休假计划。 这些参数设置默认值、原因代码和其他选项。

## <a name="configure-general-parameters"></a>配置常规参数

1. 在**福利管理**工作区中，在**设置**下，选择**人力资源共享参数**。

2. 在**常规**选项卡上，为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **国家/地区** | **国家/地区**字段确定邮政编码/省/市/自治区的显示顺序。 所选国家/地区首先显示在下拉列表中。 |
   | **登记原因代码** | 选择在开放登记处理期间创建员工计划时要使用的默认原因代码。 |
   | **取消原因代码** | 取消员工福利计划时使用的原因代码。 将在取消过程中显示在对话框中。 如有必要，用户可以更改**取消原因代码**。 |
   | **重新打开原因代码** | 重新打开员工福利计划时使用的原因代码。 将在取消过程中显示在对话框中。 如有必要，用户可以更改**重新打开原因代码**。 | 
   | **生命事件原因代码** | 生命事件发生时要使用的原因代码。 |
   | **比率更改原因代码** | 在比率更改更新流程中取消和重新打开员工福利计划时使用的原因代码。 指示比率更改更新流程更改了哪些记录。 |
   | **年度福利薪金** | 使您可以为员工设置**福利年薪**金额。 人力资源部门在确定覆盖范围金额时将使用**福利年薪**金额，而不是固定薪酬年度金额。 |
   | **新雇员符合资格** | 指定新雇员是否符合资格。 |
   | **新雇用登记期间** | 允许新雇用登记的时间段。</br></br>**注意**：此设置将覆盖您在计划资格规则中设置的所有新雇用登记期间。 |
   | **默认付薪频率** | 添加新工作人员时使用的默认付薪频率。 |
   | **生命事件已启用** | 启用生命事件。 |
   | **隐藏旧版福利窗体** | 允许您隐藏旧版福利窗体。 |

3. 选择**保存**。

## <a name="configure-employee-self-service-parameters"></a>配置员工自助服务参数

1. 在**福利管理**工作区中，在**设置**下，选择**人力资源参数**。

2. 在**员工自助服务**选项卡上，为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **福利验证** | 自助服务福利结账期间时要使用的验证文本。 |
   | **自动选择指定人员** | 指定是否根据依赖方和受益人的计划选项的资格自动选择依赖方和受益人。 |

3. 选择**保存**。
