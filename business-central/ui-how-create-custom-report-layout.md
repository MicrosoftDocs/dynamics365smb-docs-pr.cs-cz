---
title: Vytvoření a úprava vlastních rozvržení pro sestavy a doklady | Microsoft Docs
description: 'Naučte se, jak vytvořit vlastní přizpůsobená rozvržení a přizpůsobit vzhled sestavy při prohlížení, tisku nebo uložení.'
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.date: 10/01/2018
ms.author: jswymer
---
# <a name="create-and-modify-a-custom-report-or-document-layout"></a>Vytvoření a úprava vlastního rozvržení sestavy nebo dokladu
Ve výchozím nastavení bude mít sestava vestavěné rozvržení sestavy, které může být rozvržení sestavy RDLC nebo rozvržení sestavy Word, nebo obojí. Vestavěné rozvržení nelze upravovat. Můžete si však vytvořit vlastní rozvržení, která vám umožní změnit vzhled sestavy při prohlížení, tisku nebo uložení. Pro stejnou sestavu můžete vytvořit více vlastních rozvržení přehledů a poté podle potřeby přepnout rozvržení používané sestavou.

> [!NOTE]  
>   V [!INCLUDE[d365fin](includes/d365fin_md.md)], termín „sestava“ také zahrnuje externí doklady, jako jsou prodejní faktury a potvrzení objednávky, které posíláte zákazníkům jako soubory PDF.

