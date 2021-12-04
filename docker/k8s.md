kubectl get nodes

kubectl get  service

http://dockone.io/article/2682

https://www.kubernetes.org.cn/kubernetes-pod

没有service   ，pod不能被外部访问；



yaml

   replicas 副本数目；

  一个depooyment run 多个容器

Lables:

  k8s-app:kuberntes-dashbord

### kind:service

selector:

  k8s-app:kuberntes-dashbord

dashboard 镜像安装；



### Service的三种类型

1. ClusterlP  代理方式访问

2. NodePort  直接根据node节点IP+端口

3. LoadBalancer

   1. http://dockone.io/article/4884

      

![image-20201007103813897](D:\ 根目录\Code\github\document\blog\docker\k8s.assets\image-20201007103813897.png)

https://yq.aliyun.com/articles/508460?spm=a2c4e.11153940.blogcont221687.18.7dd57733hFolMo

:UserslJesse>kubectl delete deploy kubernetes-dashboard -n kube-system

kubectl delete svc kubernetes-dashboard -n kube-system



kubectl create -f

kubectl get  svc -n kubernetes-dashboard

https://jimmysong.io/kubernetes-handbook/guide/kubectl-cheatsheet.html

https://jimmysong.io/kubernetes-handbook/guide/auth-with-kubeconfig-or-token.html

 kubectl -n kubernetes-dashboard describe secret default-token-mhkn6



https://127.0.0.1:30065/#/login

eyJhbGciOiJSUzI1NiIsImtpZCI6ImFOdnJyUGVsM2FIcDlXVERya1VBaFRFMkl2cVptNHozUUpzMm9oNUZ4WlkifQ.eyJpc3MiOiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJrdWJlcm5ldGVzLWRhc2hib2FyZCIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VjcmV0Lm5hbWUiOiJkZWZhdWx0LXRva2VuLW1oa242Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9zZXJ2aWNlLWFjY291bnQubmFtZSI6ImRlZmF1bHQiLCJrdWJlcm5ldGVzLmlvL3NlcnZpY2VhY2NvdW50L3NlcnZpY2UtYWNjb3VudC51aWQiOiJlNzJkYzY5NS1iYmE0LTRjZTAtYjA2OC02MzZiNTM3MzY1YjYiLCJzdWIiOiJzeXN0ZW06c2VydmljZWFjY291bnQ6a3ViZXJuZXRlcy1kYXNoYm9hcmQ6ZGVmYXVsdCJ9.vfzKOsq7nqQ90VNMH8Y1ui_tnXyCRY5Q7cI_5mjU_kAco5W88uaf0l4xCV3S2ODoKirUHqwC6S17lhrQXaS2qWSIIBGXGyo1NiPHnJ1kwGks7seLeZLTucV5I_0ZTtQRqQtE13mm7znSbj5VmjJx_l0yE4kReX2A7hscAqOojBV9t_HqI9-46Nru9FN9x73x72iT-XZnsrRcWzW1zOzmqbAn7WeUrB_y6TSJLEIUIvjJ_peX3IbGW0IdkSlretJ1AnwQwvVZ2whE7RHcu8n1l4EXxazIZ2DpxvHmHPFknmeeSSvj_zypyBBeek5SpnJ9p5DaIZQrrtt-Owduc9Wypg



ubectl explain deployment.etada



![image-20201007124711930](D:\ 根目录\Code\github\document\blog\docker\k8s.assets\image-20201007124711930.png)