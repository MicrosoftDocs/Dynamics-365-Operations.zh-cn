---
title: "零售考勤管理"
description: "此主题描述用于时间和出勤管理在 Microsoft Dynamics 365 的中支持零售操作的节点-的方案。"
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eac0b85a17df33c860333c5c19d4fb58f160930f
ms.lasthandoff: 03/31/2017


---

# <a name="retail-time-and-attendance"></a>零售考勤管理

此主题描述用于时间和出勤管理在 Microsoft Dynamics 365 的中支持零售操作的节点-的方案。 

<a name="manage-worker-setup-and-scheduling"></a>管理工作人员设置和计划
----------------------------------

### <a name="initial-configuration"></a>初始配置

-   运行配置向导。
-   将工作人员登记为时间登记工作人员。

### <a name="plan-worker-schedules"></a>计划工作人员计划

-   使用工作进度表应用模板。 有关详细信息，请参阅 <https://technet.microsoft.com/en-us/library/aa551234.aspx>。

有关配置步骤的信息，请参阅 <https://technet.microsoft.com/en-us/library/aa496971.aspx>。

### <a name="retail-specific-configuration"></a>零售特定配置

-   为您要启用时间登记的工作人员启用打卡时间的功能配置文件。 **单击 POS 功能配置文件** &gt; ** POS 功能** &gt; **时间登记** &gt; ** **启动时间登记。
-   配置销售点 (POS) 权限组以启用查看打卡时间条目权限。 此权限允许用户查看商店中其他工作人员的打卡时间登记（以及用户与其关联的任何其他商店，通过通讯簿）。 您可能要为经理角色启用此权限，但不为出纳员角色启用。 **单击 POS 权限组** &gt; **查看时钟**条目。

## <a name="register-time"></a>登记时间
### <a name="cashier-and-non-cashier-time-registrations"></a>出纳员和非出纳员时间登记

-   在 POS 上：
    -   上班打卡操作：
        -   登录非银箱操作或新班次。
        -   选择打卡时间操作。
        -   选择所需操作：
            -   上班打卡
            -   工间休息
            -   午餐休息
            -   下班打卡

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>当前状态</th>
    <th>可用操作</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>上班打卡</td>
    <td><ul>
    <li>工间休息</li>
    <li>午餐休息</li>
    <li>下班打卡</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>工间休息</td>
    <td>上班打卡</td>
    </tr>
    <tr class="odd">
    <td>午餐休息</td>
    <td>上班打卡</td>
    </tr>
    <tr class="even">
    <td>下班打卡</td>
    <td>上班打卡</td>
    </tr>
    </tbody>
    </table>

    [] (![TimeClockStates。/media/timeclockstates.png)](。/media/timeclockstates.png)
-   查看确认消息，验证当前活动时间是否正确。
-   日志：
    -   单击**日志**查看打卡时间活动。
    -   使用时间筛选器可选择不同的时间范围。
    -   如果您在多个商店位置工作，可以查看您在那里记录时间的所有商店的时间登记。 可以使用商店筛选器查看所选商店的时间登记。

<!-- -->

-   不同时区：
    -   如果您从不同位置查看时间（用于出纳员日志，或为经理方案使用**查看打卡时间条目**），并且该位置在不同的时区，您看到的时间记录将转换为您本地的时区。 例如，您是两个商店。其中，一个在亚利桑那和其他一位经理。内华达。 出纳在上午 9:00 登记上班打卡 在亚利桑那。 此时，该时间是内华达的上午 8:00。 因此，如果您是在内华达商店并查看时间登记记录，时间登记标记为上午 8 点。

## <a name="view-worker-time-registrations"></a>查看工作人员时间登记
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>查看工作人员时间登记，并按商店或活动类型筛选

在 POS 上：

-   选择**查看打卡时间条目**。
-   您看到分配到您被分配的同一商店的所有工作人员的打卡时间登记活动。
-   您可以使用活动类型和商店筛选器筛选时间登记。

## <a name="process-and-manage-time-registrations"></a>流程和管理工时登记
工序的 Dynamics 365 -零售用户按照工作流审核计算，并且将传送时间登记到工资单。

### <a name="primary-operations"></a>主要操作

-   计算
-   批准
-   提交到工资单

### <a name="other-common-operations"></a>其他常用操作

-   批量下班打卡
-   登记缺勤

有关如何处理时间和出勤登记的详细信息，请参阅 <https://technet.microsoft.com/en-us/library/aa573180.aspx>。


