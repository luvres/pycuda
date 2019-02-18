## PyCUDA
-----

### Pull image
```
docker pull izone/pycuda
```
### Run
#### Jupyter Notebook
```
docker run --rm --runtime=nvidia --name PyCUDA \
-p 8888:8888 \
--volume=$HOME/pycuda:/root \
-ti izone/pycuda \
jupyter notebook \
	--allow-root \
	--ip=0.0.0.0 \
	--no-browser \
	--port=8888 \
	--notebook-dir=/root \
	--NotebookApp.token=''
```
```
nvidia-docker run --rm --name PyCUDA \
-p 8888:8888 \
--volume=$HOME/pycuda:/root \
-ti izone/pycuda:9.2 python
```

-----
### Access Browser
```
http://localhost:8888/
```

-----
### Build
```
docker build -t izone/pycuda .
```
```
docker build -t izone/pycuda:cuda-9.2 ./9.2/
```