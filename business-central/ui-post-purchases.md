---
title: Porozumění způsobu účtování nákupních dokladů | Microsoft Docs
description: Zjistěte více o různých funkcích účtování pro účtování nákupních dokladů.
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
# <a name="posting-purchases"></a>Účtování nákupů
V **Účtování** na dokladu o nákupu si můžete vybrat z následujících funkcí účtování:

* **Účtovat**
* **Náhled Účtování**
* **Účtovat a Vytisknout**
* **Testovací Sestava**
* **Dávkové Účtování**

Když vyplníte všechny řádky a zadáte všechny informace o nákupní objednávce, můžete ji zaúčtovat, tj. vytvořit příjemku a fakturu.

Po zaúčtování nákupní objednávky se aktualizuje účet dodavatele, hlavní kniha a položky zboží.

Pro každou nákupní objednávku se vytvoří nákupní položka v tabulce **Věcná položka**. Položka se také vytvoří na účtu dodavatele v tabulce **Položka dodavatele** a věcná položka se vytvoří na příslušném účtu závazků. Kromě toho může naúčtování objednávky vést k DPH položce a věcné položce pro částku slevy. To jestli je položka slevy naúčtovaná, záleží na obsahu pole **Účtování slevy** na stránce **Nastavení nákupu a závazků**.

Pro každý řádek nákupní objednávky se vytvoří položka zboží v tabulce **Položka zboží** (pokud nákupní řádky obsahují čísla položek) nebo bude vytvořená věcná položka v tabulce **Věcná položka** (pokud nákupní řádky obsahují finanční účet). Kromě toho jsou nákupní objednávky vždy zaznamenány v tabulkách **Hlavička Nák. Příjemky** a **Hlavička Nák. Faktury**.

Než začnete účtovat, můžete si vytisknout testovací sestavu, která obsahuje všechny informace o nákupní objednávce a naznačuje případné chyby. Chcete-li sestavu vytisknout, zvolte **Účtování**, a poté zvolte **Testovací sestava**.

> [!IMPORTANT]  
>   Když zaúčtujete objednávku, můžete vytvořit zároveň příjemku i fakturu. To lze provést současně nebo nezávisle. Můžete také před účtováním vytvořit částečnou příjemku a částečnou fakturu vyplněním polí **K příjmu** a **K fakturaci** na jednotlivých řádcích nákupních objednávek. Upozorňujeme, že nemůžete vytvořit fakturu za něco, co nebylo přijato. To znamená, že dříve, než budete moci fakturovat, musíte zaznamenat příjemku nebo se musíte rozhodnout přijmout a fakturovat současně.

Můžete buď účtovat, nebo účtovat a vytisknout. Pokud se rozhodnete účtovat a vytisknout, po zaúčtování objednávky se vytiskne sestava. Můžete také zvolit funkci **Dávkové účtování**, která vám umožní zaúčtovat několik objednávek současně.

Po dokončení účtování budou zaúčtované nákupní řádky z objednávky odstraněny. Po dokončení účtování se zobrazí zpráva. Poté budete moci zobrazit zaúčtované položky na různých stránkách, které obsahují zaúčtované položky, jako jsou stránky **Položky dodavatele**, **Věcné položky**, **Položky zboží**, **Nákupní příjemky** a **Účtované nákupní faktury**.

## <a name="see-also"></a>Viz také
[Nakupování](purchasing-manage-purchasing.md)  
[Účtování dokladů a deníků](ui-post-documents-journals.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

