FROM continuumio/anaconda3:2020.07

COPY ./packages.yml /
RUN conda env create -f /packages.yml && conda clean -a
ENV PATH /opt/conda/envs/tf/bin:$PATH

RUN mkdir -p /usr/local/pDeep2/
COPY *py /usr/local/pDeep2
COPY *txt /usr/local/pDeep2
COPY *.md /usr/local/pDeep2
COPY tf-models /usr/local/pDeep2/tf-models
COPY model /usr/local/pDeep2/model
COPY data /usr/local/pDeep2/data
