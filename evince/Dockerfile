# DESCRIPTION:	Create evince container with its dependencies (https://wiki.gnome.org/Apps/Evince)
# AUTHOR:		Christian Koep <christiankoep@gmail.com>
# USAGE:
#	# Build evince image
#	docker build -t evince .
#
#	# Run the container and mount your documents
#	docker run -it \
#		-v $HOME/documents/:/root/documents/ \
#		-v /tmp/.X11-unix:/tmp/.X11-unix \
#		-e DISPLAY=$DISPLAY \
#		evince
#

FROM debian:stretch
LABEL maintainer "Christian Koep <christiankoep@gmail.com>"

RUN apt-get -qq update && apt-get install -y \
	evince \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

CMD ["/usr/bin/evince"]
