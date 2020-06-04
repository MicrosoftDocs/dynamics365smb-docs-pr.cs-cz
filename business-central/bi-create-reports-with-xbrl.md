---
title: How to Create Reports with XBRL | Microsoft Docs
description: XBRL, which stands for eXtensible Business Reporting Language, is an XML-based language for tagging financial data, and enabling businesses to efficiently and accurately process and share their data.
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
# Vytváření sestav pomocí XBRL
XBRL, což je zkratka pro eXtensible Business Reporting Language, je jazyk založený na XML pro označování finančních dat a umožňuje podnikům efektivně a přesně zpracovávat a sdílet jejich data. Iniciativa XBRL umožňuje globální finanční výkaznictví mnoha softwarových společností ERP a mezinárodních účetních organizací. Cílem této iniciativy je poskytnout standard pro jednotné vykazování finančních informací bankám, investorům a vládním orgánům. Takové obchodní sestavy mohou zahrnovat:

• Finanční výkazy
• Finanční informace
• Nefinanční informace
• Regulační podání, jako jsou roční a čtvrtletní finanční výkazy

[!INCLUDE[d365fin](includes/d365fin_md.md)] umožňuje společnostem implementovat data do XBRL a využít flexibilitu a automatizaci, která zajišťuje sběr i sdílení dat.

## eXtensible Business Reporting Language
XBRL (e **X**tensible **B**usiness **R**eporting **L**anguage) je jazyk založený na XML pro finanční výkaznictví. XBRL poskytuje standard pro jednotné vykazování pro všechny uživatele dodavatelského řetězce finančních informací; jako jsou veřejné a soukromé společnosti, účetní profese, regulátoři, analytici, investiční komunita, kapitálové trhy a věřitelé, jakož i klíčové třetí strany, jako jsou vývojáři softwaru a agregátoři dat.

Taxonomie spravuje www.xbrl.org. Můžete si stáhnout taxonomie nebo si přečíst podrobnější informace na webu XBRL.

Někdo, kdo od vás chce finanční informace, vám poskytne taxonomii (dokument XML) obsahující jedno nebo více schémat, z nichž každé vyplní jeden nebo více řádků. Řádky odpovídají jednotlivým finančním skutečnostem požadovaným odesílatelem. Tuto taxonomii importujete do aplikace a poté vyplníte schéma (schémata) zadáním účtů, které odpovídají každému řádku, může se také použít časový rámec například čistá změna nebo zůstatek k datu. V některých případech můžete místo toho zadat konstantu, například počet zaměstnanců. Nyní jste připraveni odeslat instanční dokument (dokument XML) někomu, kdo požaduje informace. Myšlenka je taková, že se může jednat o opakující se událost, takže pokud nebyly provedeny změny v taxonomii, exportujete pouze nové instanční dokumenty pro nová období na vyžádání.

## XBRL se skládá z následujících komponent
**Specifikace** XBRL vysvětluje, co je XBRL, jak vytvářet instanční dokumenty XBRL a taxonomie XBRL. Specifikace XBRL vysvětluje XBRL z technického hlediska a je určena pro technické publikum.

**Schéma** XBRL je základ nízkoúrovňové komponenty XBRL. Schéma je fyzický soubor XSD, který vyjadřuje, jak se mají vytvářet instance a taxonomie.

**Propojení** XBRL jsou fyzické soubory XML, které obsahují různé informace o prvcích definovaných ve schématu XBRL, jako jsou popisky v jednom nebo více jazycích, jejich vzájemný vztah, sčítání prvků, atd.

**Taxonomie** XBRL je "slovní zásoba" nebo "slovník" vytvořený skupinou, která je v souladu se specifikací XBRL, za účelem výměny obchodních informací.

**Instanční dokument** XBRL je obchodní sestava, například finanční výkaz připravený pro specifikaci XBRL. Význam hodnot v instančním dokumentu je vysvětlen taxonomií. Instanční dokument je poněkud zbytečný, pokud neznáte taxonomii, na kterou je připraven.

## Vrstvené taxonomie
Taxonomie se může skládat ze základní taxonomie, například us-gaap nebo IAS, a poté může mít jedno nebo více rozšíření. Aby se to zohlednilo, taxonomie odkazuje na jedno nebo více schémat, které jsou všechny samostatné taxonomie. Když jsou do databáze načteny další taxonomie, nové prvky jsou jednoduše přidány na konec existujících prvků.

## Propojení
V XBRL Sp. 2 je taxonomie popsána v několika souborech XML. Primární soubor XML je samotný soubor schématu taxonomie (soubor.xsd), který obsahuje pouze neuspořádaný seznam prvků nebo skutečností, které se mají vykazovat. Kromě toho jsou obvykle spojeny některé soubory pomocí propojení (.xml). Soubory propojení obsahují data, která doplňují prvotní taxonomii (soubor .xsd). Existuje šest typů souborů propojení, z nichž čtyři mají význam pro název produktu XBRL. Jedná se o:

- Báze odkazů pro popisky: Tato propojení obsahuje popisky nebo názvy prvků. Soubor může obsahovat štítky v různých jazycích, které jsou identifikovány vlastností XML nazvanou 'lang'. Identifikátor jazyka XML obvykle obsahuje dvoupísmennou zkratku, a přestože by mělo být snadné uhodnout, co zkratka znamená, neexistuje žádná souvislost s kódem jazyka Windows nebo s kódy jazyků definovanými v ukázkových datech. Když tedy uživatel vyhledá jazyky pro konkrétní taxonomii, uvidí všechny štítky pro první prvek v taxonomii, což znamená, že pak může vidět příklad každého jazyka. Taxonomie může mít připojeno několik bází odkazů pro popisky, pokud tyto propojení obsahují různé jazyky.

