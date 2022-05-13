# onedrive

## first run

최초 실행시 onedrive 인증을 위해서 docker run 으로 실행이 필요함

```bash
sudo podman run -it --name onedrive \
-v "/home/crom/Docker/onedrive/etc/conf:/onedrive/conf" \
-v "/home/crom/Docker/onedrive/log/onedrive:/var/log/onedrive/" \
-v "/home/crom/OneDrive/cromksy:/onedrive/data" \
-e "ONEDRIVE_UID:1000" \
-e "ONEDRIVE_GID:1000" \
-e "ONEDRIVE_RESYNC:1" \
-e "TZ:Asia/Seoul" \
driveone/onedrive:stretch
```

## 설정파일

기본 설정 파일 위치를 /onedrive/conf 로 강제함에 따른 config 위치 확인
