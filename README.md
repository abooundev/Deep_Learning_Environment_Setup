# Deep Learning Environment Setup

# 설치 항목

- nvidia-driver 설치
- CUDA 설치
- cudnn 설치
- tensorflow/tensorflow-gpu 설치
- nvidia-docker 설치



# 버전 체크

### 1) nvidia-driver



### 2) CUDA 

* **Linux x86_64 Driver Version 기준** 
  * https://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html#cuda-major-component-versions

| CUDA Toolkit                                      | **Toolkit Driver Version** | **Minimum Required Driver Version\*** |
| ------------------------------------------------- | -------------------------- | ------------------------------------- |
| CUDA 11.3.0 GA                                    | >=465.19.01                | >= 450.80.02                          |
| CUDA 11.2.2 Update 2                              | >=460.32.03                | >= 450.80.02                          |
| CUDA 11.2.1 Update 1                              | >=460.32.03                | >= 450.80.02                          |
| CUDA 11.2.0 GA                                    | >=460.27.03                | >= 450.80.02                          |
| CUDA 11.1.1 Update 1                              | >=455.32                   | >= 450.80.02                          |
| CUDA 11.1 GA                                      | >=455.23                   | >= 450.80.02                          |
| CUDA 11.0.3 Update 1                              | >= 450.51.06               | >= 450.51.06                          |
| CUDA 11.0.2 GA                                    | >= 450.51.05               | >= 450.51.06                          |
| CUDA 11.0.1 RC                                    | >= 450.36.06               | >= 450.51.06                          |
| CUDA 10.2.89                                      | >= 440.33                  | >= 440.33                             |
| CUDA 10.1 (10.1.105 general release, and updates) | >= 418.39                  | >= 418.39                             |
| CUDA 10.0.130                                     | >= 410.48                  | >= 410.48                             |
| CUDA 9.2 (9.2.148 Update 1)                       | >= 396.37                  | >= 396.37                             |
| CUDA 9.2 (9.2.88)                                 | >= 396.26                  | >= 396.26                             |
| CUDA 9.1 (9.1.85)                                 | >= 390.46                  | >= 390.46                             |
| CUDA 9.0 (9.0.76)                                 | >= 384.81                  | >= 384.81                             |
| CUDA 8.0 (8.0.61 GA2)                             | >= 375.26                  | >= 375.26                             |
| CUDA 8.0 (8.0.44)                                 | >= 367.48                  | >= 367.48                             |
| CUDA 7.5 (7.5.16)                                 | >= 352.31                  | >= 352.31                             |
| CUDA 7.0 (7.0.28)                                 | >= 346.46                  | >= 346.46                             |



### 2) cuDNN

 * https://docs.nvidia.com/deeplearning/cudnn/support-matrix/index.html

   

