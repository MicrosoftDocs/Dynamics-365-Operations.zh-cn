---
title: 您不能使用已发布产品 V2 实体导入物料
description: 您不能使用已发布产品 V2 实体导入物料。
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026295"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="34cf8-103">您不能使用已发布产品 V2 实体导入物料</span><span class="sxs-lookup"><span data-stu-id="34cf8-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="34cf8-104">知识库编号：4611825</span><span class="sxs-lookup"><span data-stu-id="34cf8-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="34cf8-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="34cf8-105">Symptoms</span></span>

<span data-ttu-id="34cf8-106">当您尝试使用 *已发布产品 V2* 实体导入物料时，将收到类似于以下示例的错误消息：</span><span class="sxs-lookup"><span data-stu-id="34cf8-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="34cf8-107">无法在“物料 - 跟踪维度组”(EcoResTrackingDimensionGroupItem) 中创建记录。</span><span class="sxs-lookup"><span data-stu-id="34cf8-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="34cf8-108">物料编号：2040663，批。</span><span class="sxs-lookup"><span data-stu-id="34cf8-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="34cf8-109">该记录已存在。</span><span class="sxs-lookup"><span data-stu-id="34cf8-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="34cf8-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="34cf8-110">Resolution</span></span>

<span data-ttu-id="34cf8-111">要导入新的已发布产品，您必须使用 *已发布产品创建 V2* 实体而不是 *已发布产品 V2* 实体。</span><span class="sxs-lookup"><span data-stu-id="34cf8-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
