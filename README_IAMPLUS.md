# Build Tensorflow Lite C libraries.

### `Download all dependancies`
./tensorflow/tensorflow/lite/tools/make/download_dependencies.sh

## `Build`

- `Android arm64(arm64-v8a)`
```
bazel build -c opt --cxxopt=--std=c++11 --config=android_arm64 //tensorflow/lite/c:tensorflowlite_c
```

- `Android arm (armeabi-v7a)`
```
bazel build -c opt --cxxopt=--std=c++11 --config=android_arm //tensorflow/lite/c:tensorflowlite_c
```

- `IOS arm64`
```
bazel build --config=ios_arm64 -c opt //tensorflow/lite/experimental/ios:TensorFlowLiteC_framework
```

- `IOS fat(armv7,arm64,i386,x86_64)`
```
bazel build --config=ios_fat -c opt //tensorflow/lite/experimental/ios:TensorFlowLiteC_framework
```