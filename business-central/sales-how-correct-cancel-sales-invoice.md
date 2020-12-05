---
title: Correct or Cancel a Posted Sales Invoice | Microsoft Docs
description: Describes how to correct, undo, or cancel a posted sales invoice and apply a sales credit memo.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2020
ms.author: edupont

---
# Oprava nebo zrušení nezaplacené prodejní faktur

Účtovanou prodejní fakturu můžete opravit nebo zrušit. To je užitečné, pokud uděláte chybu nebo pokud zákazník požaduje změnu.

> [!Note]  
> Poté, co byla účtovaná prodejní faktura částečně nebo plně zaplacena, ji nemůžete opravit ani zrušit ze samotné účtované prodejní faktury. Místo toho musíte ručně vytvořit dobropis prodeje, který zruší prodej a odškodní zákazníka, případně je to možné udělat objednávkou prodejní vratky. Více informací viz [Provádění vrácení nebo zrušení prodeje](sales-how-process-sales-returns-cancellations.md).

Na stránce **Účtovaná prodejní faktura** můžete vybrat akci **Opravit** nebo akci **Zrušit** k provedení akcí popsaných v následující tabulce.

| Akce | Popis |
| --- | --- |
| **Opravit** | Účtovaná prodejní faktura je zrušena. Vytvoří se nová prodejní faktura se stejnými informacemi. Můžete provést opravu a pokračovat v prodejním procesu. Nová prodejní faktura má jiné číslo než původní prodejní faktura. Automaticky se vytvoří a zaúčtuje opravný prodejný dobropis, který zruší původní účtovanou prodejní fakturu. Na počáteční účtované prodejní faktuře jsou zaškrtnuta políčka Zrušeno a Zaplaceno. |
| **Zrušit** | Účtovaná prodejní faktura je zrušena. Automaticky se vytvoří a zaúčtuje opravný prodejný dobropis, který zruší původní účtovanou prodejní fakturu. Na počáteční účtované prodejní faktuře jsou zaškrtnuta políčka Zrušeno a Zaplaceno. |

Při opravě nebo zrušení zaúčtované prodejní faktury je opravný prodejní dobropis aplikován na všechny věcné a skladové položky, které byly vytvořeny při účtování původní prodejní faktury. To obrátí účtovanou prodejní fakturu ve vašich finančních záznamech a ponechá účtovaný opravný prodejní dobropis pro vaši auditní stopu.

> [!TIP]
> Pokud jste účtovali zálohovou fakturu pro prodejní fakturu, kterou poté opravíte nebo zrušíte, musíte také opravit nebo zrušit platbu předem. Více informací viz [Oprava plateb předem](finance-how-to-correct-prepayments.md).

## Pro opravu účtované prodejní faktury

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Účtované prodejní faktury** a poté vyberte související odkaz.
2. Vyberte účtovanou prodejní fakturu, kterou chcete opravit.

   > [!Note]  
   > Pokud je zaškrtnuto políčko **Zrušeno** , nelze účtovanou prodejní fakturu opravit, protože již byla opravena nebo zrušena.
3. Na stránce **Účtovaná prodejní faktura** vyberte akci **Opravit**.
4. Vytvoří se nová prodejní faktura se stejnými informacemi, kde můžete provést opravu. Pole **Zrušeno** na původní účtované prodejní faktuře se změní na **Ano**.

   Prodejní dobropis je automaticky vytvořen a účtován pro zrušení původní účtované prodejní faktury.
5. Zvolte akci **Zobrazit opravný dobropis** pro zobrazení účtovaného prodejního dobropisu, který zruší původní účtovanou prodejní fakturu.

## Pro zrušení účtované prodejní faktury

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Účtované prodejní faktury** a poté vyberte související odkaz.
2. Vyberte účtovanou prodejní fakturu, kterou chcete zrušit.

   > [!Note]  
   > Pokud je zaškrtnuto políčko **Zrušeno** , nelze zaúčtovanou prodejní fakturu zrušit, protože již byla zrušena nebo opravena.
3. Na stránce **Účtovaná prodejní faktura** vyberte akci **Zrušit**.

   Prodejní dobropis je automaticky vytvořen a účtován pro zrušení původní účtované prodejní faktury. Pole **Zrušeno** na původní účtované prodejní faktuře se změní na **Ano**.
4. Zvolte **Zobrazit opravný dobropis** pro zobrazení účtovaného prodejního dobropisu, který zruší původní účtovanou prodejní fakturu.

### Částečné účtování faktury je také podporováno.

Pokud zrušení souvisí s částečným účtováním faktury, je původní řádek prodejní objednávky aktualizován tak, aby odrážel zrušené fakturované množství. **Množství fakturovat** a **Množství Fakturovaná** pole na souvisejícím řádku prodejní objednávky jsou obnoveny na hodnoty před částečným účtováním.

## Viz také

[Prodej](sales-manage-sales.md)  
[Nastavení prodeje](sales-setup-sales.md)  
[Odesílání dokladů e-mailem](ui-how-send-documents-email.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]] (ui-work-product.md)
