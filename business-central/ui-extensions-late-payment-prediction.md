---
title: Předpověď opožděných plateb za prodejní doklady | Microsoft Docs
description: 'Pomocí našeho prediktivního modelu můžete předpovědět, zda bude faktura uhrazena včas.'
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.date: 10/01/2018
ms.author: bholtorf
---

# <a name="the-late-payment-prediction-extension"> </a>Rozšíření Late Payment Prediction

Efektivní správa pohledávek je důležitá pro celkové finanční zdraví podniku. Rozšíření Late Payment Prediction vám může pomoct snížit nesplacené pohledávky a doladit vaši strategii inkasa předpovídáním, zda budou prodejní faktury včas uhrazeny. Pokud se například předpokládá, že platba bude opožděná, můžete se rozhodnout upravit platební podmínky nebo způsob platby pro zákazníka.

## <a name="what-are-predictions-based-on"> </a>Na čem jsou předpovědi zakládány?

Rozšíření Late Payment Prediction používá prediktivní model, který jsme vyvinuli v Azure Machine Learning Studio a nastavili jsme ho pomocí dat, která reprezentují řadu malých a středních podniků. Přestože jsme ho již nastavili a vyhodnotili, náš prediktivní model se bude i nadále učit z vašich dat. Čím více budete model používat a čím více dat budete do něj vkládat, tím budou předpovědi přesnější. Ve výchozím nastavení rozšíření model vyhodnocuje a aktualizuje předpovědi každý týden. Předpovědi však můžete kdykoli aktualizovat výběrem akce **Aktualizovat předpověď** na stránce **Položky zákazníka**.  

> [!Note]
> Každý týden využíváme trochu vaší výpočetní doby, když model vyhodnocujeme a aktualizujeme vaše předpovědi. Kromě ruční aktualizace vašich předpovědí jsou tu další akce, které vyžadují výpočetní čas, při vylepšování modelu (což můžete udělat, pokud jste nedávno přidali data) a při vyhodnocování modelu (který se dívá na kvalitu modelu).

## <a name="getting-started"> </a>Začínáme

Rozšíření je zdarma v [!INCLUDE[d365fin](includes/d365fin_md.md)] a my poskytujeme předplatné služby Azure Machine Learning. Předplatné nabízí 30 minut výpočetního času za měsíc. Pokud potřebujete více, můžete si vytvořit svůj vlastní prediktivní model a místo toho ho použít. Pro více informací navštivte část _Vytvoření vlastního prediktivního modelu_ v tomto tématu.  

Když otevřete zaúčtovaný prodejní dokument, v horní části stránky se zobrazí oznámení. Chcete-li použít prodloužení predikce pozdních plateb, můžete se přihlásit výběrem možnosti **Povolit** v oznámení. Případně můžete rozšíření nastavit ručně. Pokud například litujete zamítnutí oznámení.  

Pro ruční povolení rozšíření, postupujte takto:

1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Připojení Služby** a poté vyberte související odkaz.  
2. Vyberte možnost **Nastavení Late Payment Prediction** a vyplňte pole podle potřeby.

## <a name="viewing-all-payment-predictions"> </a>Zobrazení všech platebních předpovědí

Pokud povolíte rozšíření, bude v Centru rolí **Business Manager** k dispozici dlaždice **Předpokládané opožděné platby**. Dlaždice zobrazuje počet plateb, u nichž se předpokládá, že budou zpožděny, a když otevřete stránku **Položky zákazníka**, kde můžete najít více informací o zaúčtovaných fakturách. Jsou zde tři sloupce, kterým věnujte pozornost:  

