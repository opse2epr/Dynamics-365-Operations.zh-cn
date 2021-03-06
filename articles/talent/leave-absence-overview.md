---
title: 休假和缺勤管理
description: 此主题提供休假和缺勤管理模块的概览。
author: andreabichsel
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebfaeb0696d7200ddf3c715f96a259b91db08e7a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517410"
---
# <a name="leave-and-absence-management"></a>休假和缺勤管理

[!include [banner](includes/banner.md)]

**休假爱喝缺勤管理**模块提供灵活的框架，用于定义缺勤管理流程。 可以创建休假和缺勤计划以确定员工累积假期或如何赠予休假。 员工在计划中登记后，可以提交休假申请供经理审批。 休假跟踪荣一线经理和人力资源 (HR) 经理都可以看到谁在休假，以及每位员工剩余的假期量。  

休假和缺勤管理提供以下功能： 

- **定义休假和缺勤类型。**

    休假类型定义员工可报告的各种缺勤类型。 由于这些类型由用户定义，所以可以根据组织进行调整。 典型休假类型包括带薪休假 (PTO)、休假、短期残疾、陪审员义务（这种休假类型特定于美国）和丧亡等。 

- **定义根据业务分层的休假和缺勤计划。**

    可以将休假和缺勤计划定义为按照特定频率（如年、月或半月）累积。 还可以将计划定义为赠予，这样就在特定日期累积一次。 

    休假计划中通常包含层，其中一些员工组根据其在组织中的时间享受更多福利。 这些用户定义的层允许根据定义的日期条件自动登记更多福利时数。 也可以配置休假计划以实施结转量或最小余额，以防员工使用的福利时数超过累积量。 

    典型休假计划中包含分层计划，这些分层计划为新员工赠予 80 小时的 PTO 福利，但是工作 60 个月后则赠予 120 小时的福利。 更多计划可能赠予浮动假期或基于职位的福利，如仅限管理层的福利时数。

- **单独或通过基于工作条件的批量分配为员工登记休假和缺勤计划。**

    可以使用若干基于工作的筛选器将一组员工分配给休假计划。 HR 经理可以查看员工以了解为其登记了哪些休假和缺勤计划。 HR 经理还可以查看所有计划和相关的员工登记情况。

- **暂停休假和缺勤计划。**

    可以暂停休假和缺勤计划，以使其进入静止状态并防止增加累积量。 如果员工的雇用结束，将暂停其累积。  

- **调整权利和赠予。**

    员工可以通过使用工作人员特定的日期覆盖其默认计划供应来在更高计划层中登记。 计划登记时，员工可以收到对其休假和缺勤余额的年度调整，HR 也可以随时进行年度调整。 

- **对休假请求应用工作流。**

     可以自定义工作流并应用于休假请求，以满足组织的要求。  

- **跟踪员工缺勤余额。**

    员工、其经理和 HR 可以查看休假和缺勤余额。 HR 可使用交互式报告按类型跟踪计划登记情况和休假余额。 

- **提交休假请求。**

    员工可针对其可用时数提交休假请求。 请求可以是简单的一天请求，也可以是包含多个休假和缺勤类型的多天请求。 如果不启用工作流，将自动批准请求。 如果启用工作流，可以自动执行审批，也可以要求签核，具体取决于工作流配置。
