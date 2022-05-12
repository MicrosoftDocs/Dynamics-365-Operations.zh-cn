---
title: 无法确定税码
description: 本主题说明如何排查税款计算服务中的“无法确定税码”错误。
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
ms.openlocfilehash: 3c0914f0013ad2de61cd5a59e3092fef149742e4
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645378"
---
# <a name="tax-code-cannot-be-determined"></a>无法确定税码

[!include [banner](../includes/banner.md)]

本主题介绍了在税款计算服务中收到“无法确定税码”错误时可以采取的故障排除步骤。

## <a name="symptom"></a>问题

您收到以下错误消息：“标题/行 - 1，无法确定税码。” 或者，您可以在故障排除文件中找到错误，如以下示例所示。 有关详细信息，请参阅[启用调试模式以进行故障排除](tcs-troubleshooting-enable-debug-mode.md)。

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
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
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

出现此问题的原因可能是税组和物料税组不相交。

## <a name="troubleshoot"></a>故障排除

请按照以下步骤解决此问题。

1. 在故障排除文件中，验证是否已确定税组和物料税组。 如果 **税组** 和 **物料税组** 的值为空，则尚未确定税组和物料税组。 如果已确定这些内容，则结果可能不正确。

    以下是故障排除文件的示例。

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
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

2. 验证是否已启用销售订单行详细信息的 **设置** 选项卡上的 **覆盖销售税** 选项。

    - 如果已启用，则税码由您在交易行上输入的 **税组** 和 **物料税组** 值来确定。 请验证是否正确输入了这些值。
    - 如果未启用它，请验证是否已为 **税务组适用性** 和 **物料税组适用性** 字段设置了正确的值。 有关详细信息，请参阅[找不到匹配的结果](tcs-troubleshooting-no-matching-result.md)。

3. 如果已正确确定税组和物料税组，则确定他们是否存在任何交集。

    1. 在 RCS 中，转到 **税务功能** \> **税码和组** \> **税组**。

        | 行。税组 | 税码 |
        |----------------|-----------|
        | 组 A        | A         |

    2. 转到 **税务功能** \> **税码和组** \> **物料税组**。

        | 行。物料税组 | 税码 |
        |---------------------|-----------|
        | 组 B             | B         |

    如果税组和物料税组没有交集，则无法确定税码。

## <a name="mitigation"></a>减轻

1. 浏览此主题的[疑难解答](#troubleshoot)部分中的每个步骤，并根据需要修复设置。 如果未正确确定税组和物料税组，请参阅[未找到匹配结果](tcs-troubleshooting-no-matching-result.md)。
2. 如果税组和物料税组没有交集，请在 RCS 中创建新功能版本，并修复设置。

    - 转到 **税务功能** \> **税码和组** > **物料税组**。

        | 行。物料税组 | 税码 |
        |---------------------|-----------|
        | 组 B             | A；B       |

    税码将确定为 **A**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
