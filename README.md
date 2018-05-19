# docker-python-opencv-ffmpeg
Repository for clean Dockerfile containing ffmpeg, opencv3 and python2, based on Ubuntu
Forked from https://github.com/Valian/docker-python-opencv-ffmpeg (updated Ubuntu, Opencv and Python to more recent versions)

# Versions

`:latest` Python 2.7, OpenCV 3.2, ffmpeg, Ubuntu 16.04  
`:py3` Python 3.6, OpenCV 3.4, ffmpeg, Ubuntu 18.04  
`:cuda` Python 2.7, OpenCV 3.2, ffmpeg with CUDA support, Ubuntu 16.04  
`:cuda-py3` Python 3.5, OpenCV 3.2, ffmpeg with CUDA support, Ubuntu 16.04  


# Build
You can build it on your own

``` bash
git clone https://github.com/PaulEmmanuelSotir/docker-python-opencv-ffmpeg
cd docker-python-opencv-ffmpeg
    
# takes lots of time, be prepared (to build other versions, select different Dockerfile)
docker build -t valian/docker-python-opencv-ffmpeg -f Dockerfile-py2 .
```

But I encourage you to use version from DockerHub - it's MUCH faster
``` bash
docker pull paulemmanuel/docker-python-opencv-ffmpeg
```

# Usage

Image has OpenCV3, python2.7/3.5/3.6 and ffmpeg ready to use. Example:

``` bash
docker run --rm -it -v $PWD:/srv valian/docker-python-opencv-ffmpeg python
>>> import cv2; cv2.VideoCapture('/srv/example.mp4').read()
# truncated for transparency
(True, array([[[ 46, 112, 104], ...]], dtype=uint8))
```
