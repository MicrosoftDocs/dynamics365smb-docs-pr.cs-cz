---
title: Managing VAT Rate changes | Microsoft Docs
description: learn how to sue the VAT Rate Change tool for Dynamics 365 Business Central.
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.workload: na
ms.search.keywords: VAT, VAT rate, posting, tax, value-added tax
ms.date: 06/19/2020
ms.author: andregu

---

# Správa změn sazeb DPH

Sazby DPH se mohou měnit v závislosti na místní legislativě. Jakákoli změna DPH má dopad na vaše data v [!INCLUDE[d365fin](includes/d365fin_md.md)] bez ohledu na to, zda je sazba DPH snížena, zvýšena nebo odstraněna. DPH je spojena s mnoha subjekty v [!INCLUDE[d365fin](includes/d365fin_md.md)], například zákazníci, dodavatelé, zboží, zdroje, poplatky za zboží a finanční účty. Ke změnám sazeb DPH obvykle dochází k určitému datu, od kterého okamžiku budete muset změnit nastavení DPH, účto skupiny atd., pro ujištětní, že nové prodejní objednávky a nákupní objednávky jsou vytvořeny s novou sazbou DPH.

## Změna sazeb DPH

Optimálním přístupem ke správě změny sazby DPH je úplné zaúčtování a uzavření otevřených objednávek a dalších dokladů před datem změny sazby DPH, aby se zajistilo, že tyto dokumenty nebudou změnou ovlivněny. Jedná se o nejčistší přístup, který vám umožní spustit nové objednávky a dokumenty s novou sazbou DPH.

Pro změnu sazby DPH se navrhuje následující přístup

1. Plně zaúčtovat a uzavřít otevřené objednávky, deníky a další doklady před datem přechodu. Můžete počkat až po datu změny, dokud nepřidáte nové řádky a ujistěte se, že datum účinnosti bude před datem přepnutí.
2. Vytvořte nové nastavení DPH.
3. Přepněte DPH na entity (příslušné zákazníky, dodavatele, zboží atd.).
4. K datu přepnutí sazby DPH vytvoříte nové doklady, které budou používat novou sazbu.


> [!NOTE]  
> Aktuálně aktualizujeme nástroj pro změnu sazby DPH.. Níže uvedené funkce nemusí odpovídat funkcím ve vašem prostředí. Aktualizace proběhne do 1.7.2020 a nebude pravidelnou měsíční aktualizací. Místo toho budou všechna prostředí aktualizována automaticky (oprava hotfix). Po dokončení této aktualizace se tato zpráva již nezobrazí.

## Nástroj pro změnu sazby DPH

Nástroj změna sazby DPH může do určité míry pomoci s převodem sazeb DPH na hlavních datech, denících a objednávkách. To je užitečné, pokud chcete snadněji převést DPH na kmenových datech nebo pokud máte objednávky, které nelze uzavřít před datem přechodu a budou zpracovány po delším časovým obdobím, čímž překročíte datum přechodu sazby DPH. V nástroji pro změnu sazby DPH, která platí, existují určitá omezení a omezení.

## Principy procesu a omezení převodu sazby DPH

Nástroj Změna sazby DPH provádí převody sazby DPH pro hlavní data, deníky a objednávky různými způsoby. Vybraná hlavní data a deníky budou aktualizovány novou obecnou účto skupinou zboží nebo DPH účto skupiny zboží. Pokud byla objednávka zcela nebo částečně dodána, bude dodané zboží udržovat aktuální obecnou účto skupinu zboží nebo DPH účto skupinu zboží. Bude vytvořen nový řádek objednávky pro nedodané položky a bude aktualizován tak, aby odpovídal současným a novým  účto skupinám DPH nebo DPH účto skupinám zboží. Kromě toho budou odpovídajícím způsobem aktualizovány přiřazení poplatky zboží, rezervace a informace o sledování zboží.

Na řádcích objednávky bude jednotková cena aktualizována pro všechny řádky typu Zboží a Zdroj, pokud použijete ceny včetně DPH. U ostatních typů řádku je možné rozhodnout, zda má být jednotková cena aktualizována.

Existuje několik věcí, které nástroj nepřevádí:

* Prodejní nebo nákupní objednávky a faktury, kde byly zaúčtovány dodávky. Tyto doklady jsou zaúčtovány pomocí aktuální sazby DPH.
* Doklady, které zaúčtovali jako zálohové faktury. Například jste odeslali nebo obdrželi zálohové faktury, které nebyly dokončeny před použitím nástroje pro změnu sazby DPH. V takovém případě bude rozdíl mezi splatnou DPH a DPH, která byla zaplacena v zálohách po dokončení faktury. Nástroj pro změnu sazby DPH tyto doklady přeskočí a budete je muset ručně aktualizovat.
* Prodejní nebo nákupní objednávky s integrací skladu, pokud jsou částečně dodány nebo přijaty.
* Přímá dodávka.
* Speciální dodávka.
* Montážní zakázky.
* Servisní smlouvy.
* Dobropisy.
* Objednávka vratky.
* Ceny zboží (master data)
* Prodejní ceny (master data)
* Obchodní účto skupiny pro zákazníky a dodavatele.

