# Use the Jupyter stack
FROM lobnek/jupyter:v2.3
#jupyter/minimal-notebook:45b8529a6bfc

# This is needed for beakerx
#RUN conda config --env --add pinned_packages 'openjdk>8.0.121'

# Install packages such as rise, pandas, cvxpy, ...
#RUN conda install -y -c conda-forge \
#    rise=5.4.1 pandas=0.24.1 cvxpy=1.0.14 beakerx=1.3.0 ipywidgets=7.4.2 && \
#    conda clean -y --all

# copy your work into the image
COPY ./work /home/${NB_USER}/work
#COPY ./jupyter_notebook_config.py /etc/jupyter/jupyter_notebook_config.py