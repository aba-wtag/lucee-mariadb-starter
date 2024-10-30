# Custom_Lucee
This is a `Dockerfile` that will help create a custom `lucee` server for `ColdFusion` development. The main purpose of creating this `Dockerfile` to get an `URL rewrite` enabled `lucee` image that can be used for personalized routing.



## Build

Use the following command to build the image.

```bash
docker build -t custom-lucee:latest .
```

## Run

Change the `${FOLDER_NAME}` with your desired folder path and use the following command to run the image.

```bash
docker run \
  -it \
  -rm \
  -p 8888:8888 \
  --name custom-lucee \
  --network host \
  -v "/home/abir/${FOLDER_NAME}:/var/www/" \
  -e LUCEE_ADMIN_PASSWORD=hello \
  custom-lucee:latest

```



