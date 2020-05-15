# docker-openmm
dockerfile for openmm

Start jupyter on MacOS
```
docker run --rm -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes -v "$PWD":/work matsunagalab/openmm
```

Run openmm on a Linux GPU machine
```
docker run --privileged -u $(id -u):$(id -g) -e CUDA_VISIBLE_DEVICES="0" --rm -v $(pwd):/work -w /work matsunagalab/openmm python -m simtk.testInstallation
```

