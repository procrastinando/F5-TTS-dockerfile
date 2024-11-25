# F5-TTS: A Fairytaler that Fakes Fluent and Faithful Speech with Flow Matching

### Build the image:
- Locally: `docker build -t f5-tts .`
- From the repository: `docker build -t f5-tts https://github.com/procrastinando/F5-TTS-dockerfile.git#main:.`

### Option 1: Deploy by command:
```
docker run -d -p 7861:7860 f5-tts
```
### Option 2: Deploy it as stack:
```
services:
  app:
    image: f5-tts
    ports:
      - "7861:7860"
    restart: unless-stopped
```
### To update:
```
docker rm -f f5-tts
docker build --no-cache --pull -t f5-tts https://github.com/procrastinando/F5-TTS-dockerfile.git#main:.
```
