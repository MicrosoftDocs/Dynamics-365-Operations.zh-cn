---
title: 会计日历、会计年度和期间
description: 本文讨论会计日历、会计年度和期间以及如何为法人、固定资产和预算使用它们。
author: aprilolson
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: roschlom
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f40dc7227d8ee9ccc45336e9b8968937ef5f6092
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995332"
---
# <a name="fiscal-calendars-fiscal-years-and-periods"></a>会计日历、会计年度和期间

[!include [banner](../includes/banner.md)]

本文讨论会计日历、会计年度和期间以及如何为法人、固定资产和预算使用它们。

会计年度为组织的财务活动提供一个框架。 每个会计年度包含一个或多个会计年度，并且每个会计年度包含多个期间。 会计年度可以基于一个 1 月 1 日到 12 月 31 日的日历年度，或者您选择的任意日期。 例如，选择在一年的 7 月 1 日开始并且在下一年的 6 月 30 日结束的会计日历。 

没有限制您可以创建的会计日历的数量和没有限制为会计日历创建的会计年度的数量。 每个会计日历与您的组织无关，可以由多个组织法人使用。 例如，组织具有八个部门，并且每个部门是独立的法人。 它们五个共享相同的会计日历和三种使用不同的会计日历。 您可以创建共享相同会计日历的五个法人的会计日历，然后创建其他法人的单独的会计日历。

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>创建会计日历、会计年度和期间
您可以在“会计日历”页上创建并且删除会计日历、会计年度和期间。 您还可以划分现有期间和创建可用于结算某个会计年度的结转期间。 

结算期间用于划分结算某个会计年度时生成的总帐交易记录。 当结算交易记录都处于一个会计期间时，很容易创建包括或排除不同类型结算条目的财务报表。 如果将一个会计年度划分为 12 个会计期间，这结算期通常为第 13 期。 但是，可以从具有状态“未完成”的任何期间创建结算期间。 

当您创建一个结算期间时，选择一个具有状态“未完成”并具有您要使用的日期的期间。 新的结算期间将从现有期间中复制开始日期和结束日期。 原始期间将继续存在。 例如，您选择了为该会计年度的最后一个期间并具有 8 月 1 日到 8 月 31 日这些日期的“期间 12”。 您为该结算期间输入了一个名词，如 “结算”。 当您创建了该新的结算期间后，现在您拥有原始期间和结算期间。 都含有 8 月 1 日到 8 月 31 日的日期。

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>为分类帐、固定资产和预算期间选择会计日历
会计日历用于固定资产折旧、财务交易记录和预算期间。 在您创建某一会计日历时，您可以为多个目的使用它。 您可以选择固定资产帐簿的会计日历以使其为固定资产日历。 您可以选择分类帐的会计日历以使其为分类帐日历。 并且您可以选择预算期间的会计日历以使其为预算日历。 您可以为所有这些使用相同的会计日历。

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>为您的法人选择某一会计日历

选择要为“分类帐”窗体中您的法人的分类帐使用的会计日历。 必须在“分类帐”页上为每个法人选择一个会计日历。 当您选择了一个会计日历之后，您可以针对属于会计年度一部分的任何期间在“分类帐日历”页上设置期间状态和权限。

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>选择固定资产的会计日历

您可以为固定资产帐簿选择会计日历，并且该会计日历将由使用所选帐簿的固定资产使用。 您可以从在“会计日历”页上定义的任何会计日历中进行选择。

### <a name="define-budget-cycle-time-spans"></a>定义预算周期跨度

预算期间是在期间使用预算的时间长度。 预算期间可能包含一个会计年度或多个会计年度的一部分，例如一个两年一次的预算期间或一个三年一次的预算期间。 预算期间跨度定义在预算期间包括的期间的数量。 若要指定预算周期跨度，请使用“预算周期跨度”页。

## <a name="maintain-periods-for-your-organization"></a>维护您的组织的期间
您可以使用“分类帐日历”页查看您的组织使用的会计日历、会计年度和期间的详细信息。 您还可以更改该期间的状态和选择哪些用户都可以过帐会计科目交易记录到期间。 例如，在新期间的开始，当其他组只在新期间工作时，您可能希望一组用户在前一期间完成过帐财务交易记录。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]