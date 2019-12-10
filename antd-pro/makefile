version?=0.2.0
base_image=antbear-ui-base
image_name=antbear-ui
docker_hub=registry.ahuigo.com/hd_map/
image-base:
	echo build base $(version)
	docker image build -t $(base_image):$(version) . -f Dockerfile.base
	docker tag $(base_image):$(version) $(docker_hub)$(base_image):$(version)
	docker tag $(base_image):$(version) $(docker_hub)$(base_image):latest
image:
	echo build $(version)
	docker image build -t $(image_name):$(version) .
	docker tag $(image_name):$(version) $(docker_hub)$(image_name):$(version)
push:
	docker push $(docker_hub)$(image_name):$(version)
run:
	docker run --rm -p 8000:8000 -p 3000:3000 $(image_name):${version}
nginx:
	docker run --rm -p 8000:8000 -v $(pwd)/dist:/usr/share/nginx/html -v $(pwd)/nginx.conf:/etc/nginx/conf.d/default.conf  nginx:1.16.1
