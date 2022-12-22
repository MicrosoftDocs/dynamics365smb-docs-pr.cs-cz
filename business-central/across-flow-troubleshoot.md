---
title: Troubleshoot Your Automated Workflows
description: Learn how to troubleshoot the connection between Business Central and Power Automate when you build an automated workflow.

ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
---

# Odstraňování problémů s automatickým workflow [!INCLUDE[prod_short](includes/prod_short.md)]

Když se připojíte [!INCLUDE [prod_short](includes/prod_short.md)] s Power Automate k vytvoření automatizovaných workflow, můžete narazit na chybové zprávy. Tento článek obsahuje navrhovaná řešení často se opakujících problémů.

## Flow se nespustí u všech vytvořených nebo změněných záznamů

### Problém

Pokud událost vytvoří nebo změní mnoho záznamů, Flow se nespustí na některých nebo všech záznamech.

### Možná příčina

V současné době existuje limit na počet záznamů, které může Flow zpracovat. Pokud se během 30 sekund vytvoří nebo změní více než 100 záznamů, tok se nespustí.

> [!NOTE]
> Pro vývojáře se spouštění Flow provádí prostřednictvím oznámení webhooku a toto omezení je způsobeno způsobem, jakým konektor Business Central zpracovává `sbírky` oznámení. Další informace naleznete v tématu [Práce s webhooky v Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) v nápovědě pro vývojáře a správce.

## Chyba "Sada entit nebyla nalezena"

### Problém

Když vytvoříte nový tok Power Automate pomocí [!INCLUDE[prod_short](includes/prod_short.md)] schvalování, například *Když je požadováno schválení nákupního dokladu*, může se zobrazit chybová zpráva podobné této:

`Sada entit nebyla nalezena: \<name\>`

Zástupný symbol, `\\<name\\>`, je název služby chybějící webové služby, například *workflowWebhookSubscriptions* nebo *workflowPurchaseDocumentLines*.orkflowPurchaseDocumentLines*.

### Možná příčina

Použití Power Automate pro vaše schvalování vyžaduje, aby byly určité objekty stránek a procedur publikovány jako webové služby. Ve výchozím nastavení je většina požadovaných objektů publikována jako webové služby. V některých případech však mohlo být vaše prostředí přizpůsobeno tak, aby tyto objekty již nebyly publikovány.

### Oprava

Přejděte na stránku **Webové služby** a ujistěte se, že následující objekty jsou publikovány jako webové služby. V seznamu by měla být položka pro každý objekt se zaškrtnutým políčkem **Publikováno**.

| Object Type | ID Objektu | Název objektu | Název služby |
|-----------|---------|-----------|------------|
| Codeunita | 1544 | WorkflowWebhookSubscription | WorkflowActionResponse |
| Stránka | 6408 | workflowCustomers | workflowCustomers |
| Stránka | 6406 | workflowGenJournalBatches | workflowGenJournalBatches |
| Stránka | 6407 | workflowGenJournalLines | workflowGenJournalLines |
| Stránka | 6409 | workflowItems | workflowItems |
| Stránka | 6405 | Purchase Document Line Entity | workflowPurchaseDocumentLines |
| Stránka | 6404 | workflowPurchaseDocuments | workflowPurchaseDocuments |
| Stránka | 6403 | Sales Document Line Entity | workflowSalesDocumentLines |
| Stránka | 6402 | workflowSalesDocuments | workflowSalesDocuments |
| Stránka | 6410 | workflowVendors | workflowVendors |
| Stránka | 831 | workflowWebhookSubscriptions | workflowWebhookSubscriptions |

> [!NOTE]
> Hodnota **Název služby** musí být přesně taková, jaká je uvedena v tabulce. Neměňte ani nepřekládejte název služby.

Pro více informací o publikování webových služeb navštivte [Publikování webové služby](across-how-publish-web-service.md).

## Viz také

[Použití [!INCLUDE[prod_short](includes/prod_short.md)]  v automatizovaném pracovním postupu](across-how-use-financials-data-source-flow.md)  
[Workflow](across-workflow.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]