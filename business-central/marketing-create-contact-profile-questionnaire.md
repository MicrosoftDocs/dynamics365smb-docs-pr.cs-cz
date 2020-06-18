---
title: 'Use profiles to classify contacts'
description: 'Set up profile questionnaires to help classify your business contacts'
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 04/01/2020
---

# Použití profilových dotazníků pro klasifikaci obchodních kontaktů
Můžete nastavit dotazníky profilů, které chcete použít při zadávání informací o profilech kontaktů. V každém dotazníku můžete nastavit různé otázky, které chcete položit svým kontaktům.

Dotazník můžete také spustit a automaticky odpovědět na některé otázky na základě údajů o kontaktech, zákaznících nebo dodavatelích.

## Přidání dotazníku profilu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení dotazníku** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Přidání otázek do dotazníku profilu
1. Vyberte příslušný dotazník profilu a poté vyberte akci **Upravit nastavení dotazníku**.
2. Na prvním prázdném řádku v poli **Typ** vyberte **Otázka** a zadejte svou otázku do pole **Popis**. Vyplňte ostatní pole v tomto řádku.
3. Na dalším prázdném řádku v poli **Typ** vyberte **Odpověď** a zadejte svou odpověď do pole **Popis**.
4. V poli **Priorita** vyberte prioritu. V polích **Od hodnoty** a **Do hodnoty** definujte bodový rozsah. Odpověď obdrží kontakty, které získají body v definovaném rozsahu.

Tyto kroky opakujte a zadejte všechny otázky a odpovědi do dotazníku profilu.

Po vytvoření dotazníku musíte vytvořit hodnocení kontaktů, abyste své kontakty klasifikovali. Můžete také nastavit otázky, které jsou hodnoceny automaticky na základě informací na kartě kontaktu.

> [!NOTE]
> Pokud zadáte otázku, která je automaticky zodpovězena, zvolte <STRONG>Řádek</STRONG> a poté zvolte <STRONG>Detaily otázky</STRONG> aby jste zadali kritéria pro automatickou odpověď na otázku.

## Automatická klasifikace kontaktů
Kontakty můžete automaticky klasifikovat podle informací o zákazníkovi, dodavateli a kontaktních údajích nastavením automaticky zodpovězených profilových otázek na stránce **Nastavení dotazníku profilu**.

> [!NOTE]
> Pouze kontakty, které jsou zaznamenány jako zákazníci, mohou být klasifikovány na základě údajů o zákaznících a pouze kontaktům, které jsou zaznamenány jako dodavatelé, může být přiřazena klasifikace na základě údajů o dodavatelích. Automatická klasifikace není automaticky aktualizována. V důsledku toho můžete chtít aktualizovat dotazníky profilu po aktualizaci údajů o zákazníkovi, dodavateli nebo kontaktech, na kterých jsou založeny.

Po nastavení automaticky zodpovězených otázek profilu, pokud přiřadíte dotazník profilu obsahující tyto otázky kontaktu, [!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky přiřadí správné odpovědi kontaktu.

## Příklad
Kontakty můžete klasifikovat podle toho, kolik od vás koupily:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Odpověď</strong></th>
<th><strong>Platí pro</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>kontakty, které koupily za 500 000 LM nebo více</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>kontakty, které nakupovaly za 100 000 až 499 999 LM</p></td>
</tr>
<tr class="odd">
<td><p>C</p></td>
<td><p>kontakty, kteří si koupili za 99 999 LM nebo méně</p></td>
</tr>
</tbody>
</table>

Chcete-li to provést, vyplňte stránku **Nastavení dotazníku profilu** takto:


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Typ</strong></th>
<th><strong>Popis</strong></th>
<th><strong>Automatická klasifikace</strong></th>
<th><strong>Od hodnoty</strong></th>
<th><strong>Do hodnoty</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Otázka</p></td>
<td><p>Klasifikace ABC</p></td>
<td><p>Klepnutím vložíte zaškrtnutí</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Odpověď</p></td>
<td><p>A</p></td>
<td><p> </p></td>
<td><p>500,000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Odpověď</p></td>
<td><p>B</p></td>
<td><p> </p></td>
<td><p>100,000</p></td>
<td><p>499,999</p></td>
</tr>
<tr class="even">
<td><p>Odpověď</p></td>
<td><p>C</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99,999</p></td>
</tr>
</tbody>
</table>

Poté vyplňte stránku **Detaily profilové otázky** takto:
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Pole</strong></th>
<th><strong>Hodnota</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Pole klasifikace zákazníka</strong></td>
<td><emphasis>Prodej (LM)</emphasis></td>
</tr>
<tr>
<td><strong>Metoda klasifikace</strong></td>
<td><emphasis>Definovaná hodnota</emphasis></td>
</tr>
</tbody>
</table>

Když přiřadíte dotazníku profil obsahující tuto otázku kontaktu, aplikace automaticky vloží příslušnou odpověď pro tento kontakt do profilových řádků karty kontaktu.

## Viz také
[Vytváření kontaktů](marketing-create-contact-companies.md)
