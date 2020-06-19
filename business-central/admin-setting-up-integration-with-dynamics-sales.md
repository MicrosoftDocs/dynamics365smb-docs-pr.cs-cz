---
    title: Setting Up User Accounts for Integrating with Dynamics 365 Sales | Microsoft Docs
    description: Learn how to set up the user accounts that the apps use to exchange data, and that people use to access and synchronize data in the apps.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: bholtorf

---
# Nastavení uživatelských účtů pro integraci s Dynamics 365 for Sales
Tento článek obsahuje přehled, jak nastavit uživatelské účty, které jsou nutné k integraci [!INCLUDE[crm_md](includes/crm_md.md)] s [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## Nastavení uživatelského účtu správce v prodeji
Musíte přidat svůj uživatelský účet správce pro [!INCLUDE[d365fin](includes/d365fin_md.md)] jako uživatel v [!INCLUDE[crm_md](includes/crm_md.md)] a poté povýšit uživatele na administrátora v [!INCLUDE[crm_md](includes/crm_md.md)]. Uživatelský účet správce musí mít také roli Úpravce systému a alespoň jednu další roli uživatele bez oprávnění správce, například Správce prodeje, v [!INCLUDE[crm_md](includes/crm_md.md)].

## Nastavení uživatelského účtu pro integraci
V předplatném sady Office 365 musíte vytvořit vyhrazený uživatelský účet, který lze použít k synchronizaci dat [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. Tento uživatelský účet musí být schopen přihlásit se do [!INCLUDE[crm_md](includes/crm_md.md)] což znamená, že tento uživatel musí mít licenci pro [!INCLUDE[crm_md](includes/crm_md.md)] a alespoň jednu bezpečnostní roli, která je mu přiřazena v [!INCLUDE[crm_md](includes/crm_md.md)], jak je popsáno [zde](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). Pro další informace o vytváření uživatelů v [!INCLUDE[crm_md](includes/crm_md.md)] navštivte [Správa zabezpečení, uživatelů a týmů](https://go.microsoft.com/fwlink/?LinkID=616518). Po nastavení připojení [!INCLUDE[d365fin](includes/d365fin_md.md)] přiřadí uživatelskému účtu bezpečnostní role, které potřebuje v [!INCLUDE[d365fin](includes/d365fin_md.md)] a tento účet může být nastaven na [Neinteraktivní režim přístupu](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) v [!INCLUDE[crm_md](includes/crm_md.md)].

![Průvodce asistovaným nastavením ukazující místo pro zadání přihlašovacích údajů pro synchronizaci](media/sync-user-setup.png "Stránka průvodce nastavením asistované vizualizace ukazující místo pro zadání přihlašovacích údajů pro synchronizaci")

> [!IMPORTANT]
> Nepoužívejte účet správce pro synchronizaci [!INCLUDE[crm_md](includes/crm_md.md)]. Pokud tak učiníte, dojde k přerušení synchronizace.
<x6 />Aby nedocházelo k neustálé synchronizaci, nejsou synchronizovány ani změny dat provedených uživatelským účtem integrace. <!--What changes would this account make?--> Po navázání spojení doporučujeme nastavit režim přístupu uživatelského účtu pro integraci do neinteraktivního režimu v [!INCLUDE[crm_md](includes/crm_md.md)]. Pro více informací navštivte [Vytvoření neinteraktivního uživatelského účtu](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## Nastavení účtů pro prodejce
Musíte vytvořit uživatelské účty v [!INCLUDE[crm_md](includes/crm_md.md)] pro prodejce z [!INCLUDE[d365fin](includes/d365fin_md.md)]. Aby to bylo snazší, nabízí administrátorské centrum Microsoft 365 šablonu Excel, kterou můžete použít. Na stránce **Aktivní uživatelé** vyberte **Více** a poté **Importovat více uživatelů**. Zvolte **Stáhnout pouze soubor CSV s hlavičkami** a zadejte informace pro prodejce. Chcete-li zobrazit příklad, vyberte **Stáhnout soubor CSV s hlavičkami a ukázkové informace o uživateli**. Po zadání informací o uživatelích je dalším krokem v procesu importu přiřazení uživatelských licencí k plánu zapojení zákazníků Dynamics 365.

Po importu uživatelů a přiřazení licencí pro zákaznické zasílání Dynamics 365 musíte uživateli přiřadit roli **Prodejce** v [!INCLUDE[crm_md](includes/crm_md.md)].

![Spojování prodejců s uživateli v Dynamics 365 for Sales](media/couple-salespeople.png "Vizualizace spojování prodejců s uživateli v Dynamics 365 for Sales")

## Minimální oprávnění pro uživatelské účty v [!INCLUDE[crm_md](includes/crm_md.md)]
Při instalaci integračního řešení jsou oprávnění pro uživatelský účet integrace konfigurována v [!INCLUDE[crm_md](includes/crm_md.md)]. Pokud se tato oprávnění změní, bude možná nutné je resetovat. To lze provést přeinstalací integračního řešení nebo ručním obnovením. V následujících tabulkách jsou uvedeny minimální oprávnění pro uživatelské účty v [!INCLUDE[crm_md](includes/crm_md.md)].

### Správce integrace
V následující tabulce jsou uvedena minimální oprávnění na každé kartě pro každou roli zabezpečení, která je požadována pro uživatele s oprávněními správce.

##### Přizpůsobení
| Role zabezpečení | Úroveň přístupu | Dynamics NAV 2018 a starší | Business Central <br> říjen 2018 | Business Central <br> duben 2019 |
|----|----|-----|----|----|
| Modelem řízená aplikace | Globální | Číst |
| Sestavení modulu plug-in | Globální | Číst | Číst | Číst |
| Typ modulu plug-in | Globální | Číst | Číst | Číst |
| Vztah | Globální | Číst |
| Zpráva sady SDK | Globální | Číst | Číst | Číst |
| Krok zpracování zpráv SDK | Globální | Číst | Číst | Číst |
| Obrázek kroku zpracování zprávy SDK | Globální | Číst | Číst | Číst |
| Systém od | Globální | Zápis |

##### Vlastní entity
| Role zabezpečení | Úroveň přístupu | Dynamics NAV 2018 a starší | Business Central <br> říjen 2018 | Business Central <br> duben 2019 |
|----|----|-----|----|----|
| Statistika účtu Business Central | Globální | Číst | Číst | Číst |
| Připojení Business Central | Globální | Vytvořit, číst, zapsat, odstranit | Vytvořit, číst, zapsat, odstranit | Vytvořit, číst, zapsat, odstranit |
| Po konfiguraci | Globální | Zápis |

#### Uživatel integrace
Následující tabulka zobrazuje minimální oprávnění na každé kartě pro každou roli zabezpečení, která je vyžadována pro uživatele integrace.

##### Základní záznamy
| Role zabezpečení | Úroveň přístupu | Dynamics NAV 2018 a starší | Business Central <br> říjen 2018 | Business Central <br> duben 2019 |
|----|----|-----|----|----|
| Účet | Globální | Vytvořit, číst, zapsat, připojit, připojit k, přiřadit | Vytvořit, číst, zapsat, připojit, připojit k, přiřadit | Vytvořit, číst, zapsat, připojit, připojit k, přiřadit |
| Karta akcí | Globální | Číst | Číst |
| Připojení | Globální | Číst | Číst | Číst |
| Kontakt | Globální | Vytvořit, číst, zapsat, připojit, připojit k | Vytvořit, číst, zapsat, připojit, připojit k | Vytvořit, číst, zapsat, připojit, připojit k |
| Poznámka | Globální | Vytvořit, číst, zapsat, odstranit připojení, přiřadit |
| Příležitost | Globální | Vytvořit, číst, zapsat, připojit, připojit k | Vytvořit, číst, zapsat, připojit, připojit k |
| Účtování | Globální | Vytvořit, číst, připojit k |
| Uživatelské rozhraní entity uživatele | Uživatel | Vytvořit, číst, zapsat | Vytvořit, číst, zapsat | Vytvořit, číst, zapsat |

##### Prodej
| Role zabezpečení | Úroveň přístupu | Dynamics NAV 2018 a starší | Business Central <br> říjen 2018 | Business Central <br> duben 2019 |
|----|----|-----|----|----|
| Faktura | Globální | Vytvořit, číst, zapsat, připojit, připojit k | Vytvořit, číst, zapsat, připojit, připojit k | Vytvořit, číst, zapsat, připojit, připojit k |
| Objednávka | Globální | Číst, zapsat, připojit k | Číst, zapsat, připojit k | Číst, zapsat, připojit, připojit k, přiřadit |
| Produkt | Globální | Vytvořit, číst, zapsat, připojit, připojit k | Vytvořit, číst, zapsat, připojit, připojit k | Vytvořit, číst, zapsat, připojit, připojit k |
| Vlastnost | Globální | Číst | Číst | Číst |
| Přidružení vlastnosti | Globální | Číst | Číst | Číst |
| Položka sady možností vlastnosti | Globální | Číst | Číst | Číst |
| Poptávka | Globální | Číst | Číst | Číst |

##### Služba
| Role zabezpečení | Úroveň přístupu | Dynamics NAV 2018 a starší | Business Central <br> říjen 2018 | Business Central <br> duben 2019 |
|----|----|-----|----|----|
| Případ | Globální | Číst | Číst | Číst |

##### Řízení podniku
| Role zabezpečení | Úroveň přístupu | Dynamics NAV 2018 a starší | Business Central <br> říjen 2018 | Business Central <br> duben 2019 |
|----|----|-----|----|----|
| Měna | Globální | Vytvořit, číst, zapsat | Vytvořit, číst, zapsat | Vytvořit, číst, zapsat |
| Organizace | Globální | Číst, zapsat | Číst, zapsat | Číst, zapsat |
| Role zabezpečení | Globální | Číst |
| Uživatel | Globální | Vytvořit, číst, zapsat, připojit, připojit k | Vytvořit, číst, zapsat, připojit, připojit k | Vytvořit, číst, zapsat, připojit, připojit k |
| Nastavení uživatelú | Globální | Vytvořit, číst, zapsat, odstranit, připojit k | Vytvořit, číst, zapsat, odstranit, připojit k | Vytvořit, číst, zapsat, odstranit, připojit k |
| Jednání jménem jiného uživatele | Globální | Ano | Ano | Ano |

##### Přizpůsobení
| Role zabezpečení | Úroveň přístupu | Dynamics NAV 2018 a starší | Business Central <br> říjen 2018 | Business Central <br> duben 2019 |
|----|----|-----|----|----|
| Pole | Globální | Číst | Číst |
| Sestavení modulu plug-in | Globální | Číst | Číst | Číst |
| Typ modulu plug-in | Globální | Číst | Číst | Číst |
| Zpráva sady SDK | Globální | Číst | Číst | Číst |
| Krok zpracování zprávy sady SDK | Globální | Číst | Číst | Číst |
| Webový zdroj | Globální | Číst | Číst | Číst |

##### Vlastní entity
| Role zabezpečení | Úroveň přístupu | Dynamics NAV 2018 a starší | Business Central <br> říjen 2018 | Business Central <br> duben 2019 |
|----|----|-----|----|----|
| Statistika účtu Dynamics 365 Business Central | Globální | Vytvořit, číst, zapsat, připojit k | Vytvořit, číst, zapsat, připojit k | Vytvořit, číst, zapsat, připojit k |
| Připojení Dynamics 365 Business Central | Globální | Číst | Číst | Číst |

### Uživatel dostupnosti produktu
Prodejcům můžete umožnit zobrazení úrovní zásob pro zboží, které prodávají, poskytnutím oprávnění popsaných v následující tabulce.

##### Vlastní entity
| Role zabezpečení | Úroveň přístupu | Dynamics NAV 2018 a starší | Business Central <br> říjen 2018 | Business Central <br> duben 2019 |
|----|----|-----|----|----|
| Statistika účtu Dynamics 365 Business Central | Globální | Vytvořit, číst, zapsat, připojit k | Vytvořit, číst, zapsat, připojit k | Vytvořit, číst, zapsat, připojit k |
| Připojení Dynamics 365 Business Central | Globální | Číst | Číst | Číst |

## Viz také
[Integrace s Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
