# dpc

### Document Problem Cropping

## Execution
0. 클론할 디렉토리로 이동
1. !git clone https://github.com/JeongHanJun/dpc.git
2. %cd dpc
3. !pip install -r pipreqs_dpc_requirements.txt
    Colab 기준으로 3번 실행 이후 다양한 라이브러리 dependency Error가 발생할 수 있음
    설치가 잘 되고 Error가 출력된 경우 문제없이 아래 수행
    설치가 막힌 경우에는 Tensorflow 2.5 , numpy 1.19를 벗어나지 않는 선에서 수정
    필수 패키지는 아래 참고
    h5py==3.1.0
    imgaug==0.4.0
    ipython==8.11.0
    keras==2.11.0
    keras_nightly==2.5.0.dev2021032900
    matplotlib==3.6.3
    numpy==1.19.3
    opencv_python==4.6.0.66
    pip==20.0.2
    pycocotools==2.0.6
    scikit_image==0.18.3
    scikit_learn==1.2.2
    scipy==1.7.3
    setuptools==45.2.0
    tensorflow==2.5.0

4. Pretrained Weight 다운로드
    아래 링크에서 학습된 weight 다운로드
    https://drive.google.com/drive/folders/19MOPg6HgZ1505E4AxPuHGrToB7_4nXM6?usp=sharing
    이후 아래 디렉토리에 맞게 배치 ( mask_rcnn_ai_dpc_0010.h5 가 있는 위치로 배치)
/dpc
    /mrcnn
        config.py
        model.py
        ...

    /logs
        /ai_dpc20230309T0127
            mask_rcnn_ai_dpc_0010.h5

5. Inference.ipynb에서 "수정 필요" 를 검색후 path 및 경로 관련 수정
6. Inference.ipynb 실행