---
    title: How to Set Up a Document Exchange Service | Microsoft Docs
    description: You use an external service provider to exchange electronic documents with your trading partners.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Nastavení služby směnných kurzů  
Můžete použít externí službu k výměně elektronických dokladů se svými obchodními partnery. Pro více informací navštivte sekci [Elektronická výměna dat](across-data-exchange.md).

## Pro nastavení služby směnných kurzů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat")a zadejte **Nastavení výměny  dokladů**, a poté vyberte související odkaz.
2. Vyplňte pole podle popisu v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Uživatelský agent** | Zadejte libovolný text, který lze použít k identifikaci vaší společnosti v procesech výměny dokumentů. |
   | **ID nájemce výměny dokladů** | Zadejte nájemce do služby výměny dokumentů, která představuje vaši společnost. Ten je poskytován poskytovatelem služeb pro výměnu dokumentů. |
   | **Povoleno** | Určete, zda je služba povolena. **Note:** Jakmile službu povolíte, budou vytvořeny alespoň dvě položky fronty úloh pro zpracování přenosů elektronických dokumentů ve službě [!INCLUDE[d365fin](includes/d365fin_md.md)]. Když službu zakážete, položky fronty úloh budou odstraněny. |
   | **URL registrace** | Zadejte webovou stránku, na které se chcete přihlásit ke službě pro výměnu dokumentů. |
   | **Služba URL** | Zadejte adresu služby pro výměnu dokumentů, která bude zavolána při odesílání a přijímání elektronických dokumentů. |
   | **Přihlašovací adresa URL** | Určete přihlašovací stránku pro službu výměny dokumentů, kde zadáte uživatelské jméno a heslo vaší společnosti pro přihlášení ke službě. |
   | **Klíč příjemce** | Zadejte 3-legged Oauth klíč pro klíč příjemce. Ten je poskytován poskytovatelem služeb pro výměnu dokumentů. |
   | **Tajný klíč příjemce** | Zadejte tajný klíč, který chrání klíč příjemce. Ten je poskytován poskytovatelem služeb pro výměnu dokumentů. |
   | **Token** | Zadejte 3-legged Oauth klíč pro token. Ten je poskytován poskytovatelem služeb pro výměnu dokumentů. |
   | **Token - tajné** | Zadejte tajný klíč, který chrání token. Ten je poskytován poskytovatelem služeb pro výměnu dokumentů. |

   > [!NOTE]
   > Vaše přihlašovací údaje jsou automaticky šifrovány.

## Viz také
[Nastavení výměny dat](across-set-up-data-exchange.md)
[Elektronická výměna dat](across-data-exchange.md)
