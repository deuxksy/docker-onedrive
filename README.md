# onedrive

## first run

first only docker run because *onedrive authentication realtime url check*

```bash
export ONEDRIVE_DATA_DIR="/home/crom/OneDrive/cromksy"
mkdir -p ${ONEDRIVE_DATA_DIR}
docker run -it --name onedrive \
-v "/home/crom/Docker/onedrive/etc/conf:/onedrive/conf" \
-v "${ONEDRIVE_DATA_DIR}:/onedrive/data" \
-e "ONEDRIVE_UID:1000" \
-e "ONEDRIVE_GID:1000" \
driveone/onedrive:latest
```