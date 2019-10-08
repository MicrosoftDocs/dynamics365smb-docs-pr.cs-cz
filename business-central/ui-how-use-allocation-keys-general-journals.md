---
title: Použití přidělovacího klíče ve finančních denících | Microsoft Docs
description: 'Naučte se, jak můžete v denících používat alokační klíče.'
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 10/01/2018
ms.author: edupont
---
# <a name="use-allocation-keys-in-general-journals"></a>Použití přidělovacího klíče ve finančních denících
Při účtování deníku můžete přiřadit položku ve finančním deníku několika různým účtům. Přiřazení lze provést podle množství, procenta nebo částky.

## <a name="to-set-up-allocation-keys"></a>Nastavení přidělovacích klíčů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Periodický finanční deník** a poté vyberte související odkaz.
2. Klepnutím na pole **Název listu** otevřete stránka **Listy finančního deníku**.
3. Můžete buď upravit přidělení na existující dávku v seznamu, nebo vytvořit novou dávku.
   * Chcete-li vytvořit novou dávku, vyberte akci **Nový** a přejděte k dalšímu kroku.
   * Chcete-li změnit přidělení existujícího deníku, vyberte deník a přejděte ke kroku 7.    
4. Do pole **Název** zadejte název dávky, například ČIŠTĚNÍ. Do pole **Popis** zadejte popis, například Deník čištění výdajů.
5. Až budete hotovi, zavřete stránku. Otevře se nový, prázdný periodický deník.
6. Vyplňte pole v hlavičce.
7. Zvolte akci **Rozdělení**.
8. Přidejte řádek pro každé přidělení. Musíte vyplnit buď pole **Rozdělení %**, **Rozdělené množství** nebo **Částka**. Musíte také vyplnit pole **Číslo účtu** a, pokud přidělujete transakci mezi globální dimenze, pole globální dimenze.
9. Pokud do řádku zadáte procento, automaticky se vypočítá částka v poli **Částka**. Tyto částky mají opačné znaménko než celková částka v poli **Částka** v periodickém deníku.
10. Po zadání řádků přidělení zvolte **OK** pro návrat na stránku **Periodický finanční deník**. **Rozdělená částka (USD)** je vyplněno a odpovídá poli **Částka**.
11. Zaúčtovat deník.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Změna již nastaveného alokačního klíče
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Periodický finanční deník** a poté vyberte související odkaz.
2. Na stránce **Periodický finanční deník** vyberte deník s rozdělením.
3. Vyberte řádek s rozdělením a poté vyberte akci **Rozdělení**.
4. Změňte příslušná pole a poté stiskněte tlačítko **OK**.

## <a name="see-also"></a>Viz také
[Práce s finančními deníky](ui-work-general-journals.md)  
[Účtování dokladů a deníků](ui-post-documents-journals.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
