---
    title: Set Up and Publish KPI Web Services for Account Schedules | Microsoft Docs
    description: This topic describes how to show the account-schedule KPI data based on specific account schedules.
    author: bholtorf
    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: bholtorf

---
# Nastavení a publikování webových služeb KPI na základě účetních schémat
Na stránce **Nastavení webové služby KPI účetního schématu** nastavíte způsob zobrazení dat KPI účetního schématu a konkrétní účetní schémata, na kterých mají být KPI založeny. Když vyberete tlačítko **Publikovat webovou službu** zadaná data KPI účetního schématu budou přidána do seznamu publikovaných webových služeb na stránce **Webové služby**.

## Nastavení a publikování webových služeb KPI na základě účetních schémat
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení webové služby KPI účetního schématu** a poté vyberte související odkaz.
2. Na záložce **Obecné** vyplňte pole, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Začátek hodnot prognózy** | Určete, v jakém okamžiku se budou prognózované hodnoty zobrazovat na grafe KPI s plánem účtů.<br /><br /> Prognózované hodnoty se získají z rozpočtu hlavní knihy, který vyberete v poli **Název fin.rozpočtu**. **Poznámka:**  Chcete-li získat ukazatele KPI, které zobrazují předpovídané hodnoty po určitém datu a skutečné údaje před datem, můžete změnit pole **Povolit účto od** na stránce **Nastavení financí**. Pro více informací navštivte Povolit účto od. |
   | **Název fin.rozpočtu** | Zadejte název rozpočtu hlavní knihy, který poskytuje předpokládané hodnoty účetní schémy webové služby KPI. |
   | **Období** | Určete období, na kterém je založena účetní schéma webové služby KPI. |
   | **Zobrazit podle** | Určete, v jakém intervalu je zobrazeno účetní schéma KPI. |
   | **Název webové služby** | Zadejte název účetní schémy webové služby KPI.<br /><br /> Tento název se zobrazí v poli **Název služby** na stránce **Webové služby**. |

   Určete jeden nebo více plánů účtů, které chcete publikovat jako webovou službu KPI, podle nastavení provedeného v předchozí tabulce.

3. Na záložce **Účetní schémata** vyplňte pole, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   |   **Název účetního schéma** | Určete plán účtu, na kterém je webová služba KPI založena. |
   |   **Popis účetního schématu** | Zadejte popis plánu účtu, na kterém je webová služba KPI založena. |

4. Opakujte krok 3 pro všechny účetní schémata, na kterých chcete založit účetní schému webové služby KPI.
5. Chcete-li zobrazit nebo upravit vybraný plán účtu, na záložce **Účetní schéma** vyberte akci **Upravit účetní schéma**.
6. Chcete-li zobrazit údaje účetní schémy KPI, které jste nastavili, vyberte akci **Účetní schéma webové služby KPI**.
7. Chcete-li publikovat účetní schému webové služby KPI, vyberte akci **Publikovat webovou službu**. Webová služba je přidána do seznamu publikovaných webových služeb na stránce **Webové služby**.

> [!NOTE]
> Webovou službu KPI můžete také publikovat tak, že přejdete na stránku **Nastavení webové služby KPI účetního schématu** ze stránky **Webové služby**. Pro více informací navštivte [Publikování webové služby](across-how-publish-web-service.md).

## Viz také
[Business Intelligence](bi.md)  
[Finance](finance.md)  
[Nastavení financí](finance-setup-finance.md)  
[Položky zboží a účetní osnova](finance-general-ledger.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
