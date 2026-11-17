# Machine-Learning-For-MCM-C

个人美赛 C 题机器学习资料库。八个分类目录收录十三个上游项目的源码、文档和示例，可用于学习算法、复现基线和查阅实现。每个项目都有自己的依赖与运行方式，可从对应目录的上游 README 开始。

## 目录结构

```text
Machine-Learning-For-MCM-C/
├── 01_core/
│   └── numpy-ml/
├── 02_classical_ml/
│   └── Machine-learning-Algorithm/
├── 03_deep_learning/
│   └── Machine-Learning-Collection/
├── 04_reinforcement_learning/
│   └── cleanrl/
├── 05_time_series/
│   ├── prophet/
│   ├── pytorch-forecasting/
│   └── ruptures/
├── 06_boosting/
│   ├── xgboost/
│   ├── LightGBM/
│   └── CatBoost/
├── 07_statistical_models/
│   ├── statsmodels/
│   └── pymc/
├── 08_uncertainty/
│   └── MAPIE/
└── notebooks/
```

## 项目与版本

| 项目目录 | 上游提交 · 分支 | 许可证 | 适用场景 |
| --- | --- | --- | --- |
| [numpy-ml](01_core/numpy-ml/) | [`b0359af5285f`](https://github.com/ddbourgin/numpy-ml/commit/b0359af5285fbf9699d64fd5ec059493228af03e) · `master` | [GPL-3.0](01_core/numpy-ml/LICENSE) | NumPy 实现的线性模型、树、GMM、HMM 和神经网络组件，适合核对公式和训练流程。 |
| [Machine-learning-Algorithm](02_classical_ml/Machine-learning-Algorithm/) | [`719f3f526cc2`](https://github.com/Nitin-Prata/Machine-learning-Algorithm/commit/719f3f526cc228eb29315b830a8f54f281c0ea57) · `main` | [MIT](02_classical_ml/Machine-learning-Algorithm/LICENSE) | Notebook 将手写实现与 scikit-learn 对照，涵盖回归、SVM、聚类和 PCA。可从 `LinearRegression/` 或 `K-Means-clustering/` 入手。 |
| [Machine-Learning-Collection](03_deep_learning/Machine-Learning-Collection/) | [`558557c7989f`](https://github.com/aladdinpersson/Machine-Learning-Collection/commit/558557c7989f0b10fee6e8d8f953d7269ae43d4f) · `master` | [MIT](03_deep_learning/Machine-Learning-Collection/LICENSE.txt) | PyTorch 与 TensorFlow 教程，包含 CNN、目标检测和 GAN。题目提供图像数据时，可参考其数据加载、迁移学习和训练循环。 |
| [cleanrl](04_reinforcement_learning/cleanrl/) | [`fe8d8a03c41a`](https://github.com/vwxyzjn/cleanrl/commit/fe8d8a03c41a7ef5b523e2e354bd01c363e786bb) · `master` | [MIT](04_reinforcement_learning/cleanrl/LICENSE) | PPO、DQN、SAC 等单文件实现。适合有可交互模拟器、状态、动作和奖励定义的序贯决策问题。 |
| [prophet](05_time_series/prophet/) | [`5cf15c0f6e5d`](https://github.com/meta/prophet/commit/5cf15c0f6e5d5259d9dd8d511fb4e15a45884cdc) · `main` | [MIT](05_time_series/prophet/LICENSE) | 适合有较明确趋势和季节性的序列，可用趋势、季节与节假日项说明预测结果。 |
| [pytorch-forecasting](05_time_series/pytorch-forecasting/) | [`519f05dd975a`](https://github.com/sktime/pytorch-forecasting/commit/519f05dd975a74bb1de105a4c1b92a760ee95c96) · `main` | [MIT](05_time_series/pytorch-forecasting/LICENSE) | 包含 TFT、DeepAR、N-HiTS 等模型，适合有足够历史样本、外部变量或多条相关序列的多步预测。 |
| [ruptures](05_time_series/ruptures/) | [`ee1c8ff8a548`](https://github.com/deepcharles/ruptures/commit/ee1c8ff8a548d54c641b2bb471562165931f31c7) · `master` | [BSD-2-Clause](05_time_series/ruptures/LICENSE) | PELT 等离线变点检测，用于定位序列结构发生变化的区段。 |
| [xgboost](06_boosting/xgboost/) | [`c95da6d33929`](https://github.com/dmlc/xgboost/commit/c95da6d3392981eb48f1d1fb8a76c6c75dd54600) · `master` | [Apache-2.0](06_boosting/xgboost/LICENSE) | 适合作为表格回归、分类和排序的提升树基准。 |
| [LightGBM](06_boosting/LightGBM/) | [`53350cd896c6`](https://github.com/lightgbm-org/LightGBM/commit/53350cd896c6fd76d2cc03354f452f18646830e9) · `main` | [MIT](06_boosting/LightGBM/LICENSE) | 基于直方图的树学习适合较大表格与多轮验证。小样本要关注叶节点约束和过拟合。 |
| [CatBoost](06_boosting/CatBoost/) | [`cc0ce40bee61`](https://github.com/catboost/catboost/commit/cc0ce40bee61db190a9d1ebc67d442ad5d89862c) · `master` | [Apache-2.0](06_boosting/CatBoost/LICENSE) | 适合包含较多类别字段的表格任务，训练时明确声明类别列并保留实体分组。 |
| [statsmodels](07_statistical_models/statsmodels/) | [`db1e7f3d07e4`](https://github.com/statsmodels/statsmodels/commit/db1e7f3d07e47f4f78877cb5fb76e045cfbdd829) · `main` | [BSD-3-Clause](07_statistical_models/statsmodels/LICENSE.txt) | 泊松、负二项和门槛计数模型，以及 ETS、SARIMAX 等经典时序基线。 |
| [pymc](07_statistical_models/pymc/) | [`bc3904be4119`](https://github.com/pymc-devs/pymc/commit/bc3904be4119596442d16593745fe4e2894297e9) · `main` | [Apache-2.0](07_statistical_models/pymc/LICENSE) | 概率建模，支持多项分布和 Dirichlet–Multinomial 等联合计数分布。 |
| [MAPIE](08_uncertainty/MAPIE/) | [`d5ea5e07aea0`](https://github.com/scikit-learn-contrib/MAPIE/commit/d5ea5e07aea09a897726fd8641c193850a5c540d) · `master` | [BSD-3-Clause](08_uncertainty/MAPIE/LICENSE) | 为回归模型构造共形预测区间，评估覆盖率和区间宽度。 |

Prophet 原地址 `facebook/prophet` 和 LightGBM 原地址 `microsoft/LightGBM` 已跳转到当前上游。PyTorch Forecasting 的现行官方仓库是 [sktime/pytorch-forecasting](https://github.com/sktime/pytorch-forecasting)。

## 按赛题数据选择模型

| 题目和数据 | 起步基线 | 值得比较的模型与验证方法 |
| --- | --- | --- |
| 单张表格的回归、分类或排序 | 均值或多数类预测、线性或逻辑回归 | 用同一划分比较 XGBoost、LightGBM 或 CatBoost。重复出现的运动员、队伍或用户按实体分组。回归可报告 MAE 或 RMSE，类别不均衡时可报告 PR-AUC 或 Macro-F1。 |
| 带日期的单条序列 | 最近值、季节性朴素法 | 先比较季节性朴素法、ETS 和 SARIMAX，再加入 Prophet。用滚动起点回测，分预测步长报告误差。用于未来预测的外部变量应在预测时已知。 |
| 多实体、多变量或多步序列 | 按实体构造滞后特征，加提升树或季节性朴素法 | 样本与计算预算充足时比较 TFT 或 N-HiTS。按时间构造训练和验证窗口；需要区间时可检查分位数损失、覆盖率和区间宽度。 |
| 零值较多的计数 | 泊松回归 | 过度离散时比较负二项；对有无事件与正计数分别建模时比较两阶段门槛模型。 |
| 各分量加总为 100% 的比例 | 按组估计多项概率 | 有各档计数时，可用 Dirichlet–Multinomial 表达额外的波动，按时间留出检验联合预测。 |
| 无监督分群与特征探索 | 参考传统机器学习 Notebook，从标准化与可视化开始 | 比较 K-Means、层次聚类或 DBSCAN；检查尺度、参数和抽样变化对结论的影响。 |
| 图像数据或仿真决策 | 图像任务先试预训练特征加简单分类器；仿真任务先试固定规则 | 图像任务参考深度学习教程，按图片来源分组验证；具备交互环境和可检验奖励时再尝试 CleanRL，多随机种子对比结果。 |

### 从数据到论文

1. 写清预测对象、预测时点、输入可用范围和实际评分指标。
2. 固定验证划分后拟合预处理，记录指标、误差分布和运行环境。先跑简单基线，再逐项增加特征和模型复杂度。
3. 对关键特征与假设做消融和敏感性分析。解释提升树结果时，可在验证集上计算置换重要性或 SHAP，并结合题意说明模型关联及其局限。
4. 记录随机种子、依赖版本、上游提交和数据出处。引用模型、教程或实现时，同时注明论文或文档及实际使用的版本。

## 可运行的赛题示例

示例使用可复现的模拟数据，以赛题结构组织输入、验证和输出。Notebook 使用已发布的 Python 包，源码目录用于查阅实现。

| Notebook | 方法与输出 |
| --- | --- |
| [奖牌计数与首次获奖概率](notebooks/01_medal_counts.ipynb) | 泊松、负二项、两阶段门槛计数。按届留出，报告奖牌 MAE 与首次获奖概率的 Brier 分数。 |
| [经典时序滚动回测](notebooks/02_rolling_time_series.ipynb) | 季节性朴素法、ETS、SARIMAX。在同一预测起点比较各模型，并按预测步长展示误差。 |
| [分位数与共形预测区间](notebooks/03_prediction_intervals.ipynb) | 分位数树模型、MAPIE 分割共形区间，以及按时间滚动校准。报告实际覆盖率和平均区间宽度。 |
| [网球逐分变点检测](notebooks/04_tennis_change_points.ipynb) | 先拟合发球优势基线，再比较 PELT 在不同罚项下识别的变化位置。 |
| [Wordle 七档比例联合预测](notebooks/05_wordle_compositions.ipynb) | 多项分布和 Dirichlet–Multinomial。比较留出词的概率对数评分、各档覆盖率和区间宽度。 |

使用 Python 3.13，从仓库根目录运行以下命令，再打开对应 Notebook 并运行全部单元格。

```sh
python3.13 -m venv ~/.venvs/mcm-c
source ~/.venvs/mcm-c/bin/activate
python -m pip install -r notebooks/requirements.txt
python -m notebook notebooks
```

## 获取源码与许可证

```sh
git clone --recurse-submodules https://github.com/kech061128-hub/Machine-Learning-For-MCM-C.git
```

如已普通克隆，可在仓库根目录执行 `git submodule update --init --recursive` 获取上游记录的依赖源码。各目录保留所列提交的 Git 跟踪文件、原始许可证、版权声明和上游子模块引用。需要追溯旧版本时可访问表中的上游仓库及提交。第三方组件或数据如附有单独声明，应按其各自条款使用。
