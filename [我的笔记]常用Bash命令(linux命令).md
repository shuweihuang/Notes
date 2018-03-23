# [我的笔记]常用Bash命令(linux命令)
***
Linux命令大全: http://man.linuxde.net/

## 增
- **mkdir**
> (Mkdir Directory) 创建目录
> 如:<code>mkdir sss</code>  创建一个sss的文件夹

- **touch**
> 创建文件
> 如:<code>touch index.html</code> 新建一个index.html文件

## 删

- **rm**
> (remove) 删除文件
> 如:<code>rm index.html</code> 删除index.html文件

- **rmdir**
> (remove Directory) 删除文件夹
> 注意:默认文件夹中有内容是不能直接删除的,如需要删除里面有内容的文件夹   
> <code>==rm== -rf sss</code> 删除sss文件夹和里面的内容

## 改

- **mv** 
> (move) 移动文件或重命名 
> 如:<code>mv index.html ceshi.html</code> 把index.html文件名修改为index.html;
> <code>mv index.html ceshi/index.html</code>  把当前文件夹下index.html这个文件移动到ceshi这个文件夹中(前提需要有ceshi这个文件夹)

- **cp**
> (copy)复制文件 
> 如:<code>cp index.html  ceshi/index.html</code> 把当前文件夹下index.html文件复制到ceshi文件夹中

## 查

- **pwd**
> (Print Working Directory)查看当前目录

- **ls**
> (List)查看当前目录下的内容(包括文件和文件夹)

- **cat**  
> 查看文件内容
> 如<code>cat index.html</code>  查看index.html这个文件中的内容(一般默认会用vi/vim编辑器打开)

- **cd**
> (change  Directory) 切换目录
> 如:<code>cd f:</code>  切换到f盘


## 其他

- **ssh**
> 远程登录
> 如 <code>ssh XXX@gitlab.study.com</code>

- **tab**
> 自动补全, 连续两次会将所有匹配的内容显示出来

- **history**
> 查看操作历史

- **curl**
> 打开一个url地址
> 如<code>curl http://www.baidu.com</code>  打开百度(注意是在当前界面打开,不是浏览器中打开)

- **tar** 
> 压缩解压

- **grep** 
> 匹配内容(一般会配合管道符使用)

- **|**
> 管道符(一般会配合grep使用)

- **wget**
> 下载(默认git安装的时候不会安装这个,需要手动安装)
> 如 <code>wget https://nodejs.org/dist/v4.4.0/node-v4.4.0.tar.gz</code>  

- **> 和>>**
> 重定向  
> 如: <code>ls xx> 123.txt</code>  把ls命令(也可以为其他命令)产生的结果放到123.txt这个文件中(如果没有这个文件会自动新建),123.txt中的原有的内容会被新的覆盖,而 用>> 就不会被覆盖

- **wc**
> (word count) 字数信息统计
> 如:<code>wc index.html</code> 统计index.html中的内容的字数
> **拓展:**
> - <code>wc -l filename</code> 只显示列数  
> - <code>wc -c filename</code> 只显示bytes数  
> - <code>wc -w filename</code> 只显示字数  

- **head**
> 显示文件的开头的内容(默认显示10行)
> 如: <code>head -5 index.html</code> 显示index.html文件的前5行内容

- **tail**
> 显示文件的开头的内容(默认显示10行)
> 如: <code>tail -5 index.html</code> 显示index.html文件的后5行内容
