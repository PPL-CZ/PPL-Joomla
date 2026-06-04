# Changelog

## [1.1.0] - 2026-06-04

### Přidáno
- Implementace nového mapového widgetu PPL pro výběr výdejních míst
- Nastavení a verifikace mapového widgetu podle API klíče

### Opraveno
- Oprava seznamu povolených zemí
- Oprava XML manifestů (zpětná kompatibilita s Joomla 4)
- Opravy drobných bugů

## [1.0.3] - 2026-01-26

### Přidáno
- **PPL Parcel CZ Smart To Box (SBOX)**: Podpora nové dopravy do boxů s automatickou validací rozměrů balíků
- **Nastavení kategorie produktu**: Nastavení rozměrů zásilky na úrovni kategorie produktu
- **Granulace balení**: Nastavení granulace balení produktu pro optimalizaci počtu balíků
- **Přesouvání zásilek**: Přesouvání zásilek mezi dávkami v administraci
- **Aktualizace zemí**: Aktualizace seznamu zemí dostupných pro výdejní místa (AT, NL, BG, RO, HU)
- **Cron endpointy**: Automatická aktualizace stavů zásilek, načítání config souborů a mazání starých logů
- **Error log**: Funkce pro sledování a reportování chyb při vytváření zásilek

### Opraveno
- **Ukládání stavů**: Opraveno ukládání phase_label a status_label do databáze (omezení délky textu)
- **Rušení balíků**: Opraveno předávání order_id do endpoint ShipmentController::cancel_package()
- **Mazání logů**: Opraven odkaz pro mazání logů v LogPage
- **VirtueMart verze**: Opraveno získávání VirtueMart verze v ErrorLogDenormalizer
- **Prázdný seznam metod**: Zobrazení prázdného seznamu dopravních metod nyní zobrazuje varování

### Změněno
- **Refaktorizace kódu**: Rozsáhlá refaktorizace kódu z WooCommerce verze do Joomla struktury
- **OpenAPI schema**: Aktualizace schema.json a regenerace Symfony normalizerů/denormalizerů
- **Error handling**: Vylepšení fallback logiky pro sbírání chyb v LabelShipmentForm

## [1.0.2] - 2025-12-05

### Opraveno
- **Batch tisk zásilek**: Opraveno náhodné selhání při hromadném tisku - zásilky zůstávaly v "InProcess" stavu místo "Complete"
- **Nastavení tisku**: Opravena chyba při ukládání nastavení tisku štítků (endpoint `setting.update_print`)
- **Řazení etiket**: Opraveno pořadí tisku etiket - odstraněn problematický `ShipmentNumber` z řazení
- **Batch remote ID**: Opraveno předávání `batchRemoteId` a formát sloupce `remote_batch_id` v tabulce `pplcz_batch`
- **Ukládání poznámek**: Opraveno ukládání poznámek do adresy v `AddressModelDenormalizer.php`
- **PHP warnings**: Odstranění undefined array key warnings v `CartModelDernomalizer.php`, `ShipmentSettingDenormalizer.php` a `pplshipping.php`
- **Null warnings**: Opraveny null warnings v `pplshipping.php`, `select-parcelshop-inner.php`, `CartValidator.php`
- **Zpracování dat z DB**: Opraveno zpracování dat z databáze
- **Config soubory**: Opraveno ukládání config souborů do extension tabulky
- **Validace košíku**: Opravena validace země dopravy v košíku - upravena podmínka pro zobrazení PPL metod a mapy
- **Kód země**: Opraveno získání kódu země v `CartModelDenormalizer.php`, `ShipmentSettingDenormalizer.php`, `CartValidator.php`
- **Formátování**: Upraven `label-method.css` pro správné formátování odkazu mapy

## [1.0.1] - 2025-12-01

### Opraveno
- **Instalace tabulek**: Opravena instalace databázových tabulek v `script.php` - přidána kontrola a ruční SQL instalace
- **PHP warning**: Odstraněno PHP warning v `ShipmentSettingDenormalizer.php:117` - ošetření undefined array key 'enabled'
- **PHP warning**: Odstraněno PHP warning v `pplshipping.php:273` - oprava pořadí parametrů
- **Admin menu**: Odebrána záložka "Nahlásit problém" z admin menu

## [1.0.0] - 2025-11-28

### Přidáno
- **Základní vydání**: PPL CZ komponenta pro Joomla 5.0+ a VirtueMart 4.0+
- **PPL API integrace**: Integrace s PPL API, React admin rozhraní, správa zásilek a štítků
- **ParcelShop**: Podpora ParcelShop výdejních míst, dobírek a více měn

[1.1.0]: https://github.com/PPL-CZ/PPL-Joomla/releases/tag/1.1.0
[1.0.3]: https://github.com/PPL-CZ/PPL-Joomla/releases/tag/v1.0.3
[1.0.2]: https://github.com/PPL-CZ/PPL-Joomla/releases/tag/v1.0.2
[1.0.1]: https://github.com/PPL-CZ/PPL-Joomla/releases/tag/v1.0.1
[1.0.0]: https://github.com/PPL-CZ/PPL-Joomla/releases/tag/v1.0.0
