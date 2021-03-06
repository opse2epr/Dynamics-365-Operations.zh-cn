---
title: 通过使用向导设置编号规则
description: “数序”被用于为需要它们的主数据记录和交易记录记录生成可读的唯一的标识符。
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1808ab9240ab291f9d203893a634bd390f16e2e7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560536"
---
# <a name="set-up-number-sequences-by-using-a-wizard"></a>通过使用向导设置编号规则

[!include [task guide banner](../../includes/task-guide-banner.md)]

“数序”被用于为需要它们的主数据记录和交易记录记录生成可读的唯一的标识符。 需要标识符的主数据或交易记录称为“参考”。 在您能为一个参考创建新记录之前，您必须设置编号规则并将其与参考相关联。 该过程会说明如何同时使用向导设置所有必需的数序。 创建此程序的演示数据公司是 USMF。

1. 转到“组织管理”>“标号规则”>“编号规则”。
2. 单击“生成”。
3. 单击“下一步”。
    * 在此页上您可以修改标识代码、最低值和最高值。 此外，您可以指示该编号规则是否必须是连续的。   
    * 如果您必须为该编号规则分配编号，请不要选择“连续”选项。     为了将范围段落添加到编号规则的格式，请在列表中选择该格式，然后单击“将范围包括在格式中”。     为了将范围段落从编号规则的格式中删除，请在列表中选择该格式，然后单击“从格式中删除范围”。     为了将编号规则从自动生成中排除，请在列表中选择该编号规则，然后单击“删除”。  
4. 单击“下一步”。
5. 单击“完成”。

