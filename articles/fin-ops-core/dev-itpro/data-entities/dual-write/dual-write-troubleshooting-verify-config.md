---
title: 验证 Finance and Operations 应用和 Dataverse 中的双写入配置
description: 本主题说明如何确定在 Finance and Operations 应用和 Dataverse 中是否配置了双写入。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 361d6555b60e02832c337b6f416b2b3627b6d365
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129299"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="b76bd-103">验证 Finance and Operations 应用和 Dataverse 中的双写入配置</span><span class="sxs-lookup"><span data-stu-id="b76bd-103">Verify dual-write configuration in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="b76bd-104">本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="b76bd-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="b76bd-105">具体来说，说明如何确定在 Finance and Operations 应用和 Dataverse 中是否配置了双写入。</span><span class="sxs-lookup"><span data-stu-id="b76bd-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="b76bd-106">验证 Finance and Operations 应用中是否配置了双写入</span><span class="sxs-lookup"><span data-stu-id="b76bd-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="b76bd-107">若要确定您尝试保存行以进行更新时看到的错误是否来自双写入，请首先验证是否配置了双写入。</span><span class="sxs-lookup"><span data-stu-id="b76bd-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="b76bd-108">如果您在 Finance and Operations 应用中有管理员权限，请转到 **工作区 \> 数据管理**，然后选择 **双写入** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="b76bd-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="b76bd-109">如果显示了链接环境的详细信息以及正在运行的表映射的列表，则说明配置了双写入。</span><span class="sxs-lookup"><span data-stu-id="b76bd-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![验证具有管理员权限时 Finance and Operations 应用的连接](media/verify_fin_ops_1.png)

+ <span data-ttu-id="b76bd-111">如果您没有管理员权限，则会收到错误消息 *无法将数据写入实体 \<entity name\>*。</span><span class="sxs-lookup"><span data-stu-id="b76bd-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="b76bd-112">在下图的示例中，您无法在 Finance and Operations 应用中创建客户行，因为配置了双写入，但客户组和付款期限引用数据在 Dataverse 中不存在。</span><span class="sxs-lookup"><span data-stu-id="b76bd-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![验证没有管理员权限时 Finance and Operations 应用的连接](media/verify_fin_ops_2.png)

<span data-ttu-id="b76bd-114">有关如何解决在 Finance and Operations 应用中创建数据时出现的问题的信息，请参阅[解决实时同步问题](dual-write-troubleshooting-live-sync.md)。</span><span class="sxs-lookup"><span data-stu-id="b76bd-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="b76bd-115">验证 Dataverse 中是否配置了双写入</span><span class="sxs-lookup"><span data-stu-id="b76bd-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="b76bd-116">创建数据时，如果您在 Dataverse 中的页面上看到了 **公司** 列，则说明配置了双写入。</span><span class="sxs-lookup"><span data-stu-id="b76bd-116">When you create data, if you see the **Company** column on pages in Dataverse, dual-write is configured.</span></span>

![验证 Dataverse 连接](media/verify_cds.png)

<span data-ttu-id="b76bd-118">有关如何解决在 Dataverse 中创建数据时出现的问题的信息，请参阅[解决实时同步问题](dual-write-troubleshooting-live-sync.md)。</span><span class="sxs-lookup"><span data-stu-id="b76bd-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="b76bd-119">有关在 Dataverse 中创建数据的过程中遇到错误时如何查看错误详细信息的信息，请参阅[在 Dataverse 中启用和查看插件跟踪日志来查看错误详细信息](dual-write-troubleshooting.md#enable-view-trace)。</span><span class="sxs-lookup"><span data-stu-id="b76bd-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>
