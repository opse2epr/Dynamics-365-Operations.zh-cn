---
title: 创建批处理作业
description: 批处理作业是提交到某一应用程序对象服务器 (AOS) 实例以供自动处理的一组任务。
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562873"
---
# <a name="create-a-batch-job"></a>创建批处理作业

[!include [task guide banner](../../includes/task-guide-banner.md)]

批处理作业是提交到某一应用程序对象服务器 (AOS) 实例以供自动处理的一组任务。 通过使用创建了该作业的用户的安全凭据来运行批处理作业。 使用以下过程来创建批处理作业。 创建此程序的演示数据公司是 USMF。


## <a name="create-the-batch-job"></a>创建批处理作业
1. 转到“系统管理”>“查询”>“批处理作业”。
2. 单击“新建”。
3. 在“作业描述”字段中，键入一个值。
4. 在“计划开始日期/时间”字段中，输入日期和时间。
5. 单击“保存”。

## <a name="create-a-recurrence"></a>创建重复执行
1. 在操作窗格上，单击“批处理作业”。
2. 单击“重复执行”。
    * 使用这些选项输入一个重复执行的范围和模式。  
3. 单击“确定”。

## <a name="add-alerts"></a>添加预警
1. 在操作窗格上，单击“批处理作业”。
2. 单击“预警”。
    * 指示批处理作业结束，出错或取消时是否希望发送预警消息。 然后指定是否要将预警显示为弹出消息。   
3. 单击“确定”。

