---
title: 使用阶段原因代码
description: 使用原因代码指示服务级别协议 (SLA) 已取消的原因，或者服务订单超出您在 SLA 中定义的时限的原因。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 220012011e6fb1818cffa3992a3c39f46e5c071a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259618"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="f166f-103">使用阶段原因代码</span><span class="sxs-lookup"><span data-stu-id="f166f-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f166f-104">使用原因代码指示服务级别协议 (SLA) 已取消的原因，或者服务订单超出您在 SLA 中定义的时限的原因。</span><span class="sxs-lookup"><span data-stu-id="f166f-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="f166f-105">您还可以指定在 SLA 取消时要求的原因代码，或者时限超出您在 SLA 中为服务订单指定的时间时的原因代码。</span><span class="sxs-lookup"><span data-stu-id="f166f-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="f166f-106">如果已指定要求的原因代码，则必须在以下情况中输入原因代码：</span><span class="sxs-lookup"><span data-stu-id="f166f-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="f166f-107">当服务订单移到根据该服务订单 SLA 停止时间记录的阶段。</span><span class="sxs-lookup"><span data-stu-id="f166f-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="f166f-108">在服务订单通过验证时。</span><span class="sxs-lookup"><span data-stu-id="f166f-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="f166f-109">时间记录手动停止时。</span><span class="sxs-lookup"><span data-stu-id="f166f-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="f166f-110">设置原因代码</span><span class="sxs-lookup"><span data-stu-id="f166f-110">Set up reason codes</span></span>

1.  <span data-ttu-id="f166f-111">单击 **服务管理** \> **设置** \> **服务订单** \> **阶段原因代码**。</span><span class="sxs-lookup"><span data-stu-id="f166f-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="f166f-112">在 **阶段原因代码** 窗体中，单击 **新建** 以新建原因代码。</span><span class="sxs-lookup"><span data-stu-id="f166f-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="f166f-113">在 **阶段原因代码** 字段中，输入唯一的阶段原因代码。</span><span class="sxs-lookup"><span data-stu-id="f166f-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="f166f-114">在 **说明** 字段中，输入阶段原因代码的描述。</span><span class="sxs-lookup"><span data-stu-id="f166f-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="f166f-115">关闭窗体以保存您所做更改。</span><span class="sxs-lookup"><span data-stu-id="f166f-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="f166f-116">在取消服务级别协议时要求提供原因代码</span><span class="sxs-lookup"><span data-stu-id="f166f-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="f166f-117">单击 **服务管理** \> **设置**\> **服务管理参数**。</span><span class="sxs-lookup"><span data-stu-id="f166f-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="f166f-118">在 **服务管理参数** 窗体中，单击 **常规** 链接，然后选中 **取消的原因代码** 复选框。</span><span class="sxs-lookup"><span data-stu-id="f166f-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="f166f-119">在服务订单超出服务级别协议设置的时限时需要原因代码。</span><span class="sxs-lookup"><span data-stu-id="f166f-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="f166f-120">单击 **服务管理** \> **设置**\> **服务管理参数**。</span><span class="sxs-lookup"><span data-stu-id="f166f-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="f166f-121">在 **服务管理参数** 窗体中，单击 **常规** 链接，然后选中 **超过时间的原因代码** 复选框。</span><span class="sxs-lookup"><span data-stu-id="f166f-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="f166f-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="f166f-122">See also</span></span>

[<span data-ttu-id="f166f-123">开始和停止针对服务订单的时间录制</span><span class="sxs-lookup"><span data-stu-id="f166f-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]