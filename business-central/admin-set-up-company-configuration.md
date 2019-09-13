---
title: Nastavení konfigurace společnosti | Microsoft Docs
description: 'Proces implementace, který začíná řešením Business Central, bude vyžadovat. Všechny tyto informace seskupujete do konfiguračních balíčků.'
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
# <a name="set-up-company-configuration"></a>Nastavení konfigurace společnosti
Proces implementace začíná u partnera společnosti Microsoft. Tento partner odpovídá za promyšlení konfiguračních detailů a vytvoření balíčku, který může zákazník snadno použít. Před vytvořením nové společnosti byste měli naplánovat, jak bude nakonfigurována. Musíte zvážit základní nastavení a typy dat, které vaše řešení [!INCLUDE[d365fin](includes/d365fin_md.md)] bude vyžadovat. Všechny tyto informace seskupujete do konfiguračních balíčků.

Služby RapidStart vám také poskytují nástroje, které budete používat k migraci vašich starých dat, jako jsou odběratelé a prodejci.  

Doporučujeme vytvořit konfigurační balíčky s většinou již vyplněných instalačních tabulek, takže zákazníci musí po instalaci balíčku změnit pouze několik nastavení. Pokud například vytvoříte novou společnost, tabulky **Číselná řada** a **Řádky číselné řady** jsou vyplněny sadou číselných řad a počátečních čísel. Automaticky se vyplní také odpovídající pole **Číselná řada** v tabulkách nastavení. Nemusíte dělat práci, jako je zadávání číselných řad a dalších základních nastavení. Můžete také ručně změnit všechna výchozí data, která se používají službami RapidStart, pomocí konfiguračního sešitu.  

Konfigurační balíčky jsou určené pro předkonfigurované společnosti. Po založení společnosti, která vyhovuje vašim potřebám, můžete vytvořit konfigurační balíček, který obsahuje relevantní data z této společnosti. Poté ho můžete použít, když vytvoříte novou společnost, která má být nakonfigurována stejným způsobem.  

Pro usnadnění importu hlavních dat, jako jsou informace o odběrateli a dodavateli, můžete použít konfigurační šablony. Konfigurační šablony obsahují sadu výchozích nastavení, která jsou automaticky přiřazena záznamům importovaným do [!INCLUDE[d365fin](includes/d365fin_md.md)].

Následující tabulka popisuje sekvekci úloh s odkazy na témata, které je popisují.

|**Pro**|**Navštivte**|  
|------------|-------------|  
|Naplánujte konfiguraci společnosti vyplněním konfiguračního sešitu.|[Správa konfigurace společnosti v sešitu](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Vytvořte konfigurační balíček, přizpůsobte balíček, přiřaďte tabulky balíčku, zkontrolujte nebo upravte stávající zákaznická data, vytvořte novou společnost a poté přesuňte testovací data do produkčního prostředí.|[Příprava konfiguračního balíčku](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a>Viz také  
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Správa](admin-setup-and-administration.md)
