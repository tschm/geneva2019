# Set the base image to beakerx
FROM beakerx/beakerx:latest

# set the user back to root to install further packages
USER root

# copy over the requirements file (links to our private github repositories)
COPY requirements.txt requirements.txt

# copy over the config file (contains the hashed password)
COPY jupyter_notebook_config.py /etc/jupyter/jupyter_notebook_config.py

# install our packages (which subsequently link to sqlalchemy, etc.)
# RUN /opt/conda/envs/beakerx/bin/pip install --upgrade pip
RUN /opt/conda/envs/beakerx/bin/pip install --no-cache-dir  -r requirements.txt && rm requirements.txt

# you need to specify the environemtn
RUN conda install -y -n beakerx -c conda-forge rise=5.4.1

# set the user back to NB_USER defined in Dockerfile for beakerx/beakerx
USER $NB_USER

COPY work $HOME/work