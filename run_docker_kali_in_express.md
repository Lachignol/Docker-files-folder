# Kali Docker without any dockerfile


### 1) Pull the image

```bash
 docker pull kalilinux/kali-rolling
 ```


### 2) Run the container in detach mode and give a more simple name (kali)

```bash
docker run -d -t --name kali kalilinux/kali-rolling
 ```
### 3) Enter in the container

```bash
docker exec -it kali bash
 ```
