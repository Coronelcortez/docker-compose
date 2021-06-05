FROM ubuntu as minecraft-pe
RUN apt update && apt upgrade -y && apt install build-essential libtool-bin autoconf bison -y

EXPOSE 19132


RUN wget -q -O - https://get.pmmp.io | bash -s -

ENTRYPOINT [ "/root/start.sh" ]
