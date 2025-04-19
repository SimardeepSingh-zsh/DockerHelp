FROM jupyter/scipy-notebook

WORKDIR /home/jovyan
COPY . .
CMD ["start-notebook.sh"]

RUN pip install --no-cache-dir -r requirements.txt
RUN conda install --yes --file requirements.txt
RUN conda install --yes -c conda-forge -c anaconda -c defaults -c bioconda -c r bioconductor-ggplotify=0.1.0
