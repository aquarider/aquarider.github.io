# Developer Resources - Docker

## Basic Commands

- Get images

    `docker pull kalilinux/kali-rolling`

    `docker pull ubuntu`

- Run container

    `docker run --rm --privileged -it <imagename>`

- Update image

    `docker commit <containerid> <imagename:tag>`