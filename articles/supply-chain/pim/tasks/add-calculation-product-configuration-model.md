---
title: 将计算添加到产品配置模型
description: 该过程显示如何添加新计算到产品配置模型。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9754c46010e7bbdb2edef0d6e68162f344bb1257
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570403"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>将计算添加到产品配置模型

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程显示如何添加新计算到产品配置模型。 它显示如何通过使用“If”运算符将白色扬声器高度设置为 10，将所有其他完工机柜设置为 15 来创建逻辑表达式。 该过程使用演示公司 USMF 的高端扬声器组件。


## <a name="add-a-calculation"></a>添加一个计算

## <a name="create-calculation-expression"></a>创建计算表达式
1. 单击“编辑表达式”。
2. 在“约束体”字段中，输入“如果[完工机柜==“白色”，10, 15]”。
3. 单击“验证”。
4. 单击“关闭”。
5. 单击“确定”。