* **Pozdní platba** - Označuje, zda se předpokládá, že platba za fakturu bude zpožděná.
* **Důvěra v predikci** - Označuje, jak spolehlivá by měla být předpověď. **Vysoká** znamená, že předpověď predikce je alespoň z 90 % jistá, **Střední** je mezi 80 a 90 % a **Nízká** je pod 80 %.
* **Predikce spolehlivosti %** - Zobrazuje skutečné procentu důvěryhodnosti. Ve výchozím nastavení se tento sloupec nezobrazuje, ale můžete jej přidat, pokud chcete. Pro více informací navštivte [Přizpůsobení vašeho pracovního prostoru](ui-personalization-user.md).

> [!Tip]
> Na stránce Položky zákazníka se vpravo zobrazuje také Okno s fakty. Při kontrole předpovědí mohou být užitečné informace v sekci **Detaily zákazníka**. Pokud v seznamu vyberete fakturu, zobrazí se v této části informace o zákazníkovi. Také vám umožní okamžitě jednat. Pokud například zákazník často ztrácí peněženku, můžete otevřít zákaznickou kartu z Okna s fakty a zablokovat tak budoucí prodej.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"> </a>Zobrazení predikce platby pro konkrétní prodejní doklad

Můžete také předem předpovědět pozdní platby. Na stránkách **Prodejní nabídky**, **Prodejní objednávky** a **Prodejní faktury** můžete pomocí akce **Predikce platby** vygenerovat predikci pro zobrazovaný prodejní dokument.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="building-your-own-predictive-model"> </a>Vytvoření vašeho vlastního prediktivního modelu

Máte zájem o vytvoření vlastního prediktivního modelu? Můžete použít Azure Machine Learning Studio k vytvoření vlastního prediktivního modelu a jeho použití v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pokud chcete používat svůj vlastní mode, musíte si předplatit službu Azure Machine Learning. Pro více informací navštivte [Dokumentace Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765).  

Nabízíme vám však jednodušší způsob, jak vytvořit a používat svůj vlastní prediktivní model. Můžete sdílet data z vašich faktur s naším prediktivním experimentem v Azure Machine Learning a nechat náš experiment vytvořit a nastavit prediktivní model založený na vašich datech. Chcete-li data sdílet, na stránce **Nastavení predikce pozdních plateb** vyberte akci **Vytvořit můj model**. Poté budou předpovědi vycházet z vašeho modelu a vašich dat, nikoli z našich.  

> [!Note]
>   Kvalita modelu je důležitá. Když náš prediktivní experiment použije vaše data k vylepšení modelu, určuje hodnotu kvality pro model jako procento. Kvalita modelu ukazuje, jak přesné budou předpovědi modelu. Kvalitu modelu může ovlivnit několik faktorů. Tyto faktory mohou například spočívat v tom, že nebylo k dispozici dostatek údajů nebo data neobsahovala dostatečné variace. Kvalitu modelu, který právě používáte, si můžete prohlédnout na stránce **Nastavení predikce pozdních plateb**. Můžete také určit minimální hraniční hodnotu pro kvalitu modelu. Modely s hodnotou kvality pod touto hranicí nebudou vytvářet předpovědi.  

### <a name="to-use-your-model-instead-of-ours"> </a>Použití vašeho modelu místo našeho

Pokud si v Azure Machine Learning Studio vytvoříte svůj vlastní model, aniž byste použili nástroje v [!INCLUDE[d365fin](includes/d365fin_md.md)], musíte uvést své přihlašovací údaje, aby k němu měl [!INCLUDE[d365fin](includes/d365fin_md.md)] přístup. Existuje několik kroků, jak toho dosáhnout:

1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Nastavení predikce pozdních plateb** a poté vyberte související odkaz.  
2. Zaškrtněte políčko **Použít moje předplatné Azure**.  
3. V poli **Vybraný model** vyberte možnost **Můj model**.  
4. Na pevné záložce **Moje pověření modelu** zadejte adresu rozhraní API a kód rozhraní API pro váš model.  

## <a name="see-also"> </a>Viz také

[Dokumentace Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765)  
[Přizpůsobení Business Central pomocí rozšíření](ui-extensions.md)  
[Vítejte v [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
