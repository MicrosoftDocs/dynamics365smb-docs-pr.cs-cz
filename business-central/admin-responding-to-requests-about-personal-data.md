---
title: Responding to Requests About Personal Data
description: You must respond to data subject requests.
author: bholtorf

ms.service: dynamics365-business-central
ms.author: bholtorf
ms.custom: na
ms.date: 10/01/2019
ms.reviewer: na
ms.topic: article
---

# Odpověď na žádost o osobní informace
Datové subjekty mohou požadovat několik typů akcí týkajících se jejich osobních údajů. Například podle Obecného nařízení o ochraně osobních údajů (GDPR) mají obyvatelé EU právo požadovat export, úpravu a vymazání svých osobních údajů. Toto je známo jako *Žádost subjektu údajů*. Pokud jste klasifikovali citlivost vašich dat a jste si jisti, že jsou správná, může správce reagovat na požadavky pomocí možností na záložce **Ochrana soukromí** v Centru rolí **Správce IT**. Pro více informací o klasifikaci dat a klasifikaci citlivostí dat v [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], navštivte [Klasifikace dat](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) a [Klasifikace citlivosti dat](admin-classifying-data-sensitivity.md).

## Typy žádostí

V následující tabulce jsou uvedeny příklady typů požadavků, na které můžete odpovědět.

> [!Note]
> Přestože jsme to my, kdo poskytuje možnosti reagovat na tyto typy požadavků, a tím získat přístup k osobním údajům, je vaší odpovědností zajistit, aby osobní a citlivé údaje byly správně lokalizovány a klasifikovány.

| Typ požadavku | Popis a navrhovaná odpověď |
|-----|-----|
| Žádosti o přenesení | Datový subjekt může podat žádost o přenositelnost údajů, což znamená, že musíte exportovat osobní údaje subjektu údajů ze svých systémů a poskytnout je ve strukturovaném, běžně používaném formátu. Chcete-li reagovat na tyto požadavky, můžete k exportu osobních údajů do souboru aplikace Excel nebo konfiguračního balíčku RapidStart použít **Nástroj pro ochranu dat**.  Pomocí Excelu můžete upravovat osobní data a ukládat je do běžně používaného, strojově čitelného formátu, například ve formátu CSV nebo XML. U konfiguračních balíčků RapidStart můžete nakonfigurovat tabulky hlavních dat a jejich související tabulky, které obsahují osobní data. <br><br> **Note:** Při exportu dat zadáváte minimální úroveň citlivosti. Export bude zahrnovat minimální a všechny úrovně citlivosti nad ní. Pokud se například rozhodnete exportovat data, která jsou klasifikována jako osobní, bude export zahrnovat také data, která jsou klasifikována jako citlivá. <br><br> Při exportu dat souvisejících s datovým subjektem **Nástroj pro ochranu dat** hledá přímé vztahy mezi datovým subjektem a daty vztahujícími se k subjektu údajů. Nepřímé vztahy mezi údaji souvisejícími s datovým subjektem a dalšími daty nejsou automaticky exportovány **Nástrojem pro ochranu dat**. Například tabulka kontaktů má přímo související data odpovědí profilu kontaktů a tabulka odpovědí profilu kontaktů dále souvisí s daty o profilových otázkách. Pokud chcete exportovat také profilové otázky, musíte tuto tabulku přidat ručně jako řádek s příslušnými filtry v konfiguračním balíčku, který vytvoří **Nástroj pro ochranu dat**. |
| Žádosti o výmaz | Datový subjekt může požádat o vymazání jejich osobních údajů. Existuje několik způsobů, jak odstranit osobní údaje pomocí možností přizpůsobení, ale rozhodnutí a implementace je vaší odpovědností. V některých případech se můžete rozhodnout upravit svá data přímou cestou, například odstranit kontakt a poté spustit dávkovou úlohu Odstranit položky protokolu, abyste smazali interakce kontaktu. <br><br> **Note:** Pokud jste určili datum v poli **Povolit odstranění dokladu před datem** na stránkách **Nastavení prodeje a pohledávek** nebo **Nastavení nákupu a závazků**, možná budete muset změnit datum, abyste mohli smazat zaúčtované prodejní a nákupní doklady, které jste vytiskli a které mají datum zaúčtování k tomuto datu nebo dříve. |
| Žádosti o úpravu | Datový subjekt může požadovat opravu nepřesných osobních údajů. Existuje několik způsobů, jak toho dosáhnout. V některých případech můžete exportovat seznamy do aplikace Excel a hromadně upravovat více záznamů, následně můžete importovat aktualizovaná data. Pro více informací navštivte [Export vašich obchodních dat do Excelu](about-export-data.md). Můžete také ručně upravit pole obsahující osobní údaje, například úpravy informací o zákazníkovi na kartě Zákazníka. Záznamy transakcí, jako jsou věcné položky, položky zákazníka a daně, jsou však nezbytné pro integritu systému plánování zdrojů organizace. Pokud ukládáte osobní údaje do záznamů obchodních transakcí, zvažte použití možností přizpůsobení k úpravě těchto osobních údajů. |

