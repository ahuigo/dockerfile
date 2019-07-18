build:
	docker build -t slim-py .
	docker-slim build --http-probe slim-py
init:
	docker run --name slim-py -it slim-py bash
start:
	#docker start -it slim-py  bash
	docker exec -it slim-py  bash
