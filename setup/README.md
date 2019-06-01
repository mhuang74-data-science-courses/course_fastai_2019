# README

## GCP Setup

### Use `gcloud` cli tool to create VM instance based on Third-Party Image

Use `setup_gcp.sh`, and see [here](https://course.fast.ai/start_gcp.html) for details.

Need to setup ssh tunnel since public IP is not exposed.

Do this via GCP Command Console (in browser), and use Web Preview to launch into Jupyter Lab.

```
gcloud compute ssh jupyter@my-fastai-gpu --zone=asia-east1-a -- -L 8080:localhost:8080
```

To confirm that nvidia driver is working, use the NVIDIA System Management Interface.

```
jupyter@my-fastai-gpu:~/.fastai/data$ nvidia-smi
Tue Feb 12 16:27:30 2019
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 410.72       Driver Version: 410.72       CUDA Version: 10.0     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|===============================+======================+======================|
|   0  Tesla K80           Off  | 00000000:00:04.0 Off |                    0 |
| N/A   45C    P0   140W / 149W |   2902MiB / 11441MiB |     96%      Default |
+-------------------------------+----------------------+----------------------+
+-----------------------------------------------------------------------------+
| Processes:                                                       GPU Memory |
|  GPU       PID   Type   Process name                             Usage      |
|=============================================================================|
|    0      8938      C   /opt/anaconda3/bin/python                   2891MiB |
+-----------------------------------------------------------------------------+
```
