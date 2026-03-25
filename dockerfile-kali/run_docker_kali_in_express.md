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

### 4) Install package you want

# Update package lists first

```bash
apt update
```

# Install the top 10 most popular Kali tools

```bash
apt install -y kali-tools-top10
```

# Or install specific categories

```bash
apt install -y kali-tools-web          # Web application testing
apt install -y kali-tools-information-gathering  # Reconnaissance
apt install -y kali-tools-vulnerability         # Vulnerability scanning
apt install -y kali-tools-passwords    # Password attacks
apt install -y kali-tools-exploitation # Exploitation frameworks
```
