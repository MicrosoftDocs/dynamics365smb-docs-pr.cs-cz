---
title: Troubleshooting Synchronization Errors | Microsoft Docs
description: Provides some guidance for identifying and resolving synchronization errors.
services: project-madeira
documentationcenter: ''
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 10/01/2019
ms.author: bholtorf

---
# Odstraňování potíží s chybami synchronizace
Do integrace [!INCLUDE[d365fin](includes/d365fin_md.md)] s [!INCLUDE[crm_md](includes/crm_md.md)] je zapojeno mnoho pohyblivých částí a někdy se něco pokazí. Toto téma poukazuje na některé typické chyby, které se vyskytují, a poskytuje několik rad, jak je opravit.

Chyby se často vyskytují buď kvůli něčemu, co uživatel provedl se záznamy, nebo pokud něco není v pořádku s tím, jak je integrace nastavena. V případě chyb souvisejících s propojenými záznamy mohou uživatelé tyto problémy vyřešit sami. Tyto chyby jsou způsobeny činnostmi, jako je odstranění záznamu v jedné, ale nikoli v obou obchodních aplikacích a poté synchronizace. Pro více informací navštivte [Zobrazení stavu synchronizace](admin-how-to-view-synchronization-status.md).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Chyby, které souvisejí s nastavením integrace, obvykle vyžadují pozornost správce. Tyto chyby lze zobrazit na stránce **Chyby synchronizace integrace**. Mezi příklady některých typických problémů patří:

* Oprávnění a role přiřazené uživatelům nejsou správné.
* Jako uživatel integrace byl určen účet správce.
* Heslo uživatele integrace je nastaveno tak, aby vyžadovalo změnu, když se uživatel přihlásí.
* Směnné kurzy pro měny nejsou zadány v jedné nebo druhé aplikaci.

Chyby je nutné vyřešit ručně, ale existuje několik způsobů, jak vám stránka pomůže. Například:

* Pole **Zdroj** a **Umístění** mohou obsahovat odkazy na záznam, kde byla nalezena chyba. Klepnutím na odkaz otevřete záznam a prohlédněte si chybu.
* Akce **Smazat položky starší než 7 dní** a **Smazat všechny položky** vyčistí seznam. Tyto akce obvykle používáte poté, co jste vyřešili příčinu chyby, která ovlivňuje mnoho záznamů. Buďte však opatrní. Tyto akce mohou odstranit chyby, které jsou stále relevantní.

## Viz také
[Integrace s [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)
[Nastavení uživatelských účtů pro integraci s [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)
[Nastavení připojení k [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Ruční párování a synchronizace záznamů](admin-how-to-couple-and-synchronize-records-manually.md)  
[Zobrazení stavu synchronizace](admin-how-to-view-synchronization-status.md)