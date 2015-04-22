FROM aostanin/debian

RUN apt-get update
RUN apt-get install -qy gdebi-core adduser

ADD https://downloads.plex.tv/plex-media-server/0.9.11.16.958-80f1748/plexmediaserver_0.9.11.16.958-80f1748_amd64.deb /tmp/plexmediaserver.deb
RUN gdebi -qn /tmp/plexmediaserver.deb && rm /tmp/plexmediaserver.deb

ADD start.sh /start.sh
RUN chmod a+rx /start.sh

EXPOSE 32400

CMD ["/start.sh"]
