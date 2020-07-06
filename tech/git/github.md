## 本地与github 建立连接

### 方法1

```
1 echo # repository name>> README.md
2 git init
3 git add README.md
4 git commit -m "first commit"
5 git remote add origin git@github.com:yourname/repository name.git
6 git push -u origin master
## 如果没有关联
git pull origin master --allow-unrelated-histories
```

### 方法2 直接git clone

git clone git@github.com:your name/repository name.git