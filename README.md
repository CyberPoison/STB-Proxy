Play STB portal streams via m3u player

# Docker
- Map whichever port you like to the default `8001`
- `HOST` should be the docker host ip + the port you chose
- Mounting `/config` is required if you want your credentials to persist through restarts
@@ -19,3 +20,11 @@ docker create \
-v </host/path>:/config \
chris230291/stb-proxy:latest
```

# Without Docker

- Requires: `python 3` `fastapi` `requests` `uvicorn` `jinja2` `python-multipart`
- Download the repo
- Doubble click `app.py`
- Go to `http://localhost:8001` in a browser and enter Portal URL + MAC
- Load `http://localhost:8001/playlist` in a m3u player, eg VLC
