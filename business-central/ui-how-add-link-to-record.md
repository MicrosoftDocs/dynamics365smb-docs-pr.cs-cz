---
    title: Add Attachments, Links, and Notes on Records
    description: Attach a hyperlink to a document, or a website to a specific record, such as a customer or document.
    author: SorenGP

    
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 06/24/2021
    ms.author: edupont
---
# Správa příloh, odkazů a poznámek ke kartám a dokladům

Ve FactBoxu na většině karet a dokladů můžete připojit soubory, přidávat odkazy a psát poznámky. V případě odkazů a poznámek to můžete udělat také na stránce přehledu tak, že nejprve vyberete příslušný řádek.

Chcete-li zobrazit nebo změnit některý z těchto připojených informací, musíte nejprve otevřít kartu **Přílohy** ve FactBoxu. Číslo za názvem karty udává, kolik připojených souborů, odkazů nebo poznámek existuje pro kartu nebo doklad.

Přílohy, odkazy a poznámky zůstávají připojeny, protože karta nebo doklad je zpracován do jiných oblastí systému, například z probíhající prodejní objednávky na zaúčtovanou prodejní fakturu. Žádný z typů příloh však není výstupem ze systému, například při tisku nebo při ukládání do souboru.

> [!NOTE]
> Pokud částečně dodáte a vyfakturujete prodejní objednávku nebo objednávku, bude příloha připojena pouze ke konečné faktuře dané objednávky. Podobně při fakturaci pomocí funkce Časové rozlišení je příloha připojena pouze k položkám finančního účtu za vybraný doklad, ale ne pro položky časově rozlišených položek.
>
> Pokud odstraníte objednávku před fakturací, bude odstraněna i příloha. Při fakturaci nákupních objednávek pomocí akce Získat řádky příjemky z nákupní faktury se příloha na nákupních objednávkách nepřidá k nákupní faktuře.

## Připojení souboru k nákupní faktuře
Ke kartě nebo dokladu můžete připojit libovolný typ souboru obsahujícího text, obrázek nebo video. To je užitečné například v případě, že chcete uložit fakturu dodavatele jako soubor PDF na související nákupní faktuře v [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Soubory připojené k funkci Došlé doklady nejsou zahrnuty na kartě **Přílohy**. Další informace naleznete v části [Došlé doklady](across-income-documents.md).

Následující postup je založen na nákupní faktuře. Kroky jsou podobné pro všechny ostatní podporované doklady a karty.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte Mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní faktury** a poté vyberte související odkaz.
2. Otevřete prodejní objednávku, ke které chcete připojit soubor.
3. V Informačním okně, otevřete **Přílohy**.
4. Vyberte hodnotu za polem **Dokumenty** například "0".
5. Na stránce **Připojené dokumenty** v poli **Příloha** vyberte **Vybrat soubor**.
5. Vyberte soubor z libovolného umístění a pak zvolte tlačítko **Otevřít**.

Soubor je nyní připojen k nákupní faktuře.

## Zobrazení připojeného souboru
1. V Informačním okně, otevřete **Přílohy**.
2. Vyberte hodnotu za polem **Dokumenty** například "1".
3. Na stránce **Připojené dokumenty** vyberte akci **Náhled**.
4. Otevřete stažený soubor.

## Uložení doklad jako přílohy PDF
Kdykoli potřebujete uložit doklad jako soubor, můžete použít akci **Připojit jako PDF** k uložení aktuálního obsahu dokladu jako souboru PDF připojeného ve FactBoxu dokladu. To je užitečné například tehdy, když doklady sledují několik kroků v procesu, například prodejní proces nebo workflow schvalování, a chcete odkazovat na tisk předchozího kroku.

Následující postup je založen na prodejní objednávce. Kroky jsou podobné pro všechny podporované dokumenty.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté zvolte související odkaz.
2. Vyberte prodejní objednávku a pak zvolte **Připojit jako PDF**.

Soubor PDF s aktuálním obsahem prodejní objednávky je přidán do FactBoxu **Přílohy**.

## Přidání odkazu z karty zboží
Odkaz z karty nebo dokladu můžete přidat na libovolnou URL adresu. To je užitečné například tehdy, když chcete propojit kartu zboží s katalogem zboží dodavatele.

Následující postup je založen na kartě zboží. Postup je podobný pro všechny ostatní podporované karty a doklady.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Zboží** a poté vyberte související odkaz.
2. Vyberte položku, ze které chcete přidat odkaz, a poté vyberte **Přílohy** ve FactBoxu.
3. V **Řádcích**, klikněte na ikonu **+**.
4. Do políčka **Adresa odkazu** vložte daný odkaz.

   Odkaz musí být platná internetová nebo intranetová URL adresa.

5. Do polička **Popis** vložte informaci o odkazu.
6. Zvolte tlačítko **OK**.

Odkaz je nyní připojen k kartě zboží.

## Poznámka na prodejní objednávce
Můžete napsat poznámku na dokument nebo kartu, například sdělit zvláštní pokyny ostatním uživatelům dokladu nebo karty. Do poznámek můžete zahrnout odkazy na soubory a adresy URL.

> [!NOTE]
> Poznámky v kartě **Přílohy** nesouvisejí s funkcí interních poznámek, která se používá hlavně ke komunikaci mezi uživateli. Pro více informací navštivte [Nastavení upozornění Workflow](across-setting-up-workflow-notifications.md).

Následující postup je založen na prodejní objednávce. Kroky jsou podobné pro všechny ostatní podporované doklady a karty.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté zvolte související odkaz.
2. Vyberte prodejní objednávku, ke které chcete napsat poznámku, a pak zvolte záložku **Přílohy** ve FactBoxu.
3. V sekci **Poznámky** vyberte ikonu **+**.
4. Do pole **Poznámka** napište libovolný text, například "Toto je urgentní objednávka.".
5. Zvolte tlačítko **OK**.

Poznámka je nyní připojena k prodejní objednávce.

## Viz také
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Došlé doklady](across-income-documents.md)  
[Nastavení notifikací Workflow](across-setting-up-workflow-notifications.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