### Příprava převodu změny sazby DPH

Před nastavením nástroje pro změnu sazby DPH je nutné provést následující.

* Pokud máte transakce, které používají různé sazby, musí být rozděleny do různých skupin buď vytvořením nových účtů hlavní knihy pro každou sazbu, nebo pomocí filtrů dat pro seskupení transakcí podle sazby.
* Pokud vytvoříte nové finanční účty, musíte vytvořit nové obecné účto skupiny.
* Chcete-li snížit počet převedených dokladů, zveřejněte co nejvíce dokladů a zmenšete počet neodeslaných dokladů na minimum.
* Zálohovat data.

### Nastavení nástroje pro změnu sazby DPH

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Nastavení změny sazby DPH** a vyberte související odkaz.
2. Na záložkách **Hlavní data**, **Deníky**, a **Dokumenty**, zvolte hodnotu účto skupiny ze seznamu možností pro potřebná pole. Pro každou skupinu můžete zvolit, zda chcete převést DPH účto skupiny zboží nebo obecné účto skupiny zboží, nebo převést obě hodnoty, pokud jsou k dispozici v položce kmenových dat. U některých oblastí můžete také nastavit filtr pro převod pouze podmnožiny hodnot, například finanční účty.
3. Na záložce **Ceny s DPH** zvolte typy řádků na objednávkách a pro které chcete aktualizovat jednotkové ceny. Jednotkové ceny na řádcích typu Zboží a Zdroj budou vždy aktualizovány.

### Nastavení převodu účto skupiny účto skupiny zboží

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Nastavení změny sazby DPH** a vyberte související odkaz.
2. Na stránce **Nastavení změny sazby DPH** zvolte **Konverze DPH účto skupiny** nebo **Konverze Obecné účto skupiny zboží**.
3. V poli **Od kódu** zadejte aktuální účto skupinu.
4. V poli **Ke Kódu** zadejte novou účto skupinu.

### Provedení převodu změny sazby DPH

Nástroj pro změnu sazby DPH slouží ke správě změn základní sazby DPH. Provádění převodů DPH a obecné účto skupiny, slouží ke změně sazby DPH a udržování přesné vykazování DPH. V závislosti na nastavení jsou provedeny následující změny:

* DPH a obecné účto skupiny jsou převedeny.
* Změny jsou implementovány do účtů hlavní knihy, zákazníků, dodavatelů, otevřených dokladů, řádků deníku atd.

> [!IMPORTANT]  
> Před provedením převodu na změnu sazby DPH můžete tuto konverzi otestovat. Chcete-li tak učinit, postupujte podle následujících kroků, ale zrušte políčka **Provést konverzi** a **Nástroj pro změnu sazby DPH**. Během zkušebního převodu pole **Převedno** v tabulce **Položky protokolu změn sazeb DPH** je prázdné a pole **Datum převodu** v tabulce **Položky protokolu změn sazeb DPH** je prázdné. Po dokončení převodu zvolte **Položky protokolu změn sazeb DPH** k zobrazení výsledků testovacího převodu. Před provedením převodu ověřte každou položku. Ověřte zejména transakce, které používají starou sazbu DPH.

1. Zvolte ![ žárovku, která otevře funkci ](media/ui-search/search_small.png " Řekněte mi, co chcete ") udělat, zadejte **Změny sazby DPH** a pak zvolte odkaz **Nastavení změny sazby DPH** DPH.
2. Ověřte, zda jste již nastavili převod DPH účto skupiny zboží nebo převod obecné účto skupiny zboží.
3. Zvolte políčko **Převést**.

   > [!IMPORTANT]  
   > Zrušte zaškrtuní políčka **Nástroj pro změnu sazby DPH dokončen**. Toto políčko je automaticky zaškrtnuto po dokončení převodu změny sazby DPH.

4. Vyberte akci **Převést**.
5. Po dokončení převodu vyberte akci **Položky protokolu změn sazeb DPH** a zobrazte výsledky převodu.

> [!IMPORTANT]  
> Po převodu se vybere pole **Převedeno** v tabulce **Položky protokolu změn sazeb DPH** a pole **Datum převodu** v tabulce **Položky protokolu změn sazeb DPH** zobrazuje datum převodu.

## Viz také

[Nastavení daně z přidané hodnoty ](finance-setup-vat.md)  
[Nastavení nerealizované daně z přidané hodnoty](finance-setup-unrealized-vat.md)  
[Reportování DPH finančímu úřadu](finance-how-report-vat.md)  
[Práce s DPH v prodeji a nákupu](finance-work-with-vat.md)  
[Lokální funkcionality v Business Central](about-localization.md)
