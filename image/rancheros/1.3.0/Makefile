NAME = rancher/vm-rancheros
VERSION = 1.3.0-amd64
BASE_IMAGE=RancherOS-$(VERSION).qcow2

.PHONY : all

all: build

build:
	[ -f $(BASE_IMAGE) ] || wget https://s3-us-west-1.amazonaws.com/ranchervm/$(BASE_IMAGE)
	docker build --build-arg BASE_IMAGE=$(BASE_IMAGE) -t $(NAME):$(VERSION) .

clean:
	rm -f $(BASE_IMAGE)

