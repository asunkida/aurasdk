# API接口说明

## Class 

### ObjectInfo

| 属性 | 说明 |
| :--- | :--- |
| name | 为开发者工具窗口中模具的Name**。** |
| id | 模具的id \(当影见投影区域内存在多个相同模具时通过此id来进行区分） |
| position | 模具当前在投影仪坐标系下的位置 |
| quaternion | 模具当前在投影仪坐标系下的旋转姿态contourPoints：模具的轮廓点，如果没有开启轮廓点则为null |

### ImageInfo

| 属性 | 说明 |
| :--- | :--- |
| name | 为开发者工具窗口中图像的Name**。** |
| id | 模具的四个轮廓点，如果没有开启轮廓点则为null |

### **AURA\_SystemInfo**

| 属性 | 说明 |
| :--- | :--- |
| list | 检测到的所有模型的信息，AURA\_ObjectInfo类型 |
| handPose | 手势信息，AURA\_HandPose类型 |

### **AURA\_ObjectInfo** 

| 属性 | 说明 |
| :--- | :--- |
| type | 类型ID（typeID），未知模型为“unknown”handPose |
| id | 实例ID，全局唯一 |
| matrix | RT矩阵4x4，顺序是每行 |
| contourPoints | 轮廓点（2D坐标） |

## Event

使用方式：建议在脚本Start中执行事件注册，对应函数的声明请参考对应的delegate

#### 注册模具识别事件

```csharp
void Start()
    {
        AURABehaviour.OnObjectDetected += AURABehaviour_OnObjectDetected;
        AURABehaviour.OnObjectUpdated += AURABehaviour_OnObjectUpdated;
        AURABehaviour.OnObjectLost += AURABehaviour_OnObjectLost;
    }
```

#### **模具被识别到**

```csharp
public delegate void ObjectDetected(ObjectInfo objectInfo); 
public static event ObjectDetected OnObjectDetected;  //检测到有新模具进入的时候回调一次
```

#### 模具位置更新

```csharp
public delegate void ObjectUpdated(ObjectInfo objectInfo);
public static event ObjectUpdated OnObjectUpdated; //当场景中已存在的模具位置姿态有更新的时候回调（实时更新）
```

#### 模具丢失

```csharp
public delegate void ObjectLost(ObjectInfo objectInfo);
public static event ObjectLost OnObjectLost; //当场景中的模具被拿出投影区域的时候回调一次
```

#### 注册图像识别事件

```csharp
 void Start()
    {
        AURABehaviour.OnImageDetected += AURABehaviour_OnImageDetected;
        AURABehaviour.OnImageUpdated += AURABehaviour_OnImageUpdated;
        AURABehaviour.OnImageLost += AURABehaviour_OnImageLost;
    }
```

#### **图像被识别到**

```csharp
public delegate void ImageDetected(ObjectInfo imageInfo); 
public static event ImageDetected OnImageDetected;  //检测到有新模具进入的时候回调一次
```

#### 图像位置更新

```csharp
public delegate void ImageUpdated(ImageInfo imageInfo);
public static event ImageUpdated OnImageUpdated; //当场景中已存在的模具位置姿态有更新的时候回调（实时更新）
```

#### 图像丢失

```csharp
public delegate void ImageLost(ImageInfo imageInfo);
public static event ImageLost OnImageLost; //当场景中的模具被拿出投影区域的时候回调一次
```

#### 空中手势

```csharp
Enum GestureState
{
     WaveLeft,
     WaveRight,
     OpenPalm,
     CloseFist,
}
public delegate void GestureChanged(GestureState state);
Public static Event GestureChanged OnGestureChanged;
```

#### 点击事件

{% hint style="info" %}
点击事件为安卓系统事件，不论模具上的点击还是桌面上的点击，都可以直接用Input.GetMouseButtonDown 或者 Input.GetTouch 来获得
{% endhint %}

