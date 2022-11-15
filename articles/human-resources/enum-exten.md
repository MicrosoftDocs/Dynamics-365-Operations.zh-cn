---
title: 性别基本枚举可扩展性
description: 本文概述了性别基本枚举的可扩展性。
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749308"
---
# <a name="gender-base-enum-extensibility"></a>性别基本枚举可扩展性

**性别** 枚举现在是可扩展的。 本文介绍了如果您计划扩展 **性别** 枚举，必须在代码库中进行的更改。

## <a name="gender-vs-hcmpersongender"></a>Gender 与 HcmPersonGender

性别值有两个枚举：

- **Gender**（应用程序平台）
- **HcmPersonGender**（人事管理）

**Gender** 枚举在 Microsoft Dynamics 365 Finance 中使用，而 **HcmPersonGender** 特定于人力资本管理 (HCM) 功能。 如果您在使用 HCM 功能，在对 **Gender** 枚举进行任何更改时，应考虑对 **HcmPersonGender** 进行相同的更改。 例如，如果将 **Transgender** 添加到 **Gender** 枚举，同样也将 **Transgender** 添加到 **HcmPersonGender** 枚举。

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil（类）

有一个新的 **HcmPersonGenderTranformUtil** 类已创建，以允许在两个基本枚举器之间进行转换。 在此类中，有两个方法：**convertGenderToHcmPersonGender** 和 **convertHcmPersonGenderToGender**。 您应该使用 **命令链** 类或 **事件处理程序** 创建扩展，并扩展这两个方法来映射添加到任何一个基本枚举的新值。

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP（类）

**PayrollStateWageTaxPrepDP** 是 **工资单州或省/自治区/直辖市工资税准备** SQL Server Reporting Services (SSRS) 报表的数据提供程序类。 对于美国，有三个值可用：**Male**、**Female** 和 **Unspecified**。 在 **populatePayrollStateWageTaxPrepTmp** 方法中，有一个 switch 语句用于将 **HcmPersonGender** 枚举的值映射到以下三个字段之一：**IsMale**、**IsFemale** 或 **IsUnspecifiedGender**。 switch 语句的默认值为 **IsUnspecifiedGender**。 如果将任何值添加到 **HcmPersonGender** 枚举以进行不同映射，您必须使用 **命令链** 类通过 **populatePayrollStateWageTaxPrepTmp** 方法创建扩展，以根据需要更改值。

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact（类）

**smmOutlookSync_Contact** 集成类与 **Outlook** 和 **联系人** 链接值。 **Outlook** 支持三个值：**Male**、**Female** 和 **Unspecified**。 此类有两个方法可以帮助您将 **Genders** 映射到 **OutlookGenders**。 默认方法是 **NonSpecific/UnSpecified**。 如果您为 **Gender** 枚举创建了其他值，应通过两个方法使用 **命令链** 类来创建扩展，然后根据需要进行映射。
