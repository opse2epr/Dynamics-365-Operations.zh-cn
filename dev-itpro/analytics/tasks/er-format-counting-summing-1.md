--- 
title: "针对电子申报 (ER) 创建用于盘点和合计的格式"
description: "以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a52aade62b0d05a41e22aa9e9a474999af725606
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-formate-for-counting-and-summing-for-electronic-reporting-er"></a>针对电子申报 (ER) 创建用于盘点和合计的格式

[!include[task guide banner](../../includes/task-guide-banner.md)]

以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。 这些步骤可以在任何公司执行。

为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>访问 Microsoft 提供的配置列表
1. 转到“组织管理”>“工作区”>“电子申报”。
    * 确保“Litware 公司” 提供程序可用且标记为有效。  
2. 选择“Litware 公司” 提供程序。
3. 单击“存储库”。
    * 如果已存在“运营资源”的存储库，请跳过当前子任务的其余步骤。  
4. 单击“添加”以打开下拉对话框。
5. 在“配置存储库类型”字段中，输入“运营资源”。
6. 单击“创建存储库”。
7. 单击“确定”。

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>获取 Microsoft 提供的内部统计配置
1. 单击“打开”。
2. 在树中，选择“内部统计模型\内部统计 (DE)”。
3. 单击“导入”。
    * 单击所选配置的版本 1.1 的“导入”。  
4. 单击“是”。
5. 关闭该页面。
6. 关闭该页面。
7. 单击“申报配置”。
8. 在树中，展开“内部统计模型”。
9. 在树中，选择“内部统计模型\内部统计 (DE)”。

