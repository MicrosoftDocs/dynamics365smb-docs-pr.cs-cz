---
    title: How to Archive Sales and Purchase Documents | Microsoft Docs
    description: You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.
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
# Archivování dokladů
Můžete archivovat prodejní a nákupní objednávky, nabídky, objednávky vratky a hromadné objednávky, například proto, že chcete uložit kopii dokumentu pro pozdější použití. Prodejní nebo nákupní doklad můžete archivovat několikrát a pokaždé uložit jinou archivovanou verzi.

U archivovaných dokladů, kde originál stále existuje a není zaúčtován, můžete pomocí funkce **Obnovit** přepsat originál archivovanou verzí dokladu. To je praktické, pokud potřebujete obnovit obsah dokladu do dřívějšího stavu.

U archivovaných dokladů, kde je originál odstraněn, můžete obsah znovu použít pouze zkopírováním dat, například pomocí funkce **Kopírovat doklad**.

## Nastavení automatické archivace dokladu
Před odstraněním dokladů můžete nastavit automatickou archivaci prodejních a nákupních objednávek, nabídek, hromadných objednávek a objednávek vratek.

Následující postup popisuje, jak nastavit automatickou archivaci prodejních dokladů. Kroky jsou podobné i pro nákupní dokumenty.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Nastavení prodeje a poheldávek** související odkaz.
2. Na stránce **Nastavení prodeje a pohledávek** vyplňte pole následujícím způsobem.

| Pole | Popis |
|-----|-----------|
| **Archivovaná prodejní nabídka** | **Nikdy** - Nearchivovat prodejní nabídky při jejich odstranění. **Dotaz** - Výzva uživatele, aby vybral, zda má být archivovaný doklad při mazání **Vždy** - Automatická archivace dokladu při jeho smazání. |
| **Archivovaná hromadná prodejní objednávka** | Vyberte, chcete-li automaticky archivovat hromadné prodejní objednávky při každém odstranění. |
| **Archivované  objednávky a objednávky  vratky** | Vyberte, chcete-li automaticky archivovat prodejní objednávky pokaždé, když jsou odstraněny. |

## Archivace prodejní objednávky
Následující postup popisuje, jak archivovat prodejní objednávku. Postup je podobný jako u všech objednávek, hromadných objednávek, objednávek vratek a nabídek.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Prodejní objednávky** související odkaz.
2. Otevřete prodejní objednávku, kterou chcete archivovat.
3. Vyberte tlačítko **Archivovat dokument**.

Prodejní objednávka je archivována. Můžete si ji prohlédnout na stránce **Archivované prodejní objednávky**.

## Obnovení nezaúčtované prodejní objednávky z archivu
Následující postup popisuje, jak přenést obsah archivované prodejní objednávky zpět na původní prodejní objednávku. To je možné pouze tehdy, pokud původní dokument nebyl zaúčtován. Postup je podobný jako u všech objednávek, hromadných objednávek, objednávek vratek a nabídek.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Archivované prodejní objednávky** související odkaz.
2. Vyberte archivovanou prodejní objednávku nebo její verzi, kterou chcete obnovit, a pak zvolte tlačítko **Obnovit**.

Obsah původní prodejní objednávky bude nahrazen textem vybrané archivované verze.

## Odstranění archivovaných prodejních objednávek
Následující postup popisuje, jak odstranit archivované prodejní objednávky. Postup je podobný ostatním archivovaným prodejním a nákupním dokladům.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Odstranit archivované verze prod.objednávek** související odkaz.
2. Na stránce **Odstranit archivované verze prod.objednávek** nastavte patřičné filtry.
3. Vyberte tlačítko **OK**.

## Viz také
[Sledování řádků dokladu](across-how-to-track-document-lines.md)  
[Prodej](sales-manage-sales.md)  
[Obecné obchodní Funkcionality](ui-across-business-areas.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
