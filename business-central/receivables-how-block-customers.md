---
    title: How to Block Sales to Customers
    description: If needed, you can block a customer from being included on sales documents and other sales transactions.
    author: SorenGP
    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Blokace zákazníků
Zákazníka můžete zablokovat například z důvodu platební neschopnosti, aby jej nebylo možné přidat do prodejních dokladů nebo na zákazníka nemohly být zaúčtovány žádné transakce.

Kromě blokování zákazníka můžete nastavit transakce pohledávek, aby byl zákazník v souvislosti s upomínkami pozastaven. Pro více informací navštivte [Inkaso nevyrovnaných zůstatků](receivables-collect-outstanding-balances.md).

Následující tabulka popisuje možnosti blokování zákazníků.

| Možnost | Popis |
|--------------------|------------|  
| **Prázdný** | Transakce jsou pro tohoto zákazníka povoleny. |
| **Dodávky** | Pro tohoto zákazníka nelze vytvořit nové objednávky ani nové dodávky. Existující dodávky, které ještě nebyly fakturovány, lze fakturovat. |
| **Faktury** | Pro tohoto zákazníka nelze vytvořit nové objednávky, nové dodávky ani nové faktury. Existující dodávky, které ještě nebyly fakturovány, nelze fakturovat. Zákazníkovi můžete stále posílat upomínky a penále. |
| **Vše** | Pro tohoto zákazníka není povolena žádná transakce, včetně plateb. |

## Zablokování zákazníka
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Vyberte zákazníka a poté vyberte talčítko **Úpravy**.
3. Do políčka **Uzavřeno** vyberte, co chcete blokovat, tak jak je popsáno v tabulce výše.

## Viz také
[Evidence nových zákazníků](sales-how-register-new-customers.md)  
[Inkaso nevyrovnaných zůstatků](receivables-collect-outstanding-balances.md)  
[Správa pohledávek](receivables-manage-receivables.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]