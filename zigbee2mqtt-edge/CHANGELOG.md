## Changes
- Removed pm2 in favor of using watchdog
- Unified Dockerfile into a single common file
- Moved run.sh and socat.sh to new s6 approach using rootfs
- Version control now it's only in config.json
- Stable version migrated to X.X.X-A for easier Dockerfile management
- Added local_build.sh script
- Removed some obsolete debug messages for Edge as we're no longer manipulating the options that heavily
- Removed duplicate `icon` and `logo`
- Added new pipelines in `pipeline/` with proper names
- Pipelines now reuse a common template to reduce code duplication
- Pipelines now auto-generate `arch` specific jobs based on supported arch in `config.json`
- Restricted Edge pipeline triggers to specific files - Manual trigger still works like previous setup
- Pipeline triggers migrated to `dev` branch
- Updated Edge and Stable dockerfiles to be identical with the exception of Zigbee2mqtt download source and version
- Fixed `Docker Pulls` to point to correct location and use markdown code
- Tracks latest Zigbee2mqtt [`dev branch`](https://github.com/Koenkk/zigbee2mqtt/commits/dev)