`docker build . -t python-docker-image`
`docker run --name python-docker-container -it -p 8000:8000 -v "$(pwd):/usr/src/app" python-docker-image`