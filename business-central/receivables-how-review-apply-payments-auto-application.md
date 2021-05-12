---
title: Verify Automatically Applied Payments, and Reapply Payments Manually | Microsoft Docs
description: After payments are applied automatically, you can review all the entries for a payment and manually reapply those that were applied incorrectly.

author: SorenGP

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.date: 10/01/2020
ms.author: edupont

---
# Ruční kontrola nebo vyrovnání plateb po automatickém vyrovnání
U každého řádku deníku představujícího platbu na stránce **Deníky odsouhlasení plateb** můžete otevřít stránku **Vyrovnání plateb** a zobrazit všechny kandidátní otevřené položky pro platbu a zobrazit detailní informace o každé položce o spolehlivosti párování, na které je založeno vyrovnání platby. Zde můžete ručně vyrovnat platby nebo znovu vyrovnat platby, které byly automaticky vyrovnány na nesprávnou položku. Další informace o automatickém vyrovnání nalezenete na [Odsouhlasení plateb pomocí automatického vyrovnání](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
> Pokud je bankovní účet, který odsouhlasujete nastaven na lokální měnu, poté stránka **Vyrovnání plateb** bude zobrazovat všechny otevřeně položky v lokální měně, včetně otevřených položek dokladů, které byly původně fakturovány v měně cizí. Platby vyrovnané na položky s převedenou měnou proto mohou být účtovány s jinou částkou než na původním dokladu z důvodu potenciálně různých směnných kurzů používaných bankou a [!INCLUDE[prod_short](includes/prod_short.md)].

Proto doporučujeme hledat kódy cizích měn v poli **Kód měny** na stránce **Vyrovnání plateb** a zkontrolovat, zda jsou vyrovnání založeny na převedených měnách. Chcete-li zkontrolovat původní částku dokladu v cizí měně a zobrazit použitý směnný kurz, vyberte pole **Vyrovnává položku číslo** a poté v místní nabídce kliknutím na tlačítko, které rozbalí nabídku otevřete stránky **Položky zákazníka** nebo **Položky dodavatele**.

Jakákoli úprava zisků či ztrát požadovaná v důsledku převodů měny není zpracována automaticky pomocí [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]  
> Nelze vyrovnat položky s rozdílným známénkem, než je na platbě. Chcete-li například uzavřít dobropis se záporným znaménkem a související fakturu s kladným, musíte nejprve vyrovnat dobropis na fakturu a poté vyrovnat platbu na fakturu se sníženou zbývající částkou.

> [!WARNING]  
> Pokud používáte platební slevy a datum platby je před datem splatnosti, potom pole **Zůstat. částka včetně skonta** na stránce **Vyrovnání platby** bude použito pro párování. V opačném případě bude použito pole **Zůstatek**. Pokud byla platba provedena se zlevněnou částkou po datu splatnosti platby nebo byla vyplacena celá částka, ale byla poskytnuta sleva, částka nebude spárována.

> [!NOTE]  
> Platbu můžete vyrovnat pouze na jeden účet. Pokud chcete vyrovnání rozdělit na více otevřených položek, například chcete-li vyrovnat jednorázovou platbu, musí být otevřená položka pro stejný účet. Pro více informací se podívejte na kroky 7 a 8 v postupu tohoto tématu.

## Kontrola nebo vyrovnání plateb po automatickém vyrovnání
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte Mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Deníky odsouhlasení plateb** a poté vyberte související odkaz.
2. Otevřete deník odsouhlasení plateb pro bankovní účet, pro který chcete odsouhlasit platby. Pro více informací navštivte [Automatické odsouhlasení plateb](receivables-how-reconcile-payments-auto-application.md).
3. Na stránce **Deník odsouhlasení plateb**, vyberte platbu, kterou chcete zkontrolovat nebo ručně vyrovnat k jedné nebo více otevřeným položkám a zvolte akci **Vyrovnat ručně**.
4. Vyberte políčko **Vyrovnané** na řádku u otevřené položky, na kterou chcete platbu vyrovnat.
5. Částka platby, která je také zobrazena v poli **Částka transakce** na stránce **Vyrovnání platby** je vložena do pole **Vyrovnaná částka**, ale můžete toto pole upravit, například pokud chcete vyrovnat částku na několik otevřených položek.
6. Chcete-li část zaplacené částky vyrovnat na jinou otevřenou položku pro účet, například k uplatnění paušální platby, zaškrtněte u řádku políčko **Vyrovnáno**. Vyrovnaná částka se automaticky odečte od částky transakcí, aby odrážela rozdělení na dvě otevřené položky.
7. Chcete-li část platby vyrovnat na jednu nebo více otevřených položek, které v databázi neexistují, vytvořte nový řádek pod řádkem pro stejný účet. V poli **Vyrovnaná částka**, zadejte částku, která se má vyrovnat na nový řádek, a poté upravte pole **Vyrovnaná částka** na existujícím řádku.
8. Opakujte kroky 5, 6, nebo 7 pro další otevřené položky, u kterých chcete vyrovnat celou částku nebo část platby.
9. Pokud jste zkontrolovali platební vyrovnání nebo ručně vyrovnali jednu nebo více otevřených položek, zvolte akci **Akceptovat vyrovnání**.

Stránka **Vyrovnání platby** se zavře a na stránce **Deníky odsouhlasení plateb** se hodnota v poli **Spolehlivost párování** změní na **Akceptováno** což znaměná, že jste zkontrolovali nebo ručně vyrovnali platbu.

## Viz také
[Správa pohledávek](receivables-manage-receivables.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]