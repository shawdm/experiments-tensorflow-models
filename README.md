# TensorFlow Models

This repository contains a number of different models implemented in [TensorFlow](https://www.tensorflow.org):

The [official models](official) are a collection of example models that use TensorFlow's high-level APIs. They are intended to be well-maintained, tested, and kept up to date with the latest stable TensorFlow API. They should also be reasonably optimized for fast performance while still being easy to read. We especially recommend newer TensorFlow users to start here.

The [research models](research) are a large collection of models implemented in TensorFlow by researchers. It is up to the individual researchers to maintain the models and/or provide support on issues and pull requests.

The [samples folder](samples) contains code snippets and smaller models that demonstrate features of TensorFlow, including code presented in various blog posts.

The [tutorials folder](tutorials) is a collection of models described in the [TensorFlow tutorials](https://www.tensorflow.org/tutorials/).


# DMS Installation Instructions
Taken from: https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/installation.md

## Protobuf Compilation

The Tensorflow Object Detection API uses Protobufs to configure model and
training parameters. Before the framework can be used, the Protobuf libraries
must be compiled. This should be done by running the following command from
the tensorflow/models/research/ directory:


``` bash
# From tensorflow/models/research/
protoc object_detection/protos/*.proto --python_out=.
```

## Add Libraries to PYTHONPATH

When running locally, the tensorflow/models/research/ and slim directories
should be appended to PYTHONPATH. This can be done by running the following from
tensorflow/models/research/:


``` bash
# From tensorflow/models/research/
export PYTHONPATH=$PYTHONPATH:`pwd`:`pwd`/slim
```
