# UMI-Dobot: 通用机械臂操作接口  

<div align="center">  
<img src="assets/logo.png" width="200px"/>  

[![Project Page](https://img.shields.io/badge/Project-Page-blue)](your_project_page)  
[![Documentation](https://img.shields.io/badge/Documentation-green)](your_docs_page)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  

</div>  

本项目是对 Berkeley 的 [UMI (Universal Manipulation Interface)](https://umi-gripper.github.io/) 框架的工业级复现与改进，旨在解决工业机械臂操作任务中的数据收集难、模型训练复杂等问题。通过低成本的硬件方案和高效的算法框架，我们实现了从数据采集到模型部署的全流程打通。  

## 主要特点  

- **低成本数据采集**: 使用 GoPro 相机和 3D 打印夹持器实现便携式数据采集  
- **精确位姿跟踪**: 基于 ORB-SLAM3 实现实时场景三维重建和相机位姿跟踪  
- **通用操作策略**: 采用扩散策略(Diffusion Policy)进行机械臂控制  
- **工业级部署**: 支持越疆(Dobot)系列机械臂的即插即用部署  

## 系统架构  

### 硬件组成  
- GoPro Hero 9 相机（主传感器）  
- 3D 打印夹持器（数据采集工具）  
- 越疆机械臂（执行终端）  

### 软件架构  
1. **数据采集模块**  
   - 视觉-惯性相机跟踪  
   - 实时位姿估计  
   - 自动数据过滤与标注  

2. **策略学习模块**  
   - 基于扩散模型的行为克隆  
   - 时序动作生成  
   - 多模态策略训练  

3. **部署执行模块**  
   - 实时位姿控制  
   - 轨迹规划与执行  
   - 安全监控系统  
