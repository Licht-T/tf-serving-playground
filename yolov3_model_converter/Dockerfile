FROM nvcr.io/nvidia/tensorflow:20.12-tf2-py3

ENV TF_FORCE_GPU_ALLOW_GROWTH true

ADD yolov3_to_keras.py /

CMD ls /workspace/models/*.weights \
    | xargs -I{} bash -c 'base_name=`basename {} .weights` && dir_name=`dirname {}` \
    && python /yolov3_to_keras.py ${dir_name}/${base_name}.cfg {} ${dir_name}/${base_name}.h5'

