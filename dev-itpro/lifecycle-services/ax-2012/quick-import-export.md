---
title: "使用快速导入/导出"
description: "快速导入导出的目的是让您使用较少的步骤导入和导出。"
author: margoc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 2012 R3 CU8
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: a0329cd2710820fb1e82f761a414a3f08910078b
ms.lasthandoff: 03/31/2017


---

# <a name="run-the-test-data-transfer-tool-beta-for-dynamics-ax-ax-2012"></a>运行 Dynamics AX (AX 2012) 的数据传输工具（beta 版）

[!include[banner](../../includes/banner.md)]


快速导入导出的目的是让您使用较少的步骤导入和导出。

我们添加了快速导入导出功能以使用户可以导入或导出他们希望迅速执行的简单作业。 理想情况下，在文件自动映射到系统，且用户不需要经过高级映射或创建重复导入或导出作业的情况下使用此功能。

-   此功能支持使用现成和自定义实体。
-   您可以从文件导入，如果使用 ODBC 数据源，您可以选择要用于定义导入的查询。
-   您必须以前已为 AX 或文件定义了源数据格式，并知道它们的位置。
-   您不需要创建一个处理组来使用快速导入/导出，在执行导入或导出作业时系统将自动创建。 您也可以选择保留由快速导入/导出导入的数据的历史记录。

  请注意，快速导入导出假定您熟悉 DIXF 的概念。



