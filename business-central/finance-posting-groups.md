---
title: Nastavení účto skupiny | Microsoft Docs
description: 'Přehled účtovacích skupin, které můžete použít, abyste ušetřili čas a vyhnuli se chybám při účtování transakcí.'
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'posting setup, initialize'
ms.date: 03/05/2019
ms.author: bholtorf
---
# <a name="setting-up-posting-groups"></a>Nastavení účto skupin
Účetní skupiny mapují položky, jako jsou zákazníci, dodavatelé, zboží, zdroje, nebo prodejní a nákupní doklady, do finančních účtů hlavní knihy. Šetří čas a pomáhají se vyhnout chybám při účtování transakcí. Hodnoty transakcí přejdou na účty určené v účtovací skupině pro tento konkrétní subjekt. Jediným požadavkem je mít účtovací osnovu. Další informace naleznete v části [Nastavení účtovací osnovy](finance-setup-chart-accounts.md).  

Účtovací skupiny jsou zastřešeny pod třemi podkategoriemi:  

* Obecné - Definují, od koho nakupujete a komu prodáváte, nebo co nakupujete a co prodáváte. Můžete také zkombinovat skupiny a specifikovat věci, jako jsou účty ve výsledovce, do kterých chcete účtovat, nebo použijte skupiny pro filtrování sestav.  
* Specifické - Použijte například prodejní doklady, místo přímého účtování do hlavní knihy. Když vytvoříte položky zákazníka, v hlavní knize se provedou odpovídající záznamy.  
* Daňové - Definujte procenta daně a typy výpočtu, které se vztahují na to, od koho nakupujete a komu prodáváte, nebo co nakupujete a co prodáváte.

Následující tabulka popisuje účto skupiny pod každou podskupinou.  

| Obecné účetní skupiny | Popis |
| --- | --- |
| Obecné obchodní účto skupiny |Přiřaďte tuto skupinu zákazníkům a dodavatelům a určete, komu prodáváte a od koho nakupujete. To nastavíte na **Obec.  obchodní účto skupiny** Když tak učiníte, přemýšlejte, kolik skupin budete potřebovat k rozdělení prodejů a nákupů. Seskupte například zákazníky a dodavatele podle zeměpisné oblasti nebo podle typu podnikání. |
| Obecné účto skupiny zboží |Přiřaďte tuto skupinu zboží, nebo prostředkům a určete, co prodáváte a co nakupujete. To nastavíte na **Obec.  účto skupiny zboží** Když tak učiníte, zvažte počet skupin, které budete potřebovat k rozdělení prodejů podle produktů (zboží a služeb) a nákupů podle položek. Například rozdělte tyto skupiny podle surovin, maloobchodu, zdrojů, kapacity atd. |
| Nastavení obecného účtování |Zkombinujte obchodní účtovací skupiny a účtovací skupiny zboží a vyberte účty, na které chcete účtovat. Pro každou kombinaci obchodní účtovací skupiny a účtovací skupiny zboží, můžete přiřadit sadu účtů hlavní knihy. To například znamená, že můžete prodej stejné položky zaúčtovat na různé prodejní účty v hlavní knize, protože zákazníci jsou přiřazeni k různým obchodním účtovacím skupinám. To lze nastavit na stránce **Nastavení obecného účtování**. |

