# LS-DYNA Physics Consistency Validator (GLSTAT)

![Language](https://img.shields.io/badge/Language-Python%203.x-blue.svg)
![License](https://img.shields.io/badge/License-MGOVL%20v2.0-red.svg)
![Environment](https://img.shields.io/badge/Environment-Termux%20%2F%20Linux-orange.svg)

## 📋 项目简介 (Introduction)

本项目是一款轻量级的 **LS-DYNA 物理一致性验证工具**，专为芯片架构仿真、碰撞动力学分析等高精尖领域设计。通过解析 `glstat` 能量文件，自动评估仿真模型的确定性逻辑与能量守恒状态，并一键生成专业诊断图表与交付报告。

## 🚀 核心功能 (Core Features)

- **能量守恒诊断**：自动监控总能量 (Total Energy) 的波动情况（标准 < 5%）。
- **沙漏能预警**：实时计算沙漏能与内能占比（标准 < 10%），防止网格畸变。
- **自动化报告**：生成带时间戳的 `delivery_note.txt` 交付文案，提升技术谈单专业度。
- **移动端适配**：深度优化 Termux 环境下的运行性能与图表渲染。

## 🛠️ 安装与运行 (Setup & Usage)

### 环境要求
- Python 3.x
- NumPy, Matplotlib

### 快速启动
1. 将 `glstat` 数据放入 `data/` 目录。
2. 运行验证脚本：
   ```bash
   python scripts/check.py
