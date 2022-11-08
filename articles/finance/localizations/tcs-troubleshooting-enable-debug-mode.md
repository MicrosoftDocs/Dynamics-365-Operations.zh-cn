---
title: 在“税款计算”服务中启用调试模式
description: 本文介绍了如何在“税款计算”服务中启用调试模式以调查问题。
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 2bb381939ebe32cb51caf730cdd441557d83a4c0
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2022
ms.locfileid: "9620890"
---
# <a name="enable-debug-mode-in-the-tax-calculation-service"></a>在“税款计算”服务中启用调试模式

[!include [banner](../includes/banner.md)]

本文介绍了如何在“税款计算”服务中启用调试模式以调查问题。

1. 将 **&debug=vs%2CconfirmExit&** 添加到应用程序对象服务器 (AOS) 的 URL，然后刷新页面。
2. 选择 **销售税** 以计算销售税时，将打开名为 **TaxServiceTroubleshotingLog.txt** 的文本文件。 **TaxServiceTroubleshotingLog.txt** 文件包含 **TaxableDocument** 和计算参数。 这些结果是从税务服务和异常信息中返回的，用于进行故障排除。

## <a name="sample"></a>示例

```json
===============================Tax service calculation input JSON:=====================================
{
    "TaxableDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Transaction Line ID": "5816,68719677391",
            ...
            }
        ],
        "Transaction Header ID": "2022,68719506302",
        ...
        }
    ]
    },
    "Parameter": {
    "ContinueOnErrors": true,
    ...
    },
    "Adjustment": {
    "Lines": {}
    }
}
===========================Tax service calculation result JSON:=================================
{
    "taxDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Tax Codes": {
                ...
            }
        ],
        "Measures": {
            "List Code": "EUTrade"
        },
        "Tax Registration ID": null,
        "Transaction Header ID": "2022,68719506302",
        "Errors": null
        }
    ]
    },
    "solutionId": "b51e0025-cbbe-4d37-bf0b-90d7be4f214d|1",
    "isPartialSuccess": false
}
=============================CorrelationId:==============================
"21f3a8a1-ee9a-477b-b44e-b8ec79e74d16"
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
