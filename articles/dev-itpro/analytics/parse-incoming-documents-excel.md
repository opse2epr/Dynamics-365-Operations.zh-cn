---
title: 分析 Excel 格式的传入文档
description: 本主题提供有关设计电子申报 (ER) 格式以分析传入的 Microsoft Excel 文件中包含的内容的信息。
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545045"
---
# <a name="parse-incoming-documents-in-excel-format"></a>分析 Excel 格式的传入文档

[!include[banner](../includes/banner.md)]

您可以设计电子申报 (ER) 格式以分析传入的以 Microsoft Excel 工作簿的形式表示数据的 Microsoft Excel 文件（XLSX 格式的文件）。 然后可以使用这些文件中的内容更新申请表数据。 这在以下情况下非常有用：

- 设计新的模型和格式并希望在运行时进行测试。 在这种情况下，Excel 将模拟实际的申请表数据。
- 不使用您的应用程序，而是在 Excel 中管理数据，并希望导入这些数据以提交特定报表。

若要了解此功能的详细信息，请播放任务指南 **ER 从 Microsoft Excel 文件导入数据（第 1 部分：设计格式）** 和 **ER 从 Microsoft Excel 文件导入数据（第 2 部分：导入数据）**（这些任务指南属于 7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程）。 这些任务指南演练如何通过使用 ER 格式从传入的文档导入信息并更新申请表数据来分析传入的 Excel 文件。 可从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载这些任务指南。

请下载以下文件以完成上面提到的任务指南。

| 内容描述                         | 文件                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| .XLSX 格式的传入文件 - 模板    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| .XLSX 格式的传入文件 - 示例数据 | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

如果尚未在当前 Dynamics 365 for Finance and Operation 应用程序中播放任务指南 [ER 创建要从外部文件导入数据所需的配置](./tasks/er-required-configurations-import-data.md)，请下载以下文件。

| 内容描述    | 文件                                                            |
|------------------------|-----------------------------------------------------------------|
| ER 模型配置 | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |
