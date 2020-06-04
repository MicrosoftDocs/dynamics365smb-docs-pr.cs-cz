---
title: Purchase Items or Services for a Job and Manage Supplies| Microsoft Docs
description: Describes how to manage the supply and purchase of material and services to jobs.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 10/01/2019
ms.author: sgroespe

---
# Správa dodávek projektu
Správa dodávek zboží, služeb a nákladů projektu je nedílnou a kritickou součástí provádění všech projektů. Můžete použít množství zásob nebo provádět nákupy specifické pro daný projekt pomocí nákupních objednávek nebo nákupních faktur. Například servisní úloha v počítači vyžaduje nový disk. Vytvořte nákupní fakturu k nákupu nového disku a zaznamenání projektu, na které bude použita.

Pokud nákupní proces nevyžaduje, aby byla fyzická transakce zaznamenána samostatně, tak může být nákup zpracován na stránce **Finanční deníky projektu**. Pro více informací navštivte [Evidence spotřeby na projektu](projects-how-record-job-usage.md).

## Nákup zboží nebo služeb pro projekt
Následující postup ukazuje, jak použít nákupní fakturu k nákupu produktů pro projekt. Stejné kroky platí i při použití nákupní objednávky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní faktury** a poté vyberte související odkaz.
2. Vyberte akci **Nový** vyplňte pole podle potřeby. Pro více informací navštivte [Záznam nákupních objednávek](purchasing-how-record-purchases.md).
3. Na polích **Číslo projektu** a **Číslo úlohy projektu**, vyberte informace o projektu, pro který chcete koupit položky nebo služby. Vyberte funkci **Vybrat sloupce** pokud není pole viditelné. Pro více informací navštivte [Přizpůsobení Vašeho pracovního prostoru](ui-personalization-user.md).

   Hodnota, kterou vyberete v poli **Typ řádku projektu** definuje, zda bude řádek plánování vytvořen při zaúčtování spotřeby zboží. Pokud pole obsahuje **Fakturovatelné**, vytvoří se řádky plánování úloh, které jsou připraveny k fakturaci zákazníkovi. Pro více informací navštivte [Fakturace projektů](projects-how-invoice-jobs.md).
4. Vyberte akci **Účtovat**.

## Zobrazení hodnoty nákupů projektu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Projekty** a poté vyberte související odkaz.
2. Otevřete příslušnou kartu projektu.

   Na záložce **Úlohy**, zobrazuje pole **Otevřených objednávek** celkovou nezaplacenou částku zásob v místní měně, služeb, o zásobách a službách v nákupních dokumentech pro řádek úlohy.

   Pole **Deaktivovaná nevyfakturovaná, částka** zobrazuje hodnotu položek dodaných na nákupních dokladech, ale dosud nefakturovaných..
3. Vyberte jedno z polí pro otevření stránky **Nákupní řádky**, kde si můžete prohlédnout informace o souvisejících řádcích nákupních dokladů, včetně toho, které položky nebo služby byly přijaty.

## Zaúčtování výdajů souvisejících s projektem
Pokud vám vzniknou mimořádné nebo jednorázové výdaje na projekt, můžete je pomocí stránky **Finanční deník projektu** odeslat přímo na příslušný účet projektu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deník projektu** a poté vyberte související odkaz.
2. Vytvořte nový řádek a zadejte informace o výdajích, včetně informací v polích **Číslo projektu** a **Číslo úlohy projektu**.
3. Po dokončení deníku vyberte akci **Zaúčtovat**.

## Viz také
[Správa projektů](projects-manage-projects.md)  
[Finance](finance.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
