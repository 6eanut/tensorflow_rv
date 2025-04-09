
编译命令：
bazel build --define=build_with_mkl=false --define=enable_mkl=false --define=tensorflow_mkldnn_contraction_kernel=0 --define=build_with_mkl_dnn_v1_only=false --define=tensorflow_use_mkldnn=false --define=build_with_openmp=false --host_copt="-Wno-stringop-truncation" //tensorflow/tools/pip_package:build_pip_package --verbose_failures --jobs=4 --experimental_repo_remote_exec --experimental_cc_shared_library --cxxopt="-std=c++17" --host_cxxopt="-std=c++17" --copt="-DTF_DISABLE_CHECK_OP" --copt=-DNDEBUG --per_file_copt=.*\.cpp@-fpermissive --per_file_copt=.*\.cc@-fpermissive --copt=-Wno-error

参考：
python3.9.6

Successfully installed Cython-3.0.12 MarkupSafe-3.0.2 Pillow-11.1.0 absl-py-1.4.0 array-record-0.5.1 astunparse-1.6.3 bleach-6.2.0 cachetools-5.5.2 certifi-2025.1.31 charset-normalizer-3.4.1 click-8.1.8 colorama-0.4.6 contourpy-1.3.0 cycler-0.12.1 dm-tree-0.1.8 etils-1.5.2 flatbuffers-25.2.10 fonttools-4.57.0 fsspec-2025.3.2 gast-0.4.0 gin-config-0.5.0 google-api-core-2.24.2 google-api-python-client-2.166.0 google-auth-2.38.0 google-auth-httplib2-0.2.0 google-auth-oauthlib-1.0.0 google-pasta-0.2.0 googleapis-common-protos-1.69.2 grpcio-1.71.0 h5py-3.13.0 httplib2-0.22.0 idna-3.10 immutabledict-4.2.1 importlib-metadata-8.6.1 importlib-resources-6.5.2 jax-0.4.30 jaxlib-0.4.30 kaggle-1.7.4.2 keras-2.12.0 kiwisolver-1.4.7 libclang-18.1.1 lxml-5.3.2 markdown-3.7 matplotlib-3.9.4 ml-dtypes-0.5.1 numpy-1.24.3 oauth2client-4.1.3 oauthlib-3.2.2 opencv-python-headless-4.11.0.86 opt-einsum-3.4.0 packaging-24.2 pandas-2.2.3 portalocker-3.1.1 promise-2.3 proto-plus-1.26.1 protobuf-4.21.12 psutil-7.0.0 py-cpuinfo-9.0.0 pyasn1-0.6.1 pyasn1-modules-0.4.2 pycocotools-2.0.8 pyparsing-3.2.3 python-dateutil-2.9.0.post0 python-slugify-8.0.4 pytz-2025.2 pyyaml-5.4.1 regex-2024.11.6 requests-2.32.3 requests-oauthlib-2.0.0 rsa-4.9 sacrebleu-2.5.1 scipy-1.13.1 sentencepiece-0.2.0 seqeval-0.0.10 six-1.17.0 tabulate-0.9.0 tensorboard-2.12.3 tensorboard-data-server-0.7.2 tensorflow-2.12.1 tensorflow-addons-0.23.0 tensorflow-datasets-4.9.3 tensorflow-estimator-2.12.0 tensorflow-hub-0.16.1 tensorflow-io-gcs-filesystem-0.37.1 tensorflow-metadata-1.17.0 tensorflow-model-optimization-0.8.0 tensorflow-text-2.12.1 termcolor-3.0.1 text-unidecode-1.3 tf-keras-2.15.0 tf-models-official-2.12.1 tf-slim-1.1.0 toml-0.10.2 tqdm-4.67.1 typeguard-2.13.3 typing-extensions-4.5.0 tzdata-2025.2 uritemplate-4.1.1 urllib3-2.3.0 webencodings-0.5.1 werkzeug-3.1.3 wheel-0.45.1 wrapt-1.14.1 zipp-3.21.0

pip install Cython==3.0.12
pip install MarkupSafe==3.0.2
pip install Pillow==11.1.0
pip install absl-py==1.4.0
··pip install array-record==0.5.1 没有现成的any包
ERROR: Could not find a version that satisfies the requirement array-record==0.5.1 (from versions: 0.2.0, 0.3.0, 0.4.0, 0.4.1)
ERROR: No matching distribution found for array-record==0.5.1