| Specifické účetní skupiny | Popis |
| --- | --- |
| Účtovací skupina zákazníka |Definujte účty, které se mají použít při účtování transakcí s pohledávkami. Pokud používáte inventář s pohledávkami, obecná obchodní účtovací skupina přiřazená vašemu zákazníkovi a skupina obecných účtovacích zboží přiřazená k položce inventáře určují účty, na které se řádky prodejních objednávek zaúčtují. Viz „Obecné obchodní účto skupiny“ a „Obecné účto skupiny zboží“ v **Obecné účetní skupiny**. Tyto nastavte na stránce **Účetní skupiny zákazníka**. |
| Účetní skupiny dodavatele |Definuje, kde se mají účtovat transakce u účtů závazků, účtů poplatků za služby a účtů slev. Toto je podobné Účtovacím skupinám zákazníků. Tyto nastavte na stránce **Účto skupiny dodavatele**. |
| Účetní skupiny zboží |Definujte Účetní skupiny zboží, které pak přiřadíte k příslušným účtům zboží na stránce **Nastavení účtování zásob**. Když tímto způsobem zaúčtujete položky týkající se zboží, systém zaúčtuje na účet hlavní knihy, který je nastaven pro kombinaci účetní skupiny zboží a umístění, které je se zbožím spojeno. Účetní skupiny zboží také poskytují dobrý způsob, jak uspořádat váš inventář, takže při generování sestav můžete oddělit položky podle jejich skupiny účtování. Tyto nastavte na stránce **Účto skupiny zboží**. |
| Účtovací skupina bankovního účtu |Definuje účty pro bankovní účty. To může například zjednodušit procesy trasování transakcí a sladění bankovních účtů. Tyto nastavte na stránce **Účto skupiny bankovního účtu**. |
| Účtovací skupiny dlouhodobého majetku |Definuje účty pro různé typy nákladů a nákladů, jako jsou pořizovací náklady, kumulované odpisy, pořizovací náklady na vyřazení, akumulované odpisy na vyřazení, zisky z vyřazení, ztráty z vyřazení, náklady na údržbu a odpisy. Tyto nastavte na stránce **Účto skupiny DM **. |

| Daňové účto skupiny | Popis |
| --- | --- |
| Daňové obchodní účto skupiny |Určí, jak vypočítat a účtovat daň z obratu pro zákazníky a dodavatele. Tyto nastavte na stránce **DPH obchodní účto skupiny**. Když to uděláte, přemýšlejte, kolik skupin budete potřebovat. Toto může například záviset na faktorech jako místní legislativa, anebo jestli obchodujete na domácím i mezinárodním trhu. |
| Daňové účto skupiny zboží |Uvádí daňové výpočty potřebné pro typy položek nebo prostředků, které kupujete nebo prodáváte. |
| Nastavení účtování daní |Kombinuje Daň.obch.účto skupiny a DPH účto skupiny zboží. Když vyplníte řádek finančního deníku, nákupní řádek nebo prodejní řádek, podíváme se na kombinaci, abychom identifikovali účty, které se mají použít. |

## <a name="example-of-linking-posting-groups"></a>Příklad propojení skupin účtování
Zde je scénář.  

Na kartě zákazníka jsou vybrány tyto skupiny účtování:  

* Obecné obchodní účto skupiny
* Účto skupina zákazníka  

Na kartě zboží jsou vybrány tyto skupiny účtování:  

* Obecné účto skupiny zboží  
* Účto skupiny zboží  

Při vytváření prodejního dokladu, používá záhlaví prodeje informace ze zákaznické karty a prodejní řádky používají informace z karty zboží.  

* Účtování o výnosech (výsledovka) je určeno kombinací Obecné obchodní účto skupiny a Obecné účto skupiny zboží.  
* Účtování pohledávek (rozvaha) je určováno Účto skupinou zákazníka.  
* Účtování zboží (rozvaha) je určováno Účto skupinou zboží.  
* Náklady na účtování prodaného zboží (výsledovka) je určeno kombinací Obecné obchodní účto skupiny a Obecné účto skupiny zboží.  

Vaše nastavení určuje, kdy dojde k zúčtování. Načasování je například ovlivněno, kdy vykonáváte pravidelné činnosti, jako je účtování nákladů na zásoby nebo úprava nákladových položek zboží.

## <a name="copying-posting-setup-lines"></a>Kopírování řádků nastavení účtování
Čím více skupin produktů a firemních účtů máte, tím více řádků uvidíte na stránce Nastavení obecného účtování. To může pro společnost znamenat spoustu zadávání dat, aby nastavila Nastavení obecného účtování. I když zde může existovat mnoho různých kombinací účtování skupin pro firmy a zboží, mohou se na stejné účty hlavní knihy stále přidávat různé kombinace. Chcete-li omezit množství ručního zadávání, zkopírujte účty hlavní knihy z existujícího řádku na stránce **Nastavení obecného účtování**.

## <a name="see-also"></a>Viz také
[Hlavní kniha a Účtová osnova](finance-general-ledger.md)  
[Nastavení financí](finance-setup-finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
