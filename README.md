<p align="center">
  <img src="./assets/workbench.svg" width="100%" alt="Qin-tuo — From signals to systems. An open workbench connecting circuits, robot joints and computation." />
</p>

# 陈曳 / Qin-tuo

机器人软件工程师，正在深入**边缘推理与系统性能优化**。
喜欢沿着一个问题往下追：从模型与运行时，到驱动、总线和真实硬件。

[工作台](#工作台) · [实验手记](#实验手记) · [Bilibili ↗](https://space.bilibili.com/13890708) · [所有仓库 ↗](https://github.com/Qin-tuo?tab=repositories)

---

## 工作台

### 01 / 让机器动起来

机器人最终要和真实的电机打交道。我关心的是：型号、协议和控制模式各不相同，怎样把它们接到一个清楚、可复用的接口上？

在 **khcan** 中，我把 SocketCAN 电机与串口舵机接入 ROS 2 驱动库，让配置、状态查询和控制入口各有边界。代码之外，型号参数、单位和设备状态同样值得认真对待。

`C++` · `ROS 2` · `SocketCAN` · `Motor drivers`

[阅读驱动实现 →](https://github.com/Qin-tuo/Open_Motor_SDK)

### 02 / 让模型适应机器

一块边缘设备上，感知、语言模型和其他任务会争用算力与内存。我想弄清楚：**多个任务一起运行时，延迟、内存和资源分配会怎样变化？**

我正以 **Jetson Orin NX 16GB** 为目标整理多模型推理的知识库与实验路线，继续深入 CUDA、TensorRT 和性能分析。当前处于调研与方案阶段，单模型基线和多模型并发仍待目标硬件验证。

`Learning & exploring` · `Edge inference` · `Memory` · `Scheduling`

[进入多模型推理笔记 →](https://github.com/Qin-tuo/Multi_Model_Inference)

### 03 / 保留动手的乐趣

我从自动化、电子竞赛和嵌入式设计走来，也喜欢复刻开源作品，再按自己的想法改一改。功放、显示、控制板——一个想法变成桌上能摸到的东西，这件事一直很有吸引力。

早期的数字功放、消防面罩和智能锁，是这条路径留下的作品。它们也提醒我，软件之外还有信号、电源、接口和实际使用的人。

[看看数字功放 →](https://github.com/Qin-tuo/300W-digital-amplifier) · [早期硬件作品 →](https://github.com/Qin-tuo?tab=repositories)

---

## 实验手记

<sub>2026 · 09 / 当前公开进度，随实验更新</sub>

**接口正在成形。** khcan 已提供可复用驱动库与诊断入口；继续围绕具体设备的协议、参数映射和状态管理打磨。[代码与说明 ↗](https://github.com/Qin-tuo/Open_Motor_SDK)

**先把验证路径搭起来。** S100 / SO-101 探索已有主机 mock 工作流；ACT 集成、板端推理和机械臂实测仍是后续里程碑。[当前边界与进度 ↗](https://github.com/Qin-tuo/S100_VLA#current-status)

**下一项待验证的问题。** 在 Orin 上建立可复现的单模型基线，再观察加入第二种负载之后的延迟和内存变化。[实验路线 ↗](https://github.com/Qin-tuo/Multi_Model_Inference#当前状态)

---

平时与 **C / C++、Python、Linux、ROS 2 和嵌入式硬件** 打交道；正在把 **CUDA / TensorRT / Triton** 连接到自己的系统基础上。

如果你也在折腾机器人、端侧推理，或者有意思的硬件，欢迎在相关仓库的 Issue 中交流。[Bilibili 上的我是「是陈曳呀」↗](https://space.bilibili.com/13890708)

<sub>Build something. Measure it. Understand it.</sub>
