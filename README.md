编译命令：
bazel build --define=build_with_mkl=false --define=enable_mkl=false --define=tensorflow_mkldnn_contraction_kernel=0 --define=build_with_mkl_dnn_v1_only=false --define=tensorflow_use_mkldnn=false --define=build_with_openmp=false --host_copt="-Wno-stringop-truncation" //tensorflow/tools/pip_package:build_pip_package --verbose_failures --jobs=4 --experimental_repo_remote_exec --experimental_cc_shared_library --cxxopt="-std=c++17" --host_cxxopt="-std=c++17" --copt="-DTF_DISABLE_CHECK_OP" --copt=-DNDEBUG --copt=-fpermissive

python依赖：
pip install --upgrade wheel==0.45.1 h5py==3.11.0 keras==2.12.0 six==1.17.0 numpy==1.24.3

参考：
Successfully installed MarkupSafe-2.1.5 absl-py-2.2.2 astunparse-1.6.3 cachetools-5.5.2 certifi-2025.1.31 charset-normalizer-3.4.1 flatbuffers-25.2.10 gast-0.4.0 google-auth-2.38.0 google-auth-oauthlib-1.0.0 google-pasta-0.2.0 grpcio-1.70.0 h5py-3.11.0 idna-3.10 importlib-metadata-8.5.0 jax-0.4.13 keras-2.12.0 libclang-18.1.1 markdown-3.7 ml-dtypes-0.2.0 numpy-1.24.3 oauthlib-3.2.2 opt-einsum-3.4.0 packaging-24.2 protobuf-4.25.6 pyasn1-0.6.1 pyasn1-modules-0.4.2 requests-2.32.3 requests-oauthlib-2.0.0 rsa-4.9 scipy-1.10.1 six-1.17.0 tensorboard-2.12.3 tensorboard-data-server-0.7.2 tensorflow-2.12.1 tensorflow-estimator-2.12.0 tensorflow-io-gcs-filesystem-0.34.0 termcolor-2.4.0 typing-extensions-4.5.0 urllib3-2.2.3 werkzeug-3.0.6 wheel-0.45.1 wrapt-1.14.1 zipp-3.20.2

python3.9.6
