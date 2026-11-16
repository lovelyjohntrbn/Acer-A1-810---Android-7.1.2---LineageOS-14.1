# Experimentální obnova na testovaném Acer Iconia A1-810

Zatím **není připraven veřejný univerzální instalační balíček**. Následující postup popisuje přípravu obnovy obrazu boot a system pořízeného ze stejného tabletu. Záloha zatím nebyla ověřena skutečným obnovovacím flashem a nevíme, zda bude fungovat na jiném kusu zařízení.

## Co je potřeba

- Acer Iconia A1-810, dostatečně nabitý, spolehlivý USB kabel, Windows, funkční ovladač MediaTek VCOM a SP Flash Tool.
- Vlastní ověřenou zálohu původního firmwaru a individuálních dat konkrétního zařízení a ověřený postup návratu. NVRAM a další individuální oddíly nikdy nepřebírejte z jiného tabletu.
- Odpovídající scatter, `boot.img` a `system.img` pro daný konkrétní tablet; před použitím ověřte jejich SHA-256 proti spolehlivému seznamu a porovnejte rozložení oddílů s daným zařízením.

Aktuální soukromá záloha se skládá z kopií boot a system; neobsahuje celý oddíl `/data`, osobní účet, nainstalované hry, jejich data ani případné aktualizace aplikací uložené v `/data`. Obrázek recovery je samostatná záloha, kterou při běžné obnově systému nevybírejte.

## Obnova pomocí SP Flash Tool

1. Spusťte SP Flash Tool a načtěte odpovídající scatter.
2. Zrušte zaškrtnutí všech řádků. Vyberte pouze **BOOTIMG** s ověřeným `boot.img` a **ANDROID** s ověřeným `system.img`; před pokračováním znovu zkontrolujte, že nejsou vybrané další řádky.
3. Použijte pouze **Download Only**, spusťte Download a připojte vypnutý tablet způsobem odpovídajícím používanému ovladači. Neodpojujte ho během zápisu. Počkejte na potvrzení nástroje.
4. Odpojte tablet a spusťte jej. První spuštění může trvat déle. Přihlášení a data se řídí stavem existujícího oddílu `/data`.

**Nepoužívejte Format ani Firmware Upgrade** a nevybírejte preloader, NVRAM, PROTECT, MBR ani EBR: nejde o součást tohoto postupu. Zelené potvrzení samo o sobě neprokazuje funkčnost Androidu po restartu.

## Známý stav

Na jednom zkoušeném zařízení funguje grafická akcelerace, Wi‑Fi, Bluetooth (včetně přenosu souboru), reproduktor a mikrofon, otáčení obrazovky a obchod Play. Fotoaparát není zprovozněn; VPN nebyla ověřena. Po přihlášení Google může být tablet dočasně pomalý, než doběhne synchronizace a aktualizace.

Google služby jsou v konkrétním testovaném snímku systému již přítomné. Nejde o povolení k jejich veřejné distribuci. Veřejný návod na samostatnou instalaci Google služeb bude doplněn až s ověřeným a legálně dostupným balíčkem a postupem pro recovery.
