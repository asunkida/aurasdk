# 教程1：开发物体识别应用

首先，请确保工程中已导入AuraSDK，并且已经在开发者工具窗口中选择了要被识别的模具（参考“快速入门：创建你的第一个应用”）。

然后，新建场景，或者打开已有的场景，会发现场景中存在一个叫做AURA\(Clone\)的物体，这就说明当前场景已经准备就绪，我们可以进行开发。

模具放在影见投影区域内将会触发3个阶段的事件，分别为：模具被检测到、模具被移动和模具丢失  


**1. 模具被检测到**

当模具刚被放置到投影区域内将会触发“模具被检测到”的事件，通常用于模型的实例化。

可以通过向`AURABehaviour`注册`OnObjectDetected`事件来获取。语法如下：

```text
AURABehaviour.OnObjectDetected += OnObjectDetected;
```

`OnObjectDetected`的声明形式为：

```text
OnObjectDetected (ObjectInfo objectInfo)
```

**参数说明：**objectInfo：为ObjectInfo类型，包含检测到的模具信息 （模具的name, id, 三维位姿，轮廓点）。

**2. 模具位置姿态更新**

当模具位姿发生变化时将会触发“模具位置姿态更新”的事件，通常用于更新模型的位姿。

可以通过向AURABehaviour注册OnObjectUpdated事件来获取。语法如下：

```text
AURABehaviour.OnObjectUpdated += OnObjectUpdated;
```

`OnObjectUpdated`的声明形式为：

```text
OnObjectUpdated (ObjectInfo objectInfo)
```

**参数说明：**objectInfo：为ObjectInfo类型，包含检测到的模具信息 （模具的name, id, 三维位姿，轮廓点）。

**3. 模具丢失**

当模具被从投影区域拿走时将会触发“模具丢失”的事件，通常用于销毁场景中的模型。

可以通过向AURABehaviour注册OnObjectLost事件来获取。语法如下：

```text
AURABehaviour.OnObjectLost += OnObjectLost;
```

`OnObjectLost`的声明形式为：

```text
OnObjectLost (ObjectInfo objectInfo)
```

**参数说明：**objectInfo：为ObjectInfo类型，包含检测到的模具信息 （模具的name, id, 三维位姿，轮廓点）。

