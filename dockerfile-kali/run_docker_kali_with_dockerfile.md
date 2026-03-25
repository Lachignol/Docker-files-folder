# Kali with dockerfile


### 1) Build the image (Example for Dockerfile.kali-web)

```bash
docker build -f Dockerfile.kali-web -t kali-web .
```

### 2) Run it with a volume for saving results

```bash
docker run -it --rm \
  -v $(pwd)/results:/assessments \
  kali-web
```
