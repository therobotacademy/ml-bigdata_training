# BigData_training

# 1. [Big Data Essentials: HDFS, MapReduce and Spark RDD](https://www.coursera.org/learn/big-data-essentials) by Yandex

### Hadoop Yarn Notebook
[Docker container with Hadoop Yarn Jupyter Notebook](https://hub.docker.com/r/bigdatateam/yarn-notebook/): ``yarn-notebook``
```docker run -it -p 8881:8888 --name hadoop_8881 bigdatateam/yarn-notebook
```
To SSH into the container: `$docker exec -it hadoop_8881 bash`

### Spark into Jupyter Notebook (PySpark)
[Docker container with Spark Jupyter Notebook](https://hub.docker.com/r/bigdatateam/spark-course1/): ``spark-course1``
```
docker run -it -p 8880:8888 --name spark_8880 bigdatateam/spark-course1
```
To SSH into the container: `$ docker exec -it spark_8880 bash`



# 2. [Big Data Applications: Machine Learning at Scale](https://www.coursera.org/learn/machine-learning-applications-big-data) by Yandex
[Docker container Spark course 3](https://hub.docker.com/r/bigdatateam/spark-course3/): ``spark-course1``


# 3. [Introduction to Deep Learning](https://www.coursera.org/learn/intro-to-deep-learning) por National Research University Higher School of Economics
https://github.com/hse-aml/intro-to-dl
### _________________________________ at folder ``intro-to-dl``
https://github.com/romeokienzler/CognitiveIoT

[Docker container with Jupyter Environment](https://hub.docker.com/r/zimovnov/coursera-aml-docker/): ``coursera-aml-docker``

Week 3:
-------
 - **3.1 Introduction to CNN**
 - **3.2 Modern CNNs**

Your first CNN on CIFAR-10
--------------------------
Follow the instructions on https://hub.docker.com/r/zimovnov/coursera-aml-docker/ to install Docker container with all necessary software installed.

After that you should see a Jupyter page in your browser.
```
docker run -it -p 8080:8882 --name coursera-aml-1 zimovnov/coursera-aml-docker
```

#### Container checkpoints
You might want to make a checkpoint of your work so that you can return to it later.
Think of it as a backup or commit in version control system.

#### Saving container state
You will first have to stop the container following instructions above.
Now you need to save the container state so that you can return to it later

``docker commit coursera-aml-1 coursera-aml-snap-1``

You can make sure that it's saved by running docker images.

Creating new container from previous checkpoint
If you want to continue working from a particular checkpoint, you should run a new container from your saved image by executing

``docker run -it -p 127.0.0.1:8080:8080 -p 127.0.0.1:7007:7007 --name coursera-aml-2 coursera-aml-snap-1``

Notice that we incremented index in the container name, because we created a new container.

#### Using GPU in your container
You can use NVIDIA GPU in your container on Linux host machine.

Setup docker following instructions from NVIDIA:

https://github.com/NVIDIA/nvidia-docker/wiki/Installation-(version-2.0)#prerequisites
In your container replace CPU TensorFlow version with the one that supports GPU:
```
pip3 uninstall tensorflow
pip3 install tensorflow-gpu==1.2.1
```
You will also have to install NVIDIA GPU driver, CUDA toolkit and CuDNN (requires registration with NVIDIA) in your container in order for TensorFlow to work with your GPU:
https://www.tensorflow.org/versions/r1.2/install/install_linux#nvidia_requirements_to_run_tensorflow_with_gpu_support

It can be hard to follow, so you might choose to stick to a CPU version, which is also fine for the purpose of this course.
TensorFlow provides Docker files with TensorFlow on GPU, but they don't have all the additional dependencies we need, this is for advanced users:
https://github.com/tensorflow/tensorflow/tree/master/tensorflow/tools/docker
 - **3.3 Application of CNNs**


# 4. [Applied AI with DeepLearning](https://www.coursera.org/learn/ai) by IBM

https://github.com/romeokienzler/developerWorks
### _________________________________ at folder ``developerWorks``
