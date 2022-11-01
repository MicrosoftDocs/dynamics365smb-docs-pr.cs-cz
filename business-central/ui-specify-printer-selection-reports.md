---
title: Setting Up Printers
description: Learn about setting up printers that you can use for reports and documents and the different print feature available to you in Business Central. 
author: jswymer

ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.search.form: 8900
ms.date: 06/24/2021
ms.author: jswymer
---
# Nastavení tiskáren

Tisk dokladů a sestav z [!INCLUDE[prod_short](includes/prod_short.md)] je důležitým úkolem pro uživatele. Uživatelé budou obvykle chtít odesílat tiskové úlohy přímo na jednu z tiskáren vaší organizace – bez ohledu na to, který [!INCLUDE[prod_short](includes/prod_short.md)] klient nebo aplikaci používají. Protože [!INCLUDE[prod_short](includes/prod_short.md)] je cloudová služba, nemůže se přímo dostat k místním tiskárnám připojeným k zařízením uživatelů, ale může se připojit k tiskárnám s podporou cloudu.

Pro podporu vašich tiskových potřeb [!INCLUDE[prod_short](includes/prod_short.md)] nabízí následující funkce:

| Funkce | Popis | Webový klient | Mobilní aplikace | Aplikace pro Teams |
|-------|-----------|----------|-----------|--------------|
| Universal Print | Universal Print je řešení pro správu tiskáren, které je k dispozici jako cloudová služba od společnosti Microsoft. Díky této funkci můžete nastavit tiskárny v aplikaci Universal Print a poté je zaregistrovat pro použití v [!INCLUDE[prod_short](includes/prod_short.md)]. Tato funkce vyžaduje předplatné Universal Print a rozšíření **Universal Print Integration**. | ![funguje online.](media/check.png) | ![funguje online.](media/check.png) | ![funguje online](media/check.png) |
| Tisk e-mailem | Tato funkce umožňuje nastavit tiskárny s podporou e-mailu. [!INCLUDE[prod_short](includes/prod_short.md)]  pak odešle tiskové úlohy na tiskárnu pomocí e-mailové adresy tiskárny. Tato funkce vyžaduje tiskárny s podporou e-mailu a rozšíření **Odeslat na e-mailovou tiskárnu**. | ![funguje online.](media/check.png) | ![funguje online](media/check.png) | ![funguje online](media/check.png) |
| Tisk z prohlížeče | Tiskové úlohy jsou zpracovávány tiskovou funkcí prohlížeče uživatele. Pokud není nainstalována a nastavena cloudová tiskárna nebo pokud nainstalovaná tiskárna selže, bude tisk ve výchozím nastavení odpovídat možnostem tisku v prohlížeči. Zobrazí se pole **Tiskárna** na stránce *požadavku na sestavu (zpracováno prohlížečem).* | ![funguje online](media/check.png) |

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] podporuje také vlastní rozšíření tiskárny, která přidávají ještě více tiskových funkcí. Pokud jsou tedy nainstalována nějaká vlastní rozšíření tiskárny, může vaše aplikace obsahovat tiskové funkce, které nejsou popsány v tomto článku.

## Nastavení Universal Print

Universal Print je služba založená na předplatném Microsoftu 365, která běží výhradně na Microsoft Azure. Poskytuje centralizovanou správu tiskáren prostřednictvím portálu Universal Print. [!INCLUDE[prod_short](includes/prod_short.md)] zpřístupňuje tiskárny nastavené v programu Universal Print uživatelům klientů prostřednictvím rozšíření **Universal Print Integration**.

![Nastavení Universal Print.](media/Universal-Print-arch.png)

