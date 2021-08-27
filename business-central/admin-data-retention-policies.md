---
    title: Clean Up Data with Retention Policies | Microsoft Docs
    description: You can specify how often you want to delete certain types of data.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: delete, data, retention, policy, policies
    ms.date: 04/01/2021
    ms.author: bholtorf

---
# Definování zásad uchovávání informací
Správci mohou definovat zásady uchovávání a určit, jak často chtějí [!INCLUDE[prod_short](includes/prod_short.md)] mazat zastaralá data v tabulkách, které obsahují položky protokolu a archivované záznamy. Například vyčištění položek protokolu může usnadnit práci s daty, která jsou skutečně relevantní. Zásady mohou zahrnovat všechna data v tabulkách, které jsou po datu vypršení platnosti, nebo můžete přidat kritéria filtru, která budou do zásad zahrnovat pouze určitá data, jejichž platnost vypršela.

## Požadovaná nastavení a oprávnění
Před vytvořením zásad uchovávání informací je nutné nastavit následující.

| Nastavení | Popis |
|---------|---------|
| **Povolené tabulky** | Poskytujeme seznam tabulek, které mohou být zahrnuty do zásad uchovávání informací. Pokud však chcete přidat tabulky z rozšíření k zásadám uchovávání, musí vývojář přidat své tabulky do seznamu. Další informace naleznete v tématu [Zahrnutí rozšíření do zásad uchovávání informací](admin-data-retention-policies.md#including-your-extension-in-a-retention-policy-requires-help-from-a-developer). |
| **Období uchování** | Určete časové období, po které se budou v zásadách uchovávat data v tabulkách. Období určují, jak často budou data mazána. |

Kromě toho musíte mít nastavena SUPER uživatelská oprávnění nebo oprávnění k nastavení zásad zachování. Uživatelé, kterým byla udělena sada oprávnění Nastavení zásad uchovávání, mohou definovat zásady uchovávání pro tabulky, i když pro tyto tabulky nemají oprávnění Číst a Odstranit. Položka fronty úloh musí být spuštěna jako uživatel s oprávněními ke čtení a odstraňování dat. Doporučujeme neudělit sadu oprávnění Nastavení zásad uchovávání informací uživatelům, kterým by nemělo být povoleno odstraňovat data.

> [!NOTE]
> Pokud používáte [!INCLUDE[prod_short](includes/prod_short.md)] on-premise a chcete si vyzkoušet zásady uchovávání v ukázkové databázi Cronus, musíte udělat několik věcí. Demonstrační společnost neobsahuje tabulky, které můžete použít se zásadami uchovávání informací, takže je je třeba přidat. Chcete-li to udělat, vytvořte novou prázdnou společnost v demo databázi. V nové společnosti importujte konfigurační balíček RapidStart pro vaši zemi, který odpovídá standardnímu balíčku NAV17.0.W1.ENU.STANDARD.rapidstart package. Data nastavení zásad uchovávání budou k dispozici v nové společnosti.

### Vytvoření Období uchování
Doby uchování mohou být dlouhé nebo krátké, jak chcete. Chcete-li vytvořit období uchovávání informací běžte na stránku **Zásady uchovávání informací** použijte tlačítko **Doba uchovávání**. Období, která definujete, budou k dispozici pro všechny zásady.

> [!NOTE]
> Z důvodu dodržování předpisů jsme pro některé tabulky definovali minimální dobu uchování. Pokud nastavíte dobu uchovávání, která je kratší než minimální požadovaná doba, zobrazí se povinná doba.

### Nastavení zásad uchovávání informací
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zásady uchovávání informací<x5/> a poté vyberte související odkaz.
2. V Poli **ID tabulky** yberte tabulku, kterou chcete zahrnout do zásad.
3. V poli **Doba uchovávání** určete dobu, po kterou mají být data v tabulce uchováváná.
4. Volitelné: Chcete-li zásadu použít na konkrétní data v tabulce, vyberte přepínač Použít na všechny záznamy. Zobrazí se záložka Záznam uchování záznamů, kde můžete nastavit filtry pro vytváření podmnožin dat pro každý řádek. Další informace naleznete v tématu [Filtrování](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Každý řádek má své vlastní retenční období. Pokud pro stejná data zadáte různá období uchovávání, bude použito nejdelší období. Některé tabulky také obsahují filtry, které nelze změnit ani odebrat. Abychom vám tyto filtry pomohli identifikovat, zobrazí se světlejším písmem.

## Použití zásad uchovávání informací
Pomocí položky fronty úloh můžete použít zásady uchování k automatickému odstranění dat, nebo můžete zásady použít ručně.

Chcete-li automaticky použít zásady uchovávání, stačí vytvořit a povolit zásadu. Když povolíte zásadu, vytvoříme položku fronty úloh, na které budou platit zásady uchovávání informací podle doby uchovávání. Všechny zásady uchovávání informací budou používat stejnou položku fronty úloh Ve výchozím nastavení položka fronty úloh používá zásady každý den v 02:00. Výchozí nastavení můžete změnit, ale pokud tak stane, doporučujeme, aby byla spuštěna mimo pracovní dobu. Další informace naleznete v tématu [Použití fronty úloh na plánování úloh](admin-job-queues-schedule-tasks.md).

Zásadu můžete použít ručně pomocí akce **Použít ručně** na stránce **Zásady uchovávání**. Pokud chcete zásady vždy použít ručně, zapněte přepínač **Ručně**. Položka fronty úloh nebude při spuštění zásady ignorovat.

## Zobrazení záznamů protokolu zásad uchovávání dat
Aktivitu související se zásadami uchovávání informací můžete zobrazit na stránce **Protokol zásad uchovávání informací** . Například položky se vytvářejí, když se uplatní zásada, nebo pokud došlo k chybám, když k tomu došlo.

## Zahrnutí vašeho rozšíření do zásad uchovávání informací (vyžaduje pomoc od vývojáře)
Ve výchozím nastavení se zásady uchovávání informací týkají pouze tabulek, které jsou zahrnuty v seznamu tabulek [!INCLUDE[prod_short](includes/prod_short.md)], které poskytujeme. Výchozí tabulky můžete ze seznamu odebrat a můžete přidat tabulky, které vlastníte. To znamená, že nelze přidat tabulku, kterou jste sami nevytvořili. Nemůžete například přidat další tabulky z [!INCLUDE[prod_short](includes/prod_short.md)] nebo z rozšíření, které jste zakoupili.

Chcete-li přidat své tabulky do seznamu povolených tabulek, musí vývojář přidat nějaký kód, například do codeunity pro rozšíření (codeunita s podtypem *install*).

Když vývojář přidá tabulku, může určit povinné a výchozí filtry. Povinné filtry nelze později odebrat nebo upravit, když přidáte tabulky k definování zásad uchování. Výchozí filtry jsou jen návrhy.

Následují příklady přidání tabulky do seznamu povolených tabulek s povinnými nebo výchozími filtry a bez nich. Složitější příklad najdete v proceduře 3999 "Reten. Pol. Install - BaseApp".

```al
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

Následující příklad obsahuje povinný filtr.

```al
 trigger OnInstallAppPerCompany()
    var
        ChangeLogEntry: Record "Change Log Entry";
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
        RetentionPeriod: Enum "Retention Period Enum";
        RecRef: RecordRef;
        TableFilters: JsonArray;
        Enabled: Boolean;
        Mandatory: Boolean;
    begin
        ChangeLogEntry.Reset();
        ChangeLogEntry.SetFilter("Field Log Entry Feature", '%1|%2', ChangeLogEntry."Field Log Entry Feature"::"Monitor Sensitive Fields", ChangeLogEntry."Field Log Entry Feature"::All);
        RecRef.GetTable(ChangeLogEntry);
        Enabled := true;
        Mandatory := true;
        RetenPolAllowedTables.AddTableFilterToJsonArray(TableFilters, RetentionPeriod::"28 Days", ChangeLogEntry.FieldNo(SystemCreatedAt), Enabled, Mandatory, RecRef);
        RetenPolAllowedTables.AddAllowedTable(Database::"Change Log Entry", ChangeLogEntry.FieldNo(SystemCreatedAt), TableFilters);
    end;
```

Poté, co vývojář přidá tabulky do seznamu, může je správce zahrnout do zásad uchovávání.

## Viz také

[Analýza telemetrie sledování zásad uchovávání](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Audit změny v Business Cenral](across-log-changes.md)  
[Filtrování](ui-enter-criteria-filters.md#filtering)  
[Použití front úloh k plánování úloh](admin-job-queues-schedule-tasks.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]