---
title: Dynamics 365 for Talent（2019 年 1 月 31 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d4504cebb7702c7163c94badeeb06d9af0e5467e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517392"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a>Dynamics 365 for Talent（2019 年 1 月 31 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

此主题介绍了 Dynamics 365 for Talent 中的新增功能和更改的功能

**内部版本 8.1.2128**

## <a name="core-hr-changes"></a>Core HR 更改

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>在休假人员卡上请下的休假不考虑休假计划日期
对于有在日历年不运行的休假计划的员工，**已请假**卡现在显示在计划定义的休假年中获得的休假。 例如，如果组织的休假年是 6 月 1 到 5 月 30 日，并且员工在 12 月获得了 3 天休假，1 月 15 日的**已请假**卡将显示 3 天。 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>应计金额与等级日期基础不匹配
已向休假和缺勤（**人力资源**参数）添加了新选项来允许客户确定员工的服务月日期何时有效。 对于某些组织，此日期是当月的月底，但对于其他组织，可能是下个月的月初。 例如，一个组织可能在 12 月 31 日奖励休假，而另一个组织则可能在 1 月 1 日奖励休假。 此选项允许您选择应在何时进行奖励。 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>工作人员雇用操作卡在“工作流已完成”状态
已进行更改来更正少数工作流的完成状态为“工作流已完成”的问题。 新工作流现在在工作流完成时应移到“已完成”状态。 工作流已完成状态的所有工作流都将转入错误状态以允许在需要时更新或删除。 
