---
    title: How to Block Items from Sales or Purchasing
    description: In Business Central, an item can be marked as blocked for sales, blocked for purchase, or blocked for all purposes.

    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Uzavření zboží z prodeje nebo nákupu
Můžete uzavřít zboží na prodejních nebo nákupních řádcích a můžete ho uzavřít i před zaúčtováním v jakékoli transakci.

Následující tabulka ukazuje, co se stane, když je zboží uzavřeno.

| Možnost | Popis |
|--------------------|------------|  
| **Prodej uzavřen** | Nelze zadat zboží do prodejního dokladu nebo do deníku prodeje zboží. |
| **Nákup uzavřen** | Nemůžete zadat zboží v nákupním dokladu, v deníku nákupu zboží nebo v procesech plánování nákupu. |
| **Uzavřeno** | Toto zboží nelze použít pro žádnou transakci zboží. |

> [!NOTE]
> Uzavření zboží lze vrátit. To znamená, že žádné z výše uvedených nastavení se nepoužije, když je zboží použito na objednávky vratek a dobropisy.

Použijete-li funkci **Kopírovat z dokladu** k vytvoření nových dokladů založených na existujících dokladech, budete upozorněni, pokud je některé zboží na řádcích zdrojového dokladu uzavřeno. Uzavřené řádky dokladu jsou z nového dokladu vyloučeny a v oznámení je zobrazen přehled všech řádků dokladu, které jsou uzavžené ve zdrojovém dokladu.

## Uzavření zadávaného zboží na prodejních řádcích

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží** a poté vyberte související odkaz.
2. Vyberte zboží, které chcete uzavřít, a poté zaškrtněte políčko **Prodej uzavřen**.

Pokud se pokusíte zadat zboží do prodejního dokladu nebo řádku deníku, zobrazí se chybová zpráva, že zboží je uzavženo.

## Uzavření zboží na nákupních řádcích

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží** a poté vyberte související odkaz.
2. Vyberte zboží, které chcete uzavřít, a poté zaškrtněte políčko **Nákup uzavřen**.

Pokud se pokusíte zadat zboží na nákupním dokladu nebo řádku deníku, zobrazí se chybová zpráva, že zboží je uzavřeno.

## Uzavření zaúčtování zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží** a poté vyberte související odkaz.
2. Vyberte zboží, které chcete uzavřít, a poté zaškrtněte políčko **Uzavřeno**.

Pokud se pokusíte zaúčtovat jakýkoli typ transakce pro zboží, zobrazí se chybová zpráva, že je zboží uzavřeno.

## Viz také
[Evidence nového zboží](inventory-how-register-new-items.md)  
[Zásoby](inventory-manage-inventory.md)