pip install astunparse==1.6.3
pip install bleach==6.2.0
pip install cachetools==5.5.2
pip install certifi==2025.1.31
pip install charset-normalizer==3.4.1
pip install click==8.1.8
pip install colorama==0.4.6
pip install contourpy==1.3.0
pip install cycler==0.12.1
pip install dm-tree==0.1.8
pip install etils==1.5.2
pip install flatbuffers==25.2.10
pip install fonttools==4.57.0
pip install fsspec==2025.3.2
pip install gast==0.4.0
pip install gin-config==0.5.0
pip install google-api-core==2.24.2
pip install google-api-python-client==2.166.0
pip install google-auth==2.38.0
pip install google-auth-httplib2==0.2.0
pip install google-auth-oauthlib==1.0.0
pip install google-pasta==0.2.0
pip install googleapis-common-protos==1.69.2
pip install grpcio==1.71.0
pip install h5py==3.13.0
pip install httplib2==0.22.0
pip install idna==3.10
pip install immutabledict==4.2.1
pip install importlib-metadata==8.6.1
pip install importlib-resources==6.5.2
··pip install jax==0.4.30
Collecting jax==0.4.30 numpy有关？
  Downloading jax-0.4.30-py3-none-any.whl (2.0 MB)
     |████████████████████████████████| 2.0 MB 66 kB/s
Requirement already satisfied: numpy>=1.22 in /root/.pyenv/versions/3.9.6/lib/python3.9/site-packages (from jax==0.4. (2.0.2)
ERROR: Could not find a version that satisfies the requirement jaxlib<=0.4.30,>=0.4.27 (from jax) (from versions: non
ERROR: No matching distribution found for jaxlib<=0.4.30,>=0.4.27
WARNING: You are using pip version 21.1.3; however, version 25.0.1 is available.
You should consider upgrading via the '/root/.pyenv/versions/3.9.6/bin/python3.9 -m pip install --upgrade pip' comman
ERROR: Could not find a version that satisfies the requirement jaxlib==0.4.30 (from versions: none)
ERROR: No matching distribution found for jaxlib==0.4.30

pip install jaxlib==0.4.30
pip install kaggle==1.7.4.2
pip install keras==2.12.0
pip install kiwisolver==1.4.7
pip install libclang==18.1.1
pip install lxml==5.3.2 缺包
pip install markdown==3.7
pip install matplotlib==3.9.4
pip install ml-dtypes==0.5.1
pip install numpy==1.24.3
pip install oauth2client==4.1.3
pip install oauthlib==3.2.2
pip install opencv-python-headless==4.11.0.86
pip install opt-einsum==3.4.0
pip install packaging==24.2
pip install pandas==2.2.3
pip install portalocker==3.1.1
pip install promise==2.3
pip install proto-plus==1.26.1
pip install protobuf==4.21.12
pip install psutil==7.0.0
pip install py-cpuinfo==9.0.0
pip install pyasn1==0.6.1
pip install pyasn1-modules==0.4.2
pip install pycocotools==2.0.8
pip install pyparsing==3.2.3
pip install python-dateutil==2.9.0.post0
pip install python-slugify==8.0.4
pip install pytz==2025.2
pip install pyyaml==5.4.1
pip install regex==2024.11.6
pip install requests==2.32.3
pip install requests-oauthlib==2.0.0
pip install rsa==4.9
pip install sacrebleu==2.5.1
pip install scipy==1.13.1
pip install sentencepiece==0.2.0
pip install seqeval==0.0.10
pip install six==1.17.0
pip install tabulate==0.9.0
pip install termcolor==3.0.1
pip install text-unidecode==1.3
pip install toml==0.10.2
pip install tqdm==4.67.1
pip install typeguard==2.13.3
pip install typing-extensions==4.5.0
pip install tzdata==2025.2
pip install uritemplate==4.1.1
pip install urllib3==2.3.0
pip install webencodings==0.5.1
pip install werkzeug==3.1.3
pip install wheel==0.45.1
pip install wrapt==1.14.1
pip install zipp==3.21.0

pip install tensorboard==2.12.3
pip install tensorboard-data-server==0.7.2
pip install tensorflow==2.12.1
pip install tensorflow-addons==0.23.0
pip install tensorflow-datasets==4.9.3
pip install tensorflow-estimator==2.12.0
pip install tensorflow-hub==0.16.1
pip install tensorflow-io-gcs-filesystem==0.37.1
pip install tensorflow-metadata==1.17.0
pip install tensorflow-model-optimization==0.8.0
pip install tensorflow-text==2.12.1
pip install tf-keras==2.15.0
pip install tf-models-official==2.12.1
pip install tf-slim==1.1.0
