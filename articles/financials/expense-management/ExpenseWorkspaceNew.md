---
title: 已重构的费用报表
description: 本主题介绍 Microsoft Dynamics 365 for Finance and Operations 中经过重新设计和重构的费用报表录入体验。 新体验简化了填写费用报表的流程，并缩短了所需时间。
author: ryansandness
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: c7a2b95456e812970b135d83f0f7e503310ce185
ms.sourcegitcommit: 97ed74889a09ef385f6ecbab69e84a05ff42ee41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/20/2019
ms.locfileid: "1592629"
---
# <a name="expense-reports-reimagined"></a>已重构的费用报表

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

重新设计了费用报表录入，以便简化填写费用报表的流程和缩短所需时间。 下面是新费用体验的主要组件：

- 新的费用管理工作区，用于访问委托人的费用。
- 新的收据匹配体验，用于更好地显示抬头级收据和简化将收据附加到费用行的流程。
- 新的只读网格，用于查看更多费用行和更多数据列。 现在可以查看所有明细化行和拆分行，及其父费用。
- 经过简化的费用编辑窗格。
- 错误、警告和策略消息已经过重新设计，可以帮助确保为您提供正确的上下文来了解问题及其解决方法。 Microsoft 已删除了用户有机会完成任务之前显示的大量消息，并解决了明细化消息之类问题。
- 一个新页面，用于指定哪些字段是组织必需的，哪些字段可选和哪些字段不应捕获。 此页面将减少用户必须设置的字段数量。
- 新的费用报表外观，这样此类报表外观不再像为会计人员设计的。

若要开启新体验，请使用**功能管理**工作区开启**已重构的费用报表**功能。 开启此功能时，将执行以下操作：

- 现有费用工作区替换为新工作区。
- 为费用字段可见性添加一个新菜单项。
- 不删除费用报表（现有页面）和费用报表字段的任何现有菜单项。
- 工作流和所有审核仍然会将您带到现有费用报表页。

## <a name="getting-started-video-for-new-users"></a>面向新用户的入门视频

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE2Y7gO]

YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中包含 [Dynamics 365 for Finance and Operations 中的费用体验](https://youtu.be/Ocy-MsTvEE0)视频（上面显示的）。

## <a name="new-features"></a>新功能

| 新功能 | 说明 |
|---|----|
| 费用字段可见性 | 可通过一个新的设置页面指定应对组织禁用哪些字段，哪些字段应该为必填字段，以及哪些字段为推荐字段。 |
| 必填字段 | 新的简单配置让您不必使用策略框架即可将某些字段设置为必填字段。 |
| 可选字段 | 为可选字段增加了第二页面。 这样员工不会觉得必须设置字段，但是字段仍然可以轻松访问。 |
| 添加未附加的收据 | 更容易在工作区和费用报表中查看向费用报表添加未附加的收据这一功能。 |
| 改进了消息 | 更容易查看具有警告或错误的费用行。 |
| 消息栏中减少了消息数量| 减少了信息日志消息的数量，进行了防止许多情况下显示重复消息的工作。 |
| 常用操作分组 | 对界面进行了清理，新增了针对大多数行级常用操作的操作按钮，以及针对抬头操作和其他不太常用操作的省略号按钮 (...)。 |
| 新增了用于提高可见性的工作区 | 新的工作区统一了用户用于转到其他区域的功能和链接。 |
| 创建费用期间添加现有费用和收据 | 创建费用报表时，可添加所有或所选费用和收据。 |
| 汇率计算器 | 增加了汇率计算器，用于计算多币种付现交易记录的汇率。 |
| 保存和新增费用行 | 输入新费用时可使用**保存**和**新建**按钮来帮助您快速输入费用行。 |
| 更容易查看拆分行和明细化行 | 明细化行和拆分行直接添加到费用列表，从而可以提高可见性和帮助您轻松确定是否发生了策略错误或其他错误。 |
| 明细化期间显示收据 | 可以在明细化期间显示收据。 |

初始版本重点关注费用录入方案。 所有费用报表检查或审核方案都将继续使用现有费用录入页。

现有页面中有下列功能，但新页面中还没有。 接下来的一些版本中将重新引入这些功能：

- 审核
- 应付帐款审核和会计编辑功能
- 多个入口点
- 出差申请集成
- 费用的数据实体字段可见性
- 出差津贴的录入
- 行级别工作流
- 临时审核人支持
- 高级明细
