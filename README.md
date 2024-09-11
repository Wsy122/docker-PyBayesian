

# Configuration

1. create [dockerfile](dockerfile)
2. create [docker-image.yml](.github/workflows/docker-image.yml) in `.github/workflows`
3. build with local matchine or github action

```bash
docker buildx build --platform linux/arm64,linux/amd64 -t wanke/nnu-bayes-course:2024 . --push
docker buildx build --platform linux/amd64 -t wanke/nnu-bayes-course:2024 . --load
```
