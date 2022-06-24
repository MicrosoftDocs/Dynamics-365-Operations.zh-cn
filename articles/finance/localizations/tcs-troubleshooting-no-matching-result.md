---
title: 找不到匹配的结果
description: 本文介绍如何排查税款计算服务中的“找不到匹配结果”错误。
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: d3bbc76741fdd018d1b2987538b8de7f6d92ee53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845135"
---
# <a name="no-matching-result-could-be-found"></a>找不到匹配的结果

[!include [banner](../includes/banner.md)]

本文介绍了在税款计算服务中收到“找不到匹配结果”错误时可以采取的故障排除步骤。

## <a name="symptom"></a>问题

您会收到以下错误消息：“标题/行 - 1，税组，找不到匹配的结果。”

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>原因

当 Regulatory Configuration Service (RCS) 中的功能设置不正确时会出现此问题。

## <a name="troubleshoot"></a>故障排除

1. 下载故障排除文件。 有关详细信息，请参阅[启用调试模式以进行故障排除](tcs-troubleshooting-enable-debug-mode.md)。
2. 将税务服务计算输入与功能设置进行比较以修复设置问题。

    以下示例显示税务服务计算输入。

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    下表列出了 RCS 中的税组适用性。

    | 标题。业务流程 | 行。业务单位 | 标题。发货方邮政编码 | 税组 |
    |-------------------------|---------------------|---------------------------|-----------|
    | 日记帐                 |                     |                           | 组 A   |
    | 销售额                   |                     | 30160                     | 组 B   |

    根据税务服务计算输入，**标题上的业务流程值** 为 **销售**，标题上的 **发货邮政编码** 值为 **30159**。 此输入基于 RCS 中的适用性规则的设置。 由于没有匹配的行，因此出错。

    > [!NOTE]
    > 如果适用性规则中的值为空，则该规则适用于任何值。

## <a name="mitigation"></a>减轻

请按照以下步骤减轻错误。

1. 在 RCS 中，转到 **全球化功能** \> **税务计算**。
2. 创建新版本的功能。
3. 为相应的信息添加一行。

    | 标题。业务流程 | 行。业务单位 | 标题。发货方邮政编码| 税组 |
    |-------------------------|---------------------|--------------------------|-----------|
    | 日记帐                 |                     |                          | 组 A   |
    | 销售额                   |                     | 30160                    | 组 B   |
    | 销售额                   |                     | 30159                    | 组 B   |

4. 发布功能设置版本。
5. 在 Microsoft Dynamics 365 Finance 中，转到 **税务** \> **设置** \> **税务配置** \> **税款计算参数**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
