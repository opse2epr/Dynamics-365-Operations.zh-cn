--- 
title: "恢复看板作业状态"
description: "该过程用于恢复一个不正确的看板作业状态。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 00b6ae872e60a322c994420ab69236abef7fb312
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="revert-kanban-job-status"></a>恢复看板作业状态

[!include[task guide banner](../../includes/task-guide-banner.md)]

该过程用于恢复一个不正确的看板作业状态。 此用于机器操作员更新错误作业或设置错误状态的情况。 在该过程中，先把一项看板作业错误登记为已准备，然后恢复其状态。 创建此程序的演示数据公司是 USMF。 该过程是为在 lean manufacturing 公司工作的店铺主管或机器操作员设计的。


## <a name="open-process-board-for-the-work-cell"></a>打开该工作单元的流程面板
1. 转到“处理作业的看板面板”。
2. 在“工作单元”字段中，输入或者选择一个值。
    * 选择工作单元 1260。  

## <a name="prepare-kanban-job"></a>准备看板作业
1. 单击“准备”。
    * 若无法单击“准备”是因为其显示为灰色，请确保所选看板作业的状态为“已计划”（以空看板图标表示）。 如果“准备”失败，请确保“领料单”上的所有材料为可用。  
2. 在此列表中，选择已准备作业。
    * 选择您已准备的第一个作业。  
    * 请注意，作业状态为“已准备”，以看板图标内的三角形表示。  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>恢复该已准备的看板作业的状态
1. 在列表中，标记所选的行。
    * 选择您准备好的第一个作业。  
2. 在“操作窗格”上单击“制造”。
3. 单击“恢复状态”。
    * 如果发生以下情况，您可以使用另一看板规则：- 两个规则的补货策略一致。  - 两个规则的生产流版本一样。  - 两个规则的产品供应相同。  - 两个规则的的任意下游活动必须相同，这些活动决定该看板规则的最后一项活动。  - 两个规则所设置的供应库存维度必须相同。  - 搬运单元状态必须为“未分配”。  - 事件看板的设置必须相同。  
    * 确认该新状态为“已计划”。  
4. 单击“确定”。
5. 在列表中，取消标记所选的行。
    * 选择相同作业。  
    * 请注意，该看板作业的作业状态已恢复为“已计划”（以空看板图标表示）。  