## Omezení zpracovávání dat pro datový subjekt
Datový subjekt může požádat o dočasné zastavení zpracovávání jejich osobních údajů. Chcete-li těmto požadavkům vyhovět, můžete jejich záznam označit jako blokovaný z důvodu ochrany osobních údajů a zastavit zpracovávání jejich dat. Pokud je záznam označen jako blokovaný, nelze vytvořit nové transakce, které tento záznam používají. Nemůžete například vytvořit novou fakturu pro zákazníka, když je zákazník nebo prodejce zablokován. Chcete-li označit datový subjekt jako blokovaný, otevřete kartu datového subjektu, například karty zákazníka, dodavatele nebo kartu kontaktu, a zaškrtněte pole **Uzavřeno-ochrana soukromí**. Možná budete pro zobrazení pole muset zvolit **Zobrazit více**.

## Zpracovávání žádostí datového subjektu ve zkušební verzi
Některé typy osobních údajů jsou součástí vašeho účtu Office 365 a vyžadují administrativní přístup k exportu, pokud od uživatele obdržíte žádost datového subjektu ohledně tohoto typu osobních údajů podle Obecného nařízení o ochraně osobních údajů (GDPR). Proces zpracování požadavků datového subjektu se liší v závislosti na typu klienta [!INCLUDE[d365fin](includes/d365fin_md.md)].

Pokud máte placené předplatné pro [!INCLUDE[d365fin](includes/d365fin_md.md)], musíte kontaktovat správce klienta vaší organizace a žádat subjekt údajů. Správce má administrátorská práva a nástroje pro splnění vaší žádosti.

Pokud jste se zaregistrovali pro [!INCLUDE[d365fin](includes/d365fin_md.md)] ze stránky [Zkušební verze](https://trials.dynamics.com/) a nevystoupili jste z této zkušební zkušenosti prostřednictvím placeného předplatného správcem vaší organizace, pak můžete vyplnit svou vlastní žádost subjektu údajů na stránce [ Ochrana osobních údajů v práci a škole na portálu Azure](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade). Zde můžete exportovat a stáhnout své osobní údaje.

Také na stránce Ochrana osobních údajů v práci a ve škole můžete svůj účet uzavřít. Doporučujeme však nejprve exportovat a smazat všechna data, protože smazání účtu znamená, že ztratíte přístup k [!INCLUDE[d365fin](includes/d365fin_md.md)].

Stále můžete označit uživatele jako blokované z důvodu ochrany osobních údajů a exportovat, upravovat nebo odstraňovat transakce, jak je v tomto článku vysvětleno výše.

## Exportování dat z tabulek neklasifikovaných datovým subjektem
Pokud máte situaci, kdy musíte exportovat data, která nejsou klasifikována tak, aby byla automaticky exportována, například data z tabulky Odpovědi profilů, musíte provést následující kroky:
- Zvažte, zda opravdu chcete nebo musíte exportovat tato doplňková data, která nesouvisí s kontaktem, což znamená, že k nim nemá žádný přímý vztah.
- Přidejte tuto tabulku a vztah ručně do balíčku Rapid Start a exportujte jej přímo z balíčku Rapid Start - proto pro vás vygenerujeme balíček Rapid Start, abyste jej mohli vyladit v takových situacích.

## Zpracování údajů nezletilých
Pokud je věk kontaktní osoby nižší než věk zákonného souhlasu podle zákonů ve vaší oblasti, můžete to označit zaškrtnutím políčka **Nezletilý** na kartě **Kontaktu**. Když tak učiníte, je automaticky zaškrtnuto políčko **Uzavřeno-ochrana soukromí**. Pokud obdržíte souhlas od rodiče nebo zákonného zástupce nezletilé osoby, můžete pro odblokování kontaktu zvolit pole **Rodičovský souhlas byl přijat**. Přestože můžete zpracovávat osobní údaje pro nezletilé, nemůžete použít funkci profilování v Dynamics 365 pro prodej.

> [!Note]
> Protokol změn může zaznamenávat podrobnosti, například kdy a kým bylo zaškrtnuto políčko **Rodičovský souhlas byl přijat**. Správce to může nastavit pomocí průvodce **Nastavení protokolu změn**, a také zaškrtnutím políčka **Protokolová změna rodičovského souhlasu byla přijata** na kartě **Kontaktu**. Pro více informací navštivte [Zaznamenávání změn](across-log-changes.md).

## Viz také
[Klasifikace dat](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Klasifikace citlivosti dat](admin-classifying-data-sensitivity.md)  
[Export vašich obchodních dat do Excelu](about-export-data.md)  
[Zaznamenávání změn](across-log-changes.md)  
[Žádosti datových subjektů podle GDPR](/microsoft-365/compliance/gdpr-data-subject-requests)
