---
title: Use Item Cross-References| Microsoft Docs
description: If you set up a cross-reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.** field.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 04/01/2020
ms.author: sgroespe

---
# Použití křížových odkazů zboží
Pokud nastavíte křížový odkaz mezi popisem zboží, který používáte pro zboží, a popisem, který používá prodejce daného zboží pomocí vyplnění pole **Č.křížového odkazu** je popis zboží dodavatele automaticky vložen do nákupních dokladů pro dodavatele. Stejná funkce platí pro čísla zboží zákazníků v prodejních dokladech.

Následující postupy popisují, jak používat křížové odkazy pro zboží na straně nákupu. Kroky jsou podobné i pro stranu prodeje.

## Nastavení křížového odkazu zboží na popis zboží dodavatele
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží** a poté vyberte související odkaz.
2. Otevřete kartu zboží, pro které chcete vytvořit křížový odkaz na popis zboží, který dodavatel používá pro toto zboží.
3. Vyberte akci **Křížové odkazy**.
4. Na novém řádku na stránce **Položky kříž.odkazů zboží** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## Zadání popisu zboží dodavatele v nákupní objednávce
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní objednávky** a poté vyberte související odkaz.
2. Vytvořte nákupní objednávku pro dodavatele, pro kterého jste nastavili křížový odkaz na zboží v předchozím postupu.
3. Vytvořte nákupní řádek pro zboží, pro které jste nastavili křížový odkaz na zboží v předchozím postupu.
4. V poli **Č.křížového odkazu** vyberte křížový odkaz zboží, které jste vytvořili, a poté zvolte tlačítko **OK**.

Pole **Popis** na řádku je přepsáno popisem zboží dodavatele, jak je nastaveno na položce křížového odkazu zboží.

## Viz také
[Evidence nového zboží](inventory-how-register-new-items.md)  
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
