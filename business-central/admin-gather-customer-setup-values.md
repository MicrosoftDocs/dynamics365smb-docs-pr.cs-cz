---
    title: Gather Customer Setup Values | Microsoft Docs
    description: You use the configuration questionnaire to help reduce your implementation workload by streamlining the task of setting up the new company. You can generate the configuration questionnaire in Business Central and then provide it to your customer as an Excel (.xls) or XML file.
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
# Shromážďování dat nastavení zákazníka
Pomocí konfiguračního dotazníku můžete snížit pracovní zatížení implementace pomocá zjednodušení úlohy založení nové společnosti. Můžete vygenerovat konfigurační dotazník v [!INCLUDE[d365fin](includes/d365fin_md.md)] a poté jej poskytnout zákazníkovi jako soubor Excel nebo XML.

Všechny výchozí hodnoty v dotazníku můžete změnit tak, aby lépe odpovídaly potřebám zákazníků.

> [!TIP]
> Pro více informací o definování hodnot nastavení v polích pro plánování dodávek, naleznete v části [Doporučené postupy nastavení: Plánování dodávek](setup-best-practices-supply-planning.md).

Když váš zákazník vyplní dotazník, importujete soubor do nové společnosti [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vy a váš zákazník ověříte odpovědi dotazníku před jejich nasazením do společnosti.

## Vytvoření konfiguračního dotazníku
Pomocí dotazníku můžete určit rozsah a potřeby konfigurace. Můžete vytvořit nový dotazník nebo upravit existující dotazník přidáním nových otázek nebo oblastí otázek.

Dotazníky lze vytvořit pouze pro nastavovací tabulky Tento nástroj můžete použít například k poskytnutí informací na následujících stránkách:

- Informace o společnosti
- Nastavení dlouhodobého majetku
- Nastavení financí
- Nastavení zásob
- Nastavení montáže
- Nastavení výroby
- Nastavení nákupů a závazků
- Nastavení marketingu
- Nastavení služby
- Nastavení prodeje a pohledávek
- Nastavení skladu

> [!NOTE]
> K zobrazení kompletního seznamu nastavovacích tabulek, vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení** a poté vyberte související odkaz.. K určení rozsahu migrace dat záznamů použijte funkci migrace. Pro více informací navštivte [Migrace zákaznických dat](admin-migrate-customer-data.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Konfigurační dotazník** a poté vyberte související odkaz.
2. Vyberte tlačítko **Nový**. Stránka **Konfigurační dotazníku** se otevře.
3. Vyberte možnost **Oblasti otázek** . Otevře se stránka **Oblasti otázek**.
4. Vyberte tlačítko **Nový**. Otevře se stránka **Oblasti konfiguračních otázek**.
5. Do pole **ID tabulky**, vyberte ID tabulky, pro kterou chcete shromažďovat informace. Pole **Název tabulky**se automaticky vyplní.
6. Zvolte funkci **Aktualizovat otázky**. Každé pole v tabulce je přidáno do dotazníku s otazníkem následujícím po jeho popisku.

Označení můžete změnit tak, aby bylo jasné, jak má být otázka zodpovězena. Pokud se například pole nazývá „Název“, můžete jej upravit tak, že uvedete „Jaký je <data being collected>název..." Můžete také poskytnou vodítko v poli **Reference**, obsahující odkaz na stránku, který poskytuje další informace.

Můžete také odstranit všechny otázky, které nechcete do dotazníku zahrnout.

> [!NOTE]
> Pole **Možnost odpovědi** popisuje typ a formát odpovědi příslušných dat. Pole **Odpověď** obsahuje informace dodané uživatelem.
> Podle potřeby můžete také definovat výchozí odpovědi v poli **Odpověď**. Tyto hodnoty jsou ve výchozím nastavení použity pro vlastní nastavení. Osoba vyplňující dotazník však může odpověď upravit a aktualizovat.
> 
## Dokončení konfiguračního dotazníku
Pomocí konfiguračního dotazníku můžete strukturovat a dokumentovat podrobnou diskusi o konkrétních potřebách zákazníka. Používá se také ke shromažďování dat nastavení od zákazníka za účelem konfigurace příslušných [!INCLUDE[d365fin](includes/d365fin_md.md)] nastavení tabulek, jako jsou finance, zásoby a zákazníci.

> [!NOTE]
Můžete také vytvořit svůj vlastní konfigurační dotazník podle svých potřeb.

1. Otevřete společnost, pro kterou chcete vyplnit dotazník.
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Konfigurační dotazník** a poté vyberte související odkaz.
3. Vyberte dotazník pro společnost a poté vyberte akci **Export do Excelu**, volitelně akci **Export do XML**.
4. Nechte zákazníka vyplnit konfigurační dotazník zadáním odpovědí do sešitu Excel. Pro každou oblast otázek, které byly pro dotazník vytvořeny, existují sešity.
5. Vyberte tlačítko **Import z Excelu** a vyberte soubor .xlsx s odpověďmi zákazníka.
6. Vyberte tlačítko **Oblast otázek<x2 /> a zahajte proces ověřování a použití odpovědí do konfiguračního dotazníku.

## Vyplnění dotazníku z konfiguračního sešitu
Následující postup poskytuje alternativní způsob přístupu ke konfiguračním dotazníkům. Předpokládá, že konfigurační balíček, který jste poskytli, obsahuje dotazníky.

1. Po importu konfiguračního balíčku otevřete sešit konfigurace.
2. Pro každou tabulku, pro kterou je oblast otázek, vyberte tlačítko **Otázky**. Otevře se stránka dotazníku.
3. Odpovězte na otázky a poté vyberte tlačítko **Použít odpovědi**.
4. Stisknutím tlačítka **OK** zavřete stránku dotazníku.

## Ověření konfiguračního dotazníku
Je důležité ověřit dotazník konfigurace dříve, než jej aplikujete do [!INCLUDE[d365fin](includes/d365fin_md.md)]. Je to také způsob, jak zajistit, že formátování dat bude zachováno během importu z Excelu.

Běžným úkolem ověření je zkontrolovat, zda nejsou textové řetězce zadány do datových polí. Tento proces kontroly je nezbytný, protože formát odpovědi v dotazníku není při spuštění funkce **Použít odpovědi** automaticky ověřen.

> [!NOTE]
Obecně je validace konfiguračního dotazníku ruční proces. Existují však kontroly nesrovnalostí v regionálním formátování. Kromě toho se zobrazí chyby, pokud struktura vaší databáze [!INCLUDE[d365fin](includes/d365fin_md.md)] neodpovídá struktuře migrační databáze.

1. Na stránce **Konfigurační dotazník** vyberte příslušný dotazník a poté vyberte akci **Oblasti otázek**.
2. Otevření příslušné oblasti otázek.
3. U každé otázky ověřte, zda hodnota v poli **Odpověď** odpovídá formátu poskytnutému v poli **Možnosti odpovědi** . Ověřte například, zda je adresa společnosti v textovém formátu.
4. Pokud zjistíte chyby, můžete vyřešit a provést opravy v Excelu exportováním dotazníku a následným importem. Případně můžete opravit chyby přímo v [!INCLUDE[d365fin](includes/d365fin_md.md)] při prohlížení odpovědí na stránce **Oblasti konfiguračních otázek**.
5. Tyto kroky opakujte pro každou oblast otázek.

Po dokončení ověřování jsou data připravena k použití v databázi.

## Použití odpovědí z konfiguračního dotazníku
Po importu a ověření informací z konfiguračního dotazníku můžete přenést nebo použít data nastavení do odpovídajících tabulek v databázi [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Konfigurační dotazník** a poté vyberte související odkaz. Stránka **Konfigurační dotazníku** se otevře.
2. Vyberte konfigurační dotazník ze seznamu a poté vyberte akci **Upravit sešit**.
3. Odpovědi můžete použít jedním ze dvou způsobů.

- Chcete-li použít celý dotazník, zvolte tlačítko **Použít odpovědi**
- Chcete-li použít odpovědi pouze pro určitou **Oblasti otázek**, zvolte talčítko **Oblasti otázek** , vyberte **Oblasti otázek** v seznamu a pak zvolte talčítko **Použít odpovědi** .

### Ověření úspěšného použití odpovědí
1. Zkontrolujte stránky nastavení pro různé funkční oblasti programu [!INCLUDE[d365fin](includes/d365fin_md.md)]. Chcete-li vyhledat stránku, zvolte ikonu [Žárovky, která otevře funkci Řekněte mi ](includes/d365fin_md.md)Řekněte mi, co chcete dělat![, zadejte zadejte název stránky nastavení, kterou chcete najít a poté vyberte související odkaz.
2. Ověřte, zda byla pole naplněna správnými údaji z různých oblastí otázek v konfiguračním dotazníku.

Nyní jste nakonfigurovali nastavení s obchodními informacemi a pravidly zákazníka.

## Viz také
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Administrace](admin-setup-and-administration.md)
