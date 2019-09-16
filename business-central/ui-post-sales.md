---
title: Porozumění Způsobu Účtování Prodejních Dokladů | Microsoft Docs
description: Další informace o různých způsobech účtování prodejních dokladů.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
---
# <a name="posting-sales"></a>Účtování prodeje
V **Účto skupině** v prodejním dokladu si můžete vybrat z následujících funkcí účtování:

* **Účtovat**
* **Testovací Sestava**
* **Účtovat a Odeslat**
* **Účtovat a Vytisknout**
* **Účtovat a poslat mailem**
* **Dávkové Účtování**
* **Náhled Účtování**

Jakmile vyplníte všechny řádky a zadáte všechny informace o prodejní objednávce, můžete ji zaúčtovat. Tím se vytvoří dodávka a faktura.

Po zaúčtování prodejní objednávky se aktualizuje účet zákazníka, hlavní účetní kniha a položky zboží.

Pro každou prodejní objednávku se v tabulce **Věcná položka** vytvoří záznam o prodeji. Položka je také vytvořena na účtu zákazníka v **Položkách  zákazníka** a položka účetní knihy se vytvoří na příslušném účtu pohledávek. Kromě toho může odeslání objednávky vést k zadání DPH a zápisu hlavní účetní knihy pro částku slevy. Zveřejnění záznamu o slevě závisí na obsahu pole **Účtování slevy** na stránce **Nastavení prodeje a pohledávek**.

Pro každou řádek prodejní objednávky bude v tabulce **Položka zboží**   vytvořena položka hlavní účetní knihy (pokud prodejní řádky obsahují čísla položek) nebo bude položka hlavní účetní knihy vytvořena v tabulce **Věcná položka** (pokud prodejní řádky obsahují účet hlavní knihy). Kromě toho jsou prodejní objednávky vždy zaznamenány v tabulkách **Hlavička prodejní dodávky** a **Hlavička prodejní faktury**.

> [!IMPORTANT]  
>   Při odeslání objednávky můžete vytvořit dodávku i fakturu. Lze to provést současně nebo samostatně. Můžete také vytvořit částečnou dodávky a částečnou fakturu vyplněním polí **K dodání** a **K fakturaci** na jednotlivých řádcích prodejní objednávky před zaúčtováním. Upozorňujeme, že nemůžete vytvořit fakturu za něco, co není dodáno. To znamená, že dříve, než budete moci fakturovat, musíte zaznamenat Dodávka nebo se musíte rozhodnout dodání a fakturovat současně.

Po dokončení účtování budou zaúčtované řádky z objednávky odstraněny. Po dokončení účtování se zobrazí zpráva. Poté budete moci zobrazit zaúčtované položky na různých stránkách, které obsahují zaúčtované položky, například **Zák. Stránky Položky hlavní knihy**, **Hlavní kniha**, **Položky zboží**, **Účtované prodejní dodávky** a **Účtované prodejní faktury**.

## <a name="see-also"></a>Viz také
[Prodej](sales-manage-sales.md)  
[Odeslat dokumenty e-mailem](ui-how-send-documents-email.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

