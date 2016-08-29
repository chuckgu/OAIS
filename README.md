# OAIS

Window 7 & 8 & 10
Docker install
Step 1: 다운로드 Docker 툴박스 https://www.docker.com/products/docker-toolbox
Step 2: Docker Quickstart Terminal 을 연다.
Step 3: docker-machine ls를 치면 현재 Docker machine의 상황을 보여준다.
Step 4: docker-machine create vdocker -d virtualbox을 입력하여 새로운 docker machine을 만들어준다. 여기서 vdocker는 새로운 docker machine의 이름을 의미한다.
Step 5: 다시 한번 docker-machine ls를 쳐서 새로운 docker machine이 만들어진 것을 확인한다.
Step 6: windows cmd prompt를 열고 FOR /f "tokens=*" %i IN ('docker-machine env --shell cmd vdocker') DO %i 를 입력한다. 여기서 vdocker는 방금전 만든 새로운 docker의 이름이다.
Step 7: cmd prompt 창에서 docker run –it –p 8888:8888b.gcr.io/tensorflow/tensorflow:latest-devel 


우분투/맥OS
Step 1:
# Ubuntu/Linux 64-bit:
	$ sudo apt-get install python-pip python-dev (python 2.7)
	$ sudo apt-get install python-pip3 python3-dev (python 3.5)
	
# Mac OS X:
	$ sudo easy_install pip
	$ sudo easy_install -- upgrade six

Step 2:
# Ubuntu/Linux 64-bit, CPU only, Python 2.7
	$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-	0.10.0rc0-cp27-none-linux_x86_64.whl

# Ubuntu/Linux 64-bit, GPU enabled, Python 2.7
# Requires CUDA toolkit 7.5 and CuDNN v4. For other versions, see "Install from sources".
$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow-0.10.0rc0-cp27-none-linux_x86_64.whl

# Mac OS X, CPU only, Python 2.7:
	$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-	0.10.0rc0-py2-none-any.whl

# Mac OS X, GPU enabled, Python 2.7:
	$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/mac/gpu/tensorflow-	0.10.0rc0-py2-none-any.whl


Step 3:
# Python 2
$ sudo pip install --upgrade $TF_BINARY_URL

# Python 3
$ sudo pip3 install --upgrade $TF_BINARY_URL
