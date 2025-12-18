## Podman compose deployment

Podman is natively implementing more namespace isolation that Docker.
Basically it provides more security.

### Changes from the docker implementation
- Nested path are not well supported resulting in relative path interpreted double times.
- Multiple profiles cant be setup.
- "Includes" are not well supported.
- Permissions should be managed using some tricks so user namespace is not breakin access to the config files.

### Checks
- Need delegated access to cpu count

### Identify Podman Socket
We well point the user level podman socket to the scaler and updater container.

### Updated .env

### Deploy
Docker provided syntax 