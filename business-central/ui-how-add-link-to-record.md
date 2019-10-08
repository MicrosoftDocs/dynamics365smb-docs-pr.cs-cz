---
title: Jak propojit záznamy s externími informacemi nebo programy | Microsoft Docs
description: 'Připojte hypertextový odkaz k dokumentu nebo webové stránce ke konkrétnímu záznamu, jako je zákazník nebo dokument.'
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 10/01/2018
ms.author: jswymer
---
# <a name="add-links-to-websites-documents-or-programs-on-records"></a>Přidání odkazů na webové stránky, doklady nebo programy v záznamech
Do konkrétního záznamu, například zákazníka, dokladu nebo prodejní objednávky, můžete přidat odkaz na externí dokument, web nebo program. Nebo můžete chtít odkaz, který otevře nový prázdný e-mail určitému příjemci, když jej vyberete. Stránka karty pro některé záznamy, například karty zákazníků a prodejců, obsahuje pole **Domovská stránka**, kde můžete zadat internetovou adresu (URL). Chcete-li zahrnout další odkazy, můžete použít metodu popsanou v tomto článku.

Dalším příkladem může být, když obdržíte tištěné faktury od dodavatelů. Můžete je naskenovat a uložit jako soubory PDF na webu služby SharePoint. Poté můžete vytvořit odkaz z nákupní faktury v [!INCLUDE[d365fin_md](includes/d365fin_md.md)] na odpovídající fakturu na SharePoint. Nebo můžete vytvořit odkaz z karty zboží na odpovídající stránku v online katalogu dodavatele.

## <a name="to-add-a-link-on-a-record"></a>Přidání odkazu do záznamu   

1.  Otevřete záznam, ke kterému chcete připojit odkaz, například zákaznickou kartu nebo prodejní objednávku. Pokud chcete připojit odkaz na konkrétní řádek, například řádek deníku, vyberte řádek.  

2.  Výběrem akce **Odkazy** otevřete stránku **Odkazy**, která zobrazí všechny aktuální odkazy přidané do záznamu.

3. Chcete-li přidat nový odkaz, zvolte **+nový**.

4.  Do pole **Adresa odkazu** zadejte

    -   Chcete-li vytvořit odkaz na soubor v počítači nebo síti, zadejte úplnou cestu a název souboru, například **C:My Documentsinvoice1.doc**.
    -   Chcete-li odkazovat na web, zadejte internetovou adresu (URL), například **www.microsoft.com**.
    -   Chcete-li odkazovat na web, zadejte internetovou adresu (URL), například **www.microsoft.com**.
    -   Chcete-li připojit program, zadejte konkrétní řetězec pro otevření programu. Chcete-li například otevřít OneNote s konkrétní stránkou, zadejte **onenote:/// C:MyDocumentstest.one**. Nebo pokud chcete otevřít aplikaci Outlook s novým prázdným e-mailem na konkrétní alias, zadejte **mailto:testalias**.  

5.  Do pole **Popis** zadejte informace o odkazu.  

6.  Zvolte tlačítko **Uložit**.  

## <a name="to-delete-a-link-from-a-record"></a>Odstranění odkazu ze záznamu  

Chcete-li odstranit odkaz, můžete na stránce **Odkazy** vybrat **...** a poté **Odstranit**.

Pokud odstraníte jeden záznam, například řádek prodejní objednávky, prodejní objednávku nebo zákazníka, budou odstraněny všechny odkazy připojené k záznamu. Pokud však odstraníte záznamy pomocí dávkové úlohy, jako je například dávková úloha **Odstranit fakturované prodejní objednávky**, zůstanou odkazy v databázi stále uloženy. Chcete-li odstranit odkazy z databáze, spusťte proceduru **Odstranit osamocené odkazy na záznamy**. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Odstranit osamocené odkazy na záznamy** a poté vyberte související odkaz.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Viz také  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
