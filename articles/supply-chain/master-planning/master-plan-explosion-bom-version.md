---
title: 物料清单版本的分解
description: 本文介绍涉及物料清单 (BOM) 版本分解的主计划方案。
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f3c800d96805df38a2e31018f2d6c305e3ed7da
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564569"
---
# <a name="explosion-of-a-bom-version"></a>物料清单版本的分解

[!include [banner](../includes/banner.md)]

本文介绍涉及物料清单 (BOM) 版本分解的主计划方案。

某一物料清单版本的需求分解将创建在特定站点以及可能在特定仓库的每个物料清单行物料的需求。 在特定于站点的物料清单中，可为每一物料清单行定义特定的仓库。 此外，对于每个物料清单行，该物料的维度设置将确定该仓库是否是必需的。 然后，为每一物料清单行物料产生的这一需求将成为其他需求分解的起始点。 此主计划方案涉及以下情况：

-   站点维度是必填的，必须在需求交易记录上输入。
-   站点维度是一致的。 因此，较低级别需求的站点与初始需求交易记录上的站点相同。

下图显示主计划编制需求分解的过程。 ![使用物料清单版本的需求分解](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>其他资源
--------

[主计划 - 如何确定物料清单版本](master-plan-bom-version-determined.md)

[主计划和多站点功能](master-plan-multisite-functionality.md)



