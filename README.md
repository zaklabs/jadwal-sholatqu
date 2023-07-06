# Jadwal Sholat wilayah Indonesia 

# Requirement
| PHP | Package |
| --- | --- |
| <8.0 | v1.x |
| >= 8.0 | v2.x |

# Instalation
```bash
composer require zaklabs/jadwal-shalatqu
```

# Using
```php
<?php
// Autoload
require_once 'vendor/autoload.php';

// Import class JadwalShalat
use Zaklabs\JadwalShalat\JadwalShalatQu;

// Instansiasi class JadwalShalat
$jadwalShalat = new JadwalShalatQu;

// to get provins lists, use method getProvinsi()
$provinsi = $jadwalShalat->getProvinsi();

// to get kabupaten/kota lists, use method getKabupatenKota()
// with parameter id provinsi
$kabkot = $jadwalShalat->getKabupatenKota('EO6iWQIGAJz%2BdTdDISh9DroWDN7aEy8IzRCRwmDEgmpP5vfnNUaOA5gvNi9opOIf7fvCxJEOuYPoZb4LDFb%2FfA%3D%3D');

// Note:
// id provinsi & id kabupaten/kota will be changing & expired,

// to get data jadwal shalat for 1 month, use method getJadwalShalat()
// with parameter id provinsi, id kabupaten/kota, month, dan year
$jadwal = $jadwalShalat->getJadwalShalat('EO6iWQIGAJz%2BdTdDISh9DroWDN7aEy8IzRCRwmDEgmpP5vfnNUaOA5gvNi9opOIf7fvCxJEOuYPoZb4LDFb%2FfA%3D%3D', 'hiXdUObhOxCwZltIzJP%2Fok10gA%2FWv6AyHyjV4Kv9fUFQHj8l%2Bfg6l0VlkC%2FB6%2BvlSSJ3Qbq0sC%2FE4YC8RMerGQ%3D%3D', 1, 2023);

```
