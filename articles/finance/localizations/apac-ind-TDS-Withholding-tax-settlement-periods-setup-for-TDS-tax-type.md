---
title: 设置 TDS 税务类型的预缴税金结算期间
description: 本文说明如何为从源扣缴税款 (TDS) 结算期间设置结算期间。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 855bda71f0967c53166cf0a7f5e7e465146f34a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846546"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a>设置 TDS 税务类型的预缴税金结算期间

[!include [banner](../includes/banner.md)]

本文说明如何为从源扣缴税款 (TDS) 结算期间设置结算期间。

1. 转到 **税 \> 间接税 \> 预缴税金 \> 预缴税金结算期间**。

    [![预缴税金结算期间页面。](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)

2. 在 **税务类型** 字段中，选择 **TDS** 为 TDS 税务类型设置预缴税金结算期间。
3. 选择 **新建** 创建行。
4. 在 **结算期间** 字段中，为 TDS 结算期间输入名称。
5. 在 **描述** 字段中，输入描述。
6. 在 **预缴税金主管机构** 字段中，选择您要为其定义 TDS 结算期间的 TDS 主管机构。
7. 在 **常规** 快速选项卡上，在 **期间间隔** 字段中，选择 TDS 结算期间的期间间隔类型。
8. 在 **单位数量** 字段中，指定期间间隔类型的单位数量。
9. 在 **期间** 快速选项卡上，在 **开始日期** 字段中，选择 TDS 结算期间的开始日期。 在 **结束日期** 字段中，选择结束日期。
10. 要根据期间间隔和期间单位为现有期间创建后续的 TDS 结算期间，选择 **新建期间**。
11. 要查看在特定结算期间运行的定期 TDS 结算的详细信息，选择 **预缴税金付款** 打开 **预缴税金付款** 页。

    > [!NOTE]
    > 要运行定期 TDS 结算流程，转到 **总帐 \> 定期 \> 预缴税金 \> 预缴税金付款**。

    [![预缴税金付款页面。](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)

12. 关闭该页面。
