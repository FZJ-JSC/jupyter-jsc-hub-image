FROM jupyterhub/jupyterhub:1.0

RUN apt update && DEBIAN_FRONTEND=noninteractive apt install -y tzdata=2019c-0ubuntu0.18.04 iputils-ping curl && ln -fs /usr/share/zoneinfo/Europe/Berlin /etc/localtime && dpkg-reconfigure -f noninteractive tzdata

RUN /opt/conda/bin/pip install oauthenticator==0.8.2 psycopg2-binary==2.8.5

