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
ddev phpldapadmin          # or open http://<project>.ddev.site:6443
```

| Setting | Value |
| --- | --- |
| URL | `http://<project>.ddev.site:6443` (HTTPS: `:6444`) — also `ddev phpldapadmin` |
| Login DN | `cn=admin,dc=miempresa,dc=local` |
| Password | `admin` |

Change the router ports in `.ddev/.env.ddev-docktopus-phpldapadmin` (`PHPLDAPADMIN_HTTP_PORT`, `PHPLDAPADMIN_HTTPS_PORT`).

Note: port 389 is the LDAP protocol port, not an HTTP interface — browsers block it by design (`ERR_UNSAFE_PORT`). Use this UI or a dedicated LDAP client for directory management.

## Uninstallation

```
ddev add-on remove ddev-docktopus-phpldapadmin
ddev restart
```

## License

GPL-2.0-or-later
