---
    title: How to Create Custom Company Configuration Packages | Microsoft Docs
    description: As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers. You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.
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
# Vytvoření vlastních konfiguračních balíčků společnosti
Při růstu vašeho podniku se pravděpodobně budete spoléhat na sadu typů společností, které používáte u většiny svých zákazníků. Proces implementace můžete zefektivnit tak, že tyto typy změníte do konfiguračních balíčků společnosti, které jsou k dispozici pro opakované použití.

Obecně vytvořte konfigurační balíček pro každou funkční oblast, například balíček pro nastavení výroby. To umožňuje použít a nastavit nové oblasti ve společnosti podle potřeby.

Dalším přístupem by bylo vytvoření balíčku, který bude obsahovat tabulky definující nastavení, například následující:

- Nastavení dlouhodobého majetku
- Nastavení financí
- Nastavení zásob
- Nastavení výroby
- Nastavení nákupů a závazků
- Nastavení marketingu
- Nastavení služby
- Nastavení prodeje a pohledávek
- Nastavení skladu
- Nastavení obecného účtování
- Nastavení účtování DPH
- Nastavení účtování zásob

Pro zobrazení kompletního seznamu nastavovacích tabulek, vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Ruční Nastavení** a poté vyberte související odkaz.

## Vytvoření vlastního konfiguračního balíčku společnosti
1. Vytvoření nové společnosti. Pro více informací navštivte [Vytvoření nové nové společnosti v Business Central](about-new-company.md).
3. Založte novou společnost tak, jak potřebujete. Vyplňte všechny požadované tabulky nastavení.
4. Otevřete novou společnost.
5. Otevřete stránku **Sešitu konfigurace**.
6. Přidejte do sešitu tabulky, které chcete přenést do jiné společnosti. Přiřaďte řádky sešitu k balíčku.
7. Vytvořte dotazník pro nejčastěji používané tabulky nastavení.
8. Vytvořte konfigurační šablony, které usnadní vytváření kmenových dat, jako jsou zákazníci nebo zboží.
9. Exportujte balíček jako soubor .rapidstart.

## Viz také
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Administrace](admin-setup-and-administration.md)
