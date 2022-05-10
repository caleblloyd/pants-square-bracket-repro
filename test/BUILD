files(
    name="files",
    sources=["**/*"]
)

docker_image(
    name="docker",
    repository="test",
    image_tags=["latest"],
    dependencies=[":files"],
)