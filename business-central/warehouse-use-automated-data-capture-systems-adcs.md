---
title: Use Automated Data Capture Systems (ADCS) | Microsoft Docs
description: You can use your automatic data capture system (ADCS) to register the movement of items in the warehouse and to register some journal activities, such as quantity adjustments in the warehouse item journal and physical inventories.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 08/22/2019
ms.author: sgroespe

---
# Použití automatizovaných systémů pro sběr dat (ADCS)

> [!NOTE]
> Ve standardní verzi [!INCLUDE[d365fin](includes/d365fin_md.md)], ADCS (ASSD - Automatický systém sberu dat) funguje pouze v nasazení on-premise. Partner společnosti Microsoft však může zajistit, aby fungoval v online nasazení pomocí PowerApps nebo podobnou formou.

Pomocí automatického systému sběru dat (ASSD) můžete evidovat pohyb položek ve skladu a evidovat některé činnosti deníku, jako je například úprava množství v deníku zboží skladu a fyzických inventur. ASSD obvykle zahrnuje skenování čárových kódů.

Chcete-li použít ASSD, musíte každému uloženému zboží ve skladu zadat identifikátor. Musíte také nastavit miniformuláře, ruční funkce, výměny dat a zadat nastavení pro pole, která ovládají ASSD. Určíte, zda se má použít ASSD na kartě lokace.

Na základě potřeb vašeho skladu definujete množství informací zobrazených v nastavení miniformuláře pro konkrétní ruční zařízení. Níže jsou uvedeny příklady informací, které můžete zobrazit:

- Data z tabulek v [!INCLUDE[d365fin](includes/d365fin_md.md)], jako je například seznam dokladů vyskladnění z kterých uživatel vybírá.
- Textové informace.
- Zprávy, které zobrazují potvrzení nebo chyby týkající se činností prováděných a evidovaných uživatelem ručního zařízení.

Pro více informací navštivte [Konfigurace systému automatického shromažďování dat](/dynamics-nav/Configuring-Automated-Data-Capture-System) v obsahu ITPro a nápovědě pro vývojáře.

## Nastavení skladu pro použití ASSD
Chcete-li používat ASSD, musíte určit, které lokace technologii budou používat.

> [!NOTE]
> Doporučujeme, aby jste nezapínali na lokaci ADCS, pokud lokace využívá kapacity na přihrádkách.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Ze seznamu vyberte sklad, pro který chcete povolit ADCS, a pak zvolte tlačítko **Úpravy**.
3. Na stránce **Lokace** zaškrtněte políčko **Použít ASSD**.

## Určení zboží pro použití ASSD
Každému zboží skladu, které chcete použít s ASSD, musí být přiřazen identifikační kód, který jej propojí s číslem zboží. Jako kód identifikátoru můžete například použít čárový kód zboží. Zboží může mít také více identifikačních kódů. To může být užitečné v případě, kdy je zboží k dispozici v různých měrných jednotkách, například v kusech a paletách. V takovém případě každému přiřaďte identifikační kód.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží** a poté vyberte související odkaz.
2. Vyberte ze seznamu zboží, které je součástí vašeho řešení ASSD a poté zvolte tlačítko **Úpravy**.
3. Na stránce **Karta zboží**, vyberte tlačítko **Identifikátory**.
4. Na stránce **Identifikátory zboží**, vyberte tlačítko **Nový**.
5. Do pole **Kód**, vyberte identifikátor pro dané zboží. Například identifikátor může být číslo čárového kódu zboží.

   Můžete zadat **Kód varianty** a kód **Měrné jednotky**.

6. V případě potřeby zadejte pro každé zboží více kódů.
7. Klikněte na tlačítko **OK**.
8. Chcete-li zobrazit informace, vyberte pole **Kód identifikátoru** a otevřete stránku **Identifikátory položek**.

