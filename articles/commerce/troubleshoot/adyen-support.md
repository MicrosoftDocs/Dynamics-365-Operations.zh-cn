---
title: 解决适用于 Adyen 的 Dynamics 365 付款连接器问题
description: 本主题提供了疑难解答指南，当您遇到适用于 Adyen 的 Microsoft Dynamics 365 付款连接器问题，此指南可以帮助您获得支持。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c779997d530d60f945bee19ee09bdabbff121fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801811"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="50b37-103">解决适用于 Adyen 的 Dynamics 365 付款连接器问题</span><span class="sxs-lookup"><span data-stu-id="50b37-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50b37-104">本主题提供了疑难解答指南，当您遇到适用于 Adyen 的 Microsoft Dynamics 365 付款连接器问题，此指南可以帮助您获得支持。</span><span class="sxs-lookup"><span data-stu-id="50b37-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="50b37-105">说明</span><span class="sxs-lookup"><span data-stu-id="50b37-105">Description</span></span>

<span data-ttu-id="50b37-106">在以下方面，您遇到有关适用于 Adyen 的 Dynamics 365 付款连接器 的问题，并且需要 Adyen 团队的支持：</span><span class="sxs-lookup"><span data-stu-id="50b37-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="50b37-107">销售点 (POS)、现代销售点 (MPOS)、呼叫中心或 Dynamics 365 Commerce 的配置</span><span class="sxs-lookup"><span data-stu-id="50b37-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="50b37-108">Adyen 付款服务提供商 (PSP) 参考号（例如，如果您对拒绝有疑问，包括手动关键条目 \[MKE\] 拒绝）</span><span class="sxs-lookup"><span data-stu-id="50b37-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="50b37-109">在测试或实时商家环境中无法正常工作的所有项</span><span class="sxs-lookup"><span data-stu-id="50b37-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="50b37-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="50b37-110">Resolution</span></span>

<span data-ttu-id="50b37-111">使用以下电子邮件模板开始执行 Adyen 团队支持流程。</span><span class="sxs-lookup"><span data-stu-id="50b37-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="50b37-112">为了加快故障排除速度，请确保电子邮件包含所有必需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="50b37-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="50b37-113">字段</span><span class="sxs-lookup"><span data-stu-id="50b37-113">Field</span></span>        | <span data-ttu-id="50b37-114">值</span><span class="sxs-lookup"><span data-stu-id="50b37-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="50b37-115">结束日期</span><span class="sxs-lookup"><span data-stu-id="50b37-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="50b37-116">抄送</span><span class="sxs-lookup"><span data-stu-id="50b37-116">Cc</span></span>           | |
| <span data-ttu-id="50b37-117">主题行</span><span class="sxs-lookup"><span data-stu-id="50b37-117">Subject line</span></span> | <span data-ttu-id="50b37-118">Microsoft Dynamics 支持请求</span><span class="sxs-lookup"><span data-stu-id="50b37-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="50b37-119">正文</span><span class="sxs-lookup"><span data-stu-id="50b37-119">Body</span></span>         | <p><span data-ttu-id="50b37-120">支持人员，你好：</span><span class="sxs-lookup"><span data-stu-id="50b37-120">Hi Support,</span></span></p><p><span data-ttu-id="50b37-121">请对以下问题提供支持：</span><span class="sxs-lookup"><span data-stu-id="50b37-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="50b37-122">商户帐户</span><span class="sxs-lookup"><span data-stu-id="50b37-122">Merchant account</span></span></li><li><span data-ttu-id="50b37-123">环境（测试/生产）</span><span class="sxs-lookup"><span data-stu-id="50b37-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="50b37-124">渠道（POS/呼叫中心/Commerce 电子商务）</span><span class="sxs-lookup"><span data-stu-id="50b37-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="50b37-125">PSP 参考号（如果问题涉及特定交易）（您可以在收据上、在 Adyen 客户区域中或在 POS 终端的交易菜单上找到 PSP 参考号。）</span><span class="sxs-lookup"><span data-stu-id="50b37-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="50b37-126">错误消息的屏幕截图或照片（如适用）</span><span class="sxs-lookup"><span data-stu-id="50b37-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="50b37-127">事件查看器日志（.txt 格式）</span><span class="sxs-lookup"><span data-stu-id="50b37-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="50b37-128">问题说明和尝试的故障排除步骤</span><span class="sxs-lookup"><span data-stu-id="50b37-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="50b37-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="50b37-129">Additional resources</span></span>

[<span data-ttu-id="50b37-130">使用适用于 Dynamics 365 Commerce 的 Adyen 连接器接受付款</span><span class="sxs-lookup"><span data-stu-id="50b37-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="50b37-131">适用于 Adyen 的 Dynamics 365 付款连接器</span><span class="sxs-lookup"><span data-stu-id="50b37-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="50b37-132">设置适用于 Dynamics 365 的 Adyen 付款连接器</span><span class="sxs-lookup"><span data-stu-id="50b37-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
