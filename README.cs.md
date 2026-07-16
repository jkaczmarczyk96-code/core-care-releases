# CoreCare

**Bezpečná aplikace pro zdraví a čištění Windows.**

Čeština | [English](README.md)

CoreCare pomáhá uživatelům pochopit, co zabírá místo na disku, kontrolovat bezpečné kandidáty k vyčištění, udržovat Windows a sledovat běžné ukazatele zdraví počítače. Soubory nemaže naslepo a systém nemění bez potvrzení.

> CoreCare je momentálně bezplatná beta. Windows verze je aktivně vyvíjena a je vhodné s ní zacházet stejně opatrně jako s ostatními nástroji pro údržbu systému.

## Stažení

Otevřete stránku [CoreCare Releases](https://github.com/jkaczmarczyk96-code/core-care-releases/releases) a stáhněte:

- **`CoreCare-win-Setup.exe`** - doporučený instalátor Windows s automatickými aktualizacemi.
- **`CoreCare-win-Portable.zip`** - přenosná verze určená především pro testování.
- **`.nupkg`, `RELEASES` a `releases.win.json`** - technické soubory aktualizačního systému Velopack; uživatel je nemusí ručně otevírat.

Aktuální veřejná beta je dostupná na stránce [beta.80](https://github.com/jkaczmarczyk96-code/core-care-releases/releases/tag/v0.1.0-beta.80).

## Aktuální funkce

### Smart Cleaner

- Sken vybraného pevného disku.
- Hledání velkých souborů, starých dočasných dat, cache, instalátorů, archivů, obrazů disků a složek s mnoha malými soubory.
- Klasifikace každého nálezu podle kontextu a rizika.
- Ochrana umístění Windows, nainstalovaných aplikací, her, uložených pozic a osobních dat.
- Automatický výběr pouze konzervativních položek s nízkým rizikem.
- Přesun schválených položek do Koše namísto trvalého odstranění.
- Řazení, filtrování, jednotlivý výběr, závěrečná kontrola a průběh mazání.

### Zdraví disku

- Přehled využitého a volného místa pevných disků.
- Kontrola souborového systému pouze pro čtení s průběhem a výsledkem přímo v aplikaci.
- Průvodci opravou souborů Windows, obrazu systému, optimalizací disků a nastavením úložiště.
- Administrátorské akce jsou vždy zřetelné a vyžadují potvrzení.

### Po spuštění

- Detekce aplikací spouštěných s Windows.
- Měření aktuální spotřeby procesoru a paměti běžících startup aplikací.
- Upozornění na náročné aplikace na pozadí.
- Vratné zapnutí a vypnutí položek tam, kde to Windows dovoluje.

### Ovladače a systémové aktualizace

- Detekce dostupných aktualizací ovladačů přes Windows Update.
- Výběr ovladačů a spuštění aktualizace přímo z CoreCare.
- Automatická lokální záloha ovladačů před instalací.
- Stažení a instalace vybraných ovladačů pomocí skrytého zvýšeného procesu CoreCare.
- Průběh, výsledek a požadavek na restart přímo v aplikaci.
- Historie Windows Update a stav čekajícího restartu.

### Soukromí

- Chytré čištění cookies je ve výchozím stavu vypnuté.
- Detekce starých cookies v podporovaných Chromium prohlížečích a Firefoxu.
- Výběr jednotlivých domén namísto smazání všech dat prohlížeče.
- Záloha databáze prohlížeče před odstraněním.

### Výkon

- Měření aktuálního využití procesoru a paměti.
- Seznam aplikací s významnou spotřebou prostředků na pozadí.
- Přímý přístup ke Správci úloh, nastavení napájení a aplikacím po spuštění.

## Bezpečnostní principy

1. Bez schválení uživatele se nic nemaže ani neopravuje.
2. Integrita Windows a aplikací má přednost před uvolněným místem.
3. Nejisté soubory se zobrazí ke kontrole a nevyberou se automaticky.
4. Čištění používá Koš všude, kde je to možné.
5. Instalace ovladačů začne pouze po úspěšné lokální záloze.
6. Nástroje soukromí jsou volitelné a pracují jen s vybranými doménami.

CoreCare záměrně neprovádí čištění registru, automatické systémové zásahy jedním kliknutím ani hromadné mazání historie a cookies.

## Požadavky

- 64bitový Windows 10 nebo Windows 11.
- Připojení k internetu pro kontrolu aktualizací aplikace a ovladačů.
- Potvrzení správce pro instalaci ovladačů a chráněné opravy Windows.

Instalátor je self-contained; uživatel nemusí samostatně instalovat .NET SDK ani runtime.

## Aktualizace

Nainstalovaná aplikace používá [Velopack](https://velopack.io/) a kontroluje nové verze v tomto veřejném repozitáři. Balíček se stáhne až po rozhodnutí uživatele a instalaci provede aktualizační systém CoreCare.

Od verze beta.81 se oficiální build před zabalením obfuskuje a release pipeline vyžaduje platný digitální podpis Windows. Podpis ověřuje původ a integritu souboru, ale nezaručuje nemožnost zpětné analýzy.

## Soukromí

CoreCare momentálně nevyžaduje účet, předplatné, reklamní identifikátor ani analytickou službu. Výsledky skenů a údržby zůstávají v počítači. Online připojení se používá pro kontrolu GitHub releases a uživatelem vyžádané operace Windows Update.

Podrobnosti jsou v [PRIVACY.md](PRIVACY.md).

## Omezení bety

- Aktuální verze podporuje pouze Windows.
- macOS a Linux jsou plánované, ale potřebují vlastní implementaci úložiště, aktualizací, startupu a oprav.
- Mobilní systémy mají výrazně přísnější sandbox a nejsou součástí současné desktopové bety.
- Hardwarová diagnostika, obnova jednotlivých ovladačů, odinstalace aplikací a detekce herních knihoven a uložených pozic se budou dále rozvíjet.

## Podpora a bezpečnost

- Běžné chyby a návrhy hlaste přes [GitHub Issues](https://github.com/jkaczmarczyk96-code/core-care-releases/issues).
- U citlivých bezpečnostních problémů postupujte podle [SECURITY.md](SECURITY.md). Do veřejného issue nevkládejte přihlašovací údaje, osobní soubory ani podrobnosti zneužití.
- Uveďte verzi CoreCare, verzi Windows, dotčenou část aplikace a postup reprodukce.

## Zdrojový kód a licence

Tento repozitář je oficiální veřejný kanál binárních verzí. Zdrojový repozitář CoreCare je privátní. Zveřejnění instalačních balíčků v tomto repozitáři neuděluje licenci ke zdrojovému kódu.

Copyright © přispěvatelé CoreCare. Všechna práva vyhrazena.
