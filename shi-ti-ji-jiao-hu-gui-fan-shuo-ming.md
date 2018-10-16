# 实体及交互规范说明

## **物体识别规范**

影见系统可同时支持单个或多个独立、静止放置的物体识别与跟踪。影见可识别的物体类别包括园林建筑物模型、布偶、玩具等多种复杂物体，或规则几何形体如圆柱、正方体等。

交互实体的具体规范说明如下：

### **识别单个模型**

<table>
  <thead>
    <tr>
      <th style="text-align:left">属性</th>
      <th style="text-align:left">规范说明</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">材质</td>
      <td style="text-align:left">不镂空、不透光、不易形变、浅色材质</td>
    </tr>
    <tr>
      <td style="text-align:left">尺寸</td>
      <td style="text-align:left">
        <p>单个物体上表面面积不小于 25 cm² （见下图）</p>
        <p>每个物体高度请保持在 1.5 cm 到 20 cm范围内 （见下图)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">形状/结构</td>
      <td style="text-align:left">
        <p>若单个模型为非对称不规则物体，模型各个视角信息需具有区分度</p>
        <p>请尽量避免瘦高形状的物体，避免物体表面有细长突出部分</p>
      </td>
    </tr>
  </tbody>
</table>

![&#x6A21;&#x578B;&#x7684;&#x4E0A;&#x8868;&#x9762;&#x548C;&#x9AD8;&#x5EA6;&#x8BF4;&#x660E;](https://lh3.googleusercontent.com/Ac8Mcrth2BABWz4W6Je4HdlNGm47jPLudXLkzjDEzm5p2gSL3kUrmW5ipHw97rnoCOZMoyeO_VUGNSAsdqgq1VnsHm4slpoF13W7cHAFtdAdUTaEUnCP1tBa4kJHmyKPb6ecIvHK)

![&#x7269;&#x4F53;&#x8868;&#x9762;&#x6709;&#x7EC6;&#x957F;&#x7A81;&#x51FA;&#x90E8;&#x5206;&#xFF08;&#x5DE6;&#xFF09;          &#x7626;&#x9AD8;&#x5F62;&#x72B6;&#x7269;&#x4F53;&#xFF08;&#x53F3;&#xFF09;](https://lh6.googleusercontent.com/8DAmXGkETz7Ah5siAzWQp3UqJlSGkDqxSfTutLkmg9aQk1ibhdopfSDMA6sQVxOtaIcXN9hljPc0VmVUIXmz3biJ9jpwKfOiYiQBBWbzj9onxs1KKcboMoOmoyENdp6TsHMA3mNk)

###  识别多个不同模型



<table>
  <thead>
    <tr>
      <th style="text-align:left">属性</th>
      <th style="text-align:left">规范说明</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">物体之间的差异性</td>
      <td style="text-align:left">
        <p>满足以下条件中至少一条：</p>
        <ul>
          <li>模型尺寸具有显著差别 (如高度差2cm以上，或上表面大小有显著差别）</li>
          <li>轮廓有显著差异性</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">物体之间的间距</td>
      <td style="text-align:left">物体之间的间距尽量不小于物体自身高度/2</td>
    </tr>
    <tr>
      <td style="text-align:left">最多可同时识别的模型数量</td>
      <td style="text-align:left">5 - 8 个 （延时会随着需要识别的物体种类数量、物体模型的大小、形状复杂度而增加）</td>
    </tr>
  </tbody>
</table>

![&#x591A;&#x6A21;&#x578B;&#x4E4B;&#x95F4;&#x7684;&#x5C3A;&#x5BF8;&#x5DEE;&#x5F02;&#x6027;&#x8BF4;&#x660E;&#xFF1A; &#x4E0A;&#x8868;&#x9762;&#x5927;&#x5C0F;&#x6709;&#x663E;&#x8457;&#x5DEE;&#x522B;&#xFF08;&#x5DE6;&#xFF09;  &#x9AD8;&#x5EA6;&#x5DEE;&#x6709;2cm&#x4EE5;&#x4E0A;&#xFF08;&#x53F3;&#xFF09;](https://lh3.googleusercontent.com/0xB2dNFj2q8oV-PFUH0Lki7US-aJWR8DhFWIrrGTace1-mJ5pj7kadbKk4FeW_1toKX_f7E4-f8rj6TEmuZ5AoFPjApRVycJJin0G-4thQanUwUlEJvJfZgheCsEnfwYkcIXBVpF)

![&#x591A;&#x4E2A;&#x6A21;&#x578B;&#x7684;&#x8F6E;&#x5ED3;&#x5177;&#x6709;&#x663E;&#x8457;&#x5DEE;&#x5F02;&#x6027;](https://lh4.googleusercontent.com/tnqk6UNJL6PGekg51ndbhs42y_3vjI_ezPGNaviayDoQsm-nRXDj1pkZbgDpqleKn5mJktPvqdbElkDrbBxyyntfpjXgKsQusXZkDx64RFEnxTbB6mIN820bZRo7lybqqED9_Bs4)

## **实体交互场景规范**

影见系统在发生以下交互行为时将不进行识别，请开发者设计应用时注意以下四种情况：  


![](https://lh3.googleusercontent.com/HpmN_1CCMVQAd-u2lrSGlphLN-OYjyARsObzgMLvSmaesR9Z8s33dypWkm6hyVc6FOfs9rq_VfSc7zVCEak0vbROazIdkPuD7OoahXUcVU3SU-V0g4xPsTP_96duE8KCHIB4Rc4C)

## **图像识别规范**

针对待识别的图像实体，请注意以下规范说明 ：

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>属性</b>
      </th>
      <th style="text-align:left">规范说明</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">实际尺寸</td>
      <td style="text-align:left">不小于 290 mm x 210 mm （其中绘本场景，以翻开后的尺寸为准）</td>
    </tr>
    <tr>
      <td style="text-align:left">纹理</td>
      <td style="text-align:left">
        <p>图案边缘色差尽量大 （特征点多）</p>
        <p>纹理相似度低</p>
        <p>纹理均匀分布、避免元素过于集中</p>
        <p>避免大面积留白或纯色色块</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">材质</td>
      <td style="text-align:left">不反光</td>
    </tr>
    <tr>
      <td style="text-align:left">环境</td>
      <td style="text-align:left">良好光照或对图像区域投影白光</td>
    </tr>
  </tbody>
</table>  
  


**以下是一些符合要求的与不符合要求的图像样例对比供参考：**  


|  **a. 避免纹理分布不均匀** | **b. 避免过多文字或留白** |
| :---: | :---: |
| ![](https://lh4.googleusercontent.com/2irg7_Q-27WYZEt77z7rzlJDmNxBS_XPlFILZ9PfDieSkmcYDSRjftId7664h_7rX_yZsrS0b0g-Dd9Cvm_wKHM3AcovzFg2sQFvLKiBl66xA3w5j5k6kcTSi5_CFmmT3gCHV3zG) | ![](https://lh4.googleusercontent.com/nzhEE0-i1XxzazBrldXPk0wPWWrVnXV6Rpg3LFkgfqGTrx4WI1W4pPaS7YYf4IzHSfYlcD9cgtTJTzjGpr6mCOqCqCHoqfeVbAlbCimJTZ1ULJn7-R_olA1xL3w3pHqUAg2m7unw) |
| ![](https://lh5.googleusercontent.com/i7SH7jbqdxqyHs3hBD7skBSkwuUX0Czd_OsMV2EqT9ag0WyyWxUtPs-dfnqskGIj2EffQM8PpHar4ivJ-6JEVGOtqFTpkk60RbuZCR-4A_IW3itWhsT1A2yVrD2CW_TKCXjQ34lM)纹理不均匀             ![](https://lh6.googleusercontent.com/M9eBY1H1r5CpYDiGDPhpG0R2zCTCc7NNRkoDtjur-DdZf6rClaTNufPaNsydkSB1kRvOVT7D6cHZUYWTOCnwIZ53pH7ZQXE6kkhu0eBe6rzhsx-VyndM3fWYZ70HiSSquEaZjuxo)纹理分布均匀  | ![](https://lh5.googleusercontent.com/i7SH7jbqdxqyHs3hBD7skBSkwuUX0Czd_OsMV2EqT9ag0WyyWxUtPs-dfnqskGIj2EffQM8PpHar4ivJ-6JEVGOtqFTpkk60RbuZCR-4A_IW3itWhsT1A2yVrD2CW_TKCXjQ34lM)   ****过多文字篇幅              ![](https://lh6.googleusercontent.com/M9eBY1H1r5CpYDiGDPhpG0R2zCTCc7NNRkoDtjur-DdZf6rClaTNufPaNsydkSB1kRvOVT7D6cHZUYWTOCnwIZ53pH7ZQXE6kkhu0eBe6rzhsx-VyndM3fWYZ70HiSSquEaZjuxo)无过多文字 |

| **c. 避免重复纹理** |                   **d. 避免大面积纯色色块** |
| :---: | :---: |
| ![](https://lh3.googleusercontent.com/L0LT4epC7QyihsTh6r7qJL_LjyDeUGyz-wx0YPvanzm0WVhTf-1kUKQev0LuFKwUho4ZCdyzpThhWiYrLnQQ4voE8PDWjfXZw1BVq8N3oDAli6_7cIr6b1xxoRx4y6h-j26QgizK) | ![](https://lh5.googleusercontent.com/jVL91Eu796UNeRglF5TXrWmTCAV0JSFgDlDTEzbGu4dVUpvhkZPKIkKTjntwumhj5idpzqyWkEJNREuAnJ2JsbpK_uX9-g4tz7HbIQw6rqbKKfzodnIf4WAuescyTUJXpTH_33Xh) |
| ![](https://lh5.googleusercontent.com/i7SH7jbqdxqyHs3hBD7skBSkwuUX0Czd_OsMV2EqT9ag0WyyWxUtPs-dfnqskGIj2EffQM8PpHar4ivJ-6JEVGOtqFTpkk60RbuZCR-4A_IW3itWhsT1A2yVrD2CW_TKCXjQ34lM)纹理不均匀             ![](https://lh6.googleusercontent.com/M9eBY1H1r5CpYDiGDPhpG0R2zCTCc7NNRkoDtjur-DdZf6rClaTNufPaNsydkSB1kRvOVT7D6cHZUYWTOCnwIZ53pH7ZQXE6kkhu0eBe6rzhsx-VyndM3fWYZ70HiSSquEaZjuxo)纹理分布均匀  | ![](https://lh5.googleusercontent.com/i7SH7jbqdxqyHs3hBD7skBSkwuUX0Czd_OsMV2EqT9ag0WyyWxUtPs-dfnqskGIj2EffQM8PpHar4ivJ-6JEVGOtqFTpkk60RbuZCR-4A_IW3itWhsT1A2yVrD2CW_TKCXjQ34lM)   ****过多文字篇幅              ![](https://lh6.googleusercontent.com/M9eBY1H1r5CpYDiGDPhpG0R2zCTCc7NNRkoDtjur-DdZf6rClaTNufPaNsydkSB1kRvOVT7D6cHZUYWTOCnwIZ53pH7ZQXE6kkhu0eBe6rzhsx-VyndM3fWYZ70HiSSquEaZjuxo)无过多文字 |



| **e. 两张图像纹理过于相似导致无法区分** | **f. 图像B包含图像A的大部分纹理** |
| :---: | :---: |
| ![](https://lh6.googleusercontent.com/3g9EUtbpoHaaB97mcwgMw7ew3ClO9Xr5lTSu_O9qtQ1YfHm5ETTG_V2cHsHMcC-Iu0IDEWyDWi39WiF8gMt3BV8D9Ltn3Mvk7TExquluRvRB-X2x5ytoOoVyXKRCGvlhxY7fTkYG) | ![](https://lh3.googleusercontent.com/gfSDSKsx4Z5Tu2-XZWHBKKU86AVyulF9lA9mH2lgqNCpezkhxmAO5Cqvd27HuFoDtAEA-0q-FEj53VxQMa51lx2kozbcUtGIPDDl2XtkR8sBDIAMCAf7sRZM5P9HDqz6Goy94145) |

