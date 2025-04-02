# tensorflow_rv
dnf install python3-devel python3-pip patchelf openssl-devel cmake mold

pip install numpy wheel keras_preprocessing

bazel --output_user_root=../output_user_root build   --jvmopt="-Djava.net.preferIPv4Stack=true"   --jvmopt="-Dnetworkaddress.cache.ttl=0"   --jvmopt="-Dsun.net.inetaddr.ttl=0"   --linkopt="-fuse-ld=mold"   --define=build_with_mkl=false   --define=enable_mkl=false   --define=tensorflow_mkldnn_contraction_kernel=0   --define=build_with_mkl_dnn_v1_only=false   --define=tensorflow_use_mkldnn=false   --define=build_with_openmp=false   --host_copt="-Wno-stringop-truncation"   //tensorflow/tools/pip_package:build_pip_package   --verbose_failures   --jobs=4
