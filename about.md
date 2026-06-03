# 个人技术概览

## 1. 化学类专业软件开发
> 聚焦化学领域内的各类专业需求，结合软硬件技术，实现化学业务。

### 1.1 设备垂直校准
- 手机或平板设备的垂直校准。
- 调用运动传感器，获取X、Y、Z三轴的加速度分量。
- 调用方向 / 重力传感器，获取α、β、γ三轴的重力分量。
- Demo链接：[**设备垂直校准**](https://cpuer.atomgit.net/phys-chem/experiment/contact-angle/vertical-calibration.html)

### 1.2 接触角测量软件
- 处理接触角液滴照片，获取接触角。
- 针对手机等设备适配优化，兼容电脑。
- 针对接触角测量业务自主设计UI逻辑，并使用自有算法优化接触角测量体验。
- Demo链接：[**接触角测量助手**](https://cpuer.atomgit.net/phys-chem/experiment/contact-angle/drop-pic-process.html)

### 1.3 计算机视觉 - 图像数据采集Demo
- 以计算机视觉为技术手段，通过手机 / 电脑摄像头拍照，并获取照片每个像素点的RGB值数据。
- 主要借助手机/电脑自身的硬件API实现图像采集，并借助[OpenCV.js库](https://www.npmjs.com/package/@techstark/opencv-js)实现了各类计算机视觉功能。
- Demo链接：[**图像数据采集**](https://roxszi.atomgit.net/tfjs-index/#/pages/case/cam)

### 1.4 比色法表征化学动力学
- 以获取24 / 96孔板各样品的RGB色值为业务需求，实现比色法表征化学动力学。
- Demo链接：[**比色法表征化学动力学**](https://cpuer.atomgit.net/phys-chem/experiment/outline-colorimetric/)

## 2. 化学计量学 / 机器学习&深度学习
> 以机器学习及深度学习为技术手段，立足化学计量学的药典标准，对大量数据进行处理。

### 2.1 机器学习
- 主要参考了[ml.js库](https://github.com/mljs/ml)，并结合具体业务需求，进行了各类方法的实现。
- 目前以光谱数据处理为业务需求，实现了基线校正、峰值拟合、波数对齐等功能。
- Demo链接：[**多项式迭代回归算法**](https://roxszi.atomgit.net/tfjs-index/#/pages/machine_learning/poly-iter-reg)
- Demo链接：[**滚球算法**](https://roxszi.atomgit.net/tfjs-index/#/pages/machine_learning/rolling-ball)
- Demo链接：[**迭代自适应加权惩罚最小二乘法算法(airPLS)**](https://roxszi.atomgit.net/tfjs-index/#/pages/machine_learning/airpls)
- Demo链接：[**全波谱去卷积算法(gsd)**](https://roxszi.atomgit.net/tfjs-index/#/pages/machine_learning/gsd)
- Demo链接：[**偏最小二乘算法(pls)**](https://cpuer.atomgit.net/rsdp/ml/pls)

### 2.2 深度学习
- 以深度学习为技术手段，利用卷积神经网络、循环/递归神经网络等技术，实现教学科研的业务需求。
- 技术特点为：利用[Keras(@TensorFlow.js)](https://tensorflow.google.cn/js?hl=zh-cn)库，实现WebGPU硬件加速，使得任何手机、电脑都可以开展10万级参数中小模型的深度学习。

#### 2.2.1 拉曼光谱-深度学习
- 综合应用深度神经网络、卷积神经网络模型、循环/递归神经网络实现拉曼光谱定量分析的业务演示。
- Demo链接：[**拉曼光谱深度学习**](https://roxszi.atomgit.net/tfjs-index/#/pages/case/raman)

#### 2.2.2 接触角-迁移学习
- 预训练模型：读取接触角照片，预测接触角数值。
- 迁移模型：上传接触角已知的对照组照片，并输入接触角值，系统将自动在后台进行自适应迁移学习。然后使用对照组数据校正过的迁移模型对后续接触角照片进行预测。
- Demo链接：[**接触角-迁移学习**](https://roxszi.atomgit.net/tfjs-index/#/pages/case/contact-angle)

#### 2.2.3 接触角-预训练模型训练
- 以接触角照片预测接触角数值的二维卷积神经网络模型训练。
- Demo链接：[**二维卷积神经网络模型训练**](https://roxszi.atomgit.net/tfjs-index/#/pages/case/cnn-2d-train)

## 3. 物性表征
> 各类物性表征技术的实现。

### 3.1 粒度与zeta电位表征
- 原理与应用。
- 视频链接：[https://www.bilibili.com/video/BV1Lt4y1Q79c/](https://www.bilibili.com/video/BV1Lt4y1Q79c/)

### 3.2 拉曼光谱
- 拉曼光谱原理与应用；
- 表面增强拉曼散射（Surface-enhanced Raman scattering, SERS）原理与应用；
- 空间偏移拉曼散射（Space offset Raman scattering, SORS）、逆向空间偏移拉曼散射（anti Space offset Raman scattering, anti-SORS）原理；
- 受激拉曼散射（Stimulated Raman scattering, SRS）原理；
- 相干反斯托克斯拉曼散射（Coherent anti-Stokes Raman scattering, CORS）原理；
- ...

### 3.3 其它物性表征技术手段
- 折光率
- 电导率
- 旋光/比旋光度
- 流变性（粘度、黏弹性、弹性模量、储能模量、...）
- 比表面积/孔隙率
- 吸附热力学/吸附动力学
- ...

## 4. 虚拟仿真
> 可用于交互教学及演示的技术实现

- 基于Cocos Creater引擎的技术实现，优势是快捷简单，手机即扫即用，电脑点开链接就可体验，无需安装。也支持一键生成小程序。
- 目前只有基础技术框架的简单Demo交互演示，暂无成型成熟的产品。
- Demo链接：[https://roxszi.atomgit.net/vs-demo/](https://roxszi.atomgit.net/vs-demo/)  
    ![Demo链接](public/vs-demo.png)

## 5. 3D打印实现
> 以3D打印为技术手段，通过定制化的仪器设备部件/配件打印，满足教学科研的业务需求。

### 5.1 3D建模
- 参数化建模软件：[FreeCAD](https://www.freecad.org/)
- 学习资料：[FreeCAD建模学习笔记](FreeCAD学习笔记.md)

### 5.2 光固化3D打印
- 品牌型号：[创想三维 HALOT-MAGE](https://www.creality.cn/product-100.html)
- 切片软件：[HALOT BOX](https://www.crealitycloud.cn/downloads/software/halot-box)

### 5.3 熔融挤出沉积3D打印
- 品牌型号：[创想三维 Ender-3 S1 Pro](https://www.creality.cn/product-31.html)
- 切片软件：[Creality Slicer](https://www.crealitycloud.cn/downloads/software/creality-slicer)

## 6. WebApp、小程序
> 上述各业务功能的具体封装，特点是即扫即用，无需安装。

### 6.1 仪器平台管理预约小程序
- 微信小程序
- Demo二维码：  
  ![Demo链接](public/we-app.png)

---

欢迎联系：司承运13611580728
