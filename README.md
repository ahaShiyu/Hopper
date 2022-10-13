# GMU Hopper Instructions

This is a collection of intructions for runing a python script on hopper (cpu or gpu).

#### Step 0: request and login to a worker

```
ssh ssun20@hopper-amd.orc.gmu.edu
```

transfer files:

```
ssh ssun20@hopper-amd.orc.gmu.edu
```

request a worker node

cpu:
```
salloc -p normal  -n 1  --cpus-per-task=12 --mem=15GB -t 0-01:00:00
```
gpu:

```
salloc -p gpuq -q gpu --gres=gpu:A100.40gb:1 -n 1  --mem=15G -t 0-12:00:00
```

#### Step 0.1: download and install anaconda

```
cd /scratch/ssun20
```
```
wget https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh
```
```
sh Anaconda3-2022.05-Linux-x86_64.sh
```
```
source /anaconda3/etc/profile.d/conda.sh
```

#### step 1: create virtual environment and install packages
```
conda create -n myenv python=3.9
```
```
conda activate /scratch/ssun20/myenv
```
