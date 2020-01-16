---
title: Czech Local Functionality - Inventory | Microsoft Docs
description: This section describes local functionality - Inventory
author: ACMartinKunes

ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, CashDesk, Finance, CZ, Cash, Inventory
ms.date: 12/30/2019
ms.reviewer: v-pejano
ms.author: v-makune
---

# Zásoby

## Účto skupiny v objednávkách transferu
České účetní standardy vyžadují, aby byly transfery účtovány s předepsaným Účtem adjustace Zásob odlišným od ostatních účtování v deníku zboží.
Do objednávek transferu byla doplněna pole pro obecné obchodní účto skupiny pro účtování dodávky a příjmu. Tato funkcionalita umožnuje účtovat různé objednávky transferu s různým Nastavením obecného účtování, i s nastavením různým od účtování v deníku zboží.
V trasách transferu, pole pro obecné obchodní účto skupiny pro účtování dodávky a příjmu. Toto nastavení je automaticky kopírováno do objednávky transferu na základě použité trasy transferu.
## Účtování zaokrouhlení v zásobách
Účet zaokrouhlení v zásobách umožňuje zaúčtovat všechny náklady ze zaokrouhlení na jiný finanční účet než je účet adjustace zásob.  Tato funkce umožňuje zaúčtovat částky zaokrouhlení na jiný účet než původní pořizovací cenu.
## Odsouhlasení zásoby - finance 
Podle českých specifických požadavků musí formulář matice Odsouhlasení zásoby - finance vzít v úvahu specifické české účty pro zaúčtování zásob: Účet zaokrouhlení zásob a Účet nedokončené výroby. Vzhledem k tomu, že česká lokalizovaná aplikace obsahuje úpravy v účtování zásob, musí být do formuláře Odsouhlasení zásoby - finance zahrnuty i speciální účty pro zaokrouhlování a speciální účty NV. Tyto úpravy byly zavedeny společně s změněnými procedurami výpočtu.
## Rozšíření přípravy fyzické inventury 
Pro dodržování účetních standardů vyžadují společnosti odlišení účtování mank a přebytků v rámci fyzické inventury. Díky nastavení výchozích šablon skladového pohybu pro tyto pohyby zásob v Nastavení zásob může uživatel snadno změnit Obecnou  obchodní účto skupinu v závislosti na typu pohybu zásob.
Společnosti potřebují odlišit účtování inventarizačních pohybů zásob stejného zboží, proto vyžadují rozdělení řádků deníku fyzické inventury. Takovéto účtování je vyžadováno z právních důvodů. Například, potřebují mít jiné účtování pro manka v limitu a jiné pro manka nad limit.
## Skladové účetní doklady
Uživatelé provádějí operace s inventářem jako například: snížení hodnoty, převody a přecenění zásob. Musí mít pro tyto operace možnost tisknout doklady, které splňují zákonné požadavky.
Uživatelé také chtějí tisknout doklady pro již zúčtované operace zásob. 
Z výše uvedených důvodů tato funkce poskytuje následující sestavy: 
- Sestava Pohyb zásob se používá k tisku dokumentů z deníků zboží.
- Sestava Zaúčtovaný doklad zásob se používá k tisku zaúčtovaných operací zásob.
## Doklady fyzické inventury
Na konci období uživatelé provádějí fyzickou inventuru, aby sladili skutečnou (fyzickou) hodnotu zásob s hodnotou registrovanou v systému. V rámci tohoto procesu potřebuje účetní oddělení archivovat inventarizační doklad obsahující zaúčtované hodnoty se jmény zástupců společnosti, kteří potvrdí svým podpisem, že množství a částky uvedené v tomto dokumentu odpovídají fyzicky přítomnému množství na lokacích zásob. 
Z výše uvedených důvodů tato funkce poskytuje následující sestavy: 
-   Seznam fyzické inventury se používá k tisku dokumentů   z deníku fyzické inventury (stávající sestava byla vylepšena).
-   Doklad o fyzické inventuře se používá k tisku zaúčtované fyzické inventury. fyzické inventury.



## Viz také
[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](finance.md)
