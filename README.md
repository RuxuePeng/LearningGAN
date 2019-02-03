# LearningGAN
Implementation of GANs using PyTorch

## Create dataproc cluster and run jupyter notebook
p.s. don't go with the official doc, jupyter notebook kernel doesn't work
https://github.com/GoogleCloudPlatform/dataproc-initialization-actions/issues/230
Follow this https://github.com/GoogleCloudPlatform/dataproc-initialization-actions/tree/master/jupyter
1. make cluster
export DATAPROC_CLUSTER_NAME=test1
export PROJECT=i-amlg-dev  
export ZONE=us-central1-a
export CLUSTER=test1

>
gcloud dataproc clusters create $CLUSTER \
    --zone us-central1-a \
    --initialization-actions gs://dataproc-initialization-actions/jupyter/jupyter.sh

2. ssh into the cluster via terminal:
>
cd LearningGAN
sh launch-jupyter-interface.sh

3. Chrome should open with jupyter page
