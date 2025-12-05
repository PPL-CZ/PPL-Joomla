# Changelog

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

## [1.0.1] - 2025-12-0

### Opraveno
- Opravena instalace databázových tabulek v `script.php` - přidána kontrola a ruční SQL instalace
- Odstraněno PHP warning v `ShipmentSettingDenormalizer.php:117` - ošetření undefined array key 'enabled'
- Odstraněno PHP warning v `pplshipping.php:273` - oprava pořadí parametrů
- Odebrána záložka "Nahlásit problém" z admin menu

## [1.0.0] - 2025-11-28

### Přidáno
- Základní vydání PPL CZ komponenty pro Joomla 5.0+ a VirtueMart 4.0+
- Integrace s PPL API, React admin rozhraní, správa zásilek a štítků
- Podpora ParcelShop výdejních míst, dobírek a více měn

[1.0.2]: https://github.com/PPL-CZ/PPL-Joomla/releases/tag/v1.0.2
[1.0.1]: https://github.com/PPL-CZ/PPL-Joomla/releases/tag/v1.0.1
[1.0.0]: https://github.com/PPL-CZ/PPL-Joomla/releases/tag/v1.0.0
