FROM tensorflow/tensorflow:latest-gpu-jupyter

RUN apt-get update && apt-get install -y wget ca-certificates \
    git curl vim python3-dev python3-pip \
    libfreetype6-dev 

#RUN apt-get install libpng12-dev libhdf5-dev

RUN pip3 install --upgrade pip
RUN pip3 install tensorflow-gpu
RUN pip3 install numpy pandas sklearn matplotlib seaborn jupyter pyyaml h5py
RUN pip3 install keras --no-deps
RUN pip3 install keras_applications --no-deps
RUN pip3 install keras_preprocessing --no-deps
RUN pip3 install statsmodels
RUN pip3 install tqdm 
RUN pip3 install tabulate
RUN ["mkdir", "notebooks"]
COPY jupyter_notebook_config.py /root/.jupyter/
COPY run_jupyter.sh /

# Jupyter and Tensorboard ports
EXPOSE 8888 6006

# Store notebooks in this mounted directory
VOLUME /notebooks

CMD ["/run_jupyter.sh"]
