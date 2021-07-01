---
title: Manage Work across Multiple Companies in the Company Hub
description: Learn about the company hub in Dynamics 365 Business Central that you use to manage your work across multiple companies.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: edupont
---

# Správa práce napříč více společnostmi v centru společnosti

Někteří lidé pracují ve více společnostech v [!INCLUDE [prod_short](includes/prod_short.md)] a někteří také pracují ve více než jedné organizaci, jako jsou externí účetní nebo zaměstnanci a manažeři společností s více dceřinými společnostmi. Pro tyto uživatele a mnoho dalších slouží centrum společnosti jako vstupní stránka pro správu práce v různých prostředích, ve kterém pracují, napříč společnostmi, prostředími a oblastmi.

K centru společnosti můžete přistupovat přepnutím na roli **Centra společnosti** v Mých nastaveníchnebo přímo otevřením stránky **Centra společnosti**. Stejnou práci můžete dělat na obou místech, ale akce jsou v nabídkách umístěny mírně odlišně.

> [!NOTE]
> Centra společnosti můžete připojit k tolika společnostem, kolik jich potřebujete. Centrum společnosti však můžete připojit pouze ke společnostem, které jsou hostovány v [!INCLUDE [prod_short](includes/prod_short.md)] online.

## Domovská stránka centra společnosti

Pokud používáte roli **Centrum společnosti**, na domovské stránce se zobrazí seznam společností, ke kterým máte přístup, včetně informací o KPI a odkazy na otevření každé společnosti. <!--You can customize the dashboard to show the data points that you want to see by adding or removing columns. For example, you might want to see taxes that are due, how many open sales documents each company has, or the number of purchase invoices that are due next week. You can configure the view to suit your needs. If you have added many companies, you can use filters to sort your view.--> Vyberte tlačítko **Centrum společnosti** k otevření centra společnosti, kde můžete s každou společností úzce spolupracovat.

> [!TIP]
> Chcete-li získat přístup ke konkrétní společnosti v [!INCLUDE [prod_short](includes/prod_short.md)], vyberte název společnosti nebo zvolte položku nabídky **Přejít na společnost**, do které jste automaticky přihlášení na nové záložce.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Akce pro společnost, která je uvedena v centru společnosti":::

Můžete přidat nové společnosti, například když dostanete nového klienta nebo když vaše společnost přidá novou dceřinou společnost. Další informace naleznete v [Přidání společností do centra vaší společnosti](company-hub-add-company.md).

> [!TIP]
> Aby bylo možné aktualizovat data ve Centru společností, musíte mít přístup k datům ve společnostech, ze kterých data pocházejí.

<!--## Company details

In the **Company Hub** page, you can see more information about each company by choosing the name of the company that you want to learn more about. This opens the **Company Details** pane, where you can see additional information, such as the following:  

* Cash account balances  
* Cash flow forecast  
* Overdue purchase invoices  
* Overdue sales invoices  

> [!TIP]
> You can launch predefined Excel workbooks from the **Reports** tab in the ribbon. These Excel workbooks are designed as ready-to-print key financial statements and reports, but you can also modify them to fit your needs. For more information, see [Analyzing Financial Statements in Microsoft Excel](finance-analyze-excel.md).  

Otherwise, close the details pane and continue to the next company.  -->

## Assigned tasks

In [!INCLUDE [prod_short](includes/prod_short.md)], you can assign tasks to yourself and others, and others can assign tasks to you. The company hub gives you an overview of assigned tasks for each company, and you can also access a list of all assigned tasks by choosing **My User Tasks** on the **Home** page.

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### My user tasks

The **My User Tasks** list helps you prioritize your day by showing more information about tasks assigned to you across all your companies.

You can sort by due date, for example, or any other type of data that helps you prioritize your day. By default, the list shows all tasks that are assigned to you, but you can set up filters to only show tasks that are marked as high priority, for example.

Chcete-li úlohu vybrat, jednoduše ji vyberte ze seznamu čekajících uživatelských úloh. In the ribbon, the link **Go to Task Item** opens the page where you can do the work.

Po dokončení úlohy ji jednoduše označte jako dokončenou.

For more information about companies and environments, see [Environment links](company-hub-add-company.md#environment-links).

## Access the company hub

In order to access the company hub, you must have access through either the *D365 COMPANY HUB* user group or through the *D365 COMPANY HUB*  permission set. You must also have access to the companies that are listed in your company hub, which means that you must be a user in those companies. For more information, see [Create Users According to Licenses](ui-how-users-permissions.md).

> [!IMPORTANT]
> The company hub is a company-wide list, so any user who is granted access to the company hub will be able to see all companies in their own [!INCLUDE [prod_short](includes/prod_short.md)] tenant, and all KPIs for the companies that they have access to.

If you cannot find the company hub, and you know that you have been granted access to it, then check with your administrator if the company hub is listed in the **Extension Management** page. Další informace naleznete v tématu [Přizpůsobení Business Central pomocí rozšíření](ui-extensions.md).

## Set up the company hub

To start using the company hub, you must add one or more companies to your dashboard. Další informace naleznete v [Přidání společností do centra vaší společnosti](company-hub-add-company.md).

But to add a company, you must have been given access to one or more instances of [!INCLUDE [prod_short](includes/prod_short.md)] in addition to the company that you use the company hub in.

For example, if you are an accountant, your clients can invite you to their [!INCLUDE [prod_short](includes/prod_short.md)]. For more information, see [Inviting Your External Accountant to Your Business Central](finance-accounting.md#inviteaccountant).

Administrators can use the same assisted setup guide to add you to their [!INCLUDE [prod_short](includes/prod_short.md)], or they can add you to the relevant Azure AD account in the Microsoft 365 admin center. For more information, see [Manage users and groups](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true).

## Viz také

[Add companies to your company hub](company-hub-add-company.md)  
[Accountant Experiences in Business Central](finance-accounting.md)  
[The Company Hub for Business Central Extension](ui-extensions-company-hub.md)  
[Change Basic Settings](ui-change-basic-settings.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]