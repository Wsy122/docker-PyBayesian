

# Configuration

1. create [dockerfile](dockerfile)
2. build with local matchine or github action
  

2.1 build with docker buildx
```bash
docker buildx build --platform linux/arm64,linux/amd64 -t wanke/nnu-bayes-course:2024 . --push
docker buildx build --platform linux/amd64 -t wanke/nnu-bayes-course:2024 . --load
```

2.1.1 create [docker-image.yml](.github/workflows/docker-image.yml) in `.github/workflows`
2.2.2 config github action secrets in Environment secrets. 
```
username: ${{ secrets.DOCKERHUB_USERNAME }}
password: ${{ secrets.DOCKERHUB_PASSWORD }}
```