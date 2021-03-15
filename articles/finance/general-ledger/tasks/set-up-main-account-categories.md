---
title: 设置主科目类别
description: 本主题说明如何在 Dynamics 365 Finance 中设置主科目类别。
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d53181d63f7b362662d993e21671e9b685b5dfe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968416"
---
# <a name="set-up-main-account-categories"></a>设置主科目类别

[!include [banner](../../includes/banner.md)]

本主题说明如何设置主科目类别。 主科目类别用于财务报表和 Power BI 中的默认报表。 默认创建的主科目类别可以重命名，但不可删除。 可创建其他科目类别，并用于报告和分析。 此主题使用演示公司 USMF。

## <a name="create-a-main-account-category"></a>创建主科目类别
1. 在导航窗格中，转到 **模块 > 总帐 > 会计科目表 > 科目 > 主科目类别**。
2. 选择 **新建**。
3. 在 **主科目类别** 字段中，输入唯一的名称。
4. 在 **描述** 字段中，输入主科目类别的描述。
5. 在 **主科目类型** 字段中，选择将链接到类别的主科目类型。

## <a name="link-main-accounts-to-account-category"></a>链接主科目到科目类别
1. 单击 **链接主科目**。
2. 在列表中，通过单击 **已链接** 列中的框，选择要分配给主科目类别的主科目。 在将类别用于财务报表和分析时，将主科目分配到该主科目类别将汇总科目余额。  
3. 选择或取消选择 **已链接** 选项，以选择主科目。
4. 选择 **确定**。
5. 选择 **是**。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]