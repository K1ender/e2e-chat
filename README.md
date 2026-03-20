# ChatApp (Project on Hold)

**Status:** ⚠️ On hold / WIP

This project is a secure chat application prototype with **magic link authentication** and **end-to-end encryption**.

## Features Implemented

* User registration via magic link
* Email-based login (no passwords)
* Generating per-device encryption and signing keys
* Storing encrypted private keys on the server

## Known Limitations

* **Multi-device login is not supported** — private keys are generated per device and cannot be recovered across devices.
* Key recovery across devices is **not implemented**.
* Magic link authentication works **per device only**.
* This project is a prototype and not ready for production use.

## Technology Stack

* Go (backend)
* PostgreSQL (database)
* Docker (development environment)

## Future Work (If Continued)

* Implement multi-device key management and recovery
* Optional password-based backup for keys
* Improve email/magic link workflow
* Enhance security and auditing

## Development

You can spin up the environment using Docker:

```bash
docker-compose up
```

Migrations are handled via `goose`:

```bash
make migrate-up
```