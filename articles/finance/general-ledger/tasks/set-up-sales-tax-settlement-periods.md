---
title: 设置销售税结算期间
description: 本主题说明如何在 Dynamics 365 Finance 中设置销售税结算期。
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd11068a31b5324d87416e7c00f75a59743f695a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813499"
---
# <a name="set-up-sales-tax-settlement-periods"></a>设置销售税结算期间

[!include [banner](../../includes/banner.md)]

本主题说明如何设置销售税结算期。 销售税结算期间含有有关需要申报和缴纳的销售税的期间间隔的信息。 结算流程可在结算期间或特定日期间隔内运行。 所有与结算期间相关的税务代码将进行结算。 根据相关销售税主管机构的设置，应交税金过帐到供应商或总帐科目。

此任务使用 USMF 公司演示。

1. 在导航窗格中，转到 **模块 > 纳税 > 间接税 > 销售税 > 销售税结算期**。
2. 选择 **新建**。
3. 在 **结算期间** 字段中，输入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 在 **主管机构** 字段中，选择接收为结算期间创建的报表和付款的销售税主管机构。
6. 在列表中，找到并选择所需记录。
7. 在 **付款期限** 字段中，在下拉菜单中选择所需记录。 相关销售税主管机构可以设置为供应商，销售税结算将创建开放式供应商发票。 付款期限定义开放式供应商发票的到期日期。  
8. 为结算期间间隔选择类型。
9. 输入每一期间的期间间隔单位数。 例如，1 个季度有 3 个月。
10. 选择或清除 **使用批处理进行销售税结算** 复选框。 结算期的结算流程可在后台将交易记录作为批处理作业。 这是对在期间间隔内的大量涉税交易记录的建议。  
    > [!NOTE]
    > 西班牙、日本和荷兰现在不支持。
11. 选择或清除 **防止生成抵消税交易记录** 复选框。 默认情况下，系统在结算过程中生成抵消税交易记录，如果在某期间间隔内存在大量税交易记录，这可能造成性能问题。 选择此复选框以防止生成抵消税交易记录。
12. 展开 **期间间隔** 选项卡。
13. 选择 **添加**。
14. 在新行中的 **开始日期** 字段中输入日期。
15. 在 **结束日期** 字段中输入日期。
16. 选择 **新建期间间隔**。 一旦输入第一个期间间隔，可自动创建新期间。 您可以返回和根据需要添加新期间间隔。  
17. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]