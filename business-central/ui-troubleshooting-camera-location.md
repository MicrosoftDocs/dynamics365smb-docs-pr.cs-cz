---
title: "Troubleshooting: Accessing Camera and Location"
description: "This article describes how to troubleshoot access to camera and location information in Business Central."
author: blrobl
ms.author: t-blrobl
ms.date: 04/01/2021
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
ms.service: "dynamics365-business-central"
---

# Poradce při potížích: Přístup ke kameře a umístění

Při pokusu o přístup ke kameře a informacím o poloze zařízení z [!INCLUDE[prod_short](includes/prod_short.md)] se můžete setkat s některými problémy. Možné příčiny těchto problémů a jejich řešení můžete najít níže.

## Zařízení musí mít možnosti kamery a umístění

Pro přístup ke kameře nebo poloze uživatele ze zařízení musí mít zařízení fyzickou kameru nebo schopnost načíst informace o poloze.

Pokud má vaše zařízení možnosti fotoaparátu a umístění, ale stále narazíte na problémy, je možné, že některé ovladače potřebují aktualizaci nebo přeinstalaci. I když si nejste jisti, vždy doporučujeme aktualizovat operační systém, ovladače a prohlížeč zařízení na nejnovější verzi pro nejlepší zážitek.

## Přístupová oprávnění nejsou povolena

Musíte povolit obecný přístup ke kameře a poloze z nastavení ochrany osobních údajů vašeho zařízení a výslovně dát oprávnění [!INCLUDE[prod_short](includes/prod_short.md)]. Chcete-li například zobrazit nebo změnit oprávnění pro zařízení se systémem Windows, přejděte do **Nastavení**, vyberte **Soukromí** a poté **Oprávnění aplikace**.

U mobilních zařízení musíte mobilní aplikaci [!INCLUDE[prod_short](includes/prod_short.md)] udělit přístup k fotoaparátu a poloze. Chcete-li tak učinit pro zařízení se systémem iOS, přejděte do **Nastavení**, vyberte **Soukromí**, a poté vyberte **Fotoaparát** nebo **Polohové služby**. Pro zařízení s Android přejděte **Nastavení**, vyberte **Aplikace a uporozrnění**, **Pokročilé**, **Správce oprávnění** a poté **Fotoaparát** nebo **Umístění**.

Kromě toho, pokud používáte [!INCLUDE[prod_short](includes/prod_short.md)]  prohlížeči, musíte také udělit webu [!INCLUDE[prod_short](includes/prod_short.md)] přístup k informacím o kameře nebo poloze. Chcete-li zobrazit nebo změnit oprávnění webu v prohlížeči Microsoft Edge, přejděte do **Nastavení**, vyberte **Oprávnění webu** a poté **Fotoaparát** nebo **Umístění**. U jiných prohlížečů se to může lišit.

Ve výchozím nastavení zařízení nebo prohlížeč zobrazí požadavek na přístup k těmto funkcím, když je uživatel poprvé aktivuje.

> [!NOTE]  
> Některé staré prohlížeče neudělují přístup ke kameře a poloze. Například kamera není k dispozici v prohlížeči Internet Explorer nebo ve starším prohlížeči Edge.

## Připojení webového klienta není zabezpečeno.

Funkce kamery a umístění jsou k dispozici pouze při přístupu k webovému klientovi prostřednictvím zabezpečeného připojení HTTP pomocí protokolu SSL pomocí URI schématu `https://`.

Jedinou výjimkou je připojení k `http://localhost`, které se používají pro vývojové a testovací účely.


## Práce s virtualizačními technologiemi

Při připojování k [!INCLUDE[prod_short](includes/prod_short.md)] prostřednictvím vzdálené plochy nebo jiné virtualizace nemusí být přístup k fotoaparátu nebo umístění k dispozici. V takovém případě použijte místo toho fyzický systém.

## Antivirový software
Některý antivirový software ve výchozím nastavení blokuje přístup ke fotoaparátu a umístění. Nezapomeňte zkontrolovat nastavení antivirového softwaru.

## Viz také
[Imlementace Fotoaparátu v AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Imlementace Umístění v AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]