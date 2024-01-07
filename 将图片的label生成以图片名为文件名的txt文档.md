首先将train文件夹中的ants文件改成ants_image

然后创建一个新文件夹为ants_label

![image.png](将图片的label生成以图片名为文件名的txt文档+bca13a26-8b33-438f-8284-7078f66135d0/image.png)

在新文件夹中新建一个txt文件，并将其命名为ants_image中第一张图片的名字（即为0013035）并在txt文本中编辑为ants，并进行保存（保存快捷键为Ctrl+s）

![image.png](将图片的label生成以图片名为文件名的txt文档+bca13a26-8b33-438f-8284-7078f66135d0/image 1.png)

![image.png](将图片的label生成以图片名为文件名的txt文档+bca13a26-8b33-438f-8284-7078f66135d0/image 2.png)

然后在pycharm中运行代码

```Python
import os

root_dir="p\\train"
target_dir="ants_image"
img_path=os.listdir(os.path.join(root_dir,target_dir))
label=target_dir.split('_')[0]
out_dir="ants_label"
for i in img_path:
    file_name=i.split('.jpg')[0]
    with open(os.path.join(root_dir,out_dir,"{}.txt".format(file_name)),'w') as f:
        f.write(label)
```

最后得到相对应的文件和文件名

![image.png](将图片的label生成以图片名为文件名的txt文档+bca13a26-8b33-438f-8284-7078f66135d0/image 3.png)

