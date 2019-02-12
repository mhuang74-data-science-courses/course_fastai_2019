# README

## GCP Setup

### Use `gcloud` cli tool to create VM instance based on Third-Party Image

Use `setup_gcp.sh`, and see [here](https://course.fast.ai/start_gcp.html) for details.

Need to setup ssh tunnel since public IP is not exposed.

Do this via GCP Command Console (in browser), and use Web Preview to launch into Jupyter Lab.

```
gcloud compute ssh --zone=$ZONE jupyter@$INSTANCE_NAME -- -L 8080:localhost:8080
```

