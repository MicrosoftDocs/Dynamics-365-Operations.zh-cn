---
title: 验证 Finance and Operations 应用和 Common Data Service 中是否配置了双写入
description: 本主题说明如何确定在 Finance and Operations 应用和 Common Data Service 中是否配置了双写入。
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
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997222"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="43e9d-103">验证 Finance and Operations 应用和 Common Data Service 中是否配置了双写入</span><span class="sxs-lookup"><span data-stu-id="43e9d-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="43e9d-104">本主题提供 Finance and Operations 应用与 Common Data Service 之间的双写入集成的故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="43e9d-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="43e9d-105">具体来说，说明如何确定在 Finance and Operations 应用和 Common Data Service 中是否配置了双写入。</span><span class="sxs-lookup"><span data-stu-id="43e9d-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="43e9d-106">验证 Finance and Operations 应用中是否配置了双写入</span><span class="sxs-lookup"><span data-stu-id="43e9d-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="43e9d-107">若要确定您尝试保存记录以进行更新时看到的错误是否来自双写入，请首先验证是否配置了双写入。</span><span class="sxs-lookup"><span data-stu-id="43e9d-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="43e9d-108">如果您在 Finance and Operations 应用中有管理员权限，请转到 **工作区 \> 数据管理** ，然后选择 **双写入** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="43e9d-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management** , and select the **Dual-write** tile.</span></span> <span data-ttu-id="43e9d-109">如果显示了链接环境的详细信息以及正在运行的实体映射的列表，则说明配置了双写入。</span><span class="sxs-lookup"><span data-stu-id="43e9d-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![验证具有管理员权限时 Finance and Operations 应用的连接](media/verify_fin_ops_1.png)

+ <span data-ttu-id="43e9d-111">如果您没有管理员权限，则会收到错误消息 *无法将数据写入实体 \<entity name\>* 。</span><span class="sxs-lookup"><span data-stu-id="43e9d-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="43e9d-112">在下图的示例中，您无法在 Finance and Operations 应用中创建客户记录，因为配置了双写入，但客户组和付款期限引用数据在 Common Data Service 中不存在。</span><span class="sxs-lookup"><span data-stu-id="43e9d-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![验证没有管理员权限时 Finance and Operations 应用的连接](media/verify_fin_ops_2.png)

<span data-ttu-id="43e9d-114">有关如何解决在 Finance and Operations 应用中创建数据时出现的问题的信息，请参阅[解决实时同步问题](dual-write-troubleshooting-live-sync.md)。</span><span class="sxs-lookup"><span data-stu-id="43e9d-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="43e9d-115">验证 Common Data Service 中是否配置了双写入</span><span class="sxs-lookup"><span data-stu-id="43e9d-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="43e9d-116">创建数据时，如果您在 Common Data Service 中的页面上看到了 **公司** 字段，则说明配置了双写入。</span><span class="sxs-lookup"><span data-stu-id="43e9d-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![验证 Common Data Service 连接](media/verify_cds.png)

<span data-ttu-id="43e9d-118">有关如何解决在 Common Data Service 中创建数据时出现的问题的信息，请参阅[解决实时同步问题](dual-write-troubleshooting-live-sync.md)。</span><span class="sxs-lookup"><span data-stu-id="43e9d-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="43e9d-119">有关在 Common Data Service 中创建数据的过程中遇到错误时如何查看错误详细信息的信息，请参阅[在 Common Data Service 中启用和查看插件跟踪日志来查看错误详细信息](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details)。</span><span class="sxs-lookup"><span data-stu-id="43e9d-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>
