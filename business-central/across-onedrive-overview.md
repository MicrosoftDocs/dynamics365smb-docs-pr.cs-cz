---
title: Business Central and OneDrive for Business Integration
description: You can use OneDrive for Business to store, manage, and share files, such as reports or file attachments. 
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords:
ms.date: 02/28/2022
ms.author: jswymer
---

# Integrace OneDrive pro firmy a Business Central

OneDrive pro firmy je služba cloudového úložiště, která je součástí Microsoftu 365. [!INCLUDE[prod_short](includes/prod_short.md)] usnadňuje ukládání, správu a sdílení souborů s ostatními lidmi prostřednictvím OneDrivu. Když máte soubor na OneDrivu, můžete využívat bohaté možnosti spolupráce z online verzí produktů Microsoftu, jako je Word, Excel a PowerPoint. Můžete například sdílet dokument aplikace Word a pak jej můžete společně upravovat současně. OneDrive také umožňuje otevírat jiné typy souborů, například PDF.

## Začínáme

Vytvořili jsme spojení mezi [!INCLUDE[prod_short](includes/prod_short.md)] online a OneDrive, takže je snadné jej začít používat. Jediným požadavkem je, aby uživatelé otevřeli OneDrive alespoň jednou.

Na většině stránek, kde jsou dostupné soubory, jako je Schránka sestav nebo soubory připojené k záznamům, najdete akce **Otevřít na OneDrivu** a **Sdílet**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="The Open in OneDrive and Share actions for reports":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="The Open in OneDrive and Share actions for attachments":::

| Vybrat... | K... | Zobrazit více informací... |
|---------|-----|----------------|
| Otevřít na OneDrivu | Zkopírujte soubor do složky Business Central na OneDrive a otevřete soubor. | [Otevřít ve OneDrive](across-share-onedrive.md#open-in-onedrive) |
| Sdílet | Zkopírujte soubor na OneDrive a sdílejte ho s dalšími lidmi. | [Sdílení na OneDrivu](across-share-onedrive.md#share) |

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).
-->

> [!NOTE]
> K OneDrive můžete také připojit [!INCLUDE[prod_short](includes/prod_short.md)] on-premises. Je však nutné udělat několik věcí, aby to fungovalo. Další informace naleznete v části [Konfigurace Business Central On-Premises](admin-onedrive-integration.md#configuring-business-central-on-premises).

## Viz také
[Správa integrace OneDrive s Business Central](admin-onedrive-integration.md)  
[Otevírání souborů Business Central v OneDrive](across-share-onedrive.md)  
[Nejčastější dotazy k OneDrive](admin-onedrive-faq.md)