 docker export 7691a814370e > liforeverya.tar 

docker build -t liforeverya/josen:develop .

   cat liforeverya.tar  | docker import - liforeverya/josen:develop 

$ docker save  e6a5611f2cc6     > develop.tar

docker load < develop.tar

docker load < /opt/docker/savesso.tar

docker save和docker export区别
docker save保存的是镜像（image），docker export保存的是容器（container）；
docker load用来载入镜像包，docker import用来载入容器包，但两者都会恢复为镜像；
docker load不能对载入的镜像重命名，而docker import可以为镜像指定新名称。
docker export导出的镜像文件大小  小于 save保存的镜像
docker save 没有丢失镜像的历史，可以回滚到之前的层（layer）。（查看方式：docker images --tree）docker export 再导入时会丢失镜像所有的历史，所以无法进行回滚操作（docker tag <LAYER ID> <IMAGE NAME>）

docker save  4e15896e1299  > /opt/docker/savesso.tar





1. 用load  和export 是容器导入导出，重新执行的时候会丢失endpoint

所以用save 

2. 必须要有work dir 不然  会直接在linux的根目录。netcore dll跑不起来
3. dotnet 是host dll 而不是 core dll;

