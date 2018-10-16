# 教程2：开发图像识别应用

首先，请确保工程中已导入AuraSDK。  
然后，打开“影见开发者工具”，启用图像识别功能，添加新图片，选择图片所在的目录。  


{% hint style="warning" %}
_注意：_

1. _支持 .jpg或.png格式，请确保图像不小于 300x300 像素_
2. _当前只支持单个文件夹的上传，请提前将所有要识别的图像放入同一目录中，请不要将图片放入子目录中_
3. _当前图像识别只支持英文路径，请将模型名称用英文命名，并放入英文路径下。_
{% endhint %}

新建场景，或者打开已有的场景，会发现场景中已经存在一个叫做AURA\(Clone\)的物体，这就说明当前场景已经准备就绪，我们可以进行开发。

### 1. 图像被检测到

当图像刚被放置到投影区域内将会触发“图像被检测到”的事件，通常用于图像的实例化。

可以通过向`AURABehaviour`注册`OnImageDetected`事件来获取。语法如下：

```text
AURABehaviour.OnImageDetected += OnImageDetected;
```

`OnImageDetected`的声明形式为：

```text
OnImageDetected(ImageInfo imageInfo)
```

**参数说明：**image[Info](https://docs.google.com/document/d/1ekdBRWfTT2W9BfVfmcaSZ_6LwjLAKOfW6ZYppGayIF8/edit#bookmark=id.z2d3pz11nz4r)：为[ImageInfo](https://docs.google.com/document/d/1ekdBRWfTT2W9BfVfmcaSZ_6LwjLAKOfW6ZYppGayIF8/edit#bookmark=id.147hbyb7bvfp)类型，包含检测到的图像信息 （图像的name，轮廓点）。

### 2. 图像位置姿态更新

当图像位姿发生变化时将会触发“图像位置姿态更新”的事件，通常用于更新图像的位姿。

可以通过向AURABehaviour注册OnImageUpdated事件来获取。语法如下：  


```text
AURABehaviour.OnImageUpdated += OnImageUpdated;
```

OnImageUpdated的声明形式为：

```text
OnImageUpdated(ImageInfo imageInfo)
```

**参数说明：**image[Info](https://docs.google.com/document/d/1ekdBRWfTT2W9BfVfmcaSZ_6LwjLAKOfW6ZYppGayIF8/edit#bookmark=id.z2d3pz11nz4r)：为[ImageInfo](https://docs.google.com/document/d/1ekdBRWfTT2W9BfVfmcaSZ_6LwjLAKOfW6ZYppGayIF8/edit#bookmark=id.147hbyb7bvfp)类型，包含检测到的图像信息 （图像的name，轮廓点）。  
****

### **3. 图像丢失**

当图像被从投影区域拿走时将会触发“图像丢失”的事件，通常用于销毁场景中的图像。

可以通过向AURABehaviour注册OnImageLost事件来获取。语法如下：

```text
URABehaviour.OnImageLost += OnImageLost;
```

OnImageLost的声明形式为：

```text
OnImageLost(ImageInfo imageInfo)
```

**参数说明：**image[Info](https://docs.google.com/document/d/1ekdBRWfTT2W9BfVfmcaSZ_6LwjLAKOfW6ZYppGayIF8/edit#bookmark=id.z2d3pz11nz4r)：为[ImageInfo](https://docs.google.com/document/d/1ekdBRWfTT2W9BfVfmcaSZ_6LwjLAKOfW6ZYppGayIF8/edit#bookmark=id.147hbyb7bvfp)类型，包含检测到的图像信息 （图像的name，轮廓点）。  
****

