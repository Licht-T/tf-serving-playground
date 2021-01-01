FROM nvcr.io/nvidia/tensorflow:20.12-tf2-py3

ENV TF_FORCE_GPU_ALLOW_GROWTH true

RUN pip install \
    jupyter \
    onnxruntime-gpu

RUN pip install \
    torch===1.7.1+cu110 \
    torchvision===0.8.2+cu110 \
    torchaudio===0.7.2 \
    -f https://download.pytorch.org/whl/torch_stable.html

CMD jupyter notebook \
    --ip='*' --no-browser --allow-root \
    --NotebookApp.token='' --NotebookApp.password='' \
    --NotebookApp.notebook_dir='/workspace' --port=8080

EXPOSE 8080

