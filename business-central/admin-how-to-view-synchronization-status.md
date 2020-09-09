---
    title: View the Status of Synchronization Jobs | Microsoft Docs
    description: Learn how to view the status after synchronizing coupled records.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: sales, crm, integration, sync, synchronize
    ms.date: 04/01/2020
    ms.author: bholtorf

---

# Zobrazení stavu synchronizace
Pomocí stránky **Chyby synchronizace párování dat** můžete zobrazit stav úloh synchronizace, které byly spuštěny pro spárované záznamy ve společné datové službě nebo integracích [!INCLUDE[crm_md](includes/crm_md.md)]. To zahrnuje úlohy, které byly spuštěny z fronty úloh a úlohy ruční synchronizace, které byly spuštěny v záznamech z [!INCLUDE[d365fin](includes/d365fin_md.md)]. Například zobrazení jejich stavu je užitečné při odstraňování problémů, protože vám poskytuje přístup k podrobnostem o chybách souvisejících s propojenými záznamy. Obvykle jsou tyto typy chyb způsobeny akcemi uživatele, například když:

* Dva lidé provedli změnu stejného záznamu v obou obchodních aplikacích.
* Někdo odstranil záznam v jedné z aplikací, ale ne v obou.

> [!Note]
> Na stránce **Chyby synchronizace párování dat** jsou zobrazeny informace o úlohách souvisejících se spárovánými záznamy Pokud vyřešíte všechny chyby, ale záznamy stále nejsou synchronizovány, může to mít něco společného s nastavením integrace. Obvykle správce bude muset vyřešit tyto chyby.

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## Zobrazení a řešení chyb synchronizace pro spárované záznamy
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Chyby synchronizace párování dat** a poté vyberte související odkaz.
2. Na stránce **Chyby synchronizace párování dat** zobrazuje problémy, ke kterým došlo při synchronizaci spárovaných záznamů. Následující tabulka obsahuje akce, které můžete použít k řešení problémů jeden po druhém:

| Akce | Popis |
|----|----|
| **Odstranění spárování** | Odpojí záznamy a nebudou již synchronizovány. Chcete-li obnovit synchronizaci záznamů, musíte je znovu spárovat. |
| **Opakovat** | Pro každý záznam, kde je nalezena chyba, je synchronizace přeskočena, pokud problém neopravíte ručně. Opakování bude obsahovat záznam v další synchronizaci. |
| **Synchronizace** | Aplikace se pokusí vyřešit konflikt, kdy byl záznam změněn v obou obchodních aplikacích. Můžete zvolit verzi záznamu, která se má použít v obou aplikacích. |
| **Obnovení** a **Mazání záznamů** | Ty jsou užitečné, když byl záznam odstraněn v jedné z obchodních aplikací. Odstranit záznamy odstraní záznam v aplikaci, kde stále existuje. Obnovení obnoví záznam v obchodní aplikaci, kde byl odstraněn. |

## Zobrazení protokolu synchronizace pro určitý (ručně synchronizovaný) záznam
1. Otevřete například, kartu zákazníka, zboží nebo jinou, která je synchronizována mezi [!INCLUDE[d365fin](includes/d365fin_md.md)] a Common Data Service nebo [!INCLUDE[crm_md](includes/crm_md.md)].
2. Zvolte akci **Protokol synchronizace** k zobrazení protokolu pro vybraný záznam. Například konkrétní zákazník, kterého jste synchronizovali ručně.

## Viz také
[Nastavení uživatelských účtů pro Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Použití Dynamics 365 Sales z Business Central](marketing-integrate-dynamicscrm.md)
