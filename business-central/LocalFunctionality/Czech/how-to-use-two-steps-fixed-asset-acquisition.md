---
title: Czech Local Functionality - Two steps Fixed Asset acquisition | Microsoft Docs
description: There are two steps to accomplish when acquiring a fixed asset in Czech accounting. This function describes them.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Fixed Asset, Localization, CZ
ms.date: 03/01/2021
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Dvou-krokové pořízení dlouhodobého majetku

Při pořizování dlouhodobého majetku je nutno dle českého účetnictví provést dva kroky. Pokud společnost obdrží fakturu za pořízení dlouhodobého majetku, musí být zaúčtována. O Dlouhodobém majetku se účtuje už od okamžiku jeho prvního pořízení. Jak pořízení, tak i zařazení je vyžadováno a propojeno s Věcnými položkami. Dlouhodobý majetek není odpisován, dokud není zařazen.

Pro tento postup použijte typ účtování **Vlastní 2** pro první krok (**Pořízení**) a typ účtování **Pořízení** dlouhodobého majetku pro krok druhý (**Zařazení**). Chcete-li začít používat tuto funkci, zaškrtněte políčko **Pořízení dlouhodobého majetku jako Vlastní 2** v **Nastavení DM**.
Hodnota "Custom 2" je v Češtině přejmenovaná z "Vlastní 2" na "Pořízení" pro správnou identifikaci a intuitivnější porozumění.

## Viz Také

[Dlouhodobý majetek pro Česko](ui-extensions-fixed-asset-localization-cz.md)  
[Czech Local Functionality](czech-local-functionality.md)  
