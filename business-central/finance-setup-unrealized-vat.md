---
title: Setting Up Unrealized Value Added Tax | Microsoft Docs
description: If you're using cash-based accounting, you can specify how to handle unrealized VAT for sales and purchases.
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 10/01/2019
ms.author: bholtorf

---

# Nastavení nerealizované DPH pro účetnictví založené na hotovosti
Pokud používáte metody účtování na základě hotovosti, můžete nastavit [!INCLUDE[d365fin](includes/d365fin_md.md)] pro zpracování nerealizované DPH.

## Použití účtů účetní osnovy k nerealizované DPH
Můžete zvolit, aby byly částky DPH vypočteny a zaúčtovány na dočasný účet účetní osnovy při zaúčtování faktury, poté zaúčtovány na správný účet a nakonec zahrnuty do výkazů DPH při zaúčtování skutečné platby faktury. Než to budete moci provést, musíte dokončit nastavení účtování DPH.

Chcete-li použít účty pro nerealizovanou DPH, postupujte takto:
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení financí** a vyberte související odkaz.
2. Na stránce **Nastavení financí**, zaškrtněte políčko **Nerealizovaná DPH**.
3. Vyberte ikonu **Vyhledat stránku nebo sestavu**, která otevře ![funkci Řekněte mi, co chcete dělat](media/ui-search/search_small.png "Řekněte mi co chcete dělat") a zadejte **Nastavení účtování DPH**.
4. Na stránce **Nastavení účtování DPH**, vyberte Účto skupina DPH a zvolte tlačítko **Úpravy**.
5. V poli **Typ nerealizované DPH** vyberte možnost, jak určit, jak přiřadit platby k částce faktury (bez DPH) a samotné částce DPH, a jak převést částky DPH z nerealizovaného účtu DPH na realizovaný účet. Následující tabulka popisuje možnosti.

| Možnost | Popis |
| --- | --- |
| Prázdný | Tuto možnost vyberte, pokud nechcete používat nerealizovanou funkci DPH. |
| Procento | Platby zahrnují jak DPH, tak i částku faktury v poměru k procentu platby ze zbývající částky faktury. Zaplacená částka DPH je převedena z nerealizovaného účtu DPH na realizovaný účet DPH. |
| První | Platby nejprve zahrnují částky DPH a poté fakturované částky. V tomto případě se částka převedená z nerealizovaného účtu DPH na účet DPH bude rovnat částce platby, dokud nebude zaplacena celková DPH. |
| Poslední | Platby nejprve pokrývají částku faktury a poté DPH. V takovém případě nebude z nerealizovaného účtu DPH převedena žádná částka na účet DPH, dokud nebude zaplacena celková částka faktury bez DPH. |
| První (plně zaplaceno) | Platby budou nejprve pokrývat DPH (jako možnost _První_), ale žádná částka nebude převedena na účet DPH, dokud nebude zaplacena plná částka DPH. |
| Poslední (plně zaplaceno) | Platby pokryjí nejprve částku faktury (jako možnost _Poslední_), ale žádná částka nebude převedena na účet DPH, dokud nebude zaplacena plná částka DPH. |

6. V poli **Účet nereal. prodejní DPH**, vyberte účet pro nerealizovanou prodejní DPH.

   > [!NOTE]  
   > Částka DPH bude zaúčtována na tento účet a zůstane na účtě, dokud nebude zaúčtována platba zákazníka. Částka je poté převedena na účet prodejní DPH.
7. V poli **Účet.  nereal. nákupů DPH**, zadejte účet hlavní knihy pro nerealizovanou nákupní DPH.

> [!NOTE]  
> Částka DPH bude zaúčtována na tento účet a zůstane na účtě, dokud nebude zaúčtována platba zákazníka. Částka je poté převedena na účet nákupní DPH.

## Viz také
[Nastavení DPH](finance-setup-vat.md)
