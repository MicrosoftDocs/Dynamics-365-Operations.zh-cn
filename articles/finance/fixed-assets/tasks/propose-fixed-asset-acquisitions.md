---
title: 建议固定资产购置
description: 本主题介绍如何使用固定资产日记帐中的购置方案购置固定资产。
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99202763ae32d02f94f1590783727d4f2cf7a7bbe45963d0e175bfc449b134d9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742921"
---
# <a name="propose-fixed-asset-acquisitions"></a>建议固定资产购置

[!include [banner](../../includes/banner.md)]

本主题介绍如何使用固定资产日记帐中的购置方案购置固定资产。 它为 USMF 法人实体使用会计角色和演示数据。 要通过固定资产建议日记帐获取固定资产，必须首先创建固定资产记录，然后在资产帐簿中定义购置价格。

## <a name="create-an-asset-acquisition-proposal"></a>创建资产购置方案

完成以下步骤以创建资产购置方案。 

1. 在导航窗格中，转到 **模块 > 固定资产 > 日记帐条目 > 固定资产日记帐**。
2. 选择 **新建**。
3. 在 **名称** 字段中，输入或选择一个值。
4. 在操作窗格中，选择 **行**。
5. 选择 **方案**。
6. 选择 **购置方案**。
7. 选择 **筛选器**。 选择 **重置** 以清除先前的值。
8. 选择 **固定资产编号** 行。
9. 在 **标准** 字段中，输入或选择一个值。 为您想要以此方案购置的固定资产设置其他条件。  
10. 选择 **确定** 两次退出窗格。
- 验证已创建交易行。  
- 只有在帐簿中设置了购置日期和购置价格的固定资产才会包含在购置方案中。  
11. 在页面上，选择 **帐簿** 选项卡。
12. 选择 **过帐**。

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>在购置方案中包括默认的财务维度

通过转到 **固定资产 > 日记帐条目 > 固定资产日记帐**，可以使用 Excel 加载项创建购置交易。 创建新日记帐，移动到页面上的 **行** 部分，选择 Excel 图标，然后选择固定资产日记帐行。 系统将创建并打开表示日记帐行的 Excel 模板。 您可以为要添加到模板中的日记帐行添加数据，然后将该信息发布回系统中。 

如果已为所选的资产薄和在 Excel 模板中输入的相应固定资产设置默认维度，当日记帐从 Excel 发布到系统时，将从资产薄主数据中调用默认财务维度。 若要在从 Excel 加载项发布固定资产日记帐时自动在资产簿上包括财务维度，必须预先设置默认维度。  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
