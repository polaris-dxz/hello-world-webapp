## 构建 Docker 镜像
```shell
docker build -t hello-world-webapp .
```

## 在本地 8877 端口访问前端应用 hello-world-webapp
```shell
docker run -d -p 8877:80 hello-world-webapp
```

## 推送 Docker 镜像到 Docker Hub
```shell
docker login
docker tag hello-world-webapp your_dockerhub_username/hello-world-webapp
docker push your_dockerhub_username/hello-world-webapp
```

## 创建 Helm Chart
```shell
helm create hello-world-webapp-chart
# 修改 values.yaml 和 template/deployment.yaml 文件
```

## 部署到 k8s 集群
```shell
minikube start
```

## 使用 helm 部署前端应用
```shell
helm install hello-world-webapp-release ./hello-world-webapp-chart
```

## 获取 NodePort 服务的 URL
```shell
minikube service hello-world-webapp-service --url
```
