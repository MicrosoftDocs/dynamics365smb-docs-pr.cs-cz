---
title: Jak vytvořit počáteční zůstatky deníku | Microsoft Docs
description: 'Business Central obsahuje několik dávkových úloh, které jsou poskytovány jako pomoc při převodu zůstatků starších účtů na nově nakonfigurovanou společnost. Tato data můžete snadno přenést pomocí zaúčtování deníků.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="create-journal-opening-balances"></a>Vytvoření počátečních zůstatků deníku
[!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje několik dávkových úloh, které jsou poskytovány jako pomoc při převodu zůstatků starších účtů na nově nakonfigurovanou společnost. Tato data můžete snadno přenést do deníku odběratele, deníku dodavatele, deníku zboží nebo finančního deníku.

Prvním krokem je vytvoření konfiguračního balíčku, který obsahuje tabulky nastavení pro tyto deníky. Následující postup předpokládá, že tento krok je dokončen. Pro více informací navštivte [Nastavení konfigurace společnosti](admin-set-up-company-configuration.md). Tento postup popisuje následující kroky, které zahrnují použití balíčku poskytovaného partnerem.  

Než začnete, ujistěte se, že jste na stránce Centra rolí Implementátor služeb RapidStart, protože tato role poskytuje správný kontext pro vaši konfigurační práci. Pro další informace se podívejte na [Změna základního nastavení](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Pro aplikaci položek v deníku na novou společnost  
1. Nakonfigurujte novou společnost a použijte na ni konfigurační balíček. Pro více informací navštivte [Konfigurace společnosti s průvodcem RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Nová společnost neobsahuje informace o počátečních zůstatcích deníků.  

2. Otevřete konfigurační sešit a importujte existující data o odběratelích, zboží, prodejcích a hlavní knize. Pro více informací navštivte [Migrace zákaznických dat](admin-migrate-customer-data.md).  
3. Vyberte například akci **Vytvořit řádky finančního deníku**.  
4. Podle potřeby vyplňte pevnou záložku **Možnosti** a nastavte filtry tak, jak potřebujete. Například do pole **Šablona deníku** zadejte název.  
5. Zvolte tlačítko **OK**. Záznamy jsou nyní v deníku, ale částky jsou prázdné.  
6. Exportujte tabulku deníku do Excelu a ručně zadejte informace o účtu pro zaúčtování a vyrovnávacím účtu z původních dat.
7. Importujte a aplikujte informace tabulky do nové společnosti. Řádky deníku jsou připraveny k zaúčtování.  
8. V konfiguračním sešitu vyberte řádkovou tabulku deníku a poté zvolte akci **Data databáze**.  
9. Zkontrolujte si informace a poté vyberte akci **Zaúčtovat**.  
10. Opakujte kroky k importu a zaúčtování dalších počátečních zůstatků.  

## <a name="see-also"></a>Viz také  
[Aplikování konfigurace pro nové společnosti](admin-apply-configuration-to-new-companies.md)  
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Správa](admin-setup-and-administration.md)