| cuDNN Version                                                | CUDA Version                                              |
| ------------------------------------------------------------ | --------------------------------------------------------- |
| [cuDNN 8.2.0](https://docs.nvidia.com/deeplearning/cudnn/support-matrix/index.html#cudnn-versions-820) | [11.3](https://developer.nvidia.com/cuda-toolkit-archive) |
| [cuDNN 8.1.0 - 8.1.1](https://docs.nvidia.com/deeplearning/cudnn/support-matrix/index.html#cudnn-versions-810-811) | [11.2](https://developer.nvidia.com/cuda-toolkit-archive) |
| [cuDNN 8.0.5](https://docs.nvidia.com/deeplearning/cudnn/support-matrix/index.html#cudnn-versions-804-805) | CUDA 11.1                                                 |



### 3) tensorflow

```markdown
- [NVIDIA® GPU 드라이버](https://www.nvidia.com/drivers) - CUDA® 11.0에는 450.x 이상이 필요합니다.
- [CUDA® Toolkit](https://developer.nvidia.com/cuda-toolkit-archive) - TensorFlow는 CUDA® 11을 지원합니다(TensorFlow 2.4.0 이상).
- [CUPTI](http://docs.nvidia.com/cuda/cupti/)는 CUDA® Toolkit과 함께 제공됩니다.
- [cuDNN SDK 8.0.4](https://developer.nvidia.com/cudnn)([cuDNN 버전](https://developer.nvidia.com/rdp/cudnn-archive))
- *(선택사항)* [TensorRT 6.0](https://docs.nvidia.com/deeplearning/sdk/tensorrt-install-guide/index.html) - 일부 모델에서 추론 처리량과 지연 시간을 향상합니다.

* https://www.tensorflow.org/install/source#tested_build_configurations
```

* **Linux & TensorFlow GPU**
  * https://www.tensorflow.org/install/source#tested_build_configurations

| 버전                  | Python 버전  | 컴파일러  | 빌드 도구    | cuDNN | CUDA |
| :-------------------- | :----------- | :-------- | :----------- | :---- | :--- |
| tensorflow-2.4.0      | 3.6-3.8      | GCC 7.3.1 | Bazel 3.1.0  | 8.0   | 11.0 |
| tensorflow-2.3.0      | 3.5-3.8      | GCC 7.3.1 | Bazel 3.1.0  | 7.6   | 10.1 |
| tensorflow-2.2.0      | 3.5-3.8      | GCC 7.3.1 | Bazel 2.0.0  | 7.6   | 10.1 |
| tensorflow-2.1.0      | 2.7, 3.5-3.7 | GCC 7.3.1 | Bazel 0.27.1 | 7.6   | 10.1 |
| tensorflow-2.0.0      | 2.7, 3.3-3.7 | GCC 7.3.1 | Bazel 0.26.1 | 7.4   | 10.0 |
| tensorflow_gpu-1.15.0 | 2.7, 3.3-3.7 | GCC 7.3.1 | Bazel 0.26.1 | 7.4   | 10.0 |
| tensorflow_gpu-1.14.0 | 2.7, 3.3-3.7 | GCC 4.8   | Bazel 0.24.1 | 7.4   | 10.0 |
| tensorflow_gpu-1.13.1 | 2.7, 3.3-3.7 | GCC 4.8   | Bazel 0.19.2 | 7.4   | 10.0 |
| tensorflow_gpu-1.12.0 | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.15.0 | 7     | 9    |
| tensorflow_gpu-1.11.0 | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.15.0 | 7     | 9    |
| tensorflow_gpu-1.10.0 | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.15.0 | 7     | 9    |
| tensorflow_gpu-1.9.0  | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.11.0 | 7     | 9    |
| tensorflow_gpu-1.8.0  | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.10.0 | 7     | 9    |
| tensorflow_gpu-1.7.0  | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.9.0  | 7     | 9    |
| tensorflow_gpu-1.6.0  | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.9.0  | 7     | 9    |
| tensorflow_gpu-1.5.0  | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.8.0  | 7     | 9    |
| tensorflow_gpu-1.4.0  | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.5.4  | 6     | 8    |
| tensorflow_gpu-1.3.0  | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.4.5  | 6     | 8    |
| tensorflow_gpu-1.2.0  | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.4.5  | 5.1   | 8    |
| tensorflow_gpu-1.1.0  | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.4.2  | 5.1   | 8    |
| tensorflow_gpu-1.0.0  | 2.7, 3.3-3.6 | GCC 4.8   | Bazel 0.4.2  | 5.1   | 8    |





# 설치 공식 문서

* CUDA Installation guide linux
  * https://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html

* cuDNN Installation guide linux
  * https://docs.nvidia.com/deeplearning/cudnn/archives/cudnn-820/install-guide/index.html
* Tensorflwo GPU
  * https://www.tensorflow.org/install/gpu?hl=ko

* nvidia-docker Installation guide

  * https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html#docker

  * 공식 사이트: https://github.com/NVIDIA/nvidia-docker

    

# 설치

## 1) nvidia-driver 설치

## 2) CUDA

* 설치 확인

  ```shell
  $ nvcc --version
  ```

  

## 3) cuDNN

* tar 다운 

  * https://developer.nvidia.com/rdp/cudnn-download
  * 홈페이지 로그인 필요
  * ubuntu16.04, CUDA 11.3 기준: cuDNN v8.2.0 선택
    * [Download cuDNN v8.2.0 (April 23rd, 2021), for CUDA 11.x](https://developer.nvidia.com/rdp/cudnn-download#a-collapse821-111)
    * [cuDNN Library for Linux (x86_64)](https://developer.nvidia.com/compute/machine-learning/cudnn/secure/8.2.0.53/11.3_04222021/cudnn-11.3-linux-x64-v8.2.0.53.tgz)

* cuDNN 다운 받은 폴더로 이동

* cuDNN 패키지 압축 해제

  ```shell
  $ tar -xzvf cudnn-x.x-linux-x64-v8.x.x.x.tgz
  ```

* 다음 파일을 CUDA Toolkit 폴더에 복사

  ```shell
  $ sudo cp cuda/include/cudnn*.h /usr/local/cuda/include 
  $ sudo cp -P cuda/lib64/libcudnn* /usr/local/cuda/lib64 
  $ sudo chmod a+r /usr/local/cuda/include/cudnn*.h /usr/local/cuda/lib64/libcudnn*
  ```

* 설치 확인

  * cuDNN 8.x 이상 버전 

    ```shell
    $ cat /usr/local/cuda/include/cudnn_version.h | grep CUDNN_MAJOR -A 2
    ```

  * cuDNN 8.x 이전 버전

    ```shell
    $ cat /usr/local/cuda/include/cudnn.h | grep CUDNN_MAJOR -A 2
    ```

* 설치 확인 출력 내용

  ```
  #define CUDNN_MAJOR 8
  #define CUDNN_MINOR 2
  #define CUDNN_PATCHLEVEL 0
  --
  #define CUDNN_VERSION (CUDNN_MAJOR * 1000 + CUDNN_MINOR * 100 + CUDNN_PATCHLEVEL)
  ```

  

# 기존 설치 시 이전 버전 삭제

* CUDA 삭제

```shell
$ sudo apt-get purge nvidia*
$ sudo apt-get autoremove
$ sudo apt-get autoclean
$ sudo rm -rf /usr/local/cuda*
```



[참고]

https://blog.nerdfactory.ai/2019/07/25/how-to-install-tensorflow-gpu-in-ubuntu16.04-copy.html
https://cafepurple.tistory.com/39

