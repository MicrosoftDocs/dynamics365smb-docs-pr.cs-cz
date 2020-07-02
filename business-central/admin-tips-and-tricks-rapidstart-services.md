---
    title: Tips and Tricks - RapidStart Services | Microsoft Docs
    description: When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.
    services: project-madeira
    documentationcenter: ''
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2019
    ms.author: sgroespe

---
# Tipy a triky: Služby RapidStart
Pokud konfigurujete společnosti pomocí služby RapidStart Services, existuje několik tipů a triků, které můžete využít pro bezproblémovou implementaci.

## Využijte konfiguračních šablon
Konfigurační šablony vám mohou pomoci zefektivnit proces implementace. Jejich použitím můžete zahrnout podobné zákazníky do segmentů a poté vytvořit protokol implementace, který zachází se všemi zákazníky v segmentu podobným způsobem. Tímto způsobem můžete pro každý segment použít úroveň přednastavení a pokračovat v rychlém provádění.

## Konfigurační dotazníky
Chcete-li usnadnit proces vyplňování konfiguračního dotazníku, zvažte vymezení výchozích odpovědí, abyste uvedli osvědčené postupy.

## Dávkové vytvoření řádků deníku
K migraci položek deníku doporučujeme použít dodané nástroje pro migraci dat. V opačném případě, pokud použijete dávkovou úlohu k vytvoření řádků deníku, který má omezený rozsah a také generuje pouze předvolená pole do deníku. Zbytek deníku pak musí být vyplněn ručně.

## Migrace transakcí
Doporučujeme migrovat počáteční zůstatky v následujícím pořadí.

1. Přeneste počáteční zůstatky hlavní knihy bez použití účetních položek finančního účtu. Použijte specifické protiúčty počátečního stavu, které jsou nastaveny pro každou dílčí knihu. Chcete-li povolit přímé účtování, nastavte vyrovnávací účty.
2. Migrujte položky zákazníků.
3. Migrujte položky zboží.
4. Migrovat položky dlouhodobého majetku

## Viz také
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Administrace](admin-setup-and-administration.md)
