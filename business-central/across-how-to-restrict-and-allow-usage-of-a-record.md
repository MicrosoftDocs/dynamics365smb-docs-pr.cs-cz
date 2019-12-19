---
    title: How to Restrict and Allow Usage of a Record | Microsoft Docs
    description: If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.
    services: project-madeira
    documentationcenter: ''
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
# Omezení a povolení použití záznamu
Chcete-li zabránit použití záznamu v určitých aktivitách, například do doby, než bude záznam schválen, můžete do workflow zahrnout dvě odezvy workflow, které řídí použití záznamu. Jedna odpověď workflow omezí použití záznamu podle definice událostí a podmínek workflow. Jiná odpověď workflow umožní použití záznamu podle definice událostí a podmínek workflow. V obecné verzi aplikace existují dvě odezvy [!INCLUDE[d365fin](includes/d365fin_md.md)] pro tento účel: **Omezit použití záznamu** a **Povolit použití záznamu**.

> [!NOTE]
> Obecná verze [!INCLUDE[d365fin](includes/d365fin_md.md)] nabízí podporu pro omezení záznamu v zaúčtování, v exportu jako platba a v tisku jako šek. Pro podporu jiných omezení musí partner společnosti Microsoft přizpůsobit kód aplikace.

> [!NOTE]
> Funkce workflow, která omezuje a umožňuje použití záznamů, nesouvisí s funkcí blokování účtování položek, zákazníků a dodavatelů.

Následující postup popisuje, jak omezit zaúčtování nákupních objednávek, dokud nejsou schváleny. Nový workflow bude založen na existující šabloně workflow schvalování nákupní faktury.

## Vytvoření kroku workflow, který omezuje zaúčtování neschválených nákupních objednávek
1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Workflow** a poté vyberte související odkaz.
2. Na stránce **Workflow** vytvořte nový workflow nazvaný Workflow schvalování nákupní objednávky. Pro více informací navštivte [Vytvoření workflow](across-how-to-create-workflows.md).
3. Zvolte akci **Nové workflow ze šablony**.
4. Zvolte pole **Kód původu workflow** a na stránce **Šablony workflow** zvolte šablonu workflow pro schválení nákupní faktury.

   Všimněte si, že první dva kroky workflow jsou o omezení a následném povolení použití nákupních faktur. Přejděte ke změně podmínky události v prvním kroku nového workflow a určete jej tak, aby byla použita pro nákupní objednávky.
5. Na záložce **Kroky workflow** zvolte pole **Podmínky událostí** a pak pro filtr **Typ dokladu** vyberte **Objednávka**.
6. Pokračujte v úpravách, odstranění nebo přidání dalších kroků workflow, které odpovídají obchodnímu procesu, který začíná omezením neschválených nákupních objednávek.

## Viz také
[Vytvoření Workflow](across-how-to-create-workflows.md)  
[Workflow](across-workflow.md)
