# F5-TTS: A Fairytaler that Fakes Fluent and Faithful Speech with Flow Matching

### Build the image:
- Locally: `docker build -t F5-TTS .`
- From the repository: `docker build -t F5-TTS https://github.com/procrastinando/F5-TTS-dockerfile.git#main:.`

### Option 1: Deploy by command:
```
docker run -d -p 7861:7860 F5-TTS
```
### Option 2: Deploy it as stack:
```
services:
  app:
    image: F5-TTS
    ports:
      - "7861:7860"
    restart: unless-stopped
```
### To update:
```
docker rm -f F5-TTS
docker build --no-cache --pull -t F5-TTS https://github.com/procrastinando/F5-TTS-dockerfile.git#main:.
```
