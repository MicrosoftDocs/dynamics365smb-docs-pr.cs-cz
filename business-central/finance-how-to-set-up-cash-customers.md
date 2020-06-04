---
    title: How to Set Up Cash Customers | Microsoft Docs
    description: This topic describes the steps to set up customer who pays in cash.
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
# Nastavení zákazníků platících hotovostí
Fakturu nelze vytvořit bez čísla zákazníka. To platí, i když provedete hotovostní prodej a nemáte co zaznamenávání na účtu zákazníka.

## Nastavení zákazníka platícího hotovostí
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Zákazníci** a vyberte související odkaz.
2. Vytvořte novou kartu **zákazníka**. Pro více informací navštivte [Evidence nového zákazníka](sales-how-register-new-customers.md).
3. Do pole **Číslo**, vložtě například **Hotovost**.
4. Do pole **Název**, vložte například **Hotovostní prodej**.
5. V záložce **Fakturace**, vyplňte pole **Účto skupina zákazníka** a **Obecná obch. účto  skupina**.

Nyní jste vytvořili zákazníka, který obsahuje dostatečné informace pro fakturaci.

> [!NOTE]  
> Možná jste si vybrali skupinu účtování, která se také používá pro domácí úvěrový prodej. Pokud si chcete zachovat samostatné údaje o hotovostním prodeji, například se zvláštním účtem prodeje nebo pohledávek, můžete pro tento účel zřídit zvláštní účtovací skupinu.
>
> Musíte zadat číslo účtu pohledávek pro účtovací skupinu, i když zůstatek na tomto účtu bude po odeslání faktury vždy 0.

## Viz také
[Správa pohledávek](receivables-manage-receivables.md)  
[Evidence nových zákazníků](sales-how-register-new-customers.md)    
[Finance](finance.md)

