---
title: How to Post Multiple Documents at the Same Time | Microsoft Docs
description: Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for batch posting, either for immediate posting or scheduled to, for example, the end of the day.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: sgroespe

---
# Dávkové zaúčtování dokladů
Namísto účtování jednotlivých dokladů jeden po druhém můžete vybrat více nezaúčtovaných dokladů v seznamu pro okamžité zaúčtování nebo pro dávkové zaúčtování podle plánu, například na konci dne. To může být užitečné, pokud může pouze nadřízený zaúčtovat doklady vytvořené jinými uživateli nebo, aby se zabránilo problémům s výkonem systému z účtování během pracovní doby.

## Okamžité hmoradné zaúčtování nákupních objednávek
Následující postup vysvětluje, jak okamžitě zaúčtovat více nákupních objednávek. Postup je podobný pro všechny nákupní a prodejní doklady.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní objednávky** a poté vyberte související odkaz.
2. Na stránce **Nákupní objednávky**, vyberte všechny objednávky, které mají být zaúčtovány:
3. V poli **Číslo**, zvolte tři svislé tečky, abyste otevřeli místní nabídku, a pak zvolte talčítko **Vybrat více**.
4. Zaškrtněte políčko u všech řádků představujících objednávky, které chcete zaúčtovat současně.
5. Vyberte funkci **Účtovat** a vyberte možnost **Účtovat**.
6. V potvrzovací zprávě vyberte **Ano**.

## Dávkově zaúčtování více nákupních objednávek
Následující postup vysvětluje, jak dávkově zaúčtovat nákupní objednávky. Kroky jsou podobné pro všechny nákupní a prodejní doklady, kde je k dispozici akce **Dávkové účtování**.

> [!NOTE]
> Dávkové účtování dokladů se děje na pozadí, jak je definováno položkou fronty úloh, která musí být nejprve nastavena. Pro více informací navštivte [Použití fronty úloh na plánování úloh](admin-job-queues-schedule-tasks.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní objednávky** a poté vyberte související odkaz.
2. Na stránce **Nákupní objednávky**, vyberte všechny objednávky, které mají být zaúčtovány:
3. V poli **Číslo**, zvolte tři svislé tečky, abyste otevřeli místní nabídku, a pak zvolte talčítko **Vybrat více**.
4. Zaškrtněte políčko u všech řádků představujících objednávky, které chcete zaúčtovat současně.
5. Vyberte funkci **Účtovat** a vyberte možnost **Dávkové účtování**.
6. Na stránce  **Dávkové účtování nákupních objednávek** vyplňte pole dle potřeby [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Chcete-li tisknout související doklady při účtování jako je **Potvrzení objednávky** pro prodejní objednávky,vyberte políčko **Tisk**.<br /><br /> V poli **Typ výstupu sestavy** na stránce **Nastavení prodeje a pohledávek** nebo **Nastavení nákupu a závazků** určíte, zda bude sestava vytištěna nebo bude jako PDF soubor.<br /><br /> Nezapomeňte také, že přímý tisk na vybranou tiskárnu je možný pouze na on-premises instalacích.

7. Vyberte tlačítko **OK**.
8. Chcete-li zobrazit potenciální problémy, ke kterým došlo během dávkového účtování dokumentů, otevřete stránku **Chybové zprávy**.

Objednávky budou nyní přidány do vyhrazené položky fronty úloh, která definuje, kdy budou doklady zaúčtovány. Pro více informací navštivte [Použití fronty úloh na plánování úloh](admin-job-queues-schedule-tasks.md).

Pokud vyberete **PDF** v poli **Typ výstupu sestavy** úspěšně zaúčtované nákupní objednávky budou k dispozici v **Schránka sestav** v součásti Centra rolí.

## Viz také
[Účtování dokladů a deníků](ui-post-documents-journals.md)  
[Použití fronty úloh k pravidelným úkolům](admin-job-queues-schedule-tasks.md)  
[Úprava účtovaných dokladů](across-edit-posted-document.md)  
[Oprava nebo zrušení nezaplacených účtovaných faktur](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Vyhledávání stránek a inforamcí pomocí Řekněte mi](ui-search.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
