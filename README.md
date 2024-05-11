# open-webui-k8s
Deploy open webui on alibaba cloud ACK.
This project is refered from Open Webui (https://github.com/open-webui/open-webui/), and modified to adopt ACK in Alibaba Cloud

## Precondition

1. On Alibaba cloud, setup a managed K8s cluster of ACK
2. Choose MSE Ingress (https://help.aliyun.com/zh/mse/user-guide/overview-of-mse-ingress-gateways)
3. Choose CNFS  (https://help.aliyun.com/zh/ack/ack-managed-and-ack-dedicated/user-guide/cnfs-overview)
4. Clone this project

## Add GPU node group
1. Add a node group with a GPU (e.g., v100 1 GPU card, ecs.gn6e-c12g1.3xlarge ) in ACK cluster
2. modify `mse.hkdemo.vipdocker.com` to your domain name in webui-ingress.yaml

## Install open-webui and ollama

```
kubectl apply -k .
```



