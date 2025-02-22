﻿---
title: Manage and monitor capacity (preview)
description: Learn about capacity management in Power Pages.
author: dileepsinghmicrosoft
ms.topic: conceptual
ms.custom: 
ms.date: 11/20/2023
ms.subservice: 
ms.author: dileeps
ms.reviewer: kkendrick
contributors:
    - dileepsinghmicrosoft
    - ProfessorKendrick
ms.contributors:
 - psimolin
---

# Manage and monitor capacity (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

Power Pages capacity management experience in the Power Platform admin center allows administrators to manage Power Pages capacity and monitor capacity consumption. This experience also provides an overview of the different licensing models in use.

> [!IMPORTANT]
> - This feature is a preview feature.
> - [!INCLUDE [preview-tags](../includes/cc-preview-features-definition.md)]

The capacity management features allow administrators to assign prepurchased capacity between the environments in the tenant based on the expected usage of the websites in that environment. The capacity management panel provides daily consumption data at the environment level for up to three full months, which helps determining the required capacity for the environments.

The consumption monitoring views of the capacity management experience provide daily data for the month to date, the past two full months, and monthly data for past 12 months to help with the license budgeting and planning.

The licensing summary view includes information about production websites using legacy licensing models as well, which helps planning the licensing model migration from legacy to current licensing models.

Power Pages capacity management experience allows pivoting between the two supported capacity categories: authenticated MAU (monthly active users) and anonymous MAU.

More information: [Power Platform licensing FAQs](/power-platform/admin/powerapps-flow-licensing-faq#power-pages)

These views and features can be used in addition to the [website capacity consumption reports](/admin/website-consumption-reports); however, for monitoring the consumption of current capacity (authenticated MAU and anonymous MAU) it's recommended to use these new views.

## Licensing summary view

The licensing summary view is located under **Billing (preview)** > **Licenses (preview)**. Once Power Pages is selected from the product selector, the tenant level licensing summary view displays.

:::image type="content" source="Media/capacity-management/licensing-summary.png" alt-text="A screenshot of the Licensing Summary tenent-level view inside of Power Platform admin center.":::

### License type cards

License type cards are shown at the top of the view. The cards provide information about different license types in use in production and relevant metrics such as **Total** (capacity available), and **Assigned** (capacity assigned). 

For capacity-based licensing models, the card has a link to either the capacity management experience or the legacy capacity management panel, depending on the license type. 

For Dynamics 365 Portal Add-ons (legacy license type), **View details** shows the production websites that are using add-ons licensing model. **View details** for pay as you go license type shows a list of websites in production using pay as you go license model.

The license cards have information about the legacy licensing models as well to help administrator with licensing model migration planning. The rest of the views and features only support the current capacity based licensing model (Authenticated MAU and Anonymous MAU). 

More information: [Power Platform licensing FAQs](/power-platform/admin/powerapps-flow-licensing-faq#power-pages)

#### Capacity category pivot

The capacity category pivot allows switching between authenticated capacity and anonymous capacity. This tab controls both the pie chart and graph.

#### Assignments pie chart

The assignments pie chart always shows the current data for total available prepurchased capacity, the amount of assigned capacity and the amount of unassigned capacity. Any changes the administrator makes are reflected in this control. The pie chart represents the top environments in the tenant by assigned capacity, including all other environments and unassigned capacity as well. The legend below the pie shows the top five environment names. Administrators can use this view to confirm when the new capacity is available after procurement, if there's capacity available to be assigned to an environment nearing its assigned capacity, and if any of the top environments have unused capacity that could be reassigned.

#### Consumption history graph

The consumption graph visualizes the data for assigned capacity, total available capacity, consumed capacity and overage at the tenant level, if any. Administrator can use the consumption graph to determine when new capacity needs to be procured to cover the growth. 

- Time ranges available are month to date, daily data for the past two full months, and monthly data for the past 12 months. 
- Licensing capacity consumption resets in the beginning of each month and grows as unique users access the websites and licensing capacity is consumed. 
- Daily views are cumulative. 

There's a delay of up to 24 hours for the data shown in the graph.

#### Notification cards

Notification cards appear above the licensing summary view when something requires attention.

## Capacity management

To manage prepurchased authenticated and anonymous capacity, administrators should select **Manage capacity** in licensing summary below **Capacity**. The capacity management pane opens on the right side of the view.

The capacity management pane allows administrators to view and manage the environments that are either already using this licensing type, and environments without any kind of license or capacity assigned.

At the top of the capacity management pane, administrators can see the total capacity available for the tenant, assigned capacity, and how much of the capacity is unassigned and available to be assigned. The capacity category (authenticated, anonymous) can be controlled with the tab control on the top.

Select an environment from the list to display details of the environment on the bottom of the pane, such as region and the type of the environment. Capacity assignment for the selected environment can be changed by entering the new amount in the **Assigned units** textbox and selecting **Apply**.

:::image type="content" source="Media/capacity-management/capacity-consumption.png" alt-text="A screenshot of the capacity  consumption history.":::

If the environment is nearing or over its assigned capacity, an icon is shown and the status field indicates this status. Hover over the icon to see the consumption history from the past three months to the amount of capacity required.

## Legacy capacity and license management

Legacy capacity refers to the previous Power Pages capacity based licensing model using portal logins and portal page views as metrics. Legacy license refers to Dynamics 365 Portal add-ons. Legacy capacity or legacy licenses are no longer available for purchase and new versions are available.

More information: [Power Pages licensing](/power-platform/admin/powerapps-flow-licensing-faq?branch=main#power-pages)

The licensing summary view also shows any legacy capacity in use, Dynamics 365 Portals add-ons, and pay-as-you-go sites. This information can be used for license model migration planning.

:::image type="content" source="Media/capacity-management/legacy-capacity-management.png" alt-text="A screenshot of the legacy capacity management pane.":::

For legacy capacity, **Manage capacity**, displayed under the license type, opens the legacy capacity management view on the right side of the screen. This view lists the environments and sites in this licensing model and **Manage capacity** action link next to the environment and the site opens the **Manage add-ons** view with the environment preselected. The **Manage add-ons** view allows changes to be made to the legacy capacity (page views, logins).

:::image type="content" source="Media/capacity-management/manage-add-ons.png" alt-text="A screenshot of the manage add-ons view.":::

For Dynamics 365 Portal add-ons, a list of sites is shown to help plan the migration to current licensing models. 

More information: [Convert an existing website to capacity-based model](convert-site.md#convert-an-existing-website-to-capacity-based-model)

For Pay as you go model, list of sites is shown. Usage tracking for these sites is available directly from the Azure portal. 

More information: [View usage and billing information](/power-platform/admin/pay-as-you-go-usage-costs)

## See also

- [Website capacity consumption reports](website-consumption-reports.md)
- [Power Pages licensing FAQs](/power-platform/admin/powerapps-flow-licensing-faq#power-pages)