Kompletní nastavení vyžaduje, abyste pracovali v Microsoft Azure pomocí [Azure Portal](https://portal.azure.com) a v [!INCLUDE[prod_short](includes/prod_short.md)].

### Podporované tiskárny

[!INCLUDE[prod_short](includes/prod_short.md)] podporuje stejné tiskárny jako Universal Print, což mohou být tiskárny kompatibilní s Universal Print nebo i nekompatibilní. Nekompatibilní tiskárny nemohou komunikovat s Universal Print přímo, takže vyžadují další software konektoru, který poskytuje Universal Print. Některé starší tiskárny nemusí být podporovány.

<!-- TODO If not installed, go to AppSource -->

### Předpoklady

**Pro [!INCLUDE[prod_short](includes/prod_short.md)]**

- [!INCLUDE[prod_short](includes/prod_short.md)] 2021 release wave 1 nebo starší
- Je nainstalováno rozšíření **Universal Print Integration**

   Toto rozšíření je ve výchozím nastavení publikováno a nainstalováno jako součást [!INCLUDE[prod_short](includes/prod_short.md)] online a on-premises.  Můžete ověřit, zda je nainstalován na stránce **Správa rozšíření**. Pro více informací navštivte [Instalace a odinstalování rozšíření v Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] on-premises:
   - Je nakonfigurované ověřování Azure Active Directory (AD) nebo NavUserPassword
   - Aplikace pro Business Central je zaregistrovaná ve vašem tenantu Azure AD a [!INCLUDE[prod_short](includes/prod_short.md)]

      Stejně jako ostatní služby Azure, které fungují s [!INCLUDE[prod_short](includes/prod_short.md)], vyžaduje Universal Print registraci aplikace pro [!INCLUDE[prod_short](includes/prod_short.md)] v Azure Active Directory (Azure AD). Registrace aplikace poskytuje ověřovací a autorizační služby mezi [!INCLUDE[prod_short](includes/prod_short.md)] a Universal Print.

      Vaše nasazení již může používat registraci aplikace pro jiné služby Azure, například Power BI. Pokud ano, použijte stávající registraci aplikace také pro Universal Print namísto přidání nové. Jediné, co budete muset v tomto případě udělat, je upravit registraci aplikace tak, aby zahrnovala příslušná oprávnění k tisku pro rozhraní Microsoft Graph API.

      Chcete-li zaregistrovat aplikaci a nastavit správná oprávnění, postupujte podle kroků popsaných v části [Registrace aplikace v Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

**Pro Universal Print**

- Předplatné/licence Universal Print pro vaši organizaci.

   Pro více informací navštivte [License Universal Print](/universal-print/fundamentals/universal-print-license).

- V Azure máte role **Správa tiskáren** a **Globální správce**.

   Chcete-li spravovat Universal Print, váš účet musí mít role **Správa tiskáren** a **Globální správce** v Azure AD. Tyto role jsou potřebné pouze pro správu Universal Print. Uživatelé je nevyžadují, aby používali tiskárny z [!INCLUDE[prod_short](includes/prod_short.md)].

### Nastavení Universal Print a přidání tiskáren v Microsoft Azure

Než začnete spravovat tiskárny Universal Print v Business Central, musíte projít několika úlohami, abyste Universal Print zprovoznili v Azure s tiskárnami, které chcete použít.

Podrobné pokyny k nastavení naleznete v tématu [Začínáme: Nastavení Universal Print](/universal-print/fundamentals/universal-print-getting-started) v dokumentaci Universal Print. Zde je přehled kroků, které budete muset dokončit. Většina těchto kroků se provádí v Azure Portal.

1. Přiřaďte licence Universal Print sobě a dalším uživatelům.

   Způsob přiřazení licence závisí na tom, zda integrujete s Business Central online nebo on-premises.

   - S [! INCLUDE[prod_short](includes/prod_short.md)] online přiřadíte licence pomocí Centra pro správu Microsoft 365.

      Pro více informací navštivte [Microsoft Admin Center Help - Přiřazení licencí uživatelům](/microsoft-365/admin/manage/assign-licenses-to-users).

   - S [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, přiřadíte licence ve svém tenantovi Azure pomocí Azure Portal.

      Pro více informací navštivte [Azure Directory - přiřazení nebo odebrání licencí na portálu Azure Active Directory](/azure/active-directory/fundamentals/license-users-groups).

2. Nainstalujte konektor Universal Print pro registraci tiskáren, které nemohou komunikovat přímo s Universal Print.

   Většina tiskáren na trhu nemůže komunikovat přímo s Universal Print. Pro tyto tiskárny budete muset nainstalovat konektor Universal Print. Pro více informací navštivte [Instalace konektoru pro Universal Print](/universal-print/fundamentals/universal-print-connector-installation).

3. Zaregistrujte své tiskárny v Universal Print.

   Registrací tiskárny se Universal Printer dozví o tiskárně.

   - U tiskáren, které mohou komunikovat přímo s universal print, postupujte podle kroků výrobce tiskárny.

   - U ostatních tiskáren zaregistrujte tiskárny pomocí konektoru Universal Print.

      Pro více informací navštivte [Registrace tiskárny](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Změna vlastností tiskárny (volitelné)

   Po registraci tiskárny můžete zobrazit a upravit vlastnosti tiskárny, například výchozí předvolby.

   Pro více informací navštivte [Správa nastavení tiskárny pomocí portálu Universal Print](/universal-print/portal/configure-printer-settings).

5. Sdílení tiskáren.

   Libovolná tiskárna, kterou chcete použít v [!INCLUDE[prod_short](includes/prod_short.md)] bude muset být sdílena v Universal Print.

   <!--For more information, see [Share a Printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer). -->

   Pro více informací navštivte [Sdílení tiskárny](/universal-print/portal/share-printers).

6. Udělte uživatelům oprávnění ke sdíleným tiskárnám.

   <!--For more information, see [Printer Permissions](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).-->

   Pro více informací navštivte [Oprávnění tiskárny](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).


7. Povolit převod dokumentů.

   Universal Print vykresluje obsah pro tisk ve formátu XPS. Některé starší tiskárny na trhu nepodporují vykreslování obsahu XPS – v mnoha případech pouze ve formátu PDF. Tisk na těchto tiskárnách se nezdaří, pokud není nástroj Universal Print nastaven tak, aby převáděl dokumenty do formátu podporovaného tiskárnou.

   Pro více informací navštivte [Přehled převodu dokumentů](/universal-print/portal/document-conversion).

Nyní jste připraveni přidat tiskárny do [!INCLUDE[prod_short](includes/prod_short.md)], nastavit výchozí tiskárny pro sestavy a tisknout.

### Přidání tiskáren Universal Printer do Business Central

Po nastavení a sdílení tiskáren v univerzálním tisku jste připraveni k jejich použití v Business Central. Existují dva způsoby, jak přidat tiskárny Universal Print. Tiskárny můžete přidat všechny najednou nebo jednotlivě, jednu po druhé.

Individuální přidání tiskáren vám umožní nastavit stejnou tiskárnu Universal Print v Business Central více než jednou. U každé přidané tiskárny pak můžete změnit nastavení tisku, například zásobník papíru, velikost a orientaci. Tímto způsobem můžete nastavit tiskárny pro různé sestavy a doklady, které mají speciální požadavky na výstup.

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Správa tiskáren** a poté vyberte související odkaz.
2. Vyberte **Universal Print** a pak zvolte jednu z následujících možností:

   - **Přidejte všechny tiskárny Universal Print** , chcete-li přidat všechny tiskárny, které ještě nebyly přidány. Tuto možnost můžete použít i v případě, že již byly přidány tiskárny.

   - **Přidejte tiskárnu Universal Print** a přidejte konkrétní tiskárnu.
3. Postupujte podle pokynů na obrazovce.

   - Pokud zvolíte **Přidat všechny tiskárny Universal Print** spustí se nastavení **Přidat Universal Print Tiskárny**. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

   - Pokud jste zvolili možnost **Přidat Universal Print tiskárnu** zobrazí se stránka **Nastavení Universal Printer**. Vyplňte pole **Název**, vyberte **...** vedle pole **Sdílet tiskárnu v Universal Print** a vyberte tiskárnu Universal Print. Podle potřeby vyplňte zbývající pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

   Tyto akce ověří vaše nastavení Azure AD (pro on-premises), zkontrolujte, zda máte licenci Universal Print, a nakonec přidejte tiskárny.

   > [!NOTE]
   > Pokud se jedná o on-premises připojení k Universal Print, zobrazí se stránka AZURE ACTIVE DIRECTORY SERVICE PERMISSIONS a budete vyzváni k udělení souhlasu se službami Azure. Souhlas musíte udělit pouze jednou.

Po přidání tiskárny můžete zobrazit a změnit její nastavení ve **Správě tiskáren**. Stačí vybrat tiskárnu a poté zvolit **Upravit nastavení tiskárny**.

<!--
### Troubleshooting

#### You don't see the a printer in the 

The printer is not shared in Universal Print.

### You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps

## You don't have access to the printer

- You have not been assigned a Up license
- You have not been given access to the printer in UP.
- (On-prem) The app registration has been broken
-->
## Nastavení e-mailového tisku

### Předpoklady

- [!INCLUDE[prod_short](includes/prod_short.md)] 2020 release wave 1 nebo starší
- Je nainstalováno rozšíření **Send to Email Printer**.

   Toto rozšíření je nainstalováno ve výchozím nastavení. Informace o instalaci rozšíření naleznete v tématu
- Funkce e-mailu je nastavena.

   Pro více informací navštivte [Nastavení E-mailu](admin-how-setup-email.md).

### Přidání e-mailové tiskárny

Na stránce **Správa tiskáren** se zobrazují aktuálně nastavené tiskárny. Stránka také umožňuje přístup na stránku **Nastavení** pro každou tiskárnu, kde můžete upravit stávající nastavení nebo nastavit novou tiskárnu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Správa tiskáren** a poté vyberte související odkaz.
2. Vyberte **Tisk e-mailem** a poté zvolte **Přidání e-mailovové tiskárny**.
3. Na stránce **Nastavení tisku e-mailem** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Musíte ručně vybrat vhodnou velikost papíru pro tiskárnu, protože nelze uložit žádná místní tiskárna ani uživatelská nastavení.
   >
   > Dejte si pozor na to, že rozšíření Email Printer je ve výchozím nastavení nastaveno na velikost papíru **A4**, což není vhodné například v Severní Americe.

### Oznámení o ochraně osobních údajů

Pokud používáte rozšíření Email Printer budou všechny nebo některé tiskové úlohy odeslány na e-mailovou adresu nakonfigurovanou pro tiskárnu. Důrazně doporučujeme, aby bylo jedinečné ID e-mailu vázáno na tiskové zařízení, které používá pouze oficiální služby poskytované výrobcem hardwaru, jako jsou HP ePrint, KonicaMinolta EveryonePrint nebo Epson Email Print.

Proveďte všechna nezbytná opatření v oblasti ochrany osobních údajů, včetně zajištění toho, aby řešení pro tisk e-mailů mělo správně nakonfigurovaná oprávnění, nastavení ochrany osobních údajů a zásady uchovávání informací. Je vaší odpovědností uvést správnou, ověřenou a funkční e-mailovou adresu. Pro více informací navštivte [Prohlášení společnosti Microsoft o zásadách ochrany osobních údajů](https://privacy.microsoft.com/privacystatement).


## <a name="default"></a>Nastavení výchozích tiskáren

Existuje několik způsobů, jak nastavit tiskárny, které budou ve výchozím nastavení používány pro tiskové úlohy. Výchozí tiskárna je užitečná, pokud pracujete s různými sestavami, které vyžadují různé tiskárny z důvodu jejich umístění ve společnosti nebo jejich výstupních schopností.

### Nastavení tiskárny jako výchozí tiskárny pro všechny tiskové úlohy

Stránka **Správa tiskáren** umožňuje nastavit tiskárnu jako výchozí tiskárnu pro všechny tiskové úlohy. Tiskárnu můžete určit jako výchozí pouze pro vás nebo pro všechny uživatele.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Správa tiskáren** a poté vyberte související odkaz.

   > [!TIP]
   > Můžete také otevřít stránku **Správa tiskáren** ze stránky **Výběry tiskáren** výběrem **Správa tiskárny**.
2. Na stránce **Správa tiskáren** vyberte tiskárnu ze seznamu, zvolte **Spravovat**a poté zvolte **Nastavit jako výchozí tiskárnu** nebo **Nastavit jako výchozí tiskárna pro všechny uživatele**.

> [!NOTE]
> Nastavením výchozí tiskárny z **Správa tiskáren** přidáte položku do **Výběry tiskáren**.

### Nastavení výchozí tiskárny pro konkrétní sestavy

Na stránce **Výběry tiskáren** můžete určit tiskárnu, kterou bude sestava používat ve výchozím nastavení. Výchozí tiskárny jsou nastaveny na základě uživatelského účtu. Výchozí tiskárnu můžete nastavit pouze pro sebe, jiného uživatele nebo všechny uživatele.

> [!IMPORTANT]
> Pro [!INCLUDE[prod_short](includes/prod_short.md)] on-premises lze stránku **Výběr tiskárny** použít pouze pro cloudové tiskárny definované rozšířeními tiskáren, jako jsou tiskárny Email Print a Universal Print. Nelze jej použít pro místní tiskárny

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výběry tiskáren** a poté vyberte související odkaz. Místo toho na stránce **Správa tiskáren** vyberte tiskárnu a poté zvolte akci **Výběry tiskáren**.
2. Vyberte akci **Nový**, chcete-li přidat výběr tiskárny pro konkrétní sestavu.
3. Vyplňte pole podle potřeby.

Zadaná sestava je nyní ve výchozím nastavení nastavena tak, aby se tiskla na vybrané tiskárně.

> [!NOTE]
> Při tisku dané sestavy můžete vybrat jinou tiskárnu pomocí pole **Tisk** na stránce požadavku.

> [!NOTE]
> okud na stránce **Výběr tiskárny** nenastavíte sestavu pro konkrétní tiskárnu, vytiskne se na výchozí tiskárně společnosti definované na stránce **Správa tiskáren**.

Vy nebo správce můžete na stránce **Výběry tiskáren** definovat také další varianty tisku pro uživatele a sestavy. Následující tabulka popisuje kombinaci hodnot pro určení různých nastavení tisku sestavy.

| Viz | Nastavte následující hodnoty |
|---------------------------------------------------|---------------------------------------------------------------------|
| Tisk sestavy na konkrétní tiskárně pro všechny uživatele | Zadejte hodnoty do polí **ID sestavy** a **Název tiskárny** a pole **ID uživatele** ponechte prázdné. |
| Tisk všech sestav na konkrétní tiskárně pro konkrétního uživatele | adejte hodnoty do polí **ID uživatele** a **Název tiskárny** a pole **ID sestavy** ponechte prázdné. Tato položka provede totéž jako akce **Nastavit jako výchozí tiskárnu** na stránce **Správa tiskáren**. |
| Nastavení výchozí tiskárny pro všechny sestavy pro všechny uživatele | Zadejte hodnotu do pole **Název tiskárny** a pole **ID uživatele** a **ID sestavy** ponechte prázdná. Tato položka provede totéž jako akce **Nastavit jako výchozí tiskárnu pro všechny uživatele** na stránce **Správa tiskáren**. |
| Tisk konkrétní sestavy na výchozí tiskárně uživatele | Zadejte hodnotu do pole **ID sestavy** a pole **Název tiskárny** a **ID uživatele** ponechte prázdná. |
| Tisk konkrétní sestavy na konkrétní tiskárně pro konkrétního uživatele | Zadejte hodnoty do všech tří polí. |

> [!NOTE]
> Specifičtější výběr tiskárny má přednost před obecnějším výběrem tiskárny. Například výběr tiskárny, který má hodnoty v polích **ID uživatele**, **ID sestavy** a **Název tiskárny**, má přednost před výběrem tiskárny, který má prázdné pole **ID uživatele** nebo **ID sestavy**.

### Výběr tiskárny při spuštění sestavy
Namísto použití výchozí tiskárny při spuštění sestavy můžete toto nastavení přepsat ze stránky požadavku. Jednoduše vyberte tiskárnu, kterou chcete použít pro toto vyvolání sestavy v rozevírací nabídce **Tiskárna**.

### Určování velikosti tiskových úloh

Cloudový tisk je určen pro dokumenty přiměřené velikosti. Většina cloudových služeb, včetně PrintNode a HP ePrint, má limit 10 MB na úlohu. Pokud potřebujete vytisknout větší sestavy, bude pravděpodobně nutné je rozdělit do více výtisků.

## Viz také

[Tisk sestav](ui-work-report.md#PrintReport)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Spouštění dávkových úloh](ui-how-run-batch-jobs.md)  
[Posílejte dokumenty e-mailem](ui-how-send-documents-email.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
