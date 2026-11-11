[![tests](https://github.com/juancalero/ddev-docktopus-phpldapadmin/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/juancalero/ddev-docktopus-phpldapadmin/actions/workflows/tests.yml)
[![release](https://img.shields.io/github/v/release/juancalero/ddev-docktopus-phpldapadmin)](https://github.com/juancalero/ddev-docktopus-phpldapadmin/releases/latest)

# DDEV Docktopus phpLDAPadmin

[phpLDAPadmin](http://phpldapadmin.sourceforge.net/) for DDEV, taken from the [docktopus](https://github.com/juancalero/docktopus) stack, to manage visually the OpenLDAP directory provided by [`ddev-docktopus-ldap`](https://github.com/juancalero/ddev-docktopus-ldap) (installed automatically as a dependency).

> Part of [ddev-docktopus](https://github.com/juancalero/ddev-docktopus) — the meta add-on that installs the whole docktopus stack with one command.

## Installation

```
ddev add-on get juancalero/ddev-docktopus-phpldapadmin
ddev restart
```

## Access

```
ddev phpldapadmin          # or open the URL below
```

| Setting | Value |
| --- | --- |
| URL | `http://<project>.ddev.site:6443` (HTTPS: `:6444`) |
| Login DN | `cn=admin,dc=miempresa,dc=local` |
| Password | `admin` |

The credentials are the defaults of `ddev-docktopus-ldap`; change them in `.ddev/.env.ddev-docktopus-ldap` and restart.

## Configuration

All settings live in `.ddev/.env.ddev-docktopus-phpldapadmin`:

| Variable | Default | Description |
| --- | --- | --- |
| `PHPLDAPADMIN_HTTP_PORT` | `6443` | Router port for the HTTP UI |
| `PHPLDAPADMIN_HTTPS_PORT` | `6444` | Router port for the HTTPS UI |

Note: port 389 is the LDAP protocol port, not an HTTP interface — browsers block it by design (`ERR_UNSAFE_PORT`). Use this UI or a dedicated LDAP client for directory management.

## Uninstallation

```
ddev add-on remove ddev-docktopus-phpldapadmin
ddev restart
```

## License

GPL-2.0-or-later