Chcete-li vytvořit vlastní rozvržení, můžete vytvořit kopii existujícího vlastního rozvržení nebo přidat nové vlastní rozvržení, které je ve většině případů založeno na vestavěném rozvržení. Když přidáte nové vlastní rozvržení, můžete zvolit přidání typu rozvržení sestavy RDLC, typu rozvržení sestavy Word nebo obou. Nové vlastní rozvržení bude automaticky založeno na vestavěném rozvržení pro sestavu, pokud je k dispozici. Pokud pro daný typ neexistuje vestavěné rozvržení, vytvoří se nové prázdné rozvržení, které budete muset upravit a navrhnout od nuly. Pro více informací o rozvržení sestav RDLC a Word, vestavěných a vlastních sestavách viz [Správa Rozvržení Sestav](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>Vytvoření vlastního rozvržení
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výběr rozvržení sestav** a poté vyberte související odkaz.

    Na stránce **Výběr rozvržení sestav** jsou uvedeny všechny přehledy, které jsou k dispozici ve společnosti specifikované v poli **Společnost** v horní části stránky.
2. Nastavte pole **Společnost** na společnost, ve které chcete vytvořit rozvržení sestavy.
3. Vyberte řádek sestavy, pro kterou chcete rozvržení vytvořit, a poté vyberte akci **Vlastní rozvržení**.  
   Zobrazí se stránka **Vlastní rozvržení sestav** a zobrazí se všechna vlastní rozvržení, která jsou k dispozici pro vybranou sestavu.
4. Pokud chcete vytvořit kopii existujícího vlastního rozvržení, vyberte existující vlastní rozvržení v seznamu a poté vyberte akci **Kopírovat**.  
   Kopie vlastního rozvržení se zobrazí na stránce **Vlastní rozvržení sestav** a v poli **Popis** obsahuje slova *Kopírovat z*.
5. Pokud chcete přidat nové vlastní rozvržení založené na vestavěném rozvržení, postupujte takto:  
   1. Zvolte akci **Nový**. Zobrazí se stránka **Vložit rozvržení sestavy**. Pole **ID** a **Název** jsou automaticky vyplněny.
   2. Chcete-li přidat vlastní typ rozvržení sestavy aplikace Word, zaškrtněte políčko **Vložit rozvržení Wordu**.
   3. Chcete-li přidat vlastní typ rozvržení sestavy aplikace RDLC, zaškrtněte políčko **Vložit RDLC rozvržení**.
   4. Zvolte tlačítko **OK**.  
      Nové vlastní rozvržení se zobrazí na stránce **Vlastní rozvržení sestav**. Pokud je nové rozvržení založeno na vestavěném rozvržení, bude v poli **Popis** uvedeno **Kopírovat z vestavěného rozvržení**. Pokud pro sestavu nebylo žádné vestavěné rozvržení, má nové rozvržení v poli **Popis** slova **Nové rozvržení**, což znamená, že vlastní rozvržení je prázdné.
6. Ve výchozím nastavení je pole **Název společnosti** prázdné, což znamená, že vlastní rozvržení bude k dispozici pro sestavu ve všech společnostech. Chcete-li zpřístupnit vlastní rozvržení pouze v určité společnosti, zvolte **Upravit** a poté nastavte pole **Název společnosti** na požadovanou společnost.

Vlastní rozvržení bylo vytvořeno. Nyní můžete upravit vlastní rozvržení podle potřeby.

## <a name="ModifyCustomLayout"></a>Úprava vlastního rozvržení
Chcete-li upravit rozvržení sestavy, musíte nejprve rozvržení sestavy exportovat jako soubor do umístění v počítači nebo síti a poté otevřít exportovaný dokument a provést změny. Po dokončení změn importujete rozvržení sestavy.

### <a name="to-modify-a-custom-layout"></a>Úprava vlastního rozvržení
1.  Vlastní rozvržení exportujete ze stránky **Vlastní rozvržení sestav**. Pokud tato stránka ještě není otevřená, vyhledejte a otevřete stránku **Výběr rozvržení sestav**, vyberte sestavu, která má rozvržení, které chcete upravit, a poté vyberte akci **Vlastní rozvržení**.  
2.  Na stránce **Vlastní rozvržení sestav** vyberte rozvržení, které chcete upravit, vyberte akci **Exportovat rozvržení** a poté zvolte **Uložit** nebo **Uložit jako**, chcete-li dokument rozvržení sestavy uložit do umístění v počítači nebo síti.  

3.  Otevřete dokument rozvržení sestavy, který jste právě uložili, a proveďte změny.

      Pokud měníte rozvržení aplikace Word, otevřete dokument rozvržení v aplikaci Word. Podrobnosti o úpravách naleznete v další části [Provádění změn v rozvržení sestavy](ui-how-create-custom-report-layout.md#MakeChangesToLayout).

      Rozložení sestavy RDLC je pokročilejší než rozložení sestavy Word. Další informace o úpravě rozvržení sestavy RDLC naleznete v tématu [Navrhování rozvržení sestav RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

      Po dokončení nezapomeňte uložit změny.

4.  Vraťte se na stránku **Vlastní rozvržení sestav**, vyberte rozvržení sestavy, které jste exportovali a upravili, a poté vyberte akci **Importovat rozvržení**.  

5. V dialogovém okně **Import** zvolte **Vybrat** aby jste našli a vybrali dokument, který definuje rozvržení sestavy a poté zvolte **Otevřít**.

##  <a name="MakeChangesToLayout"></a> Provádění změn v rozvržení sestavy aplikace Word  
Chcete-li provádět obecné změny formátování a rozvržení, jako je například změna textového písma, přidání a úprava tabulky nebo odstranění datového pole, stačí použít základní editační funkce aplikace Word, jako to děláte u jakéhokoli dokumentu Word.

Pokud navrhujete rozvržení sestavy aplikace Word od začátku nebo přidáváte nová datová pole, začněte přidáním tabulky, která obsahuje řádky a sloupce, které budou nakonec obsahovat datová pole.

> [!TIP]  
>  Zobrazte mřížky tabulky tak, abyste viděli hranice buněk tabulky. Po dokončení úprav nezapomeňte skrýt mřížky. Chcete-li zobrazit nebo skrýt mřížky tabulky, vyberte tabulku a v části **Rozvržení** na kartě **Tabulka** zvolte **Zobrazit mřížky**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Vkládání písem do aplikace Word z důvodu konzistence

Chcete-li zajistit, aby se sestavy vždy zobrazovaly a tiskly s zamýšlenými písmy, bez ohledu na to, kde uživatelé otevírají nebo tisknou sestavy, můžete písma vložit do dokumentu Word. Mějte však na paměti, že vkládání písem může výrazně zvětšit velikost souborů aplikace Word. Další informace o vkládání písem do aplikace Word naleznete v tématu [Vkládání písem do aplikací Word, PowerPoint nebo Excel](https://support.office.com/en-us/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Odstranění popiskových a datových polí v rozvržení Word  
 Popisky a datová pole sestavy jsou obsaženy v ovládacích prvcích obsahu v aplikaci Word. Následující obrázek znázorňuje ovládací prvek obsahu, když je vybrán v dokumentu Word.  

 ![Řízení obsahu pole v rozvržení sestavy aplikace Word](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 Název popisku nebo datového pole se zobrazí v ovládacím prvku obsahu. V příkladu je název pole SpolečnostAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>Odstranění popisku nebo datového pole  

1.  Klepněte pravým tlačítkem myši na pole, které chcete odstranit, a pak zvolte **Odstranit kontrolu obsahu**.  

     Ovládací prvek obsahu je odebrán, ale název pole zůstává jako text.  

2.  Odstraňte zbývající text podle potřeby.  

### <a name="adding-data-fields"></a>Přidání datových polí
Přidání datových polí z datového souboru sestavy je pokročilejší a vyžaduje určitou znalost datového souboru sestavy. Informace o přidávání polí pro data, štítky a obrázky naleznete v části [Přidání polí do rozvržení sestavy aplikace Word](ui-how-add-fields-word-report-layout.md).  

###


## <a name="see-also"></a>Viz také
[Správa rozvržení sestav](ui-manage-report-layouts.md)  
[Změna rozvržení, které se v sestavě aktuálně používá](ui-how-change-layout-currently-used-report.md)  
[Import a export vlastní sestavy nebo rozvržení dokumentu](ui-how-import-and-export-report-layout.md)  
[Práce se sestavami a dávkovými úlohami](ui-work-report.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