- Báze odkazů pro prezentace: Tato propojení obsahuje informace o struktuře prvků, nebo přesněji; jak emitent taxonomie navrhuje, aby aplikace prezentovala taxonomii uživateli. Propojení obsahuje řadu odkazů, z nichž každý spojuje dva prvky jako nadřazený a podřízený. Při použití všech těchto odkazů lze prvky zobrazit hierarchicky. Všimněte si, že prezentace propojení se zabývá právě tím: prezentací prvků uživateli.

- Báze odkazů pro výpočty: Tato propojení obsahuje informace o tom, ke kterým prvkům dojde. Struktura je velmi podobná bázi odkazů pro prezentace, s tím rozdílem, že každý odkaz nebo 'arc', jak se jim říká, má vlastnost takzvané hmotnosti. Hmotnost může být buď 1 nebo –1 označující, zda prvek má být přidán nebo odečten od nadřazeného prvku. Všimněte si, že souhrny nemusí nutně odpovídat vizuální prezentaci.

- Referenční báze odkazů: Tento soubor odkazů je soubor XML, který obsahuje doplňující informace o datech, které jsou vyžadovány vystavitelem taxonomie.

## Nastavení řádků XBRL
Po importu nebo aktualizaci taxonomie musí být řádky schémat zadány se všemi požadovanými informacemi. Tyto informace budou zahrnovat základní informace o společnosti, skutečnou účetní závěrku, poznámky k účetní závěrce, doplňkové plány a další informace, které jsou nezbytné pro splnění konkrétních požadavků na finanční výkaznictví.

Řádky XBRL nastavíte mapováním dat v taxonomii na data v hlavní knize.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Taxonomie XBRL** a poté vyberte související odkaz.
2. Na stránce **Taxonomie XBRL** vyberte taxonomii ze seznamu.
3. Vyberte akci **Řádky**.
4. Vyberte řádek a vyplňte pole.
5. Chcete-li si přečíst podrobné informace o tom, co vyplnit, vyberte akci **Informace**.
6. Chcete-li nastavit mapování účtů hlavní knihy v účetní osnově na řádky XBRL, vyberte akci **Řádky propojení financí**.
7. Chcete-li k finančnímu výkazu přidat poznámky, vyberte akci **Poznámky**.

> [!NOTE]
> Můžete exportovat pouze data, která odpovídají typu zdroje, který jste vybrali v poli **Typ původu**, který obsahuje popis a poznámky.

> [!NOTE]
> Řádky, které nejsou relevantní, lze označit jako typ řádku **Nelze použít** takže řádky nebudou exportovány.

## Import taxonomie XBRL
Prvním krokem při práci s funkcí XBRL je import taxonomie do databáze společnosti. Taxonomie sestává z jednoho nebo více schémat a některých propojení. Po dokončení importu schémat i vazebních základů a použití propojovacích základů schématu můžete nastavit řádky a namapovat účty hlavní knihy v účtové osnově na příslušné řádky taxonomie.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Taxonomie XBRL** a poté vyberte související odkaz.
2. Na stránce **Taxonomie XBRL** vytvořte nový řádek a zadejte název a popis taxonomie.
3. Vyberte akci **Schémata** a vložte popis schématu.
4. Chcete-li schéma importovat, vyberte na stránce **Schémata XBRL** akci **Import** a vyberte složku a soubor XSD. Vyberte tlačítko **Otevřít**.
5. Chcete-li importovat základnu propojení, na stránce **Schémata XBRL** vyberte akci **Propojení** a poté vyberte složku a soubor XML. Vyberte tlačítko **Otevřít**.
6. Nyní můžete zvolit použití propojení na schéma. Opakujte, dokud neimportujete všechny základny propojení.
7. Vyberte akci **Použít pro taxonomii**, abyste použili základnu propojení na schéma.

> [!IMPORTANT]
> Namísto jednotlivého použití propojení po importu můžete počkat, až naimportujete všechny propojení a poté je použít současně. Chcete-li to provést, zvolte tlačítko **NE** , když se zobrazí výzva k použití nově importovaného propojení do schématu. Poté vyberte řádky s propojením, které chcete použít.

## Aktualizace taxonomie XBRL
Při změně taxonomie je třeba odpovídajícím způsobem aktualizovat aktuální taxonomii. Důvodem aktualizace může být změněné schéma, změněné propojení nebo nové propojení. Po aktualizaci taxonomie stačí mapovat řádky pro změněné nebo nové řádky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Taxonomie XBRL** a poté vyberte související odkaz.
2. Na stránce **Taxonomie XBRL** vyberte akci **Schémata**.
3. Chcete-li aktualizovat schéma, vyberte schéma, které chcete aktualizovat, a poté vyberte akci **Import**.
4. Chcete-li aktualizovat nebo přidat novou základnu propojení, vyberte akci **Propojení**.
5. Vyberte příslušnou základnu odkazů nebo stiskněte Ctrl+N pro nový řádek, vyberte typ propojení a vložte popis.
6. Chcete-li importovat základnu propojení, vyberte akci **Import**.
7. Klepnutím na tlačítko **Ano** aplikujte základnu propojení na schéma.

## Viz Související školení na [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index)

## Viz také
[Finance](finance.md)  
[Business Intelligence](bi.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
