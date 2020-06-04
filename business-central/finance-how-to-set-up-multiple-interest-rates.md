---
    title: How to Set Up Multiple Interest Rates
    description: You can calculate finance charges with multiple interest rates for a specific period. The interest calculation is similar for all financial charges, with variation only in the rate of interest for a specific period.

    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Nastavení více úrokových sazeb
Pro zpožděné platby v obchodních transakcích se pro různá období používá více úrokových sazeb. Vláda například specifikuje maximální úrok, který má být pro spotřebitele vybrán. Tato úroková sazba může být změněna dvakrát ročně: 1. ledna a 1. července. Úroková sazba mezi podniky (B2B) je smluvními stranami dohodnuta a pro tuto skupinu zákazníků neexistuje žádný limit. Vyhlášená sazba je obvykle o čtyři procenta vyšší, než je obvyklý bankovní úrok.

Při vytváření podmínek penále a upomínek pro zpožděné platby penále můžete zadat více úrokových sazeb tak, aby se penále počítalo z různých úrokových sazeb v různých obdobích. Pro více informací navštivte **Evidence nového zákazníka**. Pro více informací navštivte **Inkaso nevyrovnaných zůstatků**.

## Nastavení více úrokových sazeb
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Podmínky penále** a vyberte související odkaz.
2. Na stránce **Podmínky penále** vyberte požadovaný finanční termín a poté vyberte akci **Sazby úroků**.
3. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vyberte tlačítko **OK**.
5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Podmínky upomínky** a vyberte související odkaz.
6. Na stránce **Podmínky upomínky** vyberte požadovaný termín připomenutí a poté vyberte akci **Úrovně**.
7. Na stránce **Úrovně upomínky** vyberte pole **Výpočet splatnosti**.

Když vydáte penále, zobrazí se finanční poplatky s více úrokovými sazbami pro určité časové období. Penále také obsahuje kontaktní údaje o zákazníkovi, společnosti, která oznámení vydala, další částku a celkovou částku. Úvodní položka v penálích je zobrazena tučně. Finanční poplatky se počítají s více úrokovými sazbami za určité časové období a tisknou se po otevření záznamu.

## Viz také
[Inkaso nevyrovnaných zůstatků](receivables-collect-outstanding-balances.md)  
[Nastavení financí](finance-setup-finance.md)
