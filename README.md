# docker-nginx-autoindex

This container takes official alpine nginx image and turns on autoindex.

You can do a simple mount to simply serve files from your local
file system with nginx.  Make sure to map the directory you want to serve from with the
`-v` command

```bash
docker run --rm -d --name docker-nginx-autoindex -p '80:80' \
    -v /home/crappy/html:/usr/share/nginx/html:ro crappyrules/docker-nginx-autoindex
```
Then navigate in a browser to http://127.0.0.1 and view the files in the directory you mounted in your volume
