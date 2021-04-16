---
title: 计算各个法人的固定资产折旧
description: 固定资产折旧可以一步跨多个法人运行。
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85a1e71967fb126be29a76a8a29ea5e4ae2b2199
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818456"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>计算各个法人的固定资产折旧

[!include [banner](../../includes/banner.md)]

固定资产折旧可以一步跨多个法人运行。 此过程显示如何设置和运行多个法人的过程。 它为 USMF 法人实体使用会计角色和演示数据。


## <a name="set-up-cross-company-depreciation-run-journals"></a>设置跨公司折旧运行日记帐
1. 转到固定资产>设置>固定资产参数。
2. 展开“固定资产方案”部分。
3. 单击“添加”。
4. 在“过帐层”字段中，输入或选择一个值。
5. 在“日记帐名称”字段中，输入或选择一个值。
    * 在每个法人中的固定资产参数页面上重复日记帐设置。  

## <a name="depreciation-run"></a>折旧运行
1. 转到“固定资产”>“日记帐条目”>“创建折旧方案”。
2. 在“过帐层”字段中，输入或选择一个值。
    * 日记帐名称默认来自固定资产参数。 当前法人的日记帐名称可以在此处更改。  
3. 在“结束日期”字段中输入日期。
    * 选择要包括在折旧运行中的法人。  
    * 仅具有在固定资产参数页面为固定资产方案设置的日记帐的法人才会在列表中显示。  
4. 在“过帐日记帐”字段中选择“是”。
    * 筛选字段包括为此折旧运行选择的法人的所有固定资产、组和帐簿。  
    * “批处理”选项默认情况下启用。 启用此选项后，折旧日记帐创建和过帐将在后台运行。  
5. 单击“创建日记帐”。
6. 转到固定资产>流水输入项>固定资产流水。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]