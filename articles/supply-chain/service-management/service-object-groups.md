---
title: 服务对象组
description: 对象组有用于排序和筛选有关报告和统计对象的数据。
author: sorenva
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53d51e4165797b176cfe70a8e25311e41d2999e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674748"
---
# <a name="service-object-groups"></a>服务对象组

[!include [banner](../includes/banner.md)]

对象组有用于排序和筛选有关报告和统计对象的数据。 例如，您可以按地理位置或按类型对对象进行分组。

## <a name="group-by-geographical-location"></a>按地理位置分组

您可以使用此分组方法来显示您的公司服务定位的各种不同对象的位置。 例如，如果您必须标识在特定国家/地区或区域的您的公司已为其提供服务的对象，则按地理位置对对象进行分组也是有用的。

## <a name="example-of-grouping-by-geographical-location"></a>按地理位置分组的示例

比利时的一位客户向您的呼叫中心致电，希望为对象 ABC 创建一个服务协议。 您已将地理位置为比利时的对象组附加到比利时中服务的所有对象。 通过使用此组作为筛选器，您可以快速搜索以查看您是否以在计划中拥有 ABC 记录，或您是否必须设置一个新对象。

## <a name="group-by-type"></a>按类型分组

您可以使用此分组方法以显示您的公司服务的对象的类型。 例如，如果您要基于已存在于计划中的类似对象来创建新对象，则按类型对对象进行分组也会很有用。

## <a name="example-of-grouping-by-type"></a>按类型分组的示例

一个客户致电并想要为空调机器 HIJ 设置一个服务协议。 您还没有此机器的记录。 但是，您设置了名为“空调”的对象组，而且您已将此组附加到了所有空调对象。 因此，您可以快速搜索并标识所有其他空调器并使用来自这些对象的模板信息以为 HIJ 创建服务协议行。 通过以这种方式使用对象组，您可以迅速设置新对象并确定必须在这些对象上执行的服务任务。

## <a name="create-service-object-groups"></a>创建服务对象组

创建可将服务对象分配给的组。 服务对象是执行服务的库存物料和其他产品。 通过对服务对象分组，您可以为类似和相关服务对象创建报表。 例如，服务对象组中可包括两个服务对象：一个服务对象是配套件，第二个服务对象是安装配套件的服务。

若要创建服务对象组，请执行以下步骤：

1. 单击 **服务管理 > 设置 > 服务对象 > 服务对象组**。

2. 单击 **新建** 创建一个新的服务对象组。

3. 为该服务对象组输入唯一名称和描述（可选）。

通过使用 **服务对象** 窗体，您可以将服务对象分配给组。 

## <a name="see-also"></a>请参阅

[创建服务对象](create-service-objects.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]