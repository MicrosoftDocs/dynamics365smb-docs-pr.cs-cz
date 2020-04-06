---
title: Manage, delete, or compress documents | Microsoft Docs
description: Keep your historical data or delete it.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 10/01/2019
ms.author: edupont

---
# Správa dokladů
Ústřední role, jako je například správce aplikace, musí pravidelně řešit shromažďování historických dokladů, jejich odstraněním, nebo kompresí.

## Odstranění dokladů
V určitých situacích bude možná nutné smazat fakturované nákupní objednávky, které nebyly odstraněny. [!INCLUDE[d365fin](includes/d365fin_md.md)] zkontroluje, zda jste smazané objednávky plně fakturovali. Nemůžete smazat objednávky, které jste plně nefakturovali a neobdrželi.

Objednávky vratek jsou obvykle vymazány po jejich fakturaci. Když zaúčtujete fakturu, převede se na stránku **Zaúčtovaný nák.dobropis**. Pokud jste zaškrtli políčko **Dodávka vratky při dobropisu** na stránce **Nastavení nákupu a závazků**, bude faktura převedena na stránku **Účtovaná dodávka vratky**. Dokumenty můžete odstranit pomocí dávkové úlohy **Odstranit fakt. nák. obj.vratky.**. Před odstraněním dávková úloha zkontroluje, zda jsou objednávky na vrácení zboží zcela dodány a vyfakturovány.

Nákupní hromadné objednávky nejsou po zpracování a fakturaci všech souvisejících nákupních objednávek odstraněny. Hromadné objednávky můžete odstranit dávkovou úlohou **Odstranit fakturované hrom. nák. objednávky**.

Fakturované servisní zakázky jsou obvykle po úplné fakturaci vymazány automaticky. Po zaúčtování faktury se vytvoří odpovídající položka na stránce **Zaúčtované faktury servisu**. Zaúčtovaný dokument lze zobrazit na stránce **Zaúčtované faktury servisu**.

Servisní zakázky nejsou automaticky odstraněny, pokud však celkové množství na objednávce nebylo zaúčtováno ze samotné servisní zakázky, ale ze stránky **Faktura servisu**, pak budete muset odstranit fakturované objednávky, které nebyly odstraněny. To lze provést spuštěním dávkové úlohy **Odstranit fakturované servisní zakázky**.

## Viz také
[Správa](admin-setup-and-administration.md)
