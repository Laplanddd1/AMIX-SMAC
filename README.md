# AMIX-SMAC: 基于注意力机制的单调价值函数分解方法

本项目是针对 **SMAC (StarCraft Multi-Agent Challenge)** 环境的多智能体强化学习（MARL）算法实现。核心算法 **AMIX** 旨在通过引入注意力机制（Attention Mechanism）改进经典的单调价值分解方法（如 QMIX），以增强智能体在复杂协作场景下的信用分配（Credit Assignment）能力。

## 🚀 项目亮点

- **AMIX 算法实现**：在 PyMARL 框架基础上深度定制，引入注意力机制优化混合网络（Mixing Network）。
- **实验自动化**：包含完整的训练脚本和 Colab 交互式笔记本，支持一键训练与可视化。
- **详尽的实验结果**：分类整理了 Baseline 对比、消融实验以及多种 SMAC 地图（如 MMM2, 3s_vs_5z）的性能日志。
- **毕业设计全集**：仓库内附带了毕业论文、答辩 PPT 等完整学术产出。

---

## 📂 项目结构

```text
AMIX-SMAC/
├── src/                    # 修改后的核心源码
│   └── smac_pymarl.py      # AMIX 算法的核心实现逻辑
├── notebooks/              # 交互式研究工具
│   └── smac_pymarl.ipynb   # Colab 训练与制图脚本
├── results/                # 实验产出成果
│   ├── final_models/       # 训练完成的模型权重 (Checkpoints)
│   ├── replay_videos/      # 智能体博弈录像
│   ├── figures/            # 论文图表 (Baseline对比、消融研究等)
│   └── logs/               # 训练原始日志 (Sacred 格式)
├── docs/                   # 学术文档
│   ├── slides.pdf          # 答辩 PPT
│   └── grad_project.pdf    # 毕业论文全文
├── requirements.txt        # 环境依赖清单
├── LICENSE                 # MIT 开源协议
└── README.md               # 项目中文说明文档
```

---

## 🛠️ 环境准备

建议使用 Python 3.8+ 和 CUDA 11+ 环境。

1.  **克隆仓库**：
    ```bash
    git clone https://github.com/Laplanddd1/AMIX-SMAC.git
    cd AMIX-SMAC
    ```
2.  **安装依赖**：
    ```bash
    pip install -r requirements.txt
    ```
3.  **安装 StarCraft II**：
    需按照 [PyMARL](https://github.com/oxwhirl/pymarl) 官方指引安装 SC2 引擎及 SMAC 地图。

---

## 📊 实验指南

### 运行训练
你可以直接运行 `src/` 下的脚本开始训练：
```bash
python src/main.py --config=amix --env-config=sc2 with map_name=MMM2
```

### 结果查看
-   **日志分析**：实验日志存储在 `results/logs/sacred/`。
-   **可视化**：使用 `notebooks/smac_pymarl.ipynb` 可以读取日志并生成学习曲线图。
-   **图表分类**：
    -   `01_Baseline`: 基础算法性能对比
    -   `02_AMIX_Comparison`: AMIX 与 QMIX 等算法的深度对比
    -   `03_Ablation_Studies`: 关键组件的消融实验结果

---

## 📜 引用与协议

本项目采用 **MIT License**。

如果你在研究中使用了本项目的代码或思路，请引用相关毕业论文。

---

## 👨‍💻 作者信息

-   **作者**：Lapland
-   **GitHub**：[Laplanddd1](https://github.com/Laplanddd1)
-   **项目背景**：本科毕业设计 - 复杂环境下多智能体价值分解算法研究
