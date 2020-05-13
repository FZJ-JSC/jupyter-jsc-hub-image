FROM 10.0.24.10:50000/jupyter4jsc/j4j_hub_base:1.1

RUN /opt/conda/bin/pip install -e git+https://github.com/FZJ-JSC/jupyter-jsc-jupyterhub-collection.git#egg=jupyter4jsc

RUN /opt/conda/bin/pip install --upgrade git+https://github.com/FZJ-JSC/jupyter-jsc-jupyterhub.git@jupyter-jsc-1.1.0#egg=jupyterhub

RUN adduser --disabled-password --gecos '' jupyter

COPY --chown=jupyter:jupyter ./start.sh /srv/jupyterhub/start.sh

# USER jupyter

CMD /srv/jupyterhub/start.sh
