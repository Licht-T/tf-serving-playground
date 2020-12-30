FROM nvcr.io/nvidia/tensorrt:20.07-py3

ENV TF_FORCE_GPU_ALLOW_GROWTH true

RUN /opt/tensorrt/python/python_setup.sh

RUN pip install \
    jupyter \
    onnxruntime-gpu \
    tensorflow-gpu==2.4

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