## Přidání uživatele ASSD
Jako uživatele automatizovaného systému pro sběr dat (ASSD) můžete přidat libovolného uživatele. Pokud to uděláte, musí uživatel zadat také heslo. Volitelně můžete také poskytnout připojení, které identifikuje uživatele ASSD jako zaměstnance skladu. Heslo uživatele ASSD se může lišit od přihlašovacího hesla uživatele systému Windows. Pro více informací navštivte [Správa uživatelů a práv](ui-how-users-permissions.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Uživatelé ADCS** a poté vyberte související odkaz.
2. Vyberte tlačítko **Nový**.
3. Do pole **Jméno** zadejte jméno uživatele. Název nesmí obsahovat více než 20 znaků včetně mezer.
4. Do pole **Heslo** zadejte heslo. Heslo je maskováno.

### Určení, který zaměstnanec skladu je uživatel ADCS (ASSD)
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaměstnanci skladu** a poté vyberte související odkaz.
2. V případě potřeby přidejte nového zaměstnance skladu. Pro více informací navštivte [Evidence zaměstnanců skladu](warehouse-how-to-set-up-warehouse-employees.md).
3. Vyberte tlačítko **Upravit seznam**.
4. Ze seznamu vyberte zaměstnance skladu. V poli **ADCS uživatel**, vyberte šipku rozevíracího seznamu a potom vyberte uživatele ADCS.

> [!NOTE]
> Výchozí sklad pro zaměstnance musí ten, který používá ADCS.

## Vytvoření a přizpůsobení miniformulářů
Miniformuláře se používají k popisu informací, které chcete prezentovat na kapesním zařízení. Můžete například vytvořit miniformuláře, které podpoří aktivitu skladu vyskladňování zboží. Po vytvoření miniformuláře do něj můžete přidat funkce pro běžné akce, které uživatel přebírá s kapesními zařízeními, jako je například přesunutí na řádku nahoru nebo dolů.

Chcete-li implementovat nebo změnit funkčnost funkce miniformuláře, je nutné vytvořit novou proceduru nebo upravit existující, aby byla provedena požadovaná akce nebo odezva. Další informace o funkcích ADCS se dozvíte prozkoumáním codeunit, jako je 7705, což je procedura pro přihlášení. Codeunita 7705 ukazuje, jak funguje miniformulář typu karta.

### Vytvoření miniformiuláře pro ADCS
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Miniformuláře** a poté vyberte související odkaz.
2. Vyberte tlačítko **Nový**.
3. V poli **Kód**, vložte kód pro miniformulář. Volitelně zadejte hodnoty do všech ostatních polí.

   Zaškrtnutím políčka **Počáteční miniformulář** označíte, že miniformulář je prvním formulářem, který uživatel uvidí při přihlášení.

4. Do záložky **Řádky**, definujete pole, která se zobrazí v miniformuláři. Pořadí, ve kterém zadáváte řádky, je pořadí, ve kterém se řádky objevují na kapesním zařízení.

Pokud jste vytvořili miniformulář, další kroky slouží k vytvoření funkcí a k přidružení funkčnosti pro různé vstupy klávesnice.

### Přidání podpory funkční klávesy
1. Přidejte kód podobný následujícímu příkladu do souboru .xsl pro plug-in. Tím se vytvoří funkce pro klávesu **F6** . Informace o posloupnosti kláves lze získat od výrobce zařízení.
   ```xml
   <xsl:template match="Function[.='F6']">  
   <Function Key1="27" Key2="91" Key3="49" Key4="55" Key5="126" Key6="0">  <xsl:value-of select="."/>  </Function>  </xsl:template>  
   ```
2. Ve vývojovém prostředí [!INCLUDE[d365fin](includes/d365fin_md.md)], otevřete tabulku 7702 a přidejte kód reprezentující novou klávesu. V tomto příkladu vytvořte klávesu s názvem **F6** .
3. Přidejte kód C/AL k příslušné funkci procedury specifické pro miniformulář, která bude zpracovávat funkční klávesu.

### Přizpůsobené funkcí miniformuláře
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Miniformuláře** a poté vyberte související odkaz.
2. Ze seznamu vyberte miniformulář a pak zvolte tlačítko **Úpravy**.
3. Vyberte tlačítko **Funkce**.
4. V rozevíracím seznamu **Kód funkce** vyberte kód představující funkci, kterou chcete spojit s miniformulářem. Můžete například vybrat ESC, které spojuje funkčnost s stisknutím klávesy ESC.

Ve vývojovém prostředí [!INCLUDE[d365fin](includes/d365fin_md.md)] upravte kód pro pole **Codeunit manipulace** a vytvořte nebo upravte kód pro provedení požadované akce nebo odpovědi.

Pro více informací navštivte [Konfigurace systému automatického shromažďování dat](/dynamics-nav/Configuring-Automated-Data-Capture-System) v obsahu ITPro a nápovědě pro vývojáře.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
