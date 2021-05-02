# Nextcloud Docker Image

This image extends the official [Nextcloud:fpm image](https://hub.docker.com/_/nextcloud/) with ImageMagick & FaceRecognition requirements support. Images can be found on Docker hub at [`xisdockerhub/nextcloud-facerecognition`](https://hub.docker.com/r/xisdockerhub/nextcloud-facerecognition). 

This container only ensures requirements of the [`face recognition app`](https://apps.nextcloud.com/apps/facerecognition) have been met. You need to install the NextCloud app manually in NextCloud > Apps. Also make sure to select `cron` for `background jobs` in NextCloud > Basic Settings.

![image](https://user-images.githubusercontent.com/1276421/116826747-deb7db00-ab95-11eb-9e5e-a754eb7fc554.png)

# Environment variables

MEMORY_LIMIT: Max memory used by PHP. Face recognition consumes a lot of cpu and memory. By default it's configured to use 2GB (from recommended [hardware requirements](https://github.com/matiasdelellis/facerecognition/wiki/Requirements-and-Limitations#hardware-requirements)).

# Features & additional packages
- Hourly cron for face recognition.
- Hourly cron for preview generation (needs manual install of [preview generation](https://github.com/nextcloud/previewgenerator) app). 
- ImageMagick support
- Nano for some editing convenience
