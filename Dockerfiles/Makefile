# Flags for docker image building 
CONF:= 

DOCKERHUB := alexwitt23

IMAGENAME := agaze

.PHONY: all
all: image

.PHONY: opencv_cuda
image:
	docker build -t $(DOCKERHUB)/$(IMAGENAME):latest -f Dockerfile ..
