FROM jarfil/salt-master-mini:debian-stretch

MAINTAINER shivam jha <shivamjhaonthecloud@gmail.com>

COPY . /

RUN apt-get -y update && \
	apt-get -y upgrade && \
	apt-get -y install \
		salt-minion \
		salt-ssh \
		salt-cloud && \
	apt-get -y autoremove && \
	apt-get clean && \
	rm -rf /var/lib/apt/lists/

RUN chmod +x \
	/docker-entrypoint.sh

EXPOSE 4505 4506

CMD /docker-entrypoint.sh
