---
title: 使用 Regression Suite Automation Tool 的数据不可知测试
description: 此主题讨论有关使用 Regression Suite Automation Tool 的数据不可知测试的建议。
author: kfend
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 120a88790b7cdb6a8cfcf97cbafeced4685384f2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744655"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>使用 Regression Suite Automation Tool 的数据不可知测试

[!include [banner](../includes/banner.md)]

由于 ERP 应用程序的功能验证不能是完整的数据不可知，测试有多个阶段和方法。 这些测试阶段包括：  

- SysTest 框架
- ATL 框架
- Regression Suite Automation Tool (RSAT)

[![测试分类金字塔](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>概览
-   **SysTest 框架** – SysTest 框架可以可靠地用于编写单元测试。 因为单元测试通常测试方法或功能，所以始终应该数据不可知，并且仅依赖在测试中提供的输入数据。
-   **ATL 框架** – Microsoft 有一个 ATL 框架，该框架是 SysTest 框架的精华，可以更简单、更可靠地编写功能测试。 应该使用此框架编写组件测试或简单集成测试。
-   **RSAT** – RSAT 用于集成测试和业务周期测试。 业务周期测试也称为重复验证测试，依赖于现有数据。 但是，如果考虑更多因素，这些测试可能变得数据不可知。 

    - o 在单元测试和组件测试为低级别且可能完全不可知（不依赖于现有数据集）的情况下，业务周期或回归验证测试依赖于某些现有数据。 此数据中包括设置、配置设置（参数）和主数据（客户、供应商、物料等），但是不能包含交易记录数据。 确保在最终测试中还原测试期间更改了的其中任何数据。
    - 根据特定条件选择主数据，而不是选择特定记录。 例如，如果要根据物料的维度值和存货可用性选择物料，请使用这些值筛选产品列表，选择第一个物料，然后复制要用于将来测试的编号。 如果是客户、供应商或物料之类简单主数据行，则可在自动化期间创建，并通过链接在将来的测试中使用。 
    - o 通过编号规则或通过使用 Microsoft Excel 函数（如 =TEXT(NOW(),"yyyymmddhhmm")）输入唯一标识符，如发票编号。 此函数每分钟提供一个唯一编号，这样您就可以跟踪执行的操作。 可将其用于变量，如产品收据编号和供应商发票编号。 这些测试将重复使用同一个数据库，无需进行任何还原。
    - 请始终将环境的 **编辑模式** 设置为 **读取** 或 **编辑** 来充当第一个测试案例，因为默认选项为 **自动**。**自动** 选项始终使用前一个设置，可能导致不可靠的测试。 
 
    [![“选项”页“性能”选项卡](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - 仅在筛选了特定交易记录后才验证，而不是进行常规验证。 例如，对于记录数量，筛选交易记录编号或交易记录日期，以便验证中排除其他所有交易记录。 
    - 如果检查客户余额或预算检查，请首先保存值，然后添加交易记录值以验证预期结果，而不是验证固定预期值。 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]