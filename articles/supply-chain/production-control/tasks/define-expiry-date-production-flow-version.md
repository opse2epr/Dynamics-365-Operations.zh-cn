---
title: 定义生产流版本的到期日期
description: 若要在给定日期终止某个生产流版本的有效性和处理，或计划将某个有效版本替换为新版本，必须为该版本设置到期日期。
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa0bde90273f9392a36732ed79afdad2eea8bf86
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573203"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>定义生产流版本的到期日期

[!include [task guide banner](../../includes/task-guide-banner.md)]

若要在给定日期终止某个生产流版本的有效性和处理，或计划将某个有效版本替换为新版本，必须为该版本设置到期日期。 不必停用该版本。


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a>设置到期日期以结束生产流版本
1. 转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。
2. 在列表中，找到并选择所需记录。
    * 选择已为其定义了版本的任何生产流。  
3. 在列表中，单击所选行中的链接。
4. 单击“编辑”。
5. 在列表中，标记所选的行。
6. 在“到期日期”字段中，输入日期和时间。
    * 对于到期日期，新版本将不启动或进入已激活状态。 并且还不能为此生产流创建或启动作业。 到期日期后，仍然可以完成已开始的作业。  

