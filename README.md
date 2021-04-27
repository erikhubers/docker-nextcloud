# Nextcloud Docker Image

This image extends the official Nextcloud image, ImageMagick & FaceRecognition requirements support. Images can be found on Docker hub at `xisdockerhub/nextcloud`. 

To build this image yourself, run `docker build --build-arg NEXTCLOUD_VERSION=[version] .` I build using GitLab CI by tagging this repo with the version of Nextcloud I want to extend; see `.gitlab-ci.yml`. 
