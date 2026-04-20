# LS-DYNA Physics Consistency Validator (GLSTAT)

![Language](https://img.shields.io/badge/Language-Python%203.x-blue.svg)
![License](https://img.shields.io/badge/License-MGOVL%20v2.0-red.svg)
![Environment](https://img.shields.io/badge/Environment-Termux%20%2F%20Linux-orange.svg)

## 📋 项目简介 (Introduction)

本项目是一款轻量级的 **LS-DYNA 物理一致性验证工具**。通过解析 `glstat` 能量文件，自动评估仿真模型的确定性逻辑与能量守恒状态，并一键生成专业诊断图表与交付报告。

---

## 🛠️ 傻瓜式实操流程 (Step-by-Step SOP)

如果你是第一次使用，请完全按照以下指令一行一行复制执行：

### 第一步：环境初始化 (仅需执行一次)
确保你的 Termux 已经依次安装了必要的依赖库：
```bash
pkg update && pkg upgrade
```
```bash
pkg install python numpy matplotlib

```
### 第二步：获取并进入仓库
```bash
git clone https://github.com/maomaoati-coder/glstat.git
```
```bash
cd glstat

```
### 第三步：一键运行诊断 (核心步骤)
**注意**：脚本已锁定 data/example_glstat 作为默认演示数据。小白**无需**移动任何文件，直接运行：
```bash
python scripts/check.py

```
> **预期反馈**：你会看到屏幕上打印出带 [PASSED] 字样的彩色边框报告。
> 
### 第四步：查看并提取成果
 1. **查看交付文案** (可以直接复制发给客户)：
   ```bash
   cat delivery_note.txt
   
   ```
 2. **在手机相册中查看能量曲线图**：
   运行以下命令，将生成的图片推送到手机系统相册：
   ```bash
   cp diagnosis_plot.png /storage/emulated/0/Pictures/
   
   ```
## 📂 进阶：如何校验你自己的数据？
如果你有真实的客户数据需要验证：
 1. 把你的 glstat 文件重命名为 glstat。
 2. 放入仓库根目录。
 3. 再次执行 python scripts/check.py，脚本将优先处理你的真实数据。

## ⚖️ 许可证 (License)
本项目遵循 **MGOVL v2.0** 协议，版权归 GuanghuiMao 所有。

