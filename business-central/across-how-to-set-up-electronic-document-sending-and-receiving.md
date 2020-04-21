---
    title: How to Set Up Electronic Document Sending and Receiving | Microsoft Docs
    description: As an alternative to emailing as file attachments, you can send and receive business documents electronically.
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
# Nastavení odesílání a přijímání elektronického dokladu
Jako alternativu k odesílání obchodních dokladů v přílohách e-mailů můžete obchodní dokumenty zasílat a přijímat elektronicky. Elektronickým dokladem se rozumí soubor vyhovující standardu představující obchodní doklad, jako například faktura od dodavatele, která může být obdržena a převedena na nákupní fakturu v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Výměnu elektronických dokladů mezi dvěma obchodními partnery provádí externí poskytovatel služeb pro výměnu dokladů. Obecná verze [!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje odesílání a přijímání elektronických faktur a dobropisů ve formátu PEPPOL, který je podporován největšími poskytovateli služeb pro výměnu dokladů. Hlavní poskytovatel služeb pro výměnu dokladů je předem nakonfigurován a připraven k nastavení ve vaší společnosti.

Z PDF nebo souborů s obrázky reprezentujících příchozí doklady můžeme nechat externí službu OCR (Optical Character Recognition - Optické rozpoznávání znaků) vytvořit elektronické doklady, které pak můžeme převést na došlé doklady v [!INCLUDE[d365fin](includes/d365fin_md.md)], stejně jako elektronické došlé doklady formátu PEPPOL. Pokud například od dodavatele obdržíte fakturu ve formátu PDF, můžete ji odeslat do služby OCR ze stránky  **Došlé doklady**. Po několika sekundách obdržíte soubor zpět jako elektronickou fakturu, kterou lze pro dodavatele převést na nákupní fakturu. Pokud soubor odešlete do služby OCR pomocí e-mailu, bude automaticky vytvořen nový záznam příchozího dokladu, v momentě, kdy obdržíte elektronický doklad zpět.

Formát elektronického dokumentu **PEPPOL** je předkonfigurován tak, aby vám umožnil odesílat elektronické faktury a dobropisy ve formátu PEPPOL. Nejprve je nutné nastavit různá hlavní data, například informace o společnosti, zákazníky, zboží a měrné jednotky.  Používají se k identifikaci obchodních partnerů a zboží, při převádění dat v polích v [!INCLUDE[d365fin](includes/d365fin_md.md)] na prvky v odchozích dokladech. Nakonec musíte vybrat formát na stránce **Formát elektronických dokumentů** pro každého zákazníka, kterému pošlete elektronické dokumenty PEPPOL. Pro více informací navštivte [Odeslání elektronických dokladů](sales-how-to-send-electronic-documents.md).

Definice výměny dat **PEPPOL – Faktura** a **PEPPOL – Dobropisy** jsou předkonfigurovány, aby vám umožnily přijímat elektronické faktury a dobropisy ve formátu PEPPOL. Nejprve je nutné nastavit různá hlavní data, například informace o společnosti, dodavatele, zboží a měrné jednotky. Tyto položky slouží k identifikaci obchodních partnerů a zboží při převádění dat v prvcích příchozích dokumentů do polí v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nakonec musíte vybrat definici výměny dat na stránce **Došlé doklady** pro každý došlý elektronický doklad, který chcete převést na nákupní doklad v [!INCLUDE[d365fin](includes/d365fin_md.md)].

Definice výměny dat **OCR – faktura** je předkonfigurována tak, aby umožňovala přijímat elektronické doklady, které jsou generovány službou OCR. Chcete-li například obdržet fakturu jako elektronický doklad OCR, nastavíte hlavní data a potom dokument zpracujete stejně, jako při příjmu elektronického dokumentu PEPPOL. Pro více informací navštivte [Použití funkce OCR k převedení souborů PDF a obrázkových souborů do elektronických dokumentů](across-how-use-ocr-pdf-images-files.md).

Předkonfigurované služby pro výměnu dokumentů a OCR musí být před odesláním nebo přijetím povoleny. Pro více informací navštivte [Nastavení služby směnných kurzů](across-how-to-set-up-a-document-exchange-service.md).

Téma obsahuje následující postupy:

* Nastavení společnosti pro odesílání a přijímání elektronických dokladů
* Nastavení účtování DPH pro odesílání a přijímání elektronických dokladů
* Nastavení zemí/oblastí pro odesílání a přijímání elektronických dokladů
* Nastavení položek pro odesílání a přijímání elektronických dokladů
* Nastavení měrných jednotek pro odesílání a přijímání elektronických dokladů
* Nastavení zákazníků pro odesílání elektronických dokladů
* Výběr formátu elektronického dokladu **PEPPOL** pro elektronické odesílání dokladů
* Nastavení dodavatelů pro příjem elektronických dokumentů
* Výběr definice výměny dat **PEPPOL – Faktura** pro příjem elektronických dokladů 
* Nastavení finančního účtu pro použití na nových řádcích nákupní faktury pro ne\existující a ne\identifikovatelné položky

### Nastavení společnosti pro odesílání a přijímání elektronických dokladů
1. V poli **Hledat**, zadejte **Informace o společnosti**, a pak zvolte související odkaz.
2. Na záložce s náhledem **Obecné** vyplňte pole, podle popisu v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **GLN** | Identifikujte svou společnost. <br /><br /> Například, při odesílání elektronických faktur ve formátu PEPPOL se hodnota v tomto poli používá k naplnění prvku **EndPointID** v souboru pod uzlem **AccountingSupplierParty**. Číslo je založeno na standardu GS1, který je kompatibilní s ISO 6523. |
   | **DIČ** | Určete DIČ vaší společnosti. |
   | **Centrum odpovědnosti** | Pokud je vaše společnost nastavena s centrem odpovědnosti, ujistěte se, že je vyplněno pole **Kód země/oblasti**. |

### Nastavení účtování DPH pro odesílání a přijímání elektronických dokladů
1. Do pole **Hledat**, zadejte **Nastavení účtování DPH** a poté vyberte související odkaz.
2. Pro každý řádek nastavení účtování DPH, který budete používat pro elektronické doklady, vyplňte pole popsané v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Kategorie daně** | Určuje kategorii DPH ve spojení<br /><br /> Například když posíláte elektronické faktury ve formátu PEPPOL, hodnota v tomto poli je použita k naplnění prvku **TaxApplied** v souboru pod uzlem **AccountingSupplierParty**. Číslo je založeno na standardu UNCL5305. |

### Nastavení zemí/oblastí pro odesílání a přijímání elektronických dokladů
1. V poli **Hledat**, zadejte **Země/oblasti**, a pak zvolte související odkaz.
2. Pro zemi, nebo oblast, každého subjektu, se kterým budete vyměňovat elektronické dokumenty, vyplňte pole, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Schéma DPH** | Identifikujte národní subjekt, který přiděluje DIČ pro zemi/oblast ve spojení s elektronickým odesíláním dokladů.<br /><br /> Například při odesílání elektronických faktur ve formátu PEPPOL, hodnota v tomto poli se používá k naplnění atributu **SchemeID** v souboru, pro prvek **EndPointID** pod uzly **AccountingSupplierParty** a **AccountingCustomerParty**. <br /><br /> Pole **Schéma DPH** se používá pouze v případě, kdy pole **GLN** není na stránce **Informace o společnosti** vyplněno. **Note:**  Hodnota v poli **Kód** na stránce **Země/oblasti** musí odpovídat ISO 3166\-1:Alpha2. |

### Nastavení položek pro odesílání a přijímání elektronických dokladů
1. V poli **Hledat**, zadejte **Zboží**, a pak zvolte související odkaz.
2. Pro každé zboží, které nakupujete a prodáváte na elektronických dokladech, vyplňte pole, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Číslo GTIN** | Identifikuje zboží v propojení s odesíláním a přijímáním elektronického dokladu. Pro formát PEPPOL, je pole použito následujícím způsobem:<br /><br /> Pokud má prvek **StandardItemIdentification\/ID** atribut **SchemeID** nastaven na **GTIN**, tak je prvek namapován na pole **GTIN**, které se nachází na kartě zboží. |

### Nastavení měrných jednotek pro odesílání a přijímání elektronických dokladů
1. V poli **Hledat**, zadejte **Měrné jednotky**, a pak zvolte související odkaz.
2. Pro každou měrnou jednotku, kterou budete používat na elektronických dokladech, vyplňte pole, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Mezinárodní standardní kód** | Určuje kód měrné jednotky vyjádřený podle standartu UNECERec20 ve spojení s elektronickým odesíláním prodejních dokumentů. <br /><br />Například, při posílání prodejních dokumentů skrz servis PEPPOL, hodnota v tomto poli je použita k importování atributu **unitCode** v prvku **InvoicedQuantity** pod uzlem **InvoiceLine**. **Note:**  Je-li pole **Měrná jednotka** v prodejním řádku prázdné, je vložena výchozí standardní hodnota UNECERe20 za “Kus” \(H87\). Pro více informací a seznam platných kódů měrných jednotek navštivte sekci [Recommendation No. 20 \- Units of Measure used in International Trade](https://www.unece.org/fileadmin/DAM/cefact/recommendations/rec20/rec20_rev3_Annex2e.pdf). |

### Nastavení zákazníků pro odesílání elektronických dokladů
1. V poli **Hledat**, zadejte **Zákazníci**, a pak zvolte související odkaz.
2. Pro každého zákazníka, který vám bude zasílat elektronické dokumenty, vyplňte pole, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **GLN** | Identifikuje zákazníka.<br /><br />Například když odešlete elektronické faktury ve formátu PEPPOL, hodnota v tomto poli se použije k naplnění prvku **EndPointID** pod uzlem **AccountingCustomerParty**. Číslo je založeno na standardu GS1, který je kompatibilní s ISO 6523.<br /><br /> Pokud je pole **GLN** prázdné, je použita hodnota v poli **DIČ**. |
   | **DIČ** | Určuje DIČ zákazníka. **Tip:** Zvolte tlačítko Podrobnosti a použijte webovou službu, která ověří, zda číslo existuje v obchodním rejstříku v zemi. |
   | **Centrum odpovědnosti** | Pokud je zákazník zřízen v centru odpovědnosti, ujistěte se, že je vyplněno pole **Kód země/oblasti**. |

   U každého zákazníka můžete nastavit upřednostňovanou metodu odesílání obchodních dokumentů, takže nemusíte při každém odeslání dokumentu zákazníkovi vybírat možnost odeslání. Pro více informací navštivte [Nastavení profilů odesílání dokladů](sales-how-setup-document-send-profiles.md).

### Výběr formátu elektronického dokladu PEPPOL pro elektronické odesílání dokladů.
1. Do pole **Hledat**, zadejte **Profily odesílání dokladů** a poté vyberte související odkaz.
2. Otevřete existující profil pro odesílání dokladů nebo vytvořte nový. Pro více informací navštivte [Nastavení profilů odesílání dokladů](sales-how-setup-document-send-profiles.md).
3. Na stránce **Profil odesílání dokladů**, vyberte **Elektronický formát**, zvolte řádek pro PEPPOL, a poté zvolte **OK**.
4. Na poli **Elektronický doklad** vyberte **Ano (Prostřednictvím služby výměny dokumentů)**.

   > [!NOTE]
   > [!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky detekuje, zda je dokumentem faktura nebo dobropis a použije odpovídajícím způsobem formát PEPPOL.

5. Chcete-li, aby se tento profil odesílání dokladů vztahoval na všechny zákazníky, zaškrtněte pole **Výchozí** na záložce **Obecné**. Chcete-li, aby se vztahovalo pouze na konkrétní zákazníky, vyplňte pole **Profil odesílání dokladů** na příslušných zákaznických kartách. Pro více informací navštivte [Nastavení profilů odesílání dokladů](sales-how-setup-document-send-profiles.md).

   Nyní můžete odeslat elektronický dokument obsahující převedená data. Pro více informací navštivte [Odeslání elektronických dokladů](sales-how-to-send-electronic-documents.md).

### Nastavení dodavatelů pro příjem elektronických dokumentů
1. V poli **Hledat**, zadejte **Dodavatelé**, a pak zvolte související odkaz.
2. Pro každého dodavatele, od kterého obdržíte elektronické doklady, vyplňte pole, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **GLN** | Identifikujte dodavatele. <br /><br /> Například když odešlete elektronické faktury ve formátu PEPPOL, hodnota v tomto poli se použije k naplnění prvku **EndPointID** pod uzlem **AccountingSupplierParty**. Číslo je založeno na standardu GS1, který je kompatibilní s ISO 6523.<br /><br /> Pokud je pole **GLN** prázdné, je použita hodnota v poli **DIČ**. |
   | **DIČ** | Určete DIČ dodavatele. **Tip:** Zvolte tlačítko Podrobnosti a použijte webovou službu, která ověří, zda číslo existuje v obchodním rejstříku v zemi. |
   | **Centrum odpovědnosti** | Pokud je dodavatel zřízen v centru odpovědnosti, ujistěte se, že je vyplněno pole **Kód země/oblasti**. |

### Výběr definice výměny dat PEPPOL – Faktura pro příjem elektronických dokladů 
1. zadejte v poli **Hledat** **Došlé doklady**, a pak zvolte související odkaz.
2. Na řádku elektronického dokladu, který chcete přijmout a převést, zvolte pole **Typy výměny dat** a poté vybrat **PEPPOLINVOICE**.

   Pokud je dokument, který má být přijat, dobropisem, vyberte **PEPPOLCREDITMEMO**.

   Nyní můžete přijmout elektronický dokument spuštěním procesu převodu dat na stránce **Došlé doklady**. Pro více informací navštivte [Příjem a převod elektronických dokladů](purchasing-how-to-receive-and-convert-electronic-documents.md).

### Pro nastavení finančního účtu pro nové řádky nákupní faktury pro neidentifikovatelné a neidentifikovatelné zboží
1. Do pole **Hledat**, zadejte **Nastavení nákupu a závazků** a poté vyberte související odkaz.
2. Na záložce s náhledem **Výchozí účty** vyplňte pole, podle popisu v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Finanční účet pro řádky neobsahující zboží** | Určuje finanční účet, který je automaticky vložen na nákupních řádcích, které jsou vytvořeny z elektronických dokladů, když řádek došlého dokladu neobsahuje identifikovatelné zboží. Řádek došlého dokladu, který nemá kód GTIN nebo číslo zboží dodavatele, bude převeden na nákupní řádek typu **Účet** a pole **Číslo** na nákupním řádku bude obsahovat účet, který jste vybrali v poli **Finanční účet pro řádky neobsahující zboží.**<br /><br /> Jestli necháte pole **Finanční účet pro řádky neobsahující zboží** prázdné a příchozí doklad obsahuje řádky bez identifikovatelných zboží, nebude nákupní doklad vytvořen. Chybová zpráva vás, předtím než dokončíte úlohu, vyzve k vyplnění pole **Finanční účet pro řádky neobsahující zboží**. |

## Viz také
[Elektronická výměna dat](across-data-exchange.md)  
[Fakturace prodeje](sales-how-invoice-sales.md)  
[Záznam nákupu](purchasing-how-record-purchases.md)
