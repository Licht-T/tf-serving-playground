FROM python:3.8-buster

RUN pip install \
    jupyter \
    tensorflow-serving-api

CMD jupyter notebook \
    --ip='*' --no-browser --allow-root \
    --NotebookApp.token='' --NotebookApp.password='' \
    --NotebookApp.notebook_dir='/workspace' --port=8080

EXPOSE 8080

