---
title: 电子申报示例供应商支票
description: 此主题提供有关如何使用电子申报示例支票格式的一般信息。
author: ShylaThompson
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a48a20939b346b2d8536128107a730761b13f71c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820705"
---
# <a name="electronic-reporting-sample-vendor-checks"></a><span data-ttu-id="1f4fc-103">电子申报示例供应商支票</span><span class="sxs-lookup"><span data-stu-id="1f4fc-103">Electronic reporting sample vendor checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f4fc-104">您可以使用电子申报 (ER) 来确定供应商支票格式。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-104">You can use Electronic reporting (ER) to format vendor checks.</span></span> <span data-ttu-id="1f4fc-105">市场上提供许多银行和支票提供商特定的支票格式。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-105">Many bank-specific and check provider–specific check formats are available on the market.</span></span> <span data-ttu-id="1f4fc-106">ER 工具库中的付款支票模型已经包含示例支票格式。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-106">Sample check formats have been included in the Payment check model in the ER tool repository.</span></span> <span data-ttu-id="1f4fc-107">这些示例支票标记为 **支票在中间（美国）** 和 **支票在上面，存根在下面（美国）**。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-107">These sample checks are labeled **Check in the middle (US)** and **Check on top stub below (US)**.</span></span>

## <a name="what-check-formats-are-currently-supported"></a><span data-ttu-id="1f4fc-108">目前支持哪些支票格式？</span><span class="sxs-lookup"><span data-stu-id="1f4fc-108">What check formats are currently supported?</span></span>

<span data-ttu-id="1f4fc-109">应始终转至 Microsoft Dynamics Lifecycle Services (LCS) 中的共享资产库，并查看资产类型为 **GER 配置** 的可用文件的当前列表。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-109">You should always go to the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) and view the current list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="1f4fc-110">下一部分“必须执行哪些设置？”包括一个主题的链接，该主题说明如何创建 LCS 存储库以检查可用配置和导入所选配置。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-110">The next section, “What do I have to set up?,” includes a link to a topic that explains how to create an LCS repository so that you can review available configurations and import selected configurations.</span></span>

<span data-ttu-id="1f4fc-111">Microsoft Dynamics 365 Finance 包括一个示例格式，其中支票位于顶部，后面是两个汇款部分。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-111">Microsoft Dynamics 365 Finance includes a sample format where the check is on top, followed by two remittance sections.</span></span> <span data-ttu-id="1f4fc-112">它还包括一个示例格式，其中支票在中间，后面是两个汇款部分。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-112">It also includes a sample format where the check is in the middle, between two remittance sections.</span></span> <span data-ttu-id="1f4fc-113">这些示例格式对应于 Deluxe 公司支票格式。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-113">These sample formats correspond to Deluxe business checks formats.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="1f4fc-114">我必须设置什么？</span><span class="sxs-lookup"><span data-stu-id="1f4fc-114">What do I have to set up?</span></span>

- <span data-ttu-id="1f4fc-115">在您可以使用 ER 打印支票前，必须导入至少一个有效的支票配置到您的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-115">Before you can print checks by using ER, at least one active check configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="1f4fc-116">有关说明，请参阅[从 Lifecycle Services 下载电子申报配置](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-116">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
- <span data-ttu-id="1f4fc-117">为银行帐户配置现金和银行管理支票时，选择 **一般电子导出格式** 复选框，然后选择相应的支票格式作为导出格式配置。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-117">When you configure Cash and bank management checks for the bank account, select the **Generic electronic Export format** check box, and then select the appropriate check format as an export format configuration.</span></span>
- <span data-ttu-id="1f4fc-118">您还必须指定汇款上要打印的清单行的数量。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-118">You must also specify the number of slip lines that will be printed on the remittance.</span></span> <span data-ttu-id="1f4fc-119">计算此数量时务必包括标头行。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-119">Be sure to include the header rows when you calculate this number.</span></span> <span data-ttu-id="1f4fc-120">对于这两种示例支票格式，建议的清单行数量为 17。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-120">For the two sample check formats, the recommended number of slip lines is 17.</span></span> <span data-ttu-id="1f4fc-121">但是，该数量将根据您的支票库存和打印机驱动程序而有所不同。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-121">However, this number will vary, depending on your check stock and your printer drivers.</span></span>
- <span data-ttu-id="1f4fc-122">我们建议您打印一份测试支票以验证支票版式。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-122">We recommend that you print a test check to validate the check layout.</span></span> <span data-ttu-id="1f4fc-123">若要测试打印支票，请选择 **打印测试** 选项。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-123">To print a test check, select the **Print test** option.</span></span> <span data-ttu-id="1f4fc-124">当 Microsoft Excel 的高级打印机属性中的 **边距** 设置为 **无** 时，示例支票格式的效果最佳。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-124">The sample check formats work best when **Margins** is set to **None** in the advanced printer properties for Microsoft Excel.</span></span> <span data-ttu-id="1f4fc-125">生成测试支票后，启用编辑 Excel 输出并配置页面布局，以便所有边距设置为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-125">After the test check has been generated, enable editing of the Excel output, and configure the page layout so that all margins are set to **0** (zero).</span></span> <span data-ttu-id="1f4fc-126">比较支票的测试副本与您的支票库存，并调整设置，直到您对对齐方式满意。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-126">Compare the test copy of the checks to your check stock, and adjust the settings until you're satisfied with the alignment.</span></span>
- <span data-ttu-id="1f4fc-127">为在付款日记帐中配置的银行帐户生成付款时，将使用指定的格式打印支票。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-127">When you generate payments for the configured bank account in the payment journal, the checks will be printed by using the specified format.</span></span>

<span data-ttu-id="1f4fc-128">有关详细信息，请参阅 [修改电子申报格式](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md)。</span><span class="sxs-lookup"><span data-stu-id="1f4fc-128">For more information, see [Modify an Electronic reporting format](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]