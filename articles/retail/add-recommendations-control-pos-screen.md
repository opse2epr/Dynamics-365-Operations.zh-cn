---
title: 向 POS 设备上的交易记录屏幕添加建议控件
description: 此主题介绍如何使用 Microsoft Dynamics 365 for Retail 中的屏幕布局设计器，向销售点 (POS) 设备的交易记录屏幕添加建议控件。
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f17da3db6fbc19548544a0c6c090a0b6db093673
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606841"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a>向 POS 设备上的交易记录屏幕添加建议控件

[!include [banner](includes/banner.md)]

> [!NOTE]
> 我们将移除当前的产品建议服务版本，因为我们为这项功能重新设计了更出色的算法和更新的面向零售的功能。 有关详细信息，请参阅[已删除或弃用的功能](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features)。

此主题介绍如何使用 Microsoft Dynamics 365 for Retail 中的屏幕布局设计器，向销售点 (POS) 设备的交易记录屏幕添加建议控件。

使用 Microsoft Dynamics 365 for Retail 时，可以在 POS 设备上显示产品建议。 *建议*是客户可能根据其购买历史记录感兴趣的商品、其愿望列表中的商品，以及其他客户在线商店和实体商店购买的商品。 若要显示产品建议，需要使用屏幕布局设计器向交易记录屏幕添加控件。

## <a name="open-layout-designer"></a>打开布局设计器

1. 转至**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS** &gt; **屏幕布局**。
2. 使用快速筛选查找要为其添加控件的屏幕。 例如，使用值 **F2CP16:9M** 在**屏幕布局 ID** 字段中筛选。
3. 在列表中，找到并选择所需记录。 例如，选择**名称: F2CP16:9M 屏幕布局 ID: F2CP16:9M**。
4. 单击**布局设计器**。
5. 按照提示启动布局设计器。 在提示输入凭据时，输入从**屏幕布局**页启动布局设计器时使用的相同凭据。
6. 在登录时，将显示如下页面。 布局将由为您的商店执行的自定义决定。

    [![布局设计器](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>选择显示选项

可用配置选项有两个。 选择最适合您的商店的选项，然后按照其余说明完成控件的设置。 这两个选项是：

- 始终显示建议。
- 在屏幕右侧的网格中显示**建议**选项卡。

### <a name="make-recommendations-always-visible"></a>始终显示建议

1. 缩小交易记录行明细区域的高度，使其与其左侧的客户面板高度相同。

    [![减少的交易记录行详细信息区域高度](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. 将建议控件从左侧菜单拖放到交易记录屏幕底部中央的交易记录行明细与按钮窗格之间。 调整控件大小，使其适合该空间。

    [![添加到布局中的建议控件](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)

3. 单击 **X** 保存并退出布局设计器。
4. 在 Dynamics 365 for Retail 中，转到**零售** &gt; **零售 IT** &gt; **配送计划**。
5. 在列表中，选择  **1090 收银机**。
6. 单击**立即运行**。

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>向屏幕右侧的按钮网格添加“建议”选项卡

1. 在页面右侧按钮网格中最后一个选项卡下空白区域中右键单击。
2. 单击 **自定义**。

    [![自定义 - 选项卡控件对话框](./media/pic-5.png)](./media/pic-5.png)

3. 单击**新建选项卡**。
4. 找到刚添加的新选项卡。 您可能需要向下滚动。
5. 在**目录**下拉菜单中，选择**建议的产品**。

    [![在“目录”字段中选择“建议的产品”](./media/pic-6.png)](./media/pic-6.png)

6. 在**标签**字段，键入建议选项卡的名称。例如，键入“建议的产品”。
7. 在**图像**字段中，选择要在该选项卡上显示的图像。
8. 单击 **确定**。 将在按钮网格中显示新选项卡。
9. 单击 **X** 保存并退出布局设计器。
10. 在 Dynamics 365 for Retail 中，转到**零售** &gt; **零售 IT** &gt; **配送计划**。
11. 在列表中，选择 **1090 收银机**。
12. 单击**立即运行**。

## <a name="additional-resources"></a>其他资源

[个性化产品建议概览](personalized-product-recommendations.md)
