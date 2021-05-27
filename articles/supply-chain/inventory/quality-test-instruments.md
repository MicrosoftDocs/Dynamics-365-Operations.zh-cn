---
title: 质量管理测试仪器
description: 本主题介绍如何创建可用于在 Microsoft Dynamics 365 Supply Chain Management 中对质检订单进行测试的测试仪器。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3806ca26b8909b03768dad54ddad0084e1cea4a6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021724"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="f3d4b-103">质量管理测试仪器</span><span class="sxs-lookup"><span data-stu-id="f3d4b-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3d4b-104">本主题介绍如何创建可用于在 Microsoft Dynamics 365 Supply Chain Management 中对质检订单进行测试的测试仪器。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="f3d4b-105">您将使用 **测试仪器** 页定义和查看有关用于对质检订单执行测试的设备的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="f3d4b-106">测试仪器是可选的。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-106">Test instruments are optional.</span></span> <span data-ttu-id="f3d4b-107">但是，它们可以帮助质量工作人员了解应该使用哪个设备或工具来执行特定测试。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="f3d4b-108">测试仪器示例</span><span class="sxs-lookup"><span data-stu-id="f3d4b-108">Test instrument example</span></span>

<span data-ttu-id="f3d4b-109">您在对电气组件执行各项测试。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="f3d4b-110">部分测试针对组件的电压输出，一项测试针对温度，另一项针对重量。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="f3d4b-111">每项测试使用不同的工具或设备来执行。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="f3d4b-112">例如，电压表用于测量电压，温度计用于测量温度，天平用于测量重量。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="f3d4b-113">您可以将这些设备中的每一个配置为一个测试仪器，并指明记录测试结果应使用的度量单位。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="f3d4b-114">例如，电压表得出的结果以伏特为单位记录，温度计得出的结果以华氏度或摄氏度为单位记录，天平得出的结果以磅或千克为单位记录。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="f3d4b-115">创建测试仪器</span><span class="sxs-lookup"><span data-stu-id="f3d4b-115">Create a test instrument</span></span>

1. <span data-ttu-id="f3d4b-116">转到 **库存管理 \> 设置 \> 质量控制 \> 测试仪器**。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="f3d4b-117">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="f3d4b-118">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f3d4b-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f3d4b-119">**测试仪器** – 为测试仪器输入唯一 ID 或名称。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="f3d4b-120">**描述** – 输入测试仪器的详细描述。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="f3d4b-121">**单位** – 选择仪器测量结果使用的单位。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="f3d4b-122">**精度** 字段将根据您选择的单位自动设置。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="f3d4b-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f3d4b-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3d4b-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="f3d4b-124">Additional resources</span></span>

- [<span data-ttu-id="f3d4b-125">质量管理测试</span><span class="sxs-lookup"><span data-stu-id="f3d4b-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="f3d4b-126">质量管理测试组</span><span class="sxs-lookup"><span data-stu-id="f3d4b-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
